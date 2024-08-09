# Network Services Management (final project)

Programa en el que desde una máquina virtual, y con ayuda del lenguaje de programación python y algunas librerías, entables la comunicación entre los servidores con el fin de efectuar consultas sin interactuar con los servidores.

## Requisitos previos
Tener instalados las librerías:

- gi
- pexpect
- paramiko
- pytz

## Ejecución del programa

La forma de ingresar al programa es mediante la terminal, para ejecutar el programa solo se debe de ingresar:

```cmd
python3 app.py
```

Nota:
El programa fue desarrollado en el sistema operativo Linux, por lo que es importante que el programa sea ejecutado en este entorno.
El usuario debe de tener instalado en su máquina la versión más reciente de python 3.

## Uso del programa

Una vez ejecutado el comando, se desplegará la ventana del programa:

![menu](https://github.com/user-attachments/assets/9a720c0e-f8b7-48ab-a310-cf7a6887d46c)

Dentro podremos encontrarnos con los diferentes elementos del programa que como usuario puede interactuar, entre esos es el despliegue de opciones de "Selecciona el modo de consulta", que da la opción a elegir de los protocolos de consulta, Telnet o SSH.

![query mode](https://github.com/user-attachments/assets/7f45ce92-69cd-40e3-9e51-4be3c62816fa)

Entre otro de los elementos que puede seleccionar el usuario es la opción "Selecciona el modo de consulta", que se nos despliega una lista de consultas a poder realizar:

![Type of query](https://github.com/user-attachments/assets/7e672789-37c9-4e0e-a772-e21622f2854e)

Las consultas mostradas son:
- Mostrar configuración de los dispositivos: Se muestran las interfaces activas y con su respectivo puerto de enlace.
- Mostrar versión de los dispositivos: Se muestra la información de los routers usados.
- Mostrar SSH de los routers: Muestra al usuario si la SSH está habilitada.
- Mostrar enrutamiento de cada router: Muestra el enrutamiento utilizado en cada routers con sus respectivas direcciones IP.
- Mostrar el enrutamiento de la red: Muestra el enrutamiento general utilizado en la red o topología.
- Mostrar información de las VPCs: Muestra las ARP de de los dispositivos conectados en el router, entre esas las VPC.
- Mostrar NAT: Muestra las NAT traducidas de los dispositivos.
- Mostrar las access-list: Muestra las listas de acceso implementadas en los dispositivos.

Nota: al momento de ingresar los hostname y direcciones IP, asegurarse que en dichas direcciones, en sentido de sus interfaces, no este implementado la lista de acceso. Se sugiere que se ingrese el hostname y dirección IP en la interface donde no tiene listas de acceso.

Para que el usuario ingrese el hostname y las direcciones, se hace por los cuadros de texto, al terminar de ingresar los datos se debe de dar clic en el botón Ingresar datos del router.

![Hostname and IP](https://github.com/user-attachments/assets/e8ae6fbe-9a63-4800-90b1-81d7357f5399)

Visualizaremos dos cuadros en blanco, el cuadro izquierdo mostrará el hostname y las direcciones IP ingresados de los dispositivos. 
Otra manera de ingresar los hostname y direcciones IP es por medio de un archivo JSON.

![Upload Files Field](https://github.com/user-attachments/assets/3a3c40cb-6bbf-4d6e-bf18-11b8d9dd689b)

Dicho contenido dentro del archivo debe de seguirse de la siguiente manera:

{“Nombre del hostname”:{“prompt”:”Nombre del hostname#”, “ip” :“Dirección_IP”}}

Como ejemplo del contenido que debe de tener el archivo JSON es el siguiente:

![JSON file](https://github.com/user-attachments/assets/b4e7da4c-8e87-4c1e-8f8e-52b044dde05f)

En el cuadro de la derecha, se mostrará los resultados de la consulta.
![results textbox](https://github.com/user-attachments/assets/74c7fa78-e14a-4e59-bbab-da99361fd9f1)

Entre los botones con los que se puede interactuar es:

- Vaciar datos: Vacía los hostname y dispositivos IP ingresados.
- Guardar resultados en un txt: De los resultados obtenidos en la última consulta. Se pueden guardar en un archivo txt.

![save and empty buttons](https://github.com/user-attachments/assets/55819181-1c2a-468d-88fd-76b5587a8b21)

Dentro se ingresa el hostname y dirección IP de los routers a analizar, dentro se ingresa en los cuadros en blanco.

![inputted data](https://github.com/user-attachments/assets/e14a7535-aa49-411c-88c3-3950be21347e)

Se alista el programa para realizar la consulta correspondiente mediante el protocolo Telnet.
Al dar clic en el botón de “realizar consulta”, nos aparecerá en el cuadro del lado de la derecha el resultado

![query result](https://github.com/user-attachments/assets/11ec7791-56ed-4d23-a71b-c75bc137fe94)

Se realizará la misma consulta, pero se cambiará el protocolo Telnet por SSH.

![change of protocol](https://github.com/user-attachments/assets/67396277-d751-433c-ae64-c0e6a2b4b350)

Al término de la ejecución de la consulta, nos aparecerá el siguiente resultado.

![general content](https://github.com/user-attachments/assets/347a9951-6bf3-49a1-b315-e25691583105)

En caso de guardar los resultados, se tendrá que hacer clic en el botón de guardar, y el archivo se almacenará enla ubicación donde está el programa, con el siguiente nombre

![Results file](https://github.com/user-attachments/assets/e2a1832b-ed53-444a-9089-791993232ff5)


## Licencia
Este proyecto está licenciado bajo la Licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.
