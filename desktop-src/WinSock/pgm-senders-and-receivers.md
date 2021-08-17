---
description: L’établissement d’une session PGM est semblable à la routine d’établissement de connexion associée à une session TCP.
ms.assetid: 777e0106-0314-4ec8-b064-88ceb694614b
title: Expéditeurs et destinataires PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 559ac30ace4374b48c86efeb579e1426cc455b00adb803e97244a37d8df7fda5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741066"
---
# <a name="pgm-senders-and-receivers"></a>Expéditeurs et destinataires PGM

L’établissement d’une session PGM est semblable à la routine d’établissement de connexion associée à une session TCP. La sortie significative d’une session TCP, toutefois, est que la sémantique du client et du serveur est inversée. le serveur (expéditeur PGM) se connecte à un groupe de multidiffusion, tandis que le client (récepteur PGM) attend d’accepter une connexion. Les paragraphes suivants détaillent les étapes de programmation nécessaires à la création d’un expéditeur PGM et d’un récepteur PGM. Cette page décrit également les modes de données disponibles pour les sessions PGM.

## <a name="pgm-sender"></a>Expéditeur PGM

**Pour créer un expéditeur PGM, procédez comme suit :**

1.  Créez un socket PGM.
2.  [**liez**](/windows/desktop/api/winsock/nf-winsock-bind) le socket à inaddr \_ Any.
3.  [**Connectez-vous**](/windows/desktop/api/Winsock2/nf-winsock2-connect) à l’adresse de transmission du groupe de multidiffusion.

Aucune négociation de session formelle n’est effectuée avec les clients. Le processus de connexion est similaire à une [**connexion UDP,**](/windows/desktop/api/Winsock2/nf-winsock2-connect)car il associe une adresse de point de terminaison (le groupe de multidiffusion) au socket. Une fois terminé, les données peuvent être envoyées sur le Socket.

Lorsqu’un expéditeur crée un socket PGM et le connecte à une adresse de multidiffusion, une session PGM est créée. Une session de multidiffusion fiable est définie par une combinaison de l’identificateur global unique (GUID) et du port source. Le GUID est généré par le transport. Le port sSource est spécifié par le transport, et aucun contrôle n’est fourni sur le port source utilisé.

> [!Note]  
> La réception de données sur un socket d’expéditeur n’est pas autorisée et génère une erreur.

 

L’extrait de code suivant illustre la configuration d’un expéditeur PGM :


```C++

SOCKET        s;
SOCKADDR_IN   salocal, sasession;
int           dwSessionPort;

s = socket (AF_INET, SOCK_RDM, IPPROTO_RM);

salocal.sin_family = AF_INET;
salocal.sin_port   = htons (0);    // Port is ignored here
salocal.sin_addr.s_addr = htonl (INADDR_ANY);

bind (s, (SOCKADDR *)&salocal, sizeof(salocal));

//
// Set all relevant sender socket options here
//

//
// Now, connect <entity type="hellip"/>
// Setting the connection port (dwSessionPort) has relevance, and
// can be used to multiplex multiple sessions to the same
// multicast group address over different ports
//
dwSessionPort = 0;
sasession.sin_family = AF_INET;
sasession.sin_port   = htons (dwSessionPort);
sasession.sin_addr.s_addr = inet_addr ("234.5.6.7");

connect (s, (SOCKADDR *)&sasession, sizeof(sasession));

//
// We're now ready to send data!
//



```



## <a name="pgm-receiver"></a>Récepteur PGM

**Pour créer un récepteur PGM, procédez comme suit :**

1.  Créez un socket PGM.
2.  [**liez**](/windows/desktop/api/winsock/nf-winsock-bind) le socket à l’adresse du groupe de multidiffusion sur lequel l’expéditeur transmet.
3.  Appelez la fonction [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) sur le socket pour mettre le socket en mode d’écoute. La fonction listen retourne lorsqu’une session PGM est détectée sur le port et l’adresse du groupe de multidiffusion spécifiés.
4.  Appelez la fonction [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) pour obtenir un nouveau handle de socket correspondant à la session.

Seules les données PGM d’origine (ODATA) déclenchent l’acceptation d’une nouvelle session. Par conséquent, d’autres trafics PGM (tels que les paquets SPM ou RDATA) peuvent être reçus par le transport, mais n’entraînent pas le retour de la fonction [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) .

Une fois qu’une session est acceptée, le descripteur de socket retourné est utilisé pour la réception de données.

> [!Note]  
> L’envoi de données sur un socket de réception n’est pas autorisé et génère une erreur.

 

L’extrait de code suivant illustre la configuration d’un récepteur PGM :


```C++

SOCKET        s,
              sclient;
SOCKADDR_IN   salocal,
              sasession;
int           sasessionsz, dwSessionPort;

s = socket (AF_INET, SOCK_RDM, IPPROTO_RM);

//
// The bind port (dwSessionPort) specified should match that
// which the sender specified in the connect call
//
dwSessionPort = 0;
salocal.sin_family = AF_INET;
salocal.sin_port   = htons (dwSessionPort);    
salocal.sin_addr.s_addr = inet_addr ("234.5.6.7");

bind (s, (SOCKADDR *)&salocal, sizeof(salocal));

//
// Set all relevant receiver socket options here
//

listen (s, 10);

sasessionsz = sizeof(sasession);
sclient = accept (s, (SOCKADDR *)&sasession, &sasessionsz);

//
// accept will return the client socket and we are now ready
// to receive data on the new socket!
//



```



## <a name="data-modes"></a>Modes de données

Les sessions PGM ont deux options pour les modes de données : le mode de message et le mode de diffusion en continu.

Le mode message est approprié pour les applications qui doivent envoyer des messages discrets, et est spécifié par un type de socket \_ RDM. Le mode de flux est approprié pour les applications qui doivent envoyer des données de diffusion en continu à des destinataires, tels que des applications vidéo ou vocales, et est spécifié par un type de socket de flux de chaussette \_ . Choix des effets du mode de traitement des données par Winsock.

Prenons l’exemple suivant : un expéditeur PGM en mode message effectue trois appels à la fonction [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) , chacun avec une mémoire tampon de 100 octets. Cette opération apparaît sur le câble sous forme de trois paquets PGM discrets. Du côté du récepteur, chaque appel à la fonction [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) retourne uniquement 100 octets, même si un tampon de réception plus grand est fourni. En revanche, avec un expéditeur PGM en mode flux, ces transmissions de 3 100 octets peuvent être fusionnées en moins de trois paquets physiques sur le réseau (ou fusionnés en un seul objet blob de données côté récepteur). ainsi, lorsque le récepteur appelle l’une des fonctions de réception Windows sockets, toute quantité de données reçues par le transport PGM peut être renvoyée à l’application sans tenir compte de la façon dont les données ont été physiquement transmises ou reçues.

 

 



