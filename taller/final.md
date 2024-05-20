# Redes
<p><code>Fundamentos de Redes y Cableado Estructurado</code></p>
<p>Creado por <code>Jsotelo</code> para fortalecer los fundamentos de la <code>reparacion de los equipos de computo</code> en los cursos de mantenimiento y reparacion </p>


# Taller Final Subneting

## Objetivos 

### Objetivo General
Proporcionar el conocimiento y generar las habilidades necesarias en la configuración y gestión de dispositivos de redes.

### Objetivos Específicos:
- Conocer los números necesarios para configurar y caracterizar los diferentes dispositivos de red. :+1: 

---
## 1. [Configurar el entorno de trabajo](#) ✔
1. Instalar [VSCode][1_1]
2. Instalar [Git][1_2]
3. Crear una cuenta en [github][1_3]
4. Crear un [repositorio nuevo][1_4] en Github llamado <code>Redes-dos</code>
5. Instalar la [extension de github][1_5] para VScode
6. Agregar <code>Usuario</code> y <code>Correo</code> globalmente para Git.
7. Cerrar carpeta y clonar el repositorio remoto desde VScode.
8. Crear una carpeta en el repositorio Redes-dos llamada <code>Laboratorio-uno</code>.


```bash
# Para agregar Usuario y Contraseña a GIT
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
```

[1_1]:https://code.visualstudio.com/download
[1_2]:https://git-scm.com/download/win
[1_3]:https://github.com/
[1_4]:https://github.com/new
[1_5]:https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github


## 2. [Preguntas reflexivas de ambientación](#) ✔

<ol type="a">
<li>¿Cual es la dirección de red y de broadcast de un host que tiene una ip 192.168.10.10/30?.</li>

R// 192.168.10.8/30, que es de 192.168.10.9 a 192.Teniendo en cuenta que el primer host 192.168.10.8 se utiliza como identificador de la subred y el último host (192.168.10.11) se utiliza como dirección de transmisión, la subred 192.168.10.8/30 puede tener 4 - 2 = 2 hosts utilizable.

<li>¿Que información se puede inferir de un host con la dirección 169.254.255.200/26?.</li>

R// Se puede inferir que La dirección IP 169.254.255.200/26 tiene una máscara de subred de 26 bits, lo que significa que la máscara de subred en notación de puntos decimales es 255.255.255.192. La subred 169.254.Contiene un total de 62 hosts posibles 169.254.puede tener 62 - 2 = 60 hosts utilizables, ya que el primer host (169.se utiliza como identificador de la subred y el último host (169.se utiliza como dirección de difusión.

<li>¿Cuantas sub-redes puede lograr con la mascara 172.16.0.0/22?.</li>

R// Puede crear 4 subredes 

<li>¿Cuantos clientes puede tener la sub red 172.16.0.0/22?.</li>

R// Puede haber 1.020 clientes 

<li>¿Que clase y tipo de dirección es 10.10.10.0/24?.</li>
</ol>

R// La dirección IP 10.10.10.0/24 es una dirección IP privada de clase A con una máscara de subred de 24 bits. 

## 3. [Caracterización de los adaptadores](#) ✔
|Parámetro||Valor|
|--|:--:|--:|
|Número de adaptadores Físicos|-->R//|1|
|Número de adaptadores Virtuales|-->R//|1|
|Tipo de Adaptador principal|-->R//|ethernet|
|Fabricante del Adaptador principal|-->R//|Intel R ethernet connectión 1217-LM||
|Código MAC del fabricante|-->R//|F8-B1-56-C3-0E-84|
|MAC|-->R//|F8-B1-56-C3-0E-84|

>Nota: Para obtener los parámetros de la red, usaremos los comandos [ipconfig][10], [ifconfig][8], [getmac][9].


## 4. [Caracterización de la red](#) ✔
|Parámetro|Valor|
|--|--:|
|__Subnet__R//|192.168.10.0/24|
|IPv4 R//|192.168.10.45|
|Subnet Mask decimal R//|24|
|Subnet Mask octetos R//|255.255.255.0|
|Número de direcciones de Host R//|255|
|Rango de direcciones de Host R//|192.168.10.0-255|
|IP Broadcast R//|192.168.10.255|
|Server DHCP R//|192.168.10.1|
|Server DNS R//|8.8.8.8|

>Nota: Para obtener los parámetros de la red, usaremos el comando [ipconfig][10] o [ifconfig][8].


## 5. [Caracterización de la puerta de enlace](#) ✔
|Parámetro|Valor|
|--|--:|
|Número de Entradas en la tabla ARP R// |11|
|IPv4 Gateway R//|192.168.10.1|
|MAC Gateway R//|F8-B1-56-C3-0E-84|
|ISP R//|Telmex Colombia S.A.|
|[IP Publica][5]R//|181.62.52.30|
|[Sistema Autónomo][6] R//|AS10620|


>Nota: Para obtener los parámetros de la red, usaremos el comando [arp][11] y algún servicio web/HTTP como [cual-es-mi-ip.net][5], [ipinfo.io][6] o [asrank.caida.org][9_1].


