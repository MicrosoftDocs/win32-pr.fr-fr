---
description: Détails du suivi d’événements réseau Winsock
ms.assetid: f0386bd3-15d0-45f3-82c9-365d1c9f59c5
title: Détails du suivi d’événements réseau Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588363420aee9c3b04f4f8060bbd9c77b9cc3232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204123"
---
# <a name="winsock-network-event-tracing-details"></a>Détails du suivi d’événements réseau Winsock

Les informations suivantes décrivent chacun des événements réseau Winsock qui peuvent être suivis et détaillent les paramètres et les informations qui sont journalisés.

## <a name="socket-creation"></a>Création de socket

ID d’événement = 1

Niveau = 4 (informations)

Les événements Winsock suivants sont suivis pour la création de Sockets :

-   Handles de socket créés par des appels aux fonctions [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) ou [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) .
-   Handles de socket acceptés sur les sockets d’écoute.
-   Handles de socket créés par des appels à la fonction [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) .
-   Les handles de socket réutilisés par les appels aux fonctions [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) ou [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) .

Les paramètres suivants sont enregistrés pour un événement de création de socket :



| Paramètre                                                                                                        | Description                                                                            |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>                 | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/>             | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/> |
| <span id="SocketType"></span><span id="sockettype"></span><span id="SOCKETTYPE"></span>SocketType<br/>     | Type du Socket.<br/>                                                     |
| <span id="Protocol"></span><span id="protocol"></span><span id="PROTOCOL"></span>No<br/>             | Protocole du Socket.<br/>                                                 |
| <span id="UserModePid"></span><span id="usermodepid"></span><span id="USERMODEPID"></span>UserModePid<br/> | ID de processus en mode utilisateur qui a créé le Socket.<br/>                           |



 

## <a name="socket-bind"></a>Liaison de socket

ID d’événement = 2 (IPv4), ID d’événement = 3 (IPv6)

Niveau = 4 (informations)

Les événements Winsock suivants sont suivis pour une opération de liaison :

-   Liaison implicite ou explicite d’un handle de Socket.

Les paramètres suivants sont enregistrés pour un événement de liaison :



| Paramètre                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/> | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>-<br/>     | Adresse IP locale.<br/>                                                       |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Importer<br/>                 | Numéro de port de l’adresse IP locale.<br/>                                                   |
| <span id="Status"></span><span id="status"></span><span id="STATUS"></span>Statu<br/>         | État ou code d’erreur retourné pour l’opération de liaison.<br/>                   |



 

## <a name="failed-bind"></a>Échec de la liaison

ID d’événement = 40

Niveau = 4 (informations)

Les événements Winsock suivants sont suivis pour une opération de liaison qui a échoué :

-   Liaison implicite ou explicite d’un handle de socket qui échoue.

Les paramètres suivants sont enregistrés pour un événement de liaison qui a échoué :



| Paramètre                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/> | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Erreurs<br/>             | Code d’erreur retourné pour l’opération de liaison qui a échoué.<br/>                     |



 

## <a name="socket-connect"></a>Connexion de socket

ID d’événement = 4 (IPv4), ID d’événement = 5 (IPv6)

Niveau = 4 (informations)

Les événements Winsock suivants sont suivis pour une demande d’opération de connexion (appel à la fonction [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)ou [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) ) :

-   Connexion d’un socket à une destination pour un socket orienté connexion ou sans connexion.

Les paramètres suivants sont enregistrés pour un événement de connexion :



| Paramètre                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/> | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>-<br/>     | Adresse IP distante.<br/>                                                      |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Importer<br/>                 | Numéro de port de l’adresse IP distante.<br/>                                                  |



 

## <a name="connect-completed"></a>Connexion terminée

ID d’événement = 6

Niveau = 4 (informations)

Les événements Winsock suivants sont suivis pour une connexion terminée :

-   L’opération de connexion est terminée.

Les paramètres suivants sont enregistrés pour un événement Connect terminé :



| Paramètre                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/> | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Erreurs<br/>             | Code d’erreur retourné pour l’opération de connexion.<br/>                          |



 

