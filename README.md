# Red con Enrutamiento Estático y dinámico
trabajos de con packet tracer que hice en redes de datos 
Diseñar y simular la siguiente red de tal manera que todos los dispositivos de la Subred1 la Subred 2 y la Subred 3 tengan conexión entre si.
Se selecciona el segmento de direcciones privadas: 100.29.128.0 /17. Diseñarla desperdiciando el mínimo posible de direcciones IPV4.
SubRed 1   10 Host
SubRed 2   550 Host
SubRed 3    210 Host
SubRed 4    2   Host
SubRed 5     2  Host
SubRed 6     2 Host.
SubRed 7     2 Host.
SubRed 8     2 Host.
Realizar los cálculos de todas las subredes
Configuras las direcciones IP en todos los host de la red.
Realizar la configuración de enrutamiento Estático en la subred 4 y subred 5
Realizar la configuración de enrutamiento Dinámico  en la subred 6, subred 7 y subred 8.

Red 2 necesita 550 hosts = usamos /22 (1024 IPs, 1022 útiles).
Red 3 necesita 210 hosts = usamos /24 (256 IPs, 254 útiles).
Red 1 necesita 10 hosts = usamos /27 (32 IPs, 30 útiles).
Redes de punto a punto (4 a 8) usan /30 = 4 IPs por subred (2 útiles).



Subred	Hosts necesarios	Hosts reales (potencia 2 - 2)	Máscara CIDR	Rango de IPs	Dirección de red	Broadcast
Red 2	550	1022 /22	/22	100.29.128.1 - 100.29.131.254	100.29.128.0	100.29.131.255
Red 3	210	254 /24	/24	100.29.132.1 - 100.29.132.254	100.29.132.0	100.29.132.255
Red 1	10	30 /27	/27	100.29.133.1 - 100.29.133.30	100.29.133.0	100.29.133.31
Red 4	2	2 /30	/30	100.29.133.33 - 100.29.133.34	100.29.133.32	100.29.133.35
Red 5	2	2 /30	/30	100.29.133.37 - 100.29.133.38	100.29.133.36	100.29.133.39
Red 6	2	2 /30	/30	100.29.133.41 - 100.29.133.42	100.29.133.40	100.29.133.43
Red 7	2	2 /30	/30	100.29.133.45 - 100.29.133.46	100.29.133.44	100.29.133.47
Red 8	2	2 /30	/30	100.29.133.49 - 100.29.133.50	100.29.133.48	100.29.133.51

