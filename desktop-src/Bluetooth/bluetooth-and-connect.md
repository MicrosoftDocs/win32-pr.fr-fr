---
title: Bluetooth et connexion
description: Bluetooth utilise la fonction de connexion pour se connecter à un périphérique Bluetooth cible, à l’aide d’un Socket Bluetooth créé précédemment.
ms.assetid: f9ab3934-7698-4f5e-8194-cca86685a4f8
keywords:
- Bluetooth Bluetooth
- connecter Bluetooth
- Bluetooth et connexion Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b631aabbcd44d009ba30b9deb486e92a22feaec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463618"
---
# <a name="bluetooth-and-connect"></a>Bluetooth et connexion

Bluetooth utilise la fonction de [**connexion**](/windows/desktop/api/winsock2/nf-winsock2-connect) pour se connecter à un périphérique Bluetooth cible, à l’aide d’un Socket Bluetooth créé précédemment. Le paramètre *Name* de la fonction **Connect** , qui est une [**structure \_ BTH sockaddr**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) , doit spécifier un périphérique Bluetooth cible. Deux mécanismes sont utilisés pour identifier l’appareil cible :

-   La [**structure \_ BTH sockaddr**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) peut spécifier directement le numéro de port auquel une connexion est demandée. Ce mécanisme requiert que l’application exécute ses propres requêtes SDP avant de tenter une opération de [**connexion**](/windows/desktop/api/winsock2/nf-winsock2-connect) .
-   La [**structure \_ BTH sockaddr**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) peut spécifier l’ID de classe de service unique du service auquel elle souhaite se connecter. Si l’appareil homologue a plus d’un port qui correspond à l’ID de classe de service, l’appel de fonction de [**connexion**](/windows/desktop/api/winsock2/nf-winsock2-connect) se connecte au premier service valide. Ce mécanisme peut être utilisé sans requêtes SDP antérieures.

Lors de l’utilisation de la structure [**\_ BTH sockaddr**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) avec la fonction [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) , les conditions suivantes s’appliquent :

-   Le membre **btAddr** doit être une adresse de radio distante valide.
-   Pour le membre **serviceClassId** , si le membre port est égal à zéro, le système tente d’utiliser **serviceClassId** pour résoudre le port distant correspondant au service. La classe de service est un GUID 128 bits normalisé, défini par la spécification Bluetooth. Les GUID communs sont définis par le document de nombres attribués par Bluetooth. Un GUID unique peut également être utilisé pour une application spécifique à un domaine.
-   Le membre de **port** doit être un port distant valide, ou zéro si le membre **serviceClassId** est spécifié.

Le tableau suivant répertorie les codes de résultat pour Bluetooth et la fonction [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) .

| Erreur/erreur\#                    | Description                                                                        |
|----------------------------------|------------------------------------------------------------------------------------|
| WSAEISCONN10056<br/>       | Fonction [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) appelée pour un socket déjà connecté. |
| WSAEACCES10013<br/>        | Connexion de l’application demandée, mais l’authentification a échoué.        |
| WSAENOBUFS10055<br/>       | Erreur irrécupérable de mémoire insuffisante.                                                 |
| WSAEADDRINUSE10048<br/>    | Le numéro de port/de canal demandé est utilisé.                                       |
| WSAETIMEDOUT10060<br/>     | Le délai d’e/s a expiré au niveau radio Bluetooth ( \_ délai d’attente de la page).                    |
| WSAEDISCON10101<br/>       | Canal RFCOMM déconnecté par l’homologue distant.                                    |
| WSAECONNRESET10054<br/>    | Multiplexeur RFCOMM (session) déconnecté par l’homologue distant.                      |
| WSAECONNABORTED10053<br/>  | Arrêt du socket par l’application.                                                   |
| WSAENETUNREACH10051<br/>   | Erreur différente du délai d’attente au niveau du L2CAP ou de la radio Bluetooth.                       |
| WSAEHOSTDOWN10064<br/>     | RFCOMM a reçu une réponse DM.                                                   |
| WSAENETDOWN10050<br/>      | Erreur réseau inattendue.                                                          |
| WSAESHUTDOWN10058<br/>     | Canal L2CAP déconnecté par l’homologue distant.                                     |
| WSAEADDRNOTAVAIL10049<br/> | Port/canal Bluetooth ou adresse d’appareil non valide.                                |
| WSAEINVAL10022<br/>        | Plug-and-Play, un événement de pile de pilotes ou une autre erreur provoquée par un échec.                  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**entre**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> </dl>

 

