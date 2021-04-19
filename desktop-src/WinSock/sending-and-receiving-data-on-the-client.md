---
description: Le code suivant illustre les fonctions Send et recv utilisées par le client une fois qu’une connexion est établie.
ms.assetid: 9c6d366d-2bc6-4c92-8d0b-21c51e08ed4f
title: Envoi et réception de données sur le client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d91ee507d78bc2638a6d3f7383cd6a930651e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530666"
---
# <a name="sending-and-receiving-data-on-the-client"></a>Envoi et réception de données sur le client

Le code suivant illustre les fonctions [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) et [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) utilisées par le client une fois qu’une connexion est établie.

## <a name="client"></a>Client


```C++
#define DEFAULT_BUFLEN 512

int recvbuflen = DEFAULT_BUFLEN;

const char *sendbuf = "this is a test";
char recvbuf[DEFAULT_BUFLEN];

int iResult;

// Send an initial buffer
iResult = send(ConnectSocket, sendbuf, (int) strlen(sendbuf), 0);
if (iResult == SOCKET_ERROR) {
    printf("send failed: %d\n", WSAGetLastError());
    closesocket(ConnectSocket);
    WSACleanup();
    return 1;
}

printf("Bytes Sent: %ld\n", iResult);

// shutdown the connection for sending since no more data will be sent
// the client can still use the ConnectSocket for receiving data
iResult = shutdown(ConnectSocket, SD_SEND);
if (iResult == SOCKET_ERROR) {
    printf("shutdown failed: %d\n", WSAGetLastError());
    closesocket(ConnectSocket);
    WSACleanup();
    return 1;
}

// Receive data until the server closes the connection
do {
    iResult = recv(ConnectSocket, recvbuf, recvbuflen, 0);
    if (iResult > 0)
        printf("Bytes received: %d\n", iResult);
    else if (iResult == 0)
        printf("Connection closed\n");
    else
        printf("recv failed: %d\n", WSAGetLastError());
} while (iResult > 0);
```



Les [](/windows/desktop/api/Winsock2/nf-winsock2-send) fonctions Send [](/windows/desktop/api/winsock/nf-winsock-recv) et Receive renvoient toutes deux une valeur entière correspondant au nombre d’octets envoyés ou reçus, respectivement, ou une erreur. Chaque fonction accepte également les mêmes paramètres : le socket actif, une mémoire tampon de **caractères** , le nombre d’octets à envoyer ou à recevoir, ainsi que tous les indicateurs à utiliser.

Étape suivante : [déconnexion du client](disconnecting-the-client.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main avec Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Application cliente Winsock](winsock-client-application.md)
</dt> <dt>

[Connexion à un socket](connecting-to-a-socket.md)
</dt> </dl>

 

 



