---
description: Le code suivant illustre les fonctions recv et Send utilisées par le serveur.
ms.assetid: 26990b06-196a-4fb1-92d8-c5fa096d2b09
title: Réception et envoi de données sur le serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ab20f074db750bef6459c6b9fcb5fd5636a522
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518185"
---
# <a name="receiving-and-sending-data-on-the-server"></a><span data-ttu-id="cafa3-103">Réception et envoi de données sur le serveur</span><span class="sxs-lookup"><span data-stu-id="cafa3-103">Receiving and Sending Data on the Server</span></span>

<span data-ttu-id="cafa3-104">Le code suivant illustre les fonctions [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) et [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) utilisées par le serveur.</span><span class="sxs-lookup"><span data-stu-id="cafa3-104">The following code demonstrates the [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) and [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) functions used by the server.</span></span>

### <a name="to-receive-and-send-data-on-a-socket"></a><span data-ttu-id="cafa3-105">Pour recevoir et envoyer des données sur un socket</span><span class="sxs-lookup"><span data-stu-id="cafa3-105">To receive and send data on a socket</span></span>


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



<span data-ttu-id="cafa3-106">Les [](/windows/desktop/api/Winsock2/nf-winsock2-send) fonctions Send [](/windows/desktop/api/winsock/nf-winsock-recv) et Receive renvoient toutes deux une valeur entière correspondant au nombre d’octets envoyés ou reçus, respectivement, ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="cafa3-106">The [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) and [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) functions both return an integer value of the number of bytes sent or received, respectively, or an error.</span></span> <span data-ttu-id="cafa3-107">Chaque fonction accepte également les mêmes paramètres : le socket actif, une mémoire tampon de **caractères** , le nombre d’octets à envoyer ou à recevoir, ainsi que tous les indicateurs à utiliser.</span><span class="sxs-lookup"><span data-stu-id="cafa3-107">Each function also takes the same parameters: the active socket, a **char** buffer, the number of bytes to send or receive, and any flags to use.</span></span>

<span data-ttu-id="cafa3-108">Étape suivante : [déconnexion du serveur](disconnecting-the-server.md)</span><span class="sxs-lookup"><span data-stu-id="cafa3-108">Next Step: [Disconnecting the Server](disconnecting-the-server.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="cafa3-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cafa3-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cafa3-110">Prise en main avec Winsock</span><span class="sxs-lookup"><span data-stu-id="cafa3-110">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="cafa3-111">Application de serveur Winsock</span><span class="sxs-lookup"><span data-stu-id="cafa3-111">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="cafa3-112">Acceptation d’une connexion</span><span class="sxs-lookup"><span data-stu-id="cafa3-112">Accepting a Connection</span></span>](accepting-a-connection.md)
</dt> </dl>

 

 