## <a name="afd-initiated-abort"></a>Abandon AFD-Initiated

ID d’événement = 7

Niveau = 4 (informations)

Les événements Winsock suivants sont suivis pour les abandons initiés par Winsock ou les opérations d’annulation :

-   Abandon en raison de données de réception non lues mises en mémoire tampon après la fermeture.
-   Abandon après un appel à la fonction [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) avec le paramètre *How* défini sur Receive SD \_ et un appel à la fonction [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) avec received Data Pending.
-   Abandon après l’échec d’une tentative de vidage du point de terminaison.
-   Une instruction Abort après une erreur Winsock interne s’est produite.
-   Abandon en raison d’une connexion avec des erreurs et que l’application a précédemment demandé que la connexion soit abandonnée dans certaines circonstances. Il peut s’agir, par exemple, d’une application qui a défini \_ un délai d’expiration égal à zéro et dont les données ne sont toujours pas acquittées sur la connexion.
-   Abandon sur une connexion qui n’est pas entièrement associée au point de terminaison acceptant.
-   Abandon d’un appel à la fonction [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) ou [**accepted**](/windows/win32/api/mswsock/nf-mswsock-acceptex) .
-   Abandon en raison d’une opération de réception ayant échoué.
-   Abandon en raison d’un événement de Plug-and-Play.
-   Abandon en raison d’une demande de vidage ayant échoué.
-   Abandon en raison d’une demande de réception de données expédiées ayant échoué.
-   Abandon en raison d’un échec de demande d’envoi.
-   Abandon suite à l’annulation de la demande d’envoi.
-   Abandon en raison d’un annulé appelé à la fonction [**TransmitPackets**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) .

Les paramètres suivants sont journalisés pour une opération d’annulation ou d’annulation initiée par Winsock :



| Paramètre                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/> | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/> |
| <span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Donc<br/>         | Raison de l’opération d’abandon ou d’annulation.<br/>                               |



 

## <a name="transport-initiated-abort"></a>Abandon Transport-Initiated

ID d’événement = 8

Niveau = 4 (informations)

Les événements Winsock suivants sont suivis pour les opérations d’annulation ou d’annulation initiées par le transport :

-   Réinitialisation indiquée par le transport.

Les paramètres suivants sont journalisés pour une opération d’annulation ou d’annulation initiée par Winsock :



| Paramètre                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/> | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/> |
| <span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Donc<br/>         | Raison de l’opération d’abandon ou d’annulation.<br/>                               |



 

## <a name="failed-send-request"></a>Échec de la demande d’envoi

ID d’événement = 9

Niveau = 4 (informations)

Les événements Winsock suivants sont suivis pour détecter des erreurs lors des demandes [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) ou [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) :

-   Erreurs retournées en cas d’échec d' [**envoi**](/windows/desktop/api/Winsock2/nf-winsock2-send) ou de demandes [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) .

Les paramètres suivants sont enregistrés pour les demandes d’envoi qui génèrent une erreur :



| Paramètre                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/> | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Erreurs<br/>             | Code d’erreur retourné pour l’opération.<br/>                                  |



 

## <a name="failed-wsasendmsg-request"></a>Échec de la requête WsaSendMsg

ID d’événement = 10

Niveau = 4 (informations)

Les événements Winsock suivants sont suivis pour détecter les erreurs sur les demandes [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) :

-   Erreurs renvoyées lors des demandes [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) ayant échoué.

Les paramètres suivants sont enregistrés pour les demandes d’envoi qui génèrent une erreur :



| Paramètre                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/> | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Erreurs<br/>             | Code d’erreur retourné pour l’opération.<br/>                                  |



 

## <a name="failed-recv-request"></a>Échec de la demande de réception

ID d’événement = 11

Niveau = 4 (informations)

Les événements Winsock suivants sont suivis pour détecter les erreurs sur les demandes [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)ou [**WSARecvEx**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) :

-   Erreurs renvoyées lors des demandes de réception ayant échoué.

Les paramètres suivants sont enregistrés pour les demandes d’envoi qui génèrent une erreur :



