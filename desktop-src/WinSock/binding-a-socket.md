---
description: Pour qu’un serveur accepte les connexions clientes, il doit être lié à une adresse réseau au sein du système.
ms.assetid: d08fb1a5-af17-4116-8757-ba0a513fb323
title: Liaison d’un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc71ad25837a070074fefa2e3693c5546839ec17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512968"
---
# <a name="binding-a-socket"></a><span data-ttu-id="037ad-103">Liaison d’un socket</span><span class="sxs-lookup"><span data-stu-id="037ad-103">Binding a Socket</span></span>

<span data-ttu-id="037ad-104">Pour qu’un serveur accepte les connexions clientes, il doit être lié à une adresse réseau au sein du système.</span><span class="sxs-lookup"><span data-stu-id="037ad-104">For a server to accept client connections, it must be bound to a network address within the system.</span></span> <span data-ttu-id="037ad-105">Le code suivant montre comment lier un socket qui a déjà été créé à une adresse IP et à un port.</span><span class="sxs-lookup"><span data-stu-id="037ad-105">The following code demonstrates how to bind a socket that has already been created to an IP address and port.</span></span> <span data-ttu-id="037ad-106">Les applications clientes utilisent l’adresse IP et le port pour se connecter au réseau hôte.</span><span class="sxs-lookup"><span data-stu-id="037ad-106">Client applications use the IP address and port to connect to the host network.</span></span>

## <a name="to-bind-a-socket"></a><span data-ttu-id="037ad-107">Pour lier un socket</span><span class="sxs-lookup"><span data-stu-id="037ad-107">To bind a socket</span></span>

<span data-ttu-id="037ad-108">La structure [**sockaddr**](sockaddr-2.md) contient des informations sur la famille d’adresses, l’adresse IP et le numéro de port.</span><span class="sxs-lookup"><span data-stu-id="037ad-108">The [**sockaddr**](sockaddr-2.md) structure holds information regarding the address family, IP address, and port number.</span></span>

<span data-ttu-id="037ad-109">Appelez la fonction [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) , en passant le **Socket** créé et la structure [**sockaddr**](sockaddr-2.md) retournés à partir de la fonction [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) en tant que paramètres.</span><span class="sxs-lookup"><span data-stu-id="037ad-109">Call the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function, passing the created **socket** and [**sockaddr**](sockaddr-2.md) structure returned from the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function as parameters.</span></span> <span data-ttu-id="037ad-110">Recherchez les erreurs générales.</span><span class="sxs-lookup"><span data-stu-id="037ad-110">Check for general errors.</span></span>


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



<span data-ttu-id="037ad-111">Une fois la fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) appelée, les informations d’adresse retournées par la fonction [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="037ad-111">Once the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called, the address information returned by the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is no longer needed.</span></span> <span data-ttu-id="037ad-112">La fonction [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) est appelée pour libérer la mémoire allouée par la fonction **getaddrinfo** pour ces informations d’adresse.</span><span class="sxs-lookup"><span data-stu-id="037ad-112">The [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) function is called to free the memory allocated by the **getaddrinfo** function for this address information.</span></span>


```C++
    freeaddrinfo(result);

```



<span data-ttu-id="037ad-113">Étape suivante : [écoute sur un socket](listening-on-a-socket.md)</span><span class="sxs-lookup"><span data-stu-id="037ad-113">Next Step: [Listening on a Socket](listening-on-a-socket.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="037ad-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="037ad-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="037ad-115">Prise en main avec Winsock</span><span class="sxs-lookup"><span data-stu-id="037ad-115">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="037ad-116">Application de serveur Winsock</span><span class="sxs-lookup"><span data-stu-id="037ad-116">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="037ad-117">Création d’un socket pour le serveur</span><span class="sxs-lookup"><span data-stu-id="037ad-117">Creating a Socket for the Server</span></span>](creating-a-socket-for-the-server.md)
</dt> </dl>

 

 



