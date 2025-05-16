# NAT sobrecargado
Configurar NAT sobrecargado en el enrutador de tal forma que una trama proveniente  de la RED 1 hacia SERVER 0 la IP de origen de la trama ya no sea una de las direcciones IP de los PC de la RED 1 sino la IP asignada a la interfaz  G0/0/ 1 del Router 0

Tip:  

1. Procedimiento obtenga las IP direccionables de cada red y configurar las interfaces.

2.Configurar el enrutamiento dinámico o estático en R0 y R1.  Asegurarse que responde ping de manera directa entre los PC y el servidor.

3.Configurar el NAT en el Router R0

4.Comprobar con el modo simulación del packet tracer que cuando el paquete atraviesa el router R0 la IP de origen cambia.



Red 1  10.10.10.0/24  

Red 2   200.24.24.0/24     

Red 3   112.16.15.0/30     