| Paramètre                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/> | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Erreurs<br/>             | Code d’erreur retourné pour l’opération.<br/>                                  |



 

## <a name="failed-recvfrom-request"></a>Échec de la demande recvfrom

ID d’événement = 12

Niveau = 4 (informations)

Les événements Winsock suivants sont suivis pour détecter les erreurs sur les demandes [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) ou [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) :

-   Erreurs retournées en cas d’échec de demandes [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) ou [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) .

Les paramètres suivants sont journalisés pour une demande [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) ou [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) qui génère une erreur :



| Paramètre                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/> | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Erreurs<br/>             | Code d’erreur retourné pour l’opération.<br/>                                  |



 

## <a name="socket-close"></a>Fermeture du socket

ID d’événement = 13

Niveau = 4 (informations)

Les événements Winsock suivants sont suivis pour les opérations de fermeture de socket :

-   Un handle de socket est fermé.

Les paramètres suivants sont enregistrés pour un événement de fermeture de socket :



| Paramètre                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/> | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Erreurs<br/>             | Valeur de retour de l’opération de fermeture du Socket.<br/>                            |



 

## <a name="socket-cleanup"></a>Nettoyage de socket

ID d’événement = 14

Niveau = 4 (informations)

Les événements Winsock suivants sont suivis pour les opérations de nettoyage de socket (arrêt) :

-   La fonction [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) est appelée sur un Socket.
-   Le transport indique une déconnexion normale qui a échoué.

Les paramètres suivants sont enregistrés pour un événement de nettoyage de socket (arrêt) ou de fermeture de socket :



| Paramètre                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/> | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Erreurs<br/>             | Valeur de retour pour l’opération de nettoyage de socket (arrêt).<br/>               |



 

## <a name="socket-accept"></a>Accepter le socket

ID d’événement = 15 (IPv4), ID d’événement = 16 (IPv6)

Niveau = 4 (informations)

Les événements Winsock suivants sont suivis pour une demande [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**accepted**](/windows/win32/api/mswsock/nf-mswsock-acceptex)ou [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) de la fonction :

-   Demande de fonction [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**accepted**](/windows/win32/api/mswsock/nf-mswsock-acceptex)ou [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) sur un handle de Socket.

Les paramètres suivants sont enregistrés pour un événement Accept :



| Paramètre                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/> | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>-<br/>     | Adresse IP distante.<br/>                                                      |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Importer<br/>                 | Numéro de port de l’adresse IP distante.<br/>                                                  |
| <span id="Status"></span><span id="status"></span><span id="STATUS"></span>Statu<br/>         | État ou code d’erreur retourné pour l’opération d’acceptation.<br/>                 |



 

## <a name="accept-failed"></a>Échec de l’acceptation

ID d’événement = 17

Niveau = 4 (informations)

Les événements Winsock suivants sont suivis pour une opération d’acceptation ayant échoué :

-   Une demande [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**accepted**](/windows/win32/api/mswsock/nf-mswsock-acceptex)ou [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) sur un handle de socket qui échoue.

Les paramètres suivants sont enregistrés pour un événement d’acceptation ayant échoué :



| Paramètre                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/> | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Erreurs<br/>             | Code d’erreur retourné pour l’opération d’acceptation ayant échoué.<br/>                   |



 

## <a name="send-posted"></a>Envoi publié

ID d’événement = 18

Niveau = 5 (commentaires)

Pour diagnostiquer l’altération de la mémoire tampon de l’utilisateur (par exemple, lorsqu’une application réutilise la même mémoire tampon dans un autre appel d’envoi ou de réception alors qu’elle est toujours en cours d’utilisation), la mémoire tampon de données est journalisée lors de la publication sur Winsock et à la fin du transport sous-jacent. Les événements Winsock suivants sont suivis pour les opérations de publication de tampons d’envoi et de réception de Sockets :

-   Une application publie un envoi.
-   Une opération d’envoi se termine par Winsock.

Les paramètres suivants sont journalisés pour les opérations d’envoi de socket :



