# Pickle-Rick
Write-Up de la maquina pickle rick de tryhackme

Pickle Rick

**Resalto, pude haberlo hecho entablando una reverseshell, solo que como tenía todo en bandeja de oro, decidí hacerlo por la web**

Lo primero que hice fue verificar si tenía una conexión con la maquina:
![image](https://user-images.githubusercontent.com/107098852/172544603-b56cf2e9-b894-40cb-af59-acb94e635b8b.png)

 

Luego realice una búsqueda de puertos abiertos con nmap, seguido a esto lance unos scripts básicos de reconocimiento con nmap a los puertos abiertos que encontré:
 

Como no encontré nada interesante, fui a la pagina web y revise el código fuente, en este se encontraba un nombre de usuario:

 

Después hice una búsqueda de directorios con nmap y encuentre un login.php y robots.txt

 

En el robots.txt encontré un texto, que a simple vista parecía ser una contraseña

 
Luego fui a la página de login, puse las credenciales que había encontrado y se me permitió el acceso. En esta página había un panel donde podía poner comandos, al hacer ls vi que podía ver archivos interesantes, intente abrirlos con cat pero la página había bloqueado algunos comandos, así que trate de visualizar los archivos con less y si me lo permitió, así pude ver el primer ingrediente 

 

Después seguí buscando y encontré el segundo ingrediente en la raíz del usuario rick, el cual pude leer sin problemas 


 



Luego me dio por hacer un sudo -l y me di cuenta que podía usar todos los comandos como root

 

así que fui a la carpeta root y ahí estaba el tercer ingrediente.

 
