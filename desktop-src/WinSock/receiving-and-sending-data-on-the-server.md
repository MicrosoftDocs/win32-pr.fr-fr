---
description: Le code suivant illustre les fonctions recv et Send utilisées par le serveur.
ms.assetid: 26990b06-196a-4fb1-92d8-c5fa096d2b09
title: Réception et envoi de données sur le serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ab20f074db750bef6459c6b9fcb5fd5636a522
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403964"
---
# <a name="receiving-and-sending-data-on-the-server"></a>Réception et envoi de données sur le serveur

Le code suivant illustre les fonctions [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) et [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) utilisées par le serveur.

### <a name="to-receive-and-send-data-on-a-socket"></a>Pour recevoir et envoyer des données sur un socket


```C++
#define DEFAULT_BUFLEN 512

char recvbuf[DEFAULT_BUFLEN];
int iResult, iSendResult;
int recvbuflen = DEFAULT_BUFLEN;

// Receive until the peer shuts down the connection
do {

    iResult = recv(ClientSocket, recvbuf, recvbuflen, 0);
    if (iResult > 0) {
        printf("Bytes received: %d\n", iResult);

        // Echo the buffer back to the sender
        iSendResult = send(ClientSocket, recvbuf, iResult, 0);
        if (iSendResult == SOCKET_ERROR) {
            printf("send failed: %d\n", WSAGetLastError());
            closesocket(ClientSocket);
            WSACleanup();
            return 1;
        }
        printf("Bytes sent: %d\n", iSendResult);
    } else if (iResult == 0)
        printf("Connection closing...\n");
    else {
        printf("recv failed: %d\n", WSAGetLastError());
        closesocket(ClientSocket);
        WSACleanup();
        return 1;
    }

} while (iResult > 0);
```



Les [](/windows/desktop/api/Winsock2/nf-winsock2-send) fonctions Send [](/windows/desktop/api/winsock/nf-winsock-recv) et Receive renvoient toutes deux une valeur entière correspondant au nombre d’octets envoyés ou reçus, respectivement, ou une erreur. Chaque fonction accepte également les mêmes paramètres : le socket actif, une mémoire tampon de **caractères** , le nombre d’octets à envoyer ou à recevoir, ainsi que tous les indicateurs à utiliser.

Étape suivante : [déconnexion du serveur](disconnecting-the-server.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main avec Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Application de serveur Winsock](winsock-server-application.md)
</dt> <dt>

[Acceptation d’une connexion](accepting-a-connection.md)
</dt> </dl>

 

 