| Paramètre                                                                                                            | Description                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>                     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                                                                          |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/>                 | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/>                                                     |
| <span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath<br/>                 | Valeur booléenne qui indique si l’e/s de chemin d’accès rapide a été utilisée.<br/>                                                                       |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Nombre de mémoires tampons.<br/>                                                                                                               |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Mémoire tampon<br/>                         | Adresse virtuelle de la mémoire tampon. Pour les mémoires tampons chaînées, ce paramètre est l’adresse virtuelle du premier tampon de la chaîne.<br/> |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Longueur de la mémoire tampon. Pour les mémoires tampons chaînées, ce paramètre est le nombre total d’octets dans toutes les mémoires tampons de la chaîne.<br/>  |



 

Quand FastPath a la valeur true, l’adresse de mode utilisateur de la première mémoire tampon dans le tableau de mémoires tampons est journalisée dans le paramètre buffer. Quand FastPath a la valeur false, l’adresse de mémoire tampon du noyau Winsock est enregistrée dans le paramètre buffer.

## <a name="receive-posted"></a>Réception publiée

ID d’événement = 19

Niveau = 5 (commentaires)

Pour diagnostiquer l’altération de la mémoire tampon de l’utilisateur (par exemple, lorsqu’une application réutilise la même mémoire tampon dans un autre appel d’envoi ou de réception alors qu’elle est toujours en cours d’utilisation), la mémoire tampon de données est journalisée lors de la publication sur Winsock et à la fin du transport sous-jacent. Les événements Winsock suivants sont suivis pour les opérations de publication de tampon de réception de socket :

-   Une application publie une réception.
-   Une opération de réception se termine par Winsock.

Les paramètres suivants sont journalisés pour les opérations de réception de socket :



| Paramètre                                                                                                            | Description                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>                     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                                                                          |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/>                 | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/>                                                     |
| <span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath<br/>                 | Valeur booléenne qui indique si l’e/s de chemin d’accès rapide a été utilisée.<br/>                                                                       |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Nombre de mémoires tampons.<br/>                                                                                                               |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Mémoire tampon<br/>                         | Adresse virtuelle de la mémoire tampon. Pour les mémoires tampons chaînées, ce paramètre est l’adresse virtuelle du premier tampon de la chaîne.<br/> |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Longueur de la mémoire tampon. Pour les mémoires tampons chaînées, ce paramètre est le nombre total d’octets dans toutes les mémoires tampons de la chaîne.<br/>  |



 

Quand FastPath a la valeur true, l’adresse de mode utilisateur de la première mémoire tampon dans le tableau de mémoires tampons est journalisée dans le paramètre buffer. Quand FastPath a la valeur false, l’adresse de mémoire tampon du noyau Winsock est enregistrée dans le paramètre buffer.

## <a name="recvfrom-posted"></a>RecvFrom Posté

ID d’événement = 20

Niveau = 5 (commentaires)

Pour diagnostiquer l’altération de la mémoire tampon de l’utilisateur (par exemple, lorsqu’une application réutilise la même mémoire tampon dans un autre appel d’envoi ou de réception alors qu’elle est toujours en cours d’utilisation), la mémoire tampon de données est journalisée lors de la publication sur Winsock et à la fin du transport sous-jacent. Les événements Winsock suivants sont suivis pour une opération de publication de tampon [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) sur un socket :

-   Une application publie une opération recevoir à partir de.

Les paramètres suivants sont journalisés pour l’opération recvfrom :



| Paramètre                                                                                                            | Description                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>                     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                                                                          |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/>                 | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/>                                                     |
| <span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath<br/>                 | Valeur booléenne qui indique si l’e/s de chemin d’accès rapide a été utilisée.<br/>                                                                       |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Nombre de mémoires tampons.<br/>                                                                                                               |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Mémoire tampon<br/>                         | Adresse virtuelle de la mémoire tampon. Pour les mémoires tampons chaînées, ce paramètre est l’adresse virtuelle du premier tampon de la chaîne.<br/> |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Longueur de la mémoire tampon. Pour les mémoires tampons chaînées, ce paramètre est le nombre total d’octets dans toutes les mémoires tampons de la chaîne.<br/>  |



 

