---
description: Après l’initialisation, un objet SOCKET doit être instancié pour être utilisé par le client.
ms.assetid: 088a79ef-b430-4860-8edc-902a1a03ed0d
title: Création d’un socket pour le client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f64467406f13ed40bdbe134e7796dd2aa5ff7bee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862577"
---
# <a name="creating-a-socket-for-the-client"></a><span data-ttu-id="3dbc7-103">Création d’un socket pour le client</span><span class="sxs-lookup"><span data-stu-id="3dbc7-103">Creating a socket for the client</span></span>

<span data-ttu-id="3dbc7-104">Après l’initialisation, un objet **Socket** doit être instancié pour être utilisé par le client.</span><span class="sxs-lookup"><span data-stu-id="3dbc7-104">After initialization, a **SOCKET** object must be instantiated for use by the client.</span></span>

<span data-ttu-id="3dbc7-105">**Pour créer un socket**</span><span class="sxs-lookup"><span data-stu-id="3dbc7-105">**To create a socket**</span></span>

1.  <span data-ttu-id="3dbc7-106">Déclarez un objet [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) qui contient une structure [**sockaddr**](sockaddr-2.md) et initialisez ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="3dbc7-106">Declare an [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) object that contains a [**sockaddr**](sockaddr-2.md) structure and initialize these values.</span></span> <span data-ttu-id="3dbc7-107">Pour cette application, la famille d’adresses Internet n’est pas spécifiée, de sorte qu’une adresse IPv6 ou IPv4 puisse être retournée.</span><span class="sxs-lookup"><span data-stu-id="3dbc7-107">For this application, the Internet address family is unspecified so that either an IPv6 or IPv4 address can be returned.</span></span> <span data-ttu-id="3dbc7-108">L’application demande que le type de socket soit un socket de flux pour le protocole TCP.</span><span class="sxs-lookup"><span data-stu-id="3dbc7-108">The application requests the socket type to be a stream socket for the TCP protocol.</span></span>
    ```C++
    struct addrinfo *result = NULL,
                    *ptr = NULL,
                    hints;

    ZeroMemory( &hints, sizeof(hints) );
    hints.ai_family = AF_UNSPEC;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    ```

    

2.  <span data-ttu-id="3dbc7-109">Appelez la fonction [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) en demandant l’adresse IP pour le nom de serveur transmis sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="3dbc7-109">Call the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function requesting the IP address for the server name passed on the command line.</span></span> <span data-ttu-id="3dbc7-110">Le port TCP sur le serveur auquel le client se connectera est défini par défaut sur le \_ port 27015 dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="3dbc7-110">The TCP port on the server that the client will connect to is defined by DEFAULT\_PORT as 27015 in this sample.</span></span> <span data-ttu-id="3dbc7-111">La fonction **getaddrinfo** retourne sa valeur sous la forme d’un entier dont les erreurs sont vérifiées.</span><span class="sxs-lookup"><span data-stu-id="3dbc7-111">The **getaddrinfo** function returns its value as an integer that is checked for errors.</span></span>
    ```C++
    #define DEFAULT_PORT "27015"

    // Resolve the server address and port
    iResult = getaddrinfo(argv[1], DEFAULT_PORT, &hints, &result);
    if (iResult != 0) {
        printf("getaddrinfo failed: %d\n", iResult);
        WSACleanup();
        return 1;
    }
    ```

    

3.  <span data-ttu-id="3dbc7-112">Créez un objet **Socket** appelé ConnectSocket.</span><span class="sxs-lookup"><span data-stu-id="3dbc7-112">Create a **SOCKET** object called ConnectSocket.</span></span>
    ```C++
    SOCKET ConnectSocket = INVALID_SOCKET;
    ```

    

4.  <span data-ttu-id="3dbc7-113">Appelez la fonction [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) et retournez sa valeur à la variable ConnectSocket.</span><span class="sxs-lookup"><span data-stu-id="3dbc7-113">Call the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function and return its value to the ConnectSocket variable.</span></span> <span data-ttu-id="3dbc7-114">Pour cette application, utilisez la première adresse IP retournée par l’appel à [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) qui correspondait à la famille d’adresses, au type de socket et au protocole spécifiés dans le paramètre *Hints* .</span><span class="sxs-lookup"><span data-stu-id="3dbc7-114">For this application, use the first IP address returned by the call to [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) that matched the address family, socket type, and protocol specified in the *hints* parameter.</span></span> <span data-ttu-id="3dbc7-115">Dans cet exemple, un socket de flux TCP a été spécifié avec un type de socket de flux de chaussette \_ et un protocole \_ TCP IPPROTO.</span><span class="sxs-lookup"><span data-stu-id="3dbc7-115">In this example, a TCP stream socket was specified with a socket type of SOCK\_STREAM and a protocol of IPPROTO\_TCP.</span></span> <span data-ttu-id="3dbc7-116">L’adresse \_ IP retournée peut être une adresse IPv6 ou IPv4 pour le serveur, car la famille d’adresses n’a pas été spécifiée (AF non spec).</span><span class="sxs-lookup"><span data-stu-id="3dbc7-116">The address family was left unspecified (AF\_UNSPEC), so the returned IP address could be either an IPv6 or IPv4 address for the server.</span></span>

    <span data-ttu-id="3dbc7-117">Si l’application cliente souhaite se connecter en utilisant uniquement IPv6 ou IPv4, la famille d’adresses doit être définie sur AF \_ inet6 pour IPv6 ou AF \_ inet pour IPv4 dans le paramètre *Hints* .</span><span class="sxs-lookup"><span data-stu-id="3dbc7-117">If the client application wants to connect using only IPv6 or IPv4, then the address family needs to be set to AF\_INET6 for IPv6 or AF\_INET for IPv4 in the *hints* parameter.</span></span>

    ```C++
    // Attempt to connect to the first address returned by
    // the call to getaddrinfo
    ptr=result;

    // Create a SOCKET for connecting to server
    ConnectSocket = socket(ptr->ai_family, ptr->ai_socktype, 
        ptr->ai_protocol);
    ```

    