## 6. [Retardo de la red](#) ✔
|Servidor|IP|Tiempo promedio/ms|
|--|--|--|
|DNS Google|8.8.8.8|5-30 ms|
|DNS Cloudflare|1.1.1.1|5-30 ms|
|OpenDNS|208.67.222.222|5-30ms|
|Alternate DNS|76.76.19.19|10 y 50 ms|
|DNS Quad9|9.9.9.9|10 y 50 ms|
|AdGuard DNS|94.140.14.14|10 y 50 ms|

>Nota: Para calcular el retardo de la red, usaremos el protocolo ICMP/[ping][12] con al menos 10 paquetes.

## 7.  [Identificacion de red](#) ✔
|Ip|Clase de IP|Mascara de sub red|
|--|--|--|
|192.168.10.1| R// C |255.255.255.0|
|10.254.20.10| R// A |255.0.0.0|
|172.10.10.5| R// B|255.255.0.0|
|101.45.36.255| R// A |255.0.0.0|
|112.85.95.125| R// A |255.0.0.0|
|23.58.20.0| R// A |255.0.0.0|
|223.158.20.0| R// A |255.255.255.0|
|113.8.20.12| R// A|255.0.0.0|
|191.18.20.1| R// B |255.255.0.0|


## 8. [Capacidad del canal](#) ✔
|Servidor|Ping/ms|Down/MB|Up/MB|
|--|:--:|--:|--:|
|[speed test][1]|205|3.02|0.51|
|[Netflix][2]|79|6.0|10|
|[Claro][3]|58|3.7|0.3|
|[nperf][4]|56.70|4.433|1.691|

>Nota: Para calcular el retardo de la red, usaremos el protocolo HTTP via servicio WEB.


## 9. [Distancia desde el host](#) ✔
|Servidor|Ping/ms|Numero de Saltos|
|--|:--:|--:|
|google.com|57|14|
|GMail.com|55|12|
|YouTube.com|63|14|
|dns.google|526|12|
|aws.amazon.com|2229|17|
|portal.azure.com|*|30|
|login.live.com|156|20|
|Facebook.com|107|1|
|c.ns.WhatsApp.net|154|19|
|claro.com.co|*|30|
|platzi.com|257|13|
|rappi.com.co|*|30|

>Nota: Para calcular el retardo de la red, usaremos el comando ICMP/[tracert][13].

## 10. [Diagrama de Red](#) ✔
- Realice un diagrama topológico de la red que le ofrece conectividad a internet.
- Incluya todos los detalles de la red de area local a la que se encuentra conectado.
- Incluya los saltos conocidos incluyendo el equipo de borde de su ISP.

>Nota: Para conocer el tamaño y la topología de la red, usaremos la información previa y la pagina [ASRank][9_1].

## 11. [Preguntas de conocimiento](#) ✔
1. ¿Cuál es el retardo esperado para tu red según la tecnología contratada?
R// segun la tecnologia contratada el retardo esperado es el DNS google por la calidad de la conexion a internet. 
1. ¿Por qué varia la capacidad del canal en las distintas pruebas realizadas?
R// la capacidad del canal varia en distintas pruebas que se realiza porque en cada test se elige un servidor diferente, a una distancia diferente.
1. ¿Cuál de los servicios DNS es mejor para configurar mi LAN?
R// Para configurar mi LAN el mejor DNS es google porque ofrece velocidades y alta disponibilidad. 
1. ¿Como podría medir la disponibilidad de ni conexión a internet?
R// Para medir la disponibilidad de mi conexion a internet, puedo usar herramientas las cuales esten especializadas en pruebas de conectividad y supervision de red por ejemplo ping




[1]:https://www.speedtest.net/es
[2]:https://fast.com/es/#
[3]:http://speedtest.claro.net.co/
[4]:https://www.nperf.com/es/
[5]:https://www.cual-es-mi-ip.net/
[6]:https://ipinfo.io/

[9_1]:https://asrank.caida.org/

[8]:https://man7.org/linux/man-pages/man8/ifconfig.8.html
[9]:https://learn.microsoft.com/es-es/windows-server/administration/windows-commands/getmac
[10]:https://learn.microsoft.com/es-es/windows-server/administration/windows-commands/ipconfig
[11]:https://learn.microsoft.com/es-es/windows-server/administration/windows-commands/arp
[12]:https://learn.microsoft.com/es-es/windows-server/administration/windows-commands/ping
[13]:https://learn.microsoft.com/es-es/windows-server/administration/windows-commands/tracert


---
## Mas Recursos
- [Protocolo Ipv4](https://es.wikipedia.org/wiki/IPv4) (Wikipedia)
- [Direccionamiento IP](https://es.wikipedia.org/wiki/Direcci%C3%B3n_IP) (Wikipedia)
- [Calculadora IP](https://www.calculator.net/ip-subnet-calculator.html) (Wikipedia)

---
## Evaluación y rúbrica
- Fecha máximo entrega: 05 de Mayo de 2023
- Hora de entrega: 11:59pm	
- Nota máxima: 5.0 
- Número de actividades: 10
- Valor de cada actividad: 0.5
- Ponderación: 20%
- $\color{#DD69DD}{\text{...Carpe Diem}}$