Quand FastPath a la valeur true, l’adresse de mode utilisateur de la première mémoire tampon dans le tableau de mémoires tampons est journalisée dans le paramètre buffer. Quand FastPath a la valeur false, l’adresse de mémoire tampon du noyau Winsock est enregistrée dans le paramètre buffer.

## <a name="sendto-posted"></a>SendTo envoyé

ID d’événement = 21 (IPv4), ID d’événement = 22 (IPv6)

Niveau = 5 (commentaires)

Pour diagnostiquer l’altération de la mémoire tampon de l’utilisateur (par exemple, lorsqu’une application réutilise la même mémoire tampon dans un autre appel d’envoi ou de réception alors qu’elle est toujours en cours d’utilisation), la mémoire tampon de données est journalisée lors de la publication sur Winsock et à la fin du transport sous-jacent. Les événements Winsock suivants sont suivis pour une opération de publication de mémoire tampon [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) sur un socket :

-   Une application publie un envoi à partir de.

Les paramètres suivants sont enregistrés pour l’opération [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) :



| Paramètre                                                                                                            | Description                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>                     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                                                                          |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/>                 | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/>                                                     |
| <span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath<br/>                 | Valeur booléenne qui indique si l’e/s de chemin d’accès rapide a été utilisée.<br/>                                                                       |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Nombre de mémoires tampons.<br/>                                                                                                               |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Mémoire tampon<br/>                         | Adresse virtuelle de la mémoire tampon. Pour les mémoires tampons chaînées, ce paramètre est l’adresse virtuelle du premier tampon de la chaîne.<br/> |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Longueur de la mémoire tampon. Pour les mémoires tampons chaînées, ce paramètre est le nombre total d’octets dans toutes les mémoires tampons de la chaîne.<br/>  |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>-<br/>                     | Adresse IP distante du Socket.<br/>                                                                                            |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Importer<br/>                                 | Numéro de port IP distant du Socket.<br/>                                                                                        |



 

Quand FastPath a la valeur true, l’adresse de mode utilisateur de la première mémoire tampon dans le tableau de mémoires tampons est journalisée dans le paramètre buffer. Quand FastPath a la valeur false, l’adresse de mémoire tampon du noyau Winsock est enregistrée dans le paramètre buffer.

## <a name="recv-completed"></a>Réception terminée

ID d’événement = 23

Niveau = 5 (commentaires)

Pour diagnostiquer l’altération de la mémoire tampon de l’utilisateur (par exemple, lorsqu’une application réutilise la même mémoire tampon dans un autre appel d’envoi ou de réception alors qu’elle est toujours en cours d’utilisation), la mémoire tampon de données est journalisée lors de la publication sur Winsock et à la fin du transport sous-jacent. Les événements Winsock suivants sont suivis pour les opérations de réception de socket terminées :

-   Une opération d’envoi se termine au transport.
-   Une opération de réception se termine au transport.

Les paramètres suivants sont enregistrés pour une opération d’envoi terminée ou de réception terminée :



| Paramètre                                                                                                            | Description                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>                     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                                                                                   |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/>                 | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/>                                                              |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Mémoire tampon<br/>                         | Adresse virtuelle de la mémoire tampon. Pour les mémoires tampons chaînées, ce paramètre est l’adresse virtuelle du premier tampon de la chaîne.<br/>          |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Longueur de la mémoire tampon d’octets reçus. Pour les mémoires tampons chaînées, ce paramètre est le nombre total d’octets reçus dans toutes les mémoires tampons de la chaîne.<br/> |



 

## <a name="send-completed"></a>Envoi terminé

ID d’événement = 24

Niveau = 5 (commentaires)

Pour diagnostiquer l’altération de la mémoire tampon de l’utilisateur (par exemple, lorsqu’une application réutilise la même mémoire tampon dans un autre appel d’envoi ou de réception alors qu’elle est toujours en cours d’utilisation), la mémoire tampon de données est journalisée lors de la publication sur Winsock et à la fin du transport sous-jacent. Les événements Winsock suivants sont suivis pour les opérations d’envoi de socket terminées :

