---
description: Pour qu’un serveur accepte les connexions clientes, il doit être lié à une adresse réseau au sein du système.
ms.assetid: d08fb1a5-af17-4116-8757-ba0a513fb323
title: Liaison d’un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc71ad25837a070074fefa2e3693c5546839ec17
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517712"
---
# <a name="binding-a-socket"></a>Liaison d’un socket

Pour qu’un serveur accepte les connexions clientes, il doit être lié à une adresse réseau au sein du système. Le code suivant montre comment lier un socket qui a déjà été créé à une adresse IP et à un port. Les applications clientes utilisent l’adresse IP et le port pour se connecter au réseau hôte.

## <a name="to-bind-a-socket"></a>Pour lier un socket

La structure [**sockaddr**](sockaddr-2.md) contient des informations sur la famille d’adresses, l’adresse IP et le numéro de port.

Appelez la fonction [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) , en passant le **Socket** créé et la structure [**sockaddr**](sockaddr-2.md) retournés à partir de la fonction [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) en tant que paramètres. Recherchez les erreurs générales.


```C++
    // Setup the TCP listening socket
    iResult = bind( ListenSocket, result->ai_addr, (int)result->ai_addrlen);
    if (iResult == SOCKET_ERROR) {
        printf("bind failed with error: %d\n", WSAGetLastError());
        freeaddrinfo(result);
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
```



Une fois la fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) appelée, les informations d’adresse retournées par la fonction [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) ne sont plus nécessaires. La fonction [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) est appelée pour libérer la mémoire allouée par la fonction **getaddrinfo** pour ces informations d’adresse.


```C++
    freeaddrinfo(result);

```



Étape suivante : [écoute sur un socket](listening-on-a-socket.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main avec Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Application de serveur Winsock](winsock-server-application.md)
</dt> <dt>

[Création d’un socket pour le serveur](creating-a-socket-for-the-server.md)
</dt> </dl>

 

 