5.  <span data-ttu-id="3dbc7-118">Recherchez les erreurs pour vous assurer que le socket est un socket valide.</span><span class="sxs-lookup"><span data-stu-id="3dbc7-118">Check for errors to ensure that the socket is a valid socket.</span></span>
    ```C++
    if (ConnectSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

<span data-ttu-id="3dbc7-119">Les paramètres passés à la fonction [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) peuvent être modifiés pour différentes implémentations.</span><span class="sxs-lookup"><span data-stu-id="3dbc7-119">The parameters passed to the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function can be changed for different implementations.</span></span>

<span data-ttu-id="3dbc7-120">La détection d’erreurs est un élément clé du code réseau réussi.</span><span class="sxs-lookup"><span data-stu-id="3dbc7-120">Error detection is a key part of successful networking code.</span></span> <span data-ttu-id="3dbc7-121">Si l’appel de [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) échoue, il retourne un socket non valide \_ .</span><span class="sxs-lookup"><span data-stu-id="3dbc7-121">If the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) call fails, it returns INVALID\_SOCKET.</span></span> <span data-ttu-id="3dbc7-122">L’instruction **If** dans le code précédent est utilisée pour intercepter les erreurs qui se sont produites lors de la création du Socket.</span><span class="sxs-lookup"><span data-stu-id="3dbc7-122">The **if** statement in the previous code is used to catch any errors that may have occurred while creating the socket.</span></span> <span data-ttu-id="3dbc7-123">[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne un numéro d’erreur associé à la dernière erreur qui s’est produite.</span><span class="sxs-lookup"><span data-stu-id="3dbc7-123">[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns an error number associated with the last error that occurred.</span></span>

> [!Note]  
> <span data-ttu-id="3dbc7-124">Des vérifications d’erreurs plus étendues peuvent être nécessaires en fonction de l’application.</span><span class="sxs-lookup"><span data-stu-id="3dbc7-124">More extensive error checking may be necessary depending on the application.</span></span>
>
> <span data-ttu-id="3dbc7-125">Par exemple, la définition de *hints.ai_family* sur **AF_UNSPEC** peut provoquer l’échec de l’appel de connexion.</span><span class="sxs-lookup"><span data-stu-id="3dbc7-125">For example, setting *hints.ai_family* to **AF_UNSPEC** can cause the connect call to fail.</span></span> <span data-ttu-id="3dbc7-126">Si cela se produit, utilisez une valeur IPv4 (**AF_INET**) ou IPv6 (**AF_INET6**) spécifique à la place.</span><span class="sxs-lookup"><span data-stu-id="3dbc7-126">If that happens, then use a specific IPv4 (**AF_INET**) or IPv6 (**AF_INET6**) value instead.</span></span>

<span data-ttu-id="3dbc7-127">[**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) est utilisé pour mettre fin à l’utilisation de la \_ dll WS2 32.</span><span class="sxs-lookup"><span data-stu-id="3dbc7-127">[**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) is used to terminate the use of the WS2\_32 DLL.</span></span>

<span data-ttu-id="3dbc7-128">Étape suivante : [connexion à un socket](connecting-to-a-socket.md)</span><span class="sxs-lookup"><span data-stu-id="3dbc7-128">Next Step: [Connecting to a Socket](connecting-to-a-socket.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="3dbc7-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3dbc7-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dbc7-130">Prise en main avec Winsock</span><span class="sxs-lookup"><span data-stu-id="3dbc7-130">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="3dbc7-131">Initialisation de Winsock</span><span class="sxs-lookup"><span data-stu-id="3dbc7-131">Initializing Winsock</span></span>](initializing-winsock.md)
</dt> <dt>

[<span data-ttu-id="3dbc7-132">Application cliente Winsock</span><span class="sxs-lookup"><span data-stu-id="3dbc7-132">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> </dl>

 

 
