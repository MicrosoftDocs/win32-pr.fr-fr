---
description: Une fois que le serveur a terminé de recevoir les données du client et de renvoyer les données au client, le serveur se déconnecte du client et arrête le Socket.
ms.assetid: 67f33645-d57a-48bd-9f0c-9e816f528204
title: Déconnexion du serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6abf7754da39a891b3d29c69f6c835706debd36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862573"
---
# <a name="disconnecting-the-server"></a><span data-ttu-id="566ac-103">Déconnexion du serveur</span><span class="sxs-lookup"><span data-stu-id="566ac-103">Disconnecting the Server</span></span>

<span data-ttu-id="566ac-104">Une fois que le serveur a terminé de recevoir les données du client et de renvoyer les données au client, le serveur se déconnecte du client et arrête le Socket.</span><span class="sxs-lookup"><span data-stu-id="566ac-104">Once the server is completed receiving data from the client and sending data back to the client, the server disconnects from the client and shutdowns the socket.</span></span>

<span data-ttu-id="566ac-105">**Pour déconnecter et arrêter un socket**</span><span class="sxs-lookup"><span data-stu-id="566ac-105">**To disconnect and shutdown a socket**</span></span>

1.  <span data-ttu-id="566ac-106">Une fois que le serveur a terminé l’envoi de données au client, la fonction [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) peut être appelée en spécifiant \_ l’envoi SD pour arrêter le côté envoi du Socket.</span><span class="sxs-lookup"><span data-stu-id="566ac-106">When the server is done sending data to the client, the [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function can be called specifying SD\_SEND to shutdown the sending side of the socket.</span></span> <span data-ttu-id="566ac-107">Cela permet au client de libérer certaines des ressources pour ce Socket.</span><span class="sxs-lookup"><span data-stu-id="566ac-107">This allows the client to release some of the resources for this socket.</span></span> <span data-ttu-id="566ac-108">L’application serveur peut toujours recevoir des données sur le Socket.</span><span class="sxs-lookup"><span data-stu-id="566ac-108">The server application can still receive data on the socket.</span></span>
    ```C++
    // shutdown the send half of the connection since no more data will be sent
    iResult = shutdown(ClientSocket, SD_SEND);
    if (iResult == SOCKET_ERROR) {
        printf("shutdown failed: %d\n", WSAGetLastError());
        closesocket(ClientSocket);
        WSACleanup();
        return 1;
    }
    ```

    

2.  <span data-ttu-id="566ac-109">Lorsque l’application cliente reçoit des données, la fonction [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) est appelée pour fermer le Socket.</span><span class="sxs-lookup"><span data-stu-id="566ac-109">When the client application is done receiving data, the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function is called to close the socket.</span></span>

    <span data-ttu-id="566ac-110">Lorsque l’application cliente est terminée à l’aide de la DLL Windows Sockets, la fonction [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) est appelée pour libérer des ressources.</span><span class="sxs-lookup"><span data-stu-id="566ac-110">When the client application is completed using the Windows Sockets DLL, the [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) function is called to release resources.</span></span>

    ```C++
    // cleanup
    closesocket(ClientSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-server-source-code"></a><span data-ttu-id="566ac-111">Compléter le code source du serveur</span><span class="sxs-lookup"><span data-stu-id="566ac-111">Complete Server Source Code</span></span>

-   [<span data-ttu-id="566ac-112">Compléter le code serveur</span><span class="sxs-lookup"><span data-stu-id="566ac-112">Complete Server Code</span></span>](complete-server-code.md)

## <a name="related-topics"></a><span data-ttu-id="566ac-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="566ac-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="566ac-114">Prise en main avec Winsock</span><span class="sxs-lookup"><span data-stu-id="566ac-114">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="566ac-115">Application de serveur Winsock</span><span class="sxs-lookup"><span data-stu-id="566ac-115">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="566ac-116">Réception et envoi de données sur le serveur</span><span class="sxs-lookup"><span data-stu-id="566ac-116">Receiving and Sending Data on the Server</span></span>](receiving-and-sending-data-on-the-server.md)
</dt> <dt>

[<span data-ttu-id="566ac-117">Exécution de l’exemple de code du client et du serveur Winsock</span><span class="sxs-lookup"><span data-stu-id="566ac-117">Running the Winsock Client and Server Code Sample</span></span>](finished-server-and-client-code.md)
</dt> </dl>

 

 



