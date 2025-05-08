# Diseño de redes IPV4 de diferente tamaño en packetracer

Planteamiento:
Tengo una red con bloque IPv4:  30.30.192.0 /18   Se requiere dividirla en 3 subredes: 
1 subred de 620 Host, 
1 subred de 3100 Hosts
1 subred de 16 Host. 
1. Calcule los rangos de direccionamiento para las 3 subredes.
3100 hosts se necesita mínimo 3102 = 2^12 = 4096 direcciones = /20
620 hosts se necesita mínimo 622 = 2^10 = 1024 direcciones = /22
16 hosts se necesita mínimo 18 = 2^5 = 32 direcciones = /27

2. Asignar bloques desde la red 30.30.192.0/18. 
La red 30.30.192.0/18 va desde 30.30.192.0 hasta 30.30.255.255.

Subred A (3100 hosts, /20)
	Rango: 30.30.192.0/20
	IPs disponibles: 4096 (de 30.30.192.0 a 30.30.207.255)
Subred B (620 hosts, /22)
	Siguiente bloque libre: 30.30.208.0/22
	IPs disponibles: 1024 (de 30.30.208.0 a 30.30.211.255)
Subred C (16 hosts, /27)
	Siguiente bloque libre: 30.30.212.0/27
	IPs disponibles: 32 (de 30.30.212.0 a 30.30.212.31)
