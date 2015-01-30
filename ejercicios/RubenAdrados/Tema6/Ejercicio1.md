###Ejercicio1

[Debian]:https://wiki.debian.org/KVM#Installation
[Ubuntu]:https://help.ubuntu.com/community/KVM/Installation

**Instalar los paquetes necesarios para usar KVM. Se pueden seguir estas instrucciones para Debian o estas otras para Ubuntu. **

Primero de todo debemos comprobar si el nucleo instalado en nuestro ordenador contiene este modulo. Para ello usamos la siguiente orden:

<pre>kmv-ok</pre>

Podemos observar en la captura que efectivamente lo soporta.

![](./img/img1.png)

Comenzamos la instalación (Ubuntu en mi caso):

<pre>sudo apt-get install qemu-kvm libvirt-bin ubuntu-vm-builder bridge-utils</pre>

Para añadir nuestro usuario a los grupos introducimos:

<pre>sudo adduser `id -un` libvirtd</pre>

<pre>sudo adduser `id -un` kvm</pre>

Para verificar que la instalación se ha hecho correctamente podemos comprobarlo usando:

<pre>virsh -c qemu:///system list</pre>