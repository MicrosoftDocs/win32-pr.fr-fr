---
description: Pour qu’un client communique sur un réseau, il doit se connecter à un serveur.
ms.assetid: fb52d2b7-70fa-497a-bbb4-42b25ea9d136
title: Connexion à un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a5a81c18089bdf5f35e96aa55a8ede87dc88598a98acd3bc5ab8338afb1208
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132672"
---
# <a name="connecting-to-a-socket"></a>Connexion à un socket

Pour qu’un client communique sur un réseau, il doit se connecter à un serveur.

## <a name="to-connect-to-a-socket"></a>Pour se connecter à un socket

Appelez la fonction [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) , en passant le socket créé et la structure [**sockaddr**](sockaddr-2.md) comme paramètres. Recherchez les erreurs générales.


```C++
// Connect to server.
iResult = connect( ConnectSocket, ptr->ai_addr, (int)ptr->ai_addrlen);
if (iResult == SOCKET_ERROR) {
    closesocket(ConnectSocket);
    ConnectSocket = INVALID_SOCKET;
}

// Should really try the next address returned by getaddrinfo
// if the connect call failed
// But for this simple example we just free the resources
// returned by getaddrinfo and print an error message

freeaddrinfo(result);

if (ConnectSocket == INVALID_SOCKET) {
    printf("Unable to connect to server!\n");
    WSACleanup();
    return 1;
}
```



La fonction [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) est utilisée pour déterminer les valeurs de la structure [**sockaddr**](sockaddr-2.md) . Dans cet exemple, la première adresse IP retournée par la fonction **getaddrinfo** est utilisée pour spécifier la structure **sockaddr** transmise à la [**connexion**](/windows/desktop/api/Winsock2/nf-winsock2-connect). Si l’appel de **connexion** échoue à la première adresse IP, essayez la structure [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) suivante dans la liste liée renvoyée à partir de la fonction **getaddrinfo** .

Les informations spécifiées dans la structure [**sockaddr**](sockaddr-2.md) incluent :

-   adresse IP du serveur auquel le client essaiera de se connecter.
-   Numéro de port sur le serveur auquel le client se connectera. Ce port a été spécifié en tant que port 27015 quand le client a appelé la fonction [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .

Étape suivante : [envoi et réception de données sur le client](sending-and-receiving-data-on-the-client.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main avec Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Application cliente Winsock](winsock-client-application.md)
</dt> <dt>

[Création d’un socket pour le client](creating-a-socket-for-the-client.md)
</dt> </dl>

 

 