-   Une opération d’envoi se termine au transport.

Les paramètres suivants sont enregistrés pour une opération d’envoi terminée :



| Paramètre                                                                                                            | Description                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>                     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                                                                             |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/>                 | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/>                                                        |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Mémoire tampon<br/>                         | Adresse virtuelle de la mémoire tampon. Pour les mémoires tampons chaînées, ce paramètre est l’adresse virtuelle du premier tampon de la chaîne.<br/>    |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Longueur de la mémoire tampon d’octets envoyés. Pour les mémoires tampons chaînées, ce paramètre représente le nombre total d’octets envoyés de toutes les mémoires tampons de la chaîne.<br/> |



 

## <a name="sendmsg-completed"></a>SendMsg terminé

ID d’événement = 25

Niveau = 5 (commentaires)

Pour diagnostiquer l’altération de la mémoire tampon de l’utilisateur (par exemple, lorsqu’une application réutilise la même mémoire tampon dans un autre appel d’envoi ou de réception alors qu’elle est toujours en cours d’utilisation), la mémoire tampon de données est journalisée lors de la publication sur Winsock et à la fin du transport sous-jacent. Les événements Winsock suivants sont suivis lorsqu’une opération de publication de tampon [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) se termine sur un socket :

-   Une application effectue une opération [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) .

Les paramètres suivants sont enregistrés pour la fin du [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) :



| Paramètre                                                                                                            | Description                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>                     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                                                                             |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/>                 | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/>                                                        |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Nombre de mémoires tampons.<br/>                                                                                                                  |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Mémoire tampon<br/>                         | Adresse virtuelle de la mémoire tampon. Pour les mémoires tampons chaînées, ce paramètre est l’adresse virtuelle du premier tampon de la chaîne.<br/>    |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Longueur de la mémoire tampon d’octets envoyés. Pour les mémoires tampons chaînées, ce paramètre représente le nombre total d’octets envoyés de toutes les mémoires tampons de la chaîne.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>-<br/>                     | Adresse IP distante du Socket.<br/>                                                                                               |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Importer<br/>                                 | Numéro de port IP distant du Socket.<br/>                                                                                           |



 

## <a name="recvfrom-completed"></a>RecvFrom terminé

ID d’événement = 26 (IPv4), ID d’événement = 27 (IPv6)

Niveau = 5 (commentaires)

Pour diagnostiquer l’altération de la mémoire tampon de l’utilisateur (par exemple, lorsqu’une application réutilise la même mémoire tampon dans un autre appel d’envoi ou de réception alors qu’elle est toujours en cours d’utilisation), la mémoire tampon de données est journalisée lors de la publication sur Winsock et à la fin du transport sous-jacent. Les événements Winsock suivants sont suivis lorsqu’une opération de publication de mémoire tampon [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) se termine sur un socket :

-   Une application effectue une opération [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) .

Les paramètres suivants sont enregistrés pour la fin du [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) :



| Paramètre                                                                                                            | Description                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>                     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                                                                                   |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/>                 | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/>                                                              |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Nombre de mémoires tampons.<br/>                                                                                                                        |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Mémoire tampon<br/>                         | Adresse virtuelle de la mémoire tampon. Pour les mémoires tampons chaînées, ce paramètre est l’adresse virtuelle du premier tampon de la chaîne.<br/>          |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Longueur de la mémoire tampon d’octets reçus. Pour les mémoires tampons chaînées, ce paramètre est le nombre total d’octets reçus dans toutes les mémoires tampons de la chaîne.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>-<br/>                     | Adresse IP distante du Socket.<br/>                                                                                                     |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Importer<br/>                                 | Numéro de port IP distant du Socket.<br/>                                                                                                 |



 

## <a name="sendto-completed"></a>SendTo terminé

ID d’événement = 28

Niveau = 5 (commentaires)

Pour diagnostiquer l’altération de la mémoire tampon de l’utilisateur (par exemple, lorsqu’une application réutilise la même mémoire tampon dans un autre appel d’envoi ou de réception alors qu’elle est toujours en cours d’utilisation), la mémoire tampon de données est journalisée lors de la publication sur Winsock et à la fin du transport sous-jacent. Les événements Winsock suivants sont suivis lorsqu’une opération de publication de mémoire tampon [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) se termine sur un socket :

