---
description: Une fois que le socket est à l’écoute d’une connexion, le programme doit gérer les demandes de connexion sur ce Socket.
ms.assetid: d01f3d90-4d83-442e-aada-e7b082ef7699
title: Acceptation d’une connexion (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e066b53c22dd9964ad44dc8d67c15969641362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515657"
---
# <a name="accepting-a-connection-windows-sockets-2"></a><span data-ttu-id="8c910-103">Acceptation d’une connexion (Windows Sockets 2)</span><span class="sxs-lookup"><span data-stu-id="8c910-103">Accepting a Connection (Windows Sockets 2)</span></span>

<span data-ttu-id="8c910-104">Une fois que le socket est à l’écoute d’une connexion, le programme doit gérer les demandes de connexion sur ce Socket.</span><span class="sxs-lookup"><span data-stu-id="8c910-104">Once the socket is listening for a connection, the program must handle connection requests on that socket.</span></span>

<span data-ttu-id="8c910-105">**Pour accepter une connexion sur un socket**</span><span class="sxs-lookup"><span data-stu-id="8c910-105">**To accept a connection on a socket**</span></span>

1.  <span data-ttu-id="8c910-106">Créez un objet **Socket** temporaire appelé ClientSocket pour accepter les connexions des clients.</span><span class="sxs-lookup"><span data-stu-id="8c910-106">Create a temporary **SOCKET** object called ClientSocket for accepting connections from clients.</span></span>
    ```C++
    
    SOCKET ClientSocket;

    
    ```

    

2.  <span data-ttu-id="8c910-107">Normalement, une application serveur est conçue pour écouter les connexions à partir de plusieurs clients.</span><span class="sxs-lookup"><span data-stu-id="8c910-107">Normally a server application would be designed to listen for connections from multiple clients.</span></span> <span data-ttu-id="8c910-108">Pour les serveurs à hautes performances, plusieurs threads sont couramment utilisés pour gérer les connexions client multiples.</span><span class="sxs-lookup"><span data-stu-id="8c910-108">For high-performance servers, multiple threads are commonly used to handle the multiple client connections.</span></span>

    <span data-ttu-id="8c910-109">Il existe plusieurs techniques de programmation différentes utilisant Winsock qui peuvent être utilisées pour écouter plusieurs connexions client.</span><span class="sxs-lookup"><span data-stu-id="8c910-109">There are several different programming techniques using Winsock that can be used to listen for multiple client connections.</span></span> <span data-ttu-id="8c910-110">Une technique de programmation consiste à créer une boucle continue qui vérifie les demandes de connexion à l’aide de la fonction [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) (voir [écoute sur un socket](listening-on-a-socket.md)).</span><span class="sxs-lookup"><span data-stu-id="8c910-110">One programming technique is to create a continuous loop that checks for connection requests using the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function (see [Listening on a Socket](listening-on-a-socket.md)).</span></span> <span data-ttu-id="8c910-111">Si une demande de connexion se produit, l’application appelle la fonction [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**accepted**](/windows/win32/api/mswsock/nf-mswsock-acceptex)ou [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) et transmet le travail à un autre thread pour traiter la demande.</span><span class="sxs-lookup"><span data-stu-id="8c910-111">If a connection request occurs, the application calls the [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function and passes the work to another thread to handle the request.</span></span> <span data-ttu-id="8c910-112">Plusieurs autres techniques de programmation sont possibles.</span><span class="sxs-lookup"><span data-stu-id="8c910-112">Several other programming techniques are possible.</span></span>

    <span data-ttu-id="8c910-113">Notez que cet exemple de base est très simple et n’utilise pas plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="8c910-113">Note that this basic example is very simple and does not use multiple threads.</span></span> <span data-ttu-id="8c910-114">L’exemple écoute également uniquement et accepte une seule connexion.</span><span class="sxs-lookup"><span data-stu-id="8c910-114">The example also just listens for and accepts only a single connection.</span></span>

    ```C++
    
    ClientSocket = INVALID_SOCKET;

    // Accept a client socket
    ClientSocket = accept(ListenSocket, NULL, NULL);
    if (ClientSocket == INVALID_SOCKET) {
        printf("accept failed: %d\n", WSAGetLastError());
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
     
    
    ```

    

3.  <span data-ttu-id="8c910-115">Lorsque la connexion cliente a été acceptée, une application serveur transmet normalement le socket client accepté (la variable ClientSocket dans l’exemple de code ci-dessus) à un thread de travail ou à un port de terminaison d’e/s et continue d’accepter des connexions supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="8c910-115">When the client connection has been accepted, a server application would normally pass the accepted client socket (the ClientSocket variable in the above sample code) to a worker thread or an I/O completion port and continue accepting additional connections.</span></span> <span data-ttu-id="8c910-116">Dans cet exemple de base, le serveur continue à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="8c910-116">In this basic example, the server continues to the next step.</span></span>

    <span data-ttu-id="8c910-117">Il existe un certain nombre d’autres techniques de programmation qui peuvent être utilisées pour écouter et accepter plusieurs connexions.</span><span class="sxs-lookup"><span data-stu-id="8c910-117">There are a number of other programming techniques that can be used to listen for and accept multiple connections.</span></span> <span data-ttu-id="8c910-118">Celles-ci incluent l’utilisation des fonctions [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .</span><span class="sxs-lookup"><span data-stu-id="8c910-118">These include using the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) functions.</span></span> <span data-ttu-id="8c910-119">Des exemples de certaines de ces différentes techniques de programmation sont illustrés dans les [exemples Winsock avancés](getting-started-with-winsock.md) inclus dans le kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8c910-119">Examples of some of these various programming techniques are illustrated in the [Advanced Winsock Samples](getting-started-with-winsock.md) included with the Microsoft Windows Software Development Kit (SDK).</span></span>

    > [!Note]  
    > <span data-ttu-id="8c910-120">Sur les systèmes UNIX, une technique de programmation courante pour les serveurs était de faire en sorte qu’une application écoute les connexions.</span><span class="sxs-lookup"><span data-stu-id="8c910-120">On Unix systems, a common programming technique for servers was for an application to listen for connections.</span></span> <span data-ttu-id="8c910-121">Lorsqu’une connexion a été acceptée, le processus parent appelle la fonction de **branchement** pour créer un processus enfant afin de gérer la connexion du client, en héritant du socket du parent.</span><span class="sxs-lookup"><span data-stu-id="8c910-121">When a connection was accepted, the parent process would call the **fork** function to create a new child process to handle the client connection, inheriting the socket from the parent.</span></span> <span data-ttu-id="8c910-122">Cette technique de programmation n’est pas prise en charge sur Windows, car la fonction **Fork** n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8c910-122">This programming technique is not supported on Windows, since the **fork** function is not supported.</span></span> <span data-ttu-id="8c910-123">Cette technique n’est pas non plus adaptée aux serveurs hautes performances, car les ressources nécessaires à la création d’un nouveau processus sont beaucoup plus importantes que celles nécessaires pour un thread.</span><span class="sxs-lookup"><span data-stu-id="8c910-123">This technique is also not usually suitable for high-performance servers, since the resources needed to create a new process are much greater than those needed for a thread.</span></span>

     

<span data-ttu-id="8c910-124">Étape suivante : [réception et envoi de données sur le serveur](receiving-and-sending-data-on-the-server.md)</span><span class="sxs-lookup"><span data-stu-id="8c910-124">Next Step: [Receiving and Sending Data on the Server](receiving-and-sending-data-on-the-server.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c910-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8c910-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c910-126">Prise en main avec Winsock</span><span class="sxs-lookup"><span data-stu-id="8c910-126">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="8c910-127">Application de serveur Winsock</span><span class="sxs-lookup"><span data-stu-id="8c910-127">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="8c910-128">Écoute sur un socket</span><span class="sxs-lookup"><span data-stu-id="8c910-128">Listening on a Socket</span></span>](listening-on-a-socket.md)
</dt> </dl>

 

 
