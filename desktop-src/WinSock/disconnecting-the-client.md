---
description: Une fois que le client a terminé l’envoi et la réception de données, le client se déconnecte du serveur et arrête le Socket.
ms.assetid: 33165e5b-e304-42b1-9542-45d8fe8a5218
title: Déconnexion du client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6ac34036cc92386d7d68b3d5debda4d37a92ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318389"
---
# <a name="disconnecting-the-client"></a><span data-ttu-id="b669e-103">Déconnexion du client</span><span class="sxs-lookup"><span data-stu-id="b669e-103">Disconnecting the Client</span></span>

<span data-ttu-id="b669e-104">Une fois que le client a terminé l’envoi et la réception de données, le client se déconnecte du serveur et arrête le Socket.</span><span class="sxs-lookup"><span data-stu-id="b669e-104">Once the client is completed sending and receiving data, the client disconnects from the server and shutdowns the socket.</span></span>

<span data-ttu-id="b669e-105">**Pour déconnecter et arrêter un socket**</span><span class="sxs-lookup"><span data-stu-id="b669e-105">**To disconnect and shutdown a socket**</span></span>

1.  <span data-ttu-id="b669e-106">Lorsque le client a terminé d’envoyer des données au serveur, la fonction [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) peut être appelée en spécifiant \_ l’envoi SD pour arrêter le côté envoi du Socket.</span><span class="sxs-lookup"><span data-stu-id="b669e-106">When the client is done sending data to the server, the [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function can be called specifying SD\_SEND to shutdown the sending side of the socket.</span></span> <span data-ttu-id="b669e-107">Cela permet au serveur de libérer certaines des ressources pour ce Socket.</span><span class="sxs-lookup"><span data-stu-id="b669e-107">This allows the server to release some of the resources for this socket.</span></span> <span data-ttu-id="b669e-108">L’application cliente peut toujours recevoir des données sur le Socket.</span><span class="sxs-lookup"><span data-stu-id="b669e-108">The client application can still receive data on the socket.</span></span>
    ```C++
    // shutdown the send half of the connection since no more data will be sent
    iResult = shutdown(ConnectSocket, SD_SEND);
    if (iResult == SOCKET_ERROR) {
        printf("shutdown failed: %d\n", WSAGetLastError());
        closesocket(ConnectSocket);
        WSACleanup();
        return 1;
    }
    ```

    

2.  <span data-ttu-id="b669e-109">Lorsque l’application cliente reçoit des données, la fonction [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) est appelée pour fermer le Socket.</span><span class="sxs-lookup"><span data-stu-id="b669e-109">When the client application is done receiving data, the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function is called to close the socket.</span></span>

    <span data-ttu-id="b669e-110">Lorsque l’application cliente est terminée à l’aide de la DLL Windows Sockets, la fonction [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) est appelée pour libérer des ressources.</span><span class="sxs-lookup"><span data-stu-id="b669e-110">When the client application is completed using the Windows Sockets DLL, the [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) function is called to release resources.</span></span>

    ```C++
    // cleanup
    closesocket(ConnectSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-client-source-code"></a><span data-ttu-id="b669e-111">Code source complet du client</span><span class="sxs-lookup"><span data-stu-id="b669e-111">Complete Client Source Code</span></span>

-   [<span data-ttu-id="b669e-112">Code client complet</span><span class="sxs-lookup"><span data-stu-id="b669e-112">Complete Client Code</span></span>](complete-client-code.md)

## <a name="related-topics"></a><span data-ttu-id="b669e-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b669e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b669e-114">Prise en main avec Winsock</span><span class="sxs-lookup"><span data-stu-id="b669e-114">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="b669e-115">Application cliente Winsock</span><span class="sxs-lookup"><span data-stu-id="b669e-115">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> <dt>

[<span data-ttu-id="b669e-116">Envoi et réception de données sur le client</span><span class="sxs-lookup"><span data-stu-id="b669e-116">Sending and Receiving Data on the Client</span></span>](sending-and-receiving-data-on-the-client.md)
</dt> </dl>

 

 



