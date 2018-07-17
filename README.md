## Dojo Vagrant
Vagrant es una herramienta que nos facilita el trabajo con maquinas virtuales.

#### Requisitos:
	1. Instalar Vagrant (https://www.vagrantup.com/downloads.html)
	2. Instalar VirtualBox (https://www.virtualbox.org/wiki/Downloads)
	
**Nota:** 
	* VirtualBox necesita que Hyper visor de windows este deshabilitado.
	
	* Podrás deshabilitarlo ejecutando: bcdedit /set hypervisorlaunchtype off

	* Luego podras volver a habilitarlo ejecutando: bcdedit /set hypervisorlaunchtype auto
	siempre será necesario reiniciar Windows.
	
Con el comando 'vagrant -v'  veremos la version instalada.
Box: serán las VM que usara Vagrant.
Provider: serán por ej. VirtualBox, VMWare, Parallels, etc. 

#### Que se puede hacer con vagrant
	Con vagrant podremos hacer re-uso de VMs pre-configuradas por otros usuarios o nosotros mismos, de manera fácil y rápida.

	1. Se podrán elegir que VMs deseamos ejecutar eligiendolas en https://app.vagrantup.com (al estilo Dockerhub)
	Para descargarlas usaremos: vagrant box add [nombre-box] 
	Con el comando: 'vagrant box list'  podemos ver la lista de box descargadas
	
	2. Con el commando 'vagrant init'  se crea el Vagrantfile con las configuraciones por defecto para ejecutar una box.
		En el archivo Vagrantfile es donde configuraremos las caractericticas de nuestra VM. (ver ejemplo)
	
	3. Con 'vagrant up'    se levanta la box del Vagrantfile en el directorio que nos encontramos.
	
	4. Luego 'vagrant ssh' o 'vagrant ssh vagrant@[IP o hostname]' nos permite ingresar a la box del directorio donde estoy parado
	
	5. 'vagrant suspend ' suspende la vm (guarda estado)
	
	6. Otro comandos utiles:
		vagrant status   # estado actual de la box
		vagrant resume   # levanta la box suspendida
		vagran halt      # apaga la box
		vagrant destroy  # elimina la box 
		vagrant reload   # recarga las configuraciones modificadas en Vagrantfile en la box



	



