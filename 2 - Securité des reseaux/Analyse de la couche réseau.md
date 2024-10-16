

## Rapport d’incident en cybersécurité : Analyse de la communication au niveau réseau

### Scénario

Vous êtes analyste en cybersécurité dans une entreprise spécialisée dans la fourniture de services de conseil en informatique. Plusieurs clients ont contacté votre entreprise pour signaler qu’ils n’étaient pas en mesure d’accéder au site Web de l’entreprise www.yummyrecipesforme.com et ont vu l’erreur “port de destination inaccessible” après avoir attendu le chargement de la page.

Vous êtes chargé d’analyser la situation et de déterminer quel protocole réseau a été affecté lors de cet incident. Pour commencer, vous visitez le site Web et recevez également l’erreur “port de destination inaccessible”. Ensuite, vous chargez votre outil d’analyse réseau, tcpdump, et rechargez la page Web. Cette fois-ci, vous recevez un grand nombre de paquets dans votre analyseur réseau. L’analyseur montre que lorsque vous envoyez des paquets UDP et recevez une réponse ICMP renvoyée à votre hôte, les résultats contiennent un message d’erreur : “udp port 53 unreachable”.

![image](https://github.com/user-attachments/assets/64038366-384b-463d-abf8-88df9806a2da)


Dans les journaux DNS et ICMP, vous trouvez les informations suivantes :

Dans les deux premières lignes du fichier journal, vous voyez la demande sortante initiale de votre ordinateur vers le serveur DNS demandant l’adresse IP de yummyrecipesforme.com. Cette requête est envoyée dans un paquet UDP.

Ensuite, vous trouvez des horodatages indiquant quand l’événement s’est produit. Dans le journal, c’est la première séquence de chiffres affichée. Par exemple : 13:24:32.192571. Cela affiche l’heure 13h24m32s.

L’adresse IP source et de destination est ensuite affichée. Dans le journal d’erreur, ces informations sont affichées comme suit : 192.51.100.15.52444 > 203.0.113.2.domain. L’adresse IP à gauche du symbole supérieur (>) est l’adresse source. Dans cet exemple, la source est l’adresse IP de votre ordinateur. L’adresse IP à droite du symbole supérieur (>) est l’adresse IP de destination. Dans ce cas, il s’agit de l’adresse IP du serveur DNS : 203.0.113.2.domain.

Les deuxième et troisième lignes du journal montrent la réponse à votre requête ICMP initiale. Dans ce cas, la ligne ICMP 203.0.113.2 est le début du message d’erreur indiquant que le paquet ICMP n’a pas pu être livré au port du serveur DNS.

Ensuite, le protocole et le numéro de port sont affichés, ce qui montre quel protocole a été utilisé pour gérer les communications et à quel port il a été livré. Dans le journal d’erreur, cela apparaît comme suit : udp port 53 unreachable. Cela signifie que le protocole UDP a été utilisé pour demander une résolution de nom de domaine en utilisant l’adresse du serveur DNS sur le port 53. Le port 53, qui correspond à l’extension .domain dans 203.0.113.2.domain, est un port bien connu pour le service DNS. Le mot “inaccessible” dans le message indique que le message n’a pas été acheminé jusqu’au serveur DNS. Votre navigateur n’a pas pu obtenir l’adresse IP de yummyrecipesforme.com, dont il a besoin pour accéder au site Web, car aucun service n’écoutait sur le port DNS de réception, comme l’indique le message d’erreur ICMP “udp port 53 unreachable”.

Les lignes restantes du journal indiquent que des paquets ICMP ont été envoyés deux autres fois, mais la même erreur de livraison a été reçue à chaque fois.

Maintenant que vous avez capturé les paquets de données à l’aide d’un outil d’analyse réseau, il est de votre responsabilité d’identifier quel protocole réseau et quel service ont été impactés par cet incident. Ensuite, vous devrez rédiger un rapport de suivi.

### Résumé du problème trouvé dans le journal de trafic DNS et ICMP

Le serveur DNS est indisponible en raison de l'inaccessibilité du port 53. Le paquet ICMP indique que la requête n'a pas pu atteindre le port du serveur DNS.

Étant donné que le port 53 est couramment utilisé pour le DNS, il est probable que le problème vienne d'une absence de réponse du serveur DNS, potentiellement causée par une attaque DDoS.

Le protocole UDP confirme que le serveur DNS ne répond pas. L'analyse du réseau montre que la réponse ICMP retournait l'erreur "udp port 53 inaccessible", ce qui signifie que le port 53 du serveur DNS est injoignable.

Le problème probable est que le serveur DNS ne répond pas.

### Analyse des données et explication d’au moins une cause de l’incident

**Heure de l’incident :** 13h24.

- **Explication de la manière dont l’équipe informatique a pris connaissance de l’incident :** 

Le client a signalé à l’entreprise qu’il ne pouvait pas accéder au site Web de l’entreprise. Il a ensuite été signalé que le message sur la page Web était “port inaccessible”.

- **Explication des actions menées par le service informatique pour enquêter sur l’incident :** 

Les ingénieurs en sécurité ont vérifié la page Web et ont reçu une erreur “port inaccessible”. L’équipe a utilisé TCPdump (analyseur réseau) pour visualiser le trafic réseau autour du site Web.

- **Résultats de l’enquête du service informatique:** 

Allez sur le site Web, puis chargez la page Web tout en surveillant les réseaux via TCPdump. Il a reçu beaucoup de trafic. Des paquets UDP ont été envoyés et une réponse ICMP est retournée à l’hôte indiquant que le port 53 est inaccessible.

### Cause probable de l’incident :

- Déterminez si le port 53 fonctionne ou non. S’il est fonctionnel, vérifiez le pare-feu.

- **Pare-feu :** La capacité de bloquer le trafic réseau sur des ports spécifiques. Le blocage de ports peut être utilisé pour arrêter ou prévenir une attaque.
- **DOS :** Il pourrait y avoir un afflux d’informations envoyé au périphérique réseau pour le faire planter ou le rendre incapable de fonctionner. Le pirate pourrait désactiver le serveur DNS en utilisant une attaque DOS. Ou quelqu’un au sein de l’organisation pourrait avoir désactivé le port 53 sur les pare-feux.
