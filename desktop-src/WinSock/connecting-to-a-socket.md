---
description: Pour qu’un client communique sur un réseau, il doit se connecter à un serveur.
ms.assetid: fb52d2b7-70fa-497a-bbb4-42b25ea9d136
title: Connexion à un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03aa4461e1b00ba073320529d03e3b0fe32cdae1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516874"
---
# <a name="connecting-to-a-socket"></a><span data-ttu-id="1848a-103">Connexion à un socket</span><span class="sxs-lookup"><span data-stu-id="1848a-103">Connecting to a Socket</span></span>

<span data-ttu-id="1848a-104">Pour qu’un client communique sur un réseau, il doit se connecter à un serveur.</span><span class="sxs-lookup"><span data-stu-id="1848a-104">For a client to communicate on a network, it must connect to a server.</span></span>

## <a name="to-connect-to-a-socket"></a><span data-ttu-id="1848a-105">Pour se connecter à un socket</span><span class="sxs-lookup"><span data-stu-id="1848a-105">To connect to a socket</span></span>

<span data-ttu-id="1848a-106">Appelez la fonction [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) , en passant le socket créé et la structure [**sockaddr**](sockaddr-2.md) comme paramètres.</span><span class="sxs-lookup"><span data-stu-id="1848a-106">Call the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function, passing the created socket and the [**sockaddr**](sockaddr-2.md) structure as parameters.</span></span> <span data-ttu-id="1848a-107">Recherchez les erreurs générales.</span><span class="sxs-lookup"><span data-stu-id="1848a-107">Check for general errors.</span></span>


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



<span data-ttu-id="1848a-108">La fonction [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) est utilisée pour déterminer les valeurs de la structure [**sockaddr**](sockaddr-2.md) .</span><span class="sxs-lookup"><span data-stu-id="1848a-108">The [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is used to determine the values in the [**sockaddr**](sockaddr-2.md) structure.</span></span> <span data-ttu-id="1848a-109">Dans cet exemple, la première adresse IP retournée par la fonction **getaddrinfo** est utilisée pour spécifier la structure **sockaddr** transmise à la [**connexion**](/windows/desktop/api/Winsock2/nf-winsock2-connect).</span><span class="sxs-lookup"><span data-stu-id="1848a-109">In this example, the first IP address returned by the **getaddrinfo** function is used to specify the **sockaddr** structure passed to the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect).</span></span> <span data-ttu-id="1848a-110">Si l’appel de **connexion** échoue à la première adresse IP, essayez la structure [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) suivante dans la liste liée renvoyée à partir de la fonction **getaddrinfo** .</span><span class="sxs-lookup"><span data-stu-id="1848a-110">If the **connect** call fails to the first IP address, then try the next [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) structure in the linked list returned from the **getaddrinfo** function.</span></span>

<span data-ttu-id="1848a-111">Les informations spécifiées dans la structure [**sockaddr**](sockaddr-2.md) incluent :</span><span class="sxs-lookup"><span data-stu-id="1848a-111">The information specified in the [**sockaddr**](sockaddr-2.md) structure includes:</span></span>

-   <span data-ttu-id="1848a-112">adresse IP du serveur auquel le client essaiera de se connecter.</span><span class="sxs-lookup"><span data-stu-id="1848a-112">the IP address of the server that the client will try to connect to.</span></span>
-   <span data-ttu-id="1848a-113">Numéro de port sur le serveur auquel le client se connectera.</span><span class="sxs-lookup"><span data-stu-id="1848a-113">the port number on the server that the client will connect to.</span></span> <span data-ttu-id="1848a-114">Ce port a été spécifié en tant que port 27015 quand le client a appelé la fonction [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .</span><span class="sxs-lookup"><span data-stu-id="1848a-114">This port was specified as port 27015 when the client called the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function.</span></span>

<span data-ttu-id="1848a-115">Étape suivante : [envoi et réception de données sur le client](sending-and-receiving-data-on-the-client.md)</span><span class="sxs-lookup"><span data-stu-id="1848a-115">Next Step: [Sending and Receiving Data on the Client](sending-and-receiving-data-on-the-client.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="1848a-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1848a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1848a-117">Prise en main avec Winsock</span><span class="sxs-lookup"><span data-stu-id="1848a-117">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="1848a-118">Application cliente Winsock</span><span class="sxs-lookup"><span data-stu-id="1848a-118">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> <dt>

[<span data-ttu-id="1848a-119">Création d’un socket pour le client</span><span class="sxs-lookup"><span data-stu-id="1848a-119">Creating a Socket for the Client</span></span>](creating-a-socket-for-the-client.md)
</dt> </dl>

 

 
