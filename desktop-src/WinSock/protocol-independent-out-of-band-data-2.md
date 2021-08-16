---
description: L’abstraction de socket de flux comprend la notion de données hors bande (OOB).
ms.assetid: 1a517885-2688-421f-9389-2d329e5c3d56
title: Protocol-Independent des données hors bande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1918ba1525462f4352d76c989d7fb5d92beeb59766f92cdccbdda66a5b82744d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860829"
---
# <a name="protocol-independent-out-of-band-data"></a>Protocol-Independent des données hors bande

L’abstraction de socket de flux comprend la notion de données hors bande (OOB). De nombreux protocoles permettent de marquer des parties de données entrantes comme spéciales d’une certaine façon, et ces blocs de données spéciaux peuvent être remis à l’utilisateur en dehors de la séquence normale. il peut s’agir, par exemple, de données expédiées dans X. 25 et d’autres protocoles OSI, et de données urgentes dans BSD UNIX l’utilisation de TCP. La section suivante décrit la gestion des données OOB de manière indépendante du protocole. Une discussion sur les données OOB implémentées à l’aide de données TCP urgentes suit l’explication indépendante du protocole. Dans chaque discussion, l’utilisation de [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) implique également [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)et [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom), et les références à [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) s’appliquent également à [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect).

## <a name="protocol-independent-oob-data"></a>Données OOB indépendantes du protocole

Les données OOB sont un canal de transmission logiquement indépendant associé à chaque paire de sockets de flux connectés. Les données OOB peuvent être fournies à l’utilisateur indépendamment des données normales. L’abstraction définit que les fonctionnalités de données OOB doivent prendre en charge la remise fiable d’au moins un bloc de données OOB à la fois. Ce bloc de données peut contenir au moins un octet de données, et au moins un bloc de données OOB peut être remis en attente à l’utilisateur à un moment donné. Pour les protocoles de communication qui prennent en charge la signalisation intrabande (tels que TCP, où les données urgentes sont fournies en séquence avec les données normales), le système extrait normalement les données OOB du flux de données normal et les stocke séparément (en laissant un intervalle dans le flux de données normal). Cela permet aux utilisateurs de choisir de recevoir les données OOB dans l’ordre et de les recevoir hors séquence sans avoir à mettre en mémoire tampon toutes les données intermédiaires. Il est possible de lire les données hors bande (OOB).

Un utilisateur peut déterminer si des données OOB sont en attente de lecture à l’aide de la fonction [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) ou [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) avec l’IOCTL **SIOCATMARK** . pour les protocoles où le concept de la position du bloc de données OOB dans le flux de données normal est explicite, tel que TCP, un fournisseur de services Windows sockets gère un marqueur conceptuel indiquant la position du dernier octet des données OOB dans le flux de données normal. Cela n’est pas nécessaire pour l’implémentation des fonctions **ioctlsocket** ou **WSAIoctl** qui prennent en charge **SIOCATMARK**. La présence ou l’absence de données OOB est obligatoire.

Pour les protocoles où le concept de la position du bloc de données OOB dans le flux de données normal est significatif, une application peut traiter les données hors bande en ligne, dans le cadre du flux de données normal. Cela est possible en définissant l’option de socket de sorte que \_ OOBINLINE avec la fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) . Pour les autres protocoles où les blocs de données OOB sont véritablement indépendants du flux de données normal, toute tentative de définition de SO \_ OOBINLINE génère une erreur. Une application peut utiliser la fonction [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) ou [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) avec l’IOCTL **SIOCATMARK** pour déterminer si des données OOB non lues sont précédées de la marque. Par exemple, il peut utiliser ces informations pour se resynchroniser avec son homologue en s’assurant que toutes les données jusqu’à la marque dans le flux de données sont ignorées lorsque cela est approprié.

Avec SO \_ OOBINLINE désactivé (paramètre par défaut) :

-   Windows Sockets notifie une application d’un \_ événement OOB FD, si l’application inscrite pour la notification avec [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect), exactement de la même façon que FD \_ Read est utilisée pour notifier la présence de données normales. Autrement dit, FD \_ OOB est publié quand des données OOB arrivent sans données OOB mises en file d’attente. La \_ file d’attente FD est également publiée lorsque les données sont lues à l’aide de l’indicateur de message \_ OOB alors que certaines données OOB restent en file d’attente après le retour de l’opération de lecture. Les \_ messages de lecture FD ne sont pas publiés pour les données OOB.
-   Windows Les sockets retournent de [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) avec le jeu de Sockets *exceptfds* approprié si les données OOB sont mises en file d’attente sur le Socket.
-   L’application peut appeler [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) avec MSG \_ OOB pour lire le bloc de données urgent à tout moment. Le bloc de données OOB déplace la file d’attente.
-   L’application peut appeler [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) sans msg \_ OOB pour lire le flux de données normal. Le bloc de données OOB n’apparaît pas dans le flux de données avec des données normales. si les données OOB restent après un appel à **recv**, Windows sockets avertit l’application avec FD \_ OOB ou avec *exceptfds* lors de l’utilisation de [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select).
-   Pour les protocoles où les données OOB ont une position dans le flux de données normal, une seule opération de [**réception**](/windows/desktop/api/winsock/nf-winsock-recv) ne couvre pas cette position. Un **recv** retourne les données normales avant la marque, et une deuxième **réception** est nécessaire pour commencer à lire les données après la marque.

