##Primeros pasos en GitHub

###Crear una cuenta

- Entra en GitHub y crea una cuenta
~~~
https://about.gitlab.com/
~~~


- Configurar un par de claves
	- Crear un par de claves
	~~~
	cd ~/.ssh
	ssh-keygen
	Generating public/private rsa key pair.
	Enter file in which to save the key (/Users/client/.ssh/id_rsa): 
	Enter passphrase (empty for no passphrase): 
	Enter same passphrase again: 
	Your identification has been saved in /Users/client/.ssh/id_rsa.
	Your public key has been saved in /Users/client/.ssh/id_rsa.pub.
	The key fingerprint is:
	43:c5:5b:5f:b1:f1:50:43:ad:20:a6:92:6a:1f:9a:3a client@correorlaptop.local
	ls
	~~~
	Deben listarse 2 claves: id_rsa (privada) e id_rsa.pub (pública).


	- Copiar clave pública
	~~~
	cat ~/.ssh/id_rsa.pub
	ssh-rsa AAAAB3NzaC1yc2EAAAABIwAAAQEAklOUpkDHrfHY17SbrmTIpNLTGK9Tjom/BWDSU
	GPl+nafzlHDTYW7hdI4yZ5ew18JH4JW9jbhUFrviQzM7xlELEVf4h9lFX5QVkbPppSwg0cda3
	Pbv7kOdJ/MTyBlWXFCR+HAo3FXRitBqxiX1nKhXpHAZsMciLq8V6RjsNAQwdsdMFvSlVK/7XA
	t3FaoJoAsncM1Q9x5+3V0Ww68/eIFmb1zuUFljQJKprrX88XypNDvjYNby6vw/Pb0rwert/En
	mZ+AW4OZPnTPI89ZPmVMLuayrD2cE86Z/il8b+gw3r3+1nKatmIkjn2so1d01QraTlMqVSsbx
	NrRFi9wrf+M7Q== client@correolaptop.local
	~~~
	Pegar la información anterior en la web GitHub: Settings/SSH and GPG keys/New SSH key


- Instalar Git
~~~
sudo apt-get install git
~~~


- Configurar nuestro cliente Git
~~~
git config --global user.name "nombre_cliente"
git config --global user.mail nombre_correo@correo.com
~~~
Con la opción --global permite utilizar los datos anteriores por defecto.


- Opciones adicionales
Editor de texto
~~~
git config --global core.editor nano
~~~
Herramienta de diferencias
~~~
gif config --global merge.tool vimdiff
~~~
Ver la configuración
~~~
git config --list
~~~


- Comandos básicos
Ejecutar repositorios
~~~
mkdir primer_repositorio
cd primer_repositorio
git init
~~~


Clonar un repositorio
Comando Git clone seguido de la dirección de la página de GitHub a copiar: Clone or download/Clone with SSH
~~~
git clone git@github.com:usuario_que_copia/copia.git
~~~


Agregar ficheros
~~~
git add fichero_ejemplo.txt
git commit -m "creacion fichero_ejemplo"
git push
~~~


Cambios en tu copia local - COMMIT
~~~
git commit -am 'cambio que se ha realizado'
~~~


Ver archivos cambiados pero no subidos
~~~
git status
~~~


Enviar todos cambios
~~~
git push origin master
~~~

