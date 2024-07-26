# Communication CAN
Exemple de code en C pour utiliser SocketCAN sur Linux Linux
(forked from craigpeacock/CAN-Examples)

* Basé sur la documentation : https://www.kernel.org/doc/Documentation/networking/can.txt
* Tutoriel simplifié: https://www.beyondlogic.org/example-c-socketcan-code/
* Par défaut le port can0 est utilisé en tant que périphérique CAN.

Pour installer le bus reel CAN:
$ ip link set can0 up type can bitrate 125000

Pour installer virtuel VCAN:
$ sudo ip link add dev vcan0 type vcan 
$ sudo ifconfig vcan0 up

Pour 'Compile et Build', utiliser gcc:
$ gcc cantransmit.c -o cantransmit
$ gcc canreceive.c -o canreceive
$ gcc canfilter.c -o canfilter
