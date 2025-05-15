# Red con Enrutamiento Estático
trabajos de con packet tracer que hice en redes de datos 

## Planteamiento:
Simular la red que se muestra en la imagen y que permita conectar los host de la red izquierda (red A) con los host de la red de la derecha  (red B) usando enrutamiento estático

1.	Usar el siguiente espacio de direcciones:
Dividir la red 100.150.64.0/18  en dos subredes
Red A 2000 host
Red B 180 host

3.	Dividir la red 30.10.50.0 /24 en 4 subredes  de 2 host y usarla para las conexiones entre los routers
4.	Configurar el enrutamiento estático para que las tramas que salen de la red A hacia la red B sigan la ruta R2 - R0 - R3
5.	Configurar el enrutamiento estático para que las tramas que salen de la red B hacia la red A sigan la ruta R3 - R1 - R2


1.	Usar el siguiente espacio de direcciones: Dividir la red 100.150.64.0/18  en dos subredes

Espacio de red principal:
100.150.64.0/18 = Tiene 16,382 hosts posibles.

Dividiremos esta en:
Red A (2000 hosts):
Necesitamos al menos 2048 direcciones (2^11).
Subred: 100.150.64.0/21 (rango: 100.150.64.1 – 100.150.71.254)

Red B (180 hosts):
Necesitamos al menos 256 direcciones (2^8).
Subred: 100.150.72.0/24 (rango: 100.150.72.1 – 100.150.72.254)

2.	Dividir la red 30.10.50.0 /24 en 4 subredes de 2 host y usarla para las conexiones entre los routers

Red: 30.10.50.0/24 = Se divide en 4 subredes de 2 hosts.

Cada subred /30 da 4 direcciones (2 para hosts):

Subred1: tiene dirección 30.10.50.0/30 (rango: 30.10.50.1 – 30.10.50.2)

Subred2: tiene dirección 30.10.50.4/30 (rango: 30.10.50.5 – 30.10.50.6)

Subred3: tiene dirección 30.10.50.8/30 (rango: 30.10.50.9 – 30.10.50.10)

Subred4: tiene dirección 30.10.50.12/30 (rango: 30.10.50.13 – 30.10.50.14)


Enrutamiento en R2
ip route 100.150.72.0 255.255.255.0 30.10.50.2

Enrutamiento en R0
ip route 100.150.72.0 255.255.255.0 30.10.50.6

ip route 100.150.64.0 255.255.248.0 30.10.50.1

Enrutamiento en R1
ip route 100.150.64.0 255.255.248.0 30.10.50.9

ip route 100.150.72.0 255.255.255.0 30.10.50.14