-   Une application effectue une opération [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) .

Les paramètres suivants sont enregistrés pour la fin de l’exécution de l’opération [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) :



| Paramètre                                                                                                            | Description                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>                     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                                                                             |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/>                 | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/>                                                        |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Nombre de mémoires tampons.<br/>                                                                                                                  |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Mémoire tampon<br/>                         | Adresse virtuelle de la mémoire tampon. Pour les mémoires tampons chaînées, ce paramètre est l’adresse virtuelle du premier tampon de la chaîne.<br/>    |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Longueur de la mémoire tampon d’octets envoyés. Pour les mémoires tampons chaînées, ce paramètre représente le nombre total d’octets envoyés de toutes les mémoires tampons de la chaîne.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>-<br/>                     | Adresse IP distante du Socket.<br/>                                                                                               |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Importer<br/>                                 | Numéro de port IP distant du Socket.<br/>                                                                                           |



 

## <a name="socket-option-set"></a>Ensemble d’options de socket

ID d’événement = 29

Niveau = 5 (commentaires)

Chaque fois qu’une application modifie certaines valeurs d’option de socket et les IOCTL, les nouvelles valeurs sont consignées. Les options journalisées peuvent être utilisées pour diagnostiquer des performances médiocres ou un comportement étrange dans les applications. Les événements Winsock suivants sont suivis pour certaines options de socket et IOCTL :

-   \_SNDBUF change donc.
-   \_RCVBUF change donc.
-   FIONBIO
-   SIO \_ activer \_ la \_ file d’attente circulaire
-   SIO \_ UDP \_ CONNRESET
-   \_OOBINLINE

Les paramètres suivants sont consignés pour les appels de fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) et [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) qui modifient les valeurs ci-dessus :



| Paramètre                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/> | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/> |
| <span id="Option"></span><span id="option"></span><span id="OPTION"></span>Option<br/>         | Option de socket ou IOCTL modifiée. <br/>                                |
| <span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée<br/>             | Nouvelle valeur pour l’option de socket ou ioctl. <br/>                              |



 

## <a name="selectpoll-posted"></a>Sélection/interrogation publiée

ID d’événement = 30

Niveau = 5 (commentaires)

Les événements Winsock suivants sont suivis lorsqu’une application appelle la fonction [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) :

