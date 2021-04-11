---
description: Après l’initialisation, un objet SOCKET doit être instancié pour être utilisé par le serveur.
ms.assetid: 2f3a7cab-3296-41ec-ac7e-224655b92a7c
title: Création d’un socket pour le serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd3fb00cb8b1155f4d26d94c9a88328256effe23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113090"
---
# <a name="creating-a-socket-for-the-server"></a><span data-ttu-id="55273-103">Création d’un socket pour le serveur</span><span class="sxs-lookup"><span data-stu-id="55273-103">Creating a Socket for the Server</span></span>

<span data-ttu-id="55273-104">Après l’initialisation, un objet **Socket** doit être instancié pour être utilisé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="55273-104">After initialization, a **SOCKET** object must be instantiated for use by the server.</span></span>

<span data-ttu-id="55273-105">**Pour créer un socket pour le serveur**</span><span class="sxs-lookup"><span data-stu-id="55273-105">**To create a socket for the server**</span></span>

1.  <span data-ttu-id="55273-106">La fonction [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) est utilisée pour déterminer les valeurs de la structure [**sockaddr**](sockaddr-2.md) :</span><span class="sxs-lookup"><span data-stu-id="55273-106">The [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is used to determine the values in the [**sockaddr**](sockaddr-2.md) structure:</span></span>

    -   <span data-ttu-id="55273-107">**AF \_ INET** est utilisé pour spécifier la famille d’adresses IPv4.</span><span class="sxs-lookup"><span data-stu-id="55273-107">**AF\_INET** is used to specify the IPv4 address family.</span></span>
    -   <span data-ttu-id="55273-108">**Chaussette \_ STREAM** est utilisé pour spécifier un socket de flux.</span><span class="sxs-lookup"><span data-stu-id="55273-108">**SOCK\_STREAM** is used to specify a stream socket.</span></span>
    -   <span data-ttu-id="55273-109">**IPPROTO \_ TCP** est utilisé pour spécifier le protocole TCP.</span><span class="sxs-lookup"><span data-stu-id="55273-109">**IPPROTO\_TCP** is used to specify the TCP protocol .</span></span>
    -   <span data-ttu-id="55273-110">**IA \_ Indicateur passif** indique que l’appelant a l’intention d’utiliser la structure d’adresse de socket retournée dans un appel à la fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) .</span><span class="sxs-lookup"><span data-stu-id="55273-110">**AI\_PASSIVE** flag indicates the caller intends to use the returned socket address structure in a call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function.</span></span> <span data-ttu-id="55273-111">Lorsque l’indicateur **ai \_ passif** est défini et que le paramètre *nodename* à la fonction [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) est un pointeur **null** , la partie adresse IP de la structure de l’adresse du socket est définie sur **inadr \_ any** pour les adresses IPv4 ou **IN6ADDR \_ Any \_ init** pour les adresses IPv6.</span><span class="sxs-lookup"><span data-stu-id="55273-111">When the **AI\_PASSIVE** flag is set and *nodename* parameter to the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is a **NULL** pointer, the IP address portion of the socket address structure is set to **INADDR\_ANY** for IPv4 addresses or **IN6ADDR\_ANY\_INIT** for IPv6 addresses.</span></span>
    -   <span data-ttu-id="55273-112">27015 est le numéro de port associé au serveur auquel le client se connectera.</span><span class="sxs-lookup"><span data-stu-id="55273-112">27015 is the port number associated with the server that the client will connect to.</span></span>

    <span data-ttu-id="55273-113">La structure [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) est utilisée par la fonction [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .</span><span class="sxs-lookup"><span data-stu-id="55273-113">The [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) structure is used by the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function.</span></span>

    ```C++
    #define DEFAULT_PORT "27015"

    struct addrinfo *result = NULL, *ptr = NULL, hints;

    ZeroMemory(&hints, sizeof (hints));
    hints.ai_family = AF_INET;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    hints.ai_flags = AI_PASSIVE;

    // Resolve the local address and port to be used by the server
    iResult = getaddrinfo(NULL, DEFAULT_PORT, &hints, &result);
    if (iResult != 0) {
        printf("getaddrinfo failed: %d\n", iResult);
        WSACleanup();
        return 1;
    }
    ```

    

2.  <span data-ttu-id="55273-114">Créez un objet **Socket** appelé ListenSocket pour que le serveur écoute les connexions clientes.</span><span class="sxs-lookup"><span data-stu-id="55273-114">Create a **SOCKET** object called ListenSocket for the server to listen for client connections.</span></span>
    ```C++
    SOCKET ListenSocket = INVALID_SOCKET;
    ```

    

3.  <span data-ttu-id="55273-115">Appelez la fonction [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) et retournez sa valeur à la variable ListenSocket.</span><span class="sxs-lookup"><span data-stu-id="55273-115">Call the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function and return its value to the ListenSocket variable.</span></span> <span data-ttu-id="55273-116">Pour cette application serveur, utilisez la première adresse IP retournée par l’appel à [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) qui correspondait à la famille d’adresses, au type de socket et au protocole spécifiés dans le paramètre *Hints* .</span><span class="sxs-lookup"><span data-stu-id="55273-116">For this server application, use the first IP address returned by the call to [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) that matched the address family, socket type, and protocol specified in the *hints* parameter.</span></span> <span data-ttu-id="55273-117">Dans cet exemple, un socket de flux TCP pour IPv4 a été demandé avec une famille d’adresses IPv4, un type de socket de flux de chaussette \_ et un protocole de \_ TCP IPPROTO.</span><span class="sxs-lookup"><span data-stu-id="55273-117">In this example, a TCP stream socket for IPv4 was requested with an address family of IPv4, a socket type of SOCK\_STREAM and a protocol of IPPROTO\_TCP.</span></span> <span data-ttu-id="55273-118">Une adresse IPv4 est donc demandée pour le ListenSocket.</span><span class="sxs-lookup"><span data-stu-id="55273-118">So an IPv4 address is requested for the ListenSocket.</span></span>

    <span data-ttu-id="55273-119">Si l’application serveur souhaite écouter IPv6, la famille d’adresses doit être définie sur AF \_ inet6 dans le paramètre *Hints* .</span><span class="sxs-lookup"><span data-stu-id="55273-119">If the server application wants to listen on IPv6, then the address family needs to be set to AF\_INET6 in the *hints* parameter.</span></span> <span data-ttu-id="55273-120">Si un serveur souhaite écouter à la fois IPv6 et IPv4, deux sockets d’écoute doivent être créés, un pour IPv6 et un pour IPv4.</span><span class="sxs-lookup"><span data-stu-id="55273-120">If a server wants to listen on both IPv6 and IPv4, two listen sockets must be created, one for IPv6 and one for IPv4.</span></span> <span data-ttu-id="55273-121">Ces deux sockets doivent être gérés séparément par l’application.</span><span class="sxs-lookup"><span data-stu-id="55273-121">These two sockets must be handled separately by the application.</span></span>

    <span data-ttu-id="55273-122">Windows Vista et les versions ultérieures offrent la possibilité de créer un seul socket IPv6 mis en mode pile double pour écouter à la fois IPv6 et IPv4.</span><span class="sxs-lookup"><span data-stu-id="55273-122">Windows Vista and later offer the ability to create a single IPv6 socket that is put in dual stack mode to listen on both IPv6 and IPv4.</span></span> <span data-ttu-id="55273-123">Pour plus d’informations sur cette fonctionnalité, consultez [sockets à double pile](dual-stack-sockets.md).</span><span class="sxs-lookup"><span data-stu-id="55273-123">For more information on this feature, see [Dual-Stack Sockets](dual-stack-sockets.md).</span></span>

    ```C++
    // Create a SOCKET for the server to listen for client connections

    ListenSocket = socket(result->ai_family, result->ai_socktype, result->ai_protocol);
    ```

    

4.  <span data-ttu-id="55273-124">Recherchez les erreurs pour vous assurer que le socket est un socket valide.</span><span class="sxs-lookup"><span data-stu-id="55273-124">Check for errors to ensure that the socket is a valid socket.</span></span>
    ```C++
    if (ListenSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

<span data-ttu-id="55273-125">Étape suivante : [liaison d’un socket](binding-a-socket.md)</span><span class="sxs-lookup"><span data-stu-id="55273-125">Next Step: [Binding a Socket](binding-a-socket.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="55273-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="55273-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55273-127">Prise en main avec Winsock</span><span class="sxs-lookup"><span data-stu-id="55273-127">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="55273-128">Initialisation de Winsock</span><span class="sxs-lookup"><span data-stu-id="55273-128">Initializing Winsock</span></span>](initializing-winsock.md)
</dt> <dt>

[<span data-ttu-id="55273-129">Application de serveur Winsock</span><span class="sxs-lookup"><span data-stu-id="55273-129">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> </dl>

 

 
