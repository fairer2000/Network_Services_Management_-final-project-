# Network Services Management

Program in which, from a virtual machine, and with the help of the Python programming language and some libraries, you can establish communication between servers in order to perform queries without interacting with the servers.

## Previous requirements
You must have the following libraries installed:

- gi
- pexpect
- paramiko
- pytz

## Execution of the program

The way to enter the program is through the terminal, to run the program you only have to enter:

```cmd
python3 app.py
```

Note:
The program was developed on the Linux operating system, so it is important that the program be run in this environment.
The user must have the latest version of python 3 installed on his machine.

## Use of the program

Once the command is executed, the program window will be displayed:

![menu](https://github.com/user-attachments/assets/9a720c0e-f8b7-48ab-a310-cf7a6887d46c)

Inside we will be able to find the different elements of the program that as a user can interact with, among those is the display of options of “Selecciona el modo de consulta”, which gives the option to choose from the query protocols, Telnet or SSH.

![query mode](https://github.com/user-attachments/assets/7f45ce92-69cd-40e3-9e51-4be3c62816fa)

Another of the elements that can be selected by the user is the option “Selecciona el modo de consulta”, which displays a list of queries that can be made:

![Type of query](https://github.com/user-attachments/assets/7e672789-37c9-4e0e-a772-e21622f2854e)

The queries shown are:
- Mostrar configuración de los dispositivos: The active interfaces are shown with their respective gateway port.
- Mostrar versión de los dispositivos: The information of the used routers is shown.
- Mostrar SSH de los routers: Shows the user if SSH is enabled.
- Mostrar enrutamiento de cada router: Displays the routing used on each router with their respective IP addresses.
- Mostrar el enrutamiento de la red: Shows the general routing used in the network or topology.
- Mostrar información de las VPCs: Displays the ARP of the devices connected to the router, including the VPCs.
- Mostrar NAT: Displays the translated NATs of the devices.
- Mostrar las access-list: Displays the access lists implemented on the devices.

Note: when entering the hostname and IP addresses, make sure that the access list is not implemented on these addresses in the sense of their interfaces. It is suggested that you enter the hostname and IP address on the interface where you do not have access lists.

For the user to enter the hostname and addresses, it is done through the text boxes. When the user has finished entering the data, click on the Enter router data button.

![Hostname and IP](https://github.com/user-attachments/assets/e8ae6fbe-9a63-4800-90b1-81d7357f5399)

We will see two blank boxes, the left box will show the entered hostname and IP addresses of the devices. 
Another way to enter the hostname and IP addresses is by means of a JSON file.

![Upload Files Field](https://github.com/user-attachments/assets/3a3c40cb-6bbf-4d6e-bf18-11b8d9dd689b)

Such content within the file should be followed as follows:

{“Nombre del hostname”:{“prompt”:”Nombre del hostname#”, “ip” :“Dirección_IP”}}

As an example of the content that the JSON file should have is the following:

![JSON file](https://github.com/user-attachments/assets/b4e7da4c-8e87-4c1e-8f8e-52b044dde05f)

In the box on the right, the results of the query will be displayed.
![results textbox](https://github.com/user-attachments/assets/74c7fa78-e14a-4e59-bbab-da99361fd9f1)

Among the buttons that can be interacted with are:

- Empty data: Empty the hostname and IP devices entered.
- Save results in a txt: From the results obtained in the last query. They can be saved in a txt file.

![save and empty buttons](https://github.com/user-attachments/assets/55819181-1c2a-468d-88fd-76b5587a8b21)

Inside, enter the hostname and IP address of the routers to be analyzed, then enter them in the blank boxes.

![inputted data](https://github.com/user-attachments/assets/e14a7535-aa49-411c-88c3-3950be21347e)

The program is ready to perform the corresponding query through the Telnet protocol.
When clicking on the “perform query” button, the result will appear in the box on the right side of the screen

![query result](https://github.com/user-attachments/assets/11ec7791-56ed-4d23-a71b-c75bc137fe94)

The same query will be performed, but the Telnet protocol will be changed to SSH.

![change of protocol](https://github.com/user-attachments/assets/67396277-d751-433c-ae64-c0e6a2b4b350)

At the end of the query execution, the following result will appear.

![general content](https://github.com/user-attachments/assets/347a9951-6bf3-49a1-b315-e25691583105)

In case of saving the results, you will have to click on the save button, and the file will be stored in the location where the program is, with the following name

![Results file](https://github.com/user-attachments/assets/e2a1832b-ed53-444a-9089-791993232ff5)


## License
This project is licensed under the MIT License. Consult the file [LICENSE](LICENSE) for more details.