-   L’application publie une requête [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .

Les paramètres suivants sont enregistrés pour les événements [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) :



| Paramètre                                                                                                        | Description                                                                                                    |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>                 | ID du processus propriétaire.<br/>                                                                              |
| <span id="HandleCount"></span><span id="handlecount"></span><span id="HANDLECOUNT"></span>HandleCount<br/> | Nombre de handles passés par l’application (valide uniquement sur l’événement de lancement).<br/>            |
| <span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>Expiré<br/>                 | Durée d’attente maximale de la fonction [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .<br/> |



 

## <a name="selectpoll-completed"></a>Sélection/interrogation terminée

ID d’événement = 31

Niveau = 5 (commentaires)

Les événements Winsock suivants sont suivis lorsqu’une application appelle la fonction [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) :

-   Winsock termine un appel [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .

Les paramètres suivants sont journalisés lors de l’exécution d’une opération [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) :



| Paramètre                                                                                            | Description                                                                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                                              |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/> | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/>                         |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Erreurs<br/>             | Code d’erreur retourné pour l’opération [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .<br/> |



 

## <a name="wsaeventselect"></a>WSAEventSelect

ID d’événement = 32

Niveau = 5 (commentaires)

Les événements Winsock suivants sont suivis lorsqu’une application appelle la fonction [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) :

-   Consignez le masque d’événement passé dans la fonction [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) .

Les paramètres suivants sont consignés pour les appels de fonction [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) :



| Paramètre                                                                                                | Description                                                                            |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>         | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/>     | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/> |
| <span id="EventMask"></span><span id="eventmask"></span><span id="EVENTMASK"></span>EventMask<br/> | Valeur du masque d’événement. <br/>                                              |



 

## <a name="dropped-datagram"></a>Datagramme supprimé

ID d’événement = 33 (IPv4), ID d’événement = 34 (IPv6)

Niveau = 5 (commentaires)

Pour faciliter le diagnostic des problèmes concernant les applications de datagramme, les événements Winsock suivants sont suivis :

-   Lorsqu’un datagramme arrive et qu’il est supprimé, l’espace de mémoire tampon est insuffisant.
-   Sur un datagramme connecté, si les données arrivent d’une source autre que la destination connectée.

Les paramètres suivants sont journalisés pour les datagrammes supprimés :



| Paramètre                                                                                                    | Description                                                                            |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>             | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/>         | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/> |
| <span id="PacketSize"></span><span id="packetsize"></span><span id="PACKETSIZE"></span>Taille paquet<br/> | Taille du paquet qui a été supprimé. <br/>                                   |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>-<br/>             | Adresse IP de la source du paquet. <br/>                                |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Importer<br/>                         | Numéro de port IP de la source du paquet.<br/>                             |
| <span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Donc<br/>                 | Code d’erreur ou raison de la suppression du paquet.<br/>                            |



 

## <a name="connection-indicated"></a>Connexion indiquée

ID d’événement = 35 (IPv4), ID d’événement = 36 (IPv6)

Niveau = 5 (commentaires)

Les événements Winsock suivants sont suivis pour les opérations indiquées par la connexion :

-   Une application reçoit une demande de connexion.

Les paramètres suivants sont consignés pour les connexions indiquées à partir d’événements de transport :



| Paramètre                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/> | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>-<br/>     | Adresse IP distante. <br/>                                                     |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Importer<br/>                 | Numéro de port de l’adresse IP distante.<br/>                                                  |



 

## <a name="data-indicated"></a>Données indiquées

ID d’événement = 37

Niveau = 5 (commentaires)

Les événements Winsock suivants sont suivis pour les opérations indiquées par les données :

-   Une application reçoit des données sur un socket connecté.

Les paramètres suivants sont enregistrés pour les données indiquées à partir des événements de transport :



| Paramètre                                                                                                                        | Description                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>                                 | ID du processus propriétaire.<br/>                                                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/>                             | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/> |
| <span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Octets indiqués<br/> | Nombre d’octets reçus sur le Socket.<br/>                                 |



 

## <a name="data-indicated-from-transport"></a>Données indiquées à partir du transport

ID d’événement = 38 (IPv4), ID d’événement = 39 (IPv6)

Niveau = 5 (commentaires)

Les événements Winsock suivants sont suivis pour les données indiquées à partir des opérations de transport :

-   Une application publie une demande de réception et reçoit des données.

Les paramètres suivants sont enregistrés pour les données indiquées à partir des événements de transport :



| Paramètre                                                                                                                        | Description                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>                                 | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/>                             | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>-<br/>                                 | Adresse IP distante. <br/>                                                     |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Importer<br/>                                             | Numéro de port de l’adresse IP distante.<br/>                                                  |
| <span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Octets indiqués<br/> | Nombre d’octets reçus sur le Socket.<br/>                                 |



 

## <a name="disconnect-indicated-from-transport"></a>Déconnexion indiquée à partir du transport

ID d’événement = 41

Niveau = 5 (commentaires)

Les événements Winsock suivants sont suivis pour les opérations de déconnexion indiquées :

-   Une application reçoit une indication de déconnexion.

Les paramètres suivants sont enregistrés pour la déconnexion indiqué à partir des événements de transport :



| Paramètre                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Traiter<br/>     | Adresse de la structure EPROCESS du noyau pour le processus.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste<br/> | Adresse de socket du noyau Winsock utilisée comme identificateur unique pour un Socket.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôle du suivi Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Suivi Winsock](winsock-tracing.md)
</dt> <dt>

[Détails du suivi de modification du catalogue Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[Niveaux de suivi Winsock](winsock-tracing-levels.md)
</dt> </dl>

 

 
