# Pickle-Rick @TryHackMe
Write-Up de la maquina pickle rick de tryhackme:

**Resalto, pude haberlo hecho entablando una reverseshell, solo que como tenía todo en bandeja de oro, decidí hacerlo por la web**

Lo primero que hice fue verificar si tenía una conexión con la maquina:

![image](https://user-images.githubusercontent.com/107098852/172544680-0169b766-ea86-4229-8017-77975ad750c6.png)

Luego realice una búsqueda de puertos abiertos con nmap, seguido a esto lance unos scripts básicos de reconocimiento con nmap a los puertos abiertos que encontré:

 ![image](https://user-images.githubusercontent.com/107098852/172544696-c054fd7e-a2c9-4f57-8d82-4c5e7c15df66.png)
 
Como no encontré nada interesante, fui a la pagina web y revise el código fuente, en este se encontraba un nombre de usuario:

 ![image](https://user-images.githubusercontent.com/107098852/172544708-65f30800-2e47-4d0d-9b36-bb7146bdee3c.png)
 
Después hice una búsqueda de directorios con nmap y encuentre un login.php y robots.txt

 ![image](https://user-images.githubusercontent.com/107098852/172544722-47baa86c-3262-48f2-b4e1-67c773e43f43.png)
 
En el robots.txt encontré un texto, que a simple vista parecía ser una contraseña
![image](https://user-images.githubusercontent.com/107098852/172544733-b5ccd66b-d21f-4c76-9caa-f31a2fa1c4ae.png)

Luego fui a la página de login, puse las credenciales que había encontrado y se me permitió el acceso. En esta página había un panel donde podía poner comandos, al hacer ls vi que podía ver archivos interesantes, intente abrirlos con cat pero la página había bloqueado algunos comandos, así que trate de visualizar los archivos con less y si me lo permitió, así pude ver el primer ingredientes

![image](https://user-images.githubusercontent.com/107098852/172544746-9708c7e2-e9d0-480d-965a-46e303b03cfc.png)

Después seguí buscando y encontré el segundo ingrediente en la raíz del usuario rick, el cual pude leer sin problemas 

![image](https://user-images.githubusercontent.com/107098852/172544756-a5e8aaf1-27e6-4c05-a5e8-0b32d42d4d42.png)

Luego me dio por hacer un sudo -l y me di cuenta que podía usar todos los comandos como root

 ![image](https://user-images.githubusercontent.com/107098852/172544774-ef6b7fa5-a852-486a-9749-8616d7b6e166.png)
 
así que fui a la carpeta root y ahí estaba el tercer ingrediente.

![image](https://user-images.githubusercontent.com/107098852/172544785-c7020d6c-7304-4099-a72d-2feed3bf247f.png)

 
