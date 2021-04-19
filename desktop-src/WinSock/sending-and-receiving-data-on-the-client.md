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
# <a name="sending-and-receiving-data-on-the-client"></a><span data-ttu-id="62cb7-103">Envoi et réception de données sur le client</span><span class="sxs-lookup"><span data-stu-id="62cb7-103">Sending and Receiving Data on the Client</span></span>

<span data-ttu-id="62cb7-104">Le code suivant illustre les fonctions [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) et [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) utilisées par le client une fois qu’une connexion est établie.</span><span class="sxs-lookup"><span data-stu-id="62cb7-104">The following code demonstrates the [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) and [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) functions used by the client once a connection is established.</span></span>

## <a name="client"></a><span data-ttu-id="62cb7-105">Client</span><span class="sxs-lookup"><span data-stu-id="62cb7-105">Client</span></span>


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



<span data-ttu-id="62cb7-106">Les [](/windows/desktop/api/Winsock2/nf-winsock2-send) fonctions Send [](/windows/desktop/api/winsock/nf-winsock-recv) et Receive renvoient toutes deux une valeur entière correspondant au nombre d’octets envoyés ou reçus, respectivement, ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="62cb7-106">The [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) and [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) functions both return an integer value of the number of bytes sent or received, respectively, or an error.</span></span> <span data-ttu-id="62cb7-107">Chaque fonction accepte également les mêmes paramètres : le socket actif, une mémoire tampon de **caractères** , le nombre d’octets à envoyer ou à recevoir, ainsi que tous les indicateurs à utiliser.</span><span class="sxs-lookup"><span data-stu-id="62cb7-107">Each function also takes the same parameters: the active socket, a **char** buffer, the number of bytes to send or receive, and any flags to use.</span></span>

<span data-ttu-id="62cb7-108">Étape suivante : [déconnexion du client](disconnecting-the-client.md)</span><span class="sxs-lookup"><span data-stu-id="62cb7-108">Next Step: [Disconnecting the Client](disconnecting-the-client.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="62cb7-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="62cb7-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62cb7-110">Prise en main avec Winsock</span><span class="sxs-lookup"><span data-stu-id="62cb7-110">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="62cb7-111">Application cliente Winsock</span><span class="sxs-lookup"><span data-stu-id="62cb7-111">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> <dt>

[<span data-ttu-id="62cb7-112">Connexion à un socket</span><span class="sxs-lookup"><span data-stu-id="62cb7-112">Connecting to a Socket</span></span>](connecting-to-a-socket.md)
</dt> </dl>

 

 



