MDOS
====

Concept
-------

MDOS est un syst�me de zombie, g�rables � partir d'une interface Web s�curis�e que je d�veloppe, permettant de diriger les zombies pour leur faire accomplir diff�rentes actions, notamment une attaque HTTP DoS et TCP SYN Flood, il faut donc pas mal de connaissances.
Il s'agit de cr�er une interface mall�able, capable d'�tre mise � jour de mani�re ais�e et de s'adapter aux connexions des clients compromis.

Fonctionnement
--------------

Pour l'attaque HTTP DoS, je pensais binder SlowLoris dans un programme en C++ ou C avec Qt ou autre, �a reste assez accessible.
Pour l'attaque TCP SYN Flood, un petit script bien fait suffira amplement.
C'est donc un syst�me client infect�\master serveur classique, � ceci pr�t que le serveur principal est en PHP (=>TCP sous protocole HTTP), donc h�bergable sur un serveur distant pour �viter la contrainte de l'IP (remonter � la source est plus facile avec des clients classiques).

Le zombie effectuera les attaques en lisant des informations � partir du master server h�berg�.
Le programme final sera donc l'interface en ligne PHP et le g�n�rateur de client.

Pour plus d'infos :
Un super cours de Polytech Grenoble sur les botnets, c'est vraiment une tuerie (plus ax� sur les architectures centralis�es) :
http://mescal.imag.f...ssi-Bremond.pdf