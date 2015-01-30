###Ejercicio5

**Crear una máquina virtual ubuntu e instalar en ella un servidor nginx para poder acceder mediante web.**

Para ver el funcionamiento de nginx he creado 3 maquinas virtuales. Una de ellas actuara de balanceador y las otras dos de servidores.

IP balanceador:

![](./img/img5.png)

Hosts del balanceador:

![](./img/img6.png)

Una vez instalado nginx lo configuramos usando el algoritmo Round-Robin con ponderación (suponemos que la maquina1 tiene el doble de capacidad que la maquina2).

![](./img/img7.png)

Reiniciamos nginx para que se efectuen los cambios:

<pre>service nginx restart</pre>

Finalmente compobamos que balancea correctamente:

![](./img/img8.png)

Como se puede apreciar en la imagen el Servidor 1 corespondiente a la maquina1 aparace mas veces.

Para detener nginx usamos:

<pre>service nginx stop</pre>