Avec SO \_ OOBINLINE activé :

-   Les \_ messages OOB FD ne sont pas publiés pour les données OOB. Les données OOB sont considérées comme normales dans le cadre des fonctions [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) et [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) et sont indiquées en définissant le socket dans *readfds* ou en envoyant un \_ message FD Read respectivement.
-   L’application ne peut pas appeler [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) avec l’indicateur de message \_ OOB défini pour lire le bloc de données OOB. Le code d’erreur WSAEINVAL est retourné.
-   L’application peut appeler [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) sans l’indicateur de message \_ OOB défini. Toutes les données OOB sont remises dans le bon ordre dans le flux de données normal. Les données OOB ne sont jamais mélangées avec des données normales. Il doit y avoir trois demandes de lecture pour se trouver au-delà des données OOB. La première retourne les données normales avant le bloc de données OOB, le second retourne les données OOB, le troisième retourne les données normales qui suivent les données OOB. En d’autres termes, les limites du bloc de données OOB sont conservées.

La routine [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) est particulièrement bien adaptée pour gérer la notification de la présence de données hors bande lorsque \_ OOBINLINE est désactivé.

## <a name="oob-data-in-tcp"></a>Données OOB dans TCP

> [!IMPORTANT]
> La discussion suivante sur les données hors bande (OOB), implémentées à l’aide de données urgentes TCP, suit le modèle utilisé dans la distribution de logiciels Berkeley. Les utilisateurs et les responsables de l’implémentation doivent savoir que :

 

-   Il existe actuellement deux interprétations conflictuelles de [RFC 793](https://www.ietf.org/rfc/rfc793.txt) (où le concept est introduit).
-   L’implémentation de données OOB dans la distribution de logiciels Berkeley (BSD) n’est pas conforme aux exigences de l’ordinateur hôte spécifiées dans le [document RFC 1122](https://www.ietf.org/rfc/rfc1122.txt).

    Plus précisément, le pointeur d’urgence TCP dans BSD pointe vers l’octet qui suit l’octet de données urgent et un pointeur TCP urgent conforme aux spécifications RFC pointe vers l’octet de données urgent. Par conséquent, si une application envoie des données urgentes d’une implémentation compatible BSD à une implémentation compatible avec la norme RFC 1122, le destinataire lit l’octet de données urgent incorrect (il lit l’octet situé après l’octet correct dans le flux de données en tant qu’octet de données urgent).

    Pour réduire les problèmes d’interopérabilité, les auteurs d’applications sont invités à ne pas utiliser les données OOB, sauf si cela est nécessaire pour interagir avec un service existant. Windows Les fournisseurs de sockets sont invités à documenter la sémantique OOB (BSD ou RFC 1122) implémentée par le produit.

L’arrivée d’un segment TCP avec l’indicateur URG (pour urgent) indique l’existence d’un seul octet de données OOB dans le flux de données TCP. La taille du bloc de données OOB est d’un octet. Le pointeur urgent est un décalage positif par rapport au numéro de séquence actuel dans l’en-tête TCP qui indique l’emplacement du bloc de données OOB (ambigu, comme indiqué dans le précédent). Elle peut donc pointer vers des données qui n’ont pas encore été reçues.

Si SO \_ OOBINLINE est désactivé (valeur par défaut) lorsque le segment TCP contenant l’octet pointé par le pointeur urgent arrive, le bloc de données OOB (un octet) est supprimé du flux de données et mis en mémoire tampon. Si un segment TCP suivant arrive avec l’indicateur urgent défini (et un nouveau pointeur urgent), l’octet OOB mis en file d’attente peut être perdu, car il est remplacé par le nouveau bloc de données OOB (comme c’est le cas dans Berkeley Software Distribution). Toutefois, il n’est jamais remplacé dans le flux de données.

Si \_ OOBINLINE est activé, les données urgentes restent dans le flux de données. Par conséquent, le bloc de données OOB n’est jamais perdu lorsqu’un nouveau segment TCP arrive contenant des données urgentes. La marque de données OOB existante est mise à jour vers la nouvelle position.

> [!Note]  
> Lorsque l' \_ option de socket so OOBINLINE est définie, l’IOCTL SIOCATMARK retourne toujours la **valeur true** et les données OOB sont renvoyées à l’utilisateur sous forme de données normales.

 

 

 



