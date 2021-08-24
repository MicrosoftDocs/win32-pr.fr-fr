---
title: Bluetooth et se connecter
description: Bluetooth utilise la fonction connect pour se connecter à un appareil Bluetooth cible, à l’aide d’un socket Bluetooth créé précédemment.
ms.assetid: f9ab3934-7698-4f5e-8194-cca86685a4f8
keywords:
- Bluetooth Bluetooth
- se connecter Bluetooth
- Bluetooth et se connecter Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d38e00456b3174c49676e081a0fa6188da13fd54f8e07940edcf703e7f5b680d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588459"
---
# <a name="bluetooth-and-connect"></a>Bluetooth et se connecter

Bluetooth utilise la fonction [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) pour se connecter à un appareil Bluetooth cible, à l’aide d’un socket Bluetooth créé précédemment. le paramètre *name* de la fonction **connect** , qui est une [**structure \_ BTH SOCKADDR**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) , doit spécifier un appareil Bluetooth cible. Deux mécanismes sont utilisés pour identifier l’appareil cible :

-   La [**structure \_ BTH sockaddr**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) peut spécifier directement le numéro de port auquel une connexion est demandée. Ce mécanisme requiert que l’application exécute ses propres requêtes SDP avant de tenter une opération de [**connexion**](/windows/desktop/api/winsock2/nf-winsock2-connect) .
-   La [**structure \_ BTH sockaddr**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) peut spécifier l’ID de classe de service unique du service auquel elle souhaite se connecter. Si l’appareil homologue a plus d’un port qui correspond à l’ID de classe de service, l’appel de fonction de [**connexion**](/windows/desktop/api/winsock2/nf-winsock2-connect) se connecte au premier service valide. Ce mécanisme peut être utilisé sans requêtes SDP antérieures.

Lors de l’utilisation de la structure [**\_ BTH sockaddr**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) avec la fonction [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) , les conditions suivantes s’appliquent :

-   Le membre **btAddr** doit être une adresse de radio distante valide.
-   Pour le membre **serviceClassId** , si le membre port est égal à zéro, le système tente d’utiliser **serviceClassId** pour résoudre le port distant correspondant au service. la classe de service est un GUID 128 bits normalisé, défini par la spécification Bluetooth. les guid communs sont définis par le Bluetooth document de nombres affectés. Un GUID unique peut également être utilisé pour une application spécifique à un domaine.
-   Le membre de **port** doit être un port distant valide, ou zéro si le membre **serviceClassId** est spécifié.

le tableau suivant répertorie les codes de résultat pour Bluetooth et la fonction [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) .

| Erreur/erreur\#                    | Description                                                                        |
|----------------------------------|------------------------------------------------------------------------------------|
| WSAEISCONN10056<br/>       | Fonction [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) appelée pour un socket déjà connecté. |
| WSAEACCES10013<br/>        | Connexion de l’application demandée, mais l’authentification a échoué.        |
| WSAENOBUFS10055<br/>       | Erreur irrécupérable de mémoire insuffisante.                                                 |
| WSAEADDRINUSE10048<br/>    | Le numéro de port/de canal demandé est utilisé.                                       |
| WSAETIMEDOUT10060<br/>     | le délai d’e/s a expiré au niveau radio Bluetooth ( \_ délai d’attente de la PAGE).                    |
| WSAEDISCON10101<br/>       | Canal RFCOMM déconnecté par l’homologue distant.                                    |
| WSAECONNRESET10054<br/>    | Multiplexeur RFCOMM (session) déconnecté par l’homologue distant.                      |
| WSAECONNABORTED10053<br/>  | Arrêt du socket par l’application.                                                   |
| WSAENETUNREACH10051<br/>   | erreur différente du délai d’attente au niveau de la radio L2CAP ou Bluetooth.                       |
| WSAEHOSTDOWN10064<br/>     | RFCOMM a reçu une réponse DM.                                                   |
| WSAENETDOWN10050<br/>      | Erreur réseau inattendue.                                                          |
| WSAESHUTDOWN10058<br/>     | Canal L2CAP déconnecté par l’homologue distant.                                     |
| WSAEADDRNOTAVAIL10049<br/> | port/canal ou adresse de l’appareil Bluetooth non valide.                                |
| WSAEINVAL10022<br/>        | Plug-and-Play, un événement de pile de pilotes ou une autre erreur provoquée par un échec.                  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**entre**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> </dl>

 

