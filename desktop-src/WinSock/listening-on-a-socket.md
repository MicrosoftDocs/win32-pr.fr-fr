---
description: Une fois que le socket est lié à une adresse IP et à un port sur le système, le serveur doit ensuite écouter cette adresse IP et ce port pour les demandes de connexion entrante.
ms.assetid: 83c9f0e7-2e6d-449b-8d97-3d13154112cd
title: Écoute sur un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c36fe1718493d1b92ca52bb3c648ebd1aa5b0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515448"
---
# <a name="listening-on-a-socket"></a><span data-ttu-id="e4ee9-103">Écoute sur un socket</span><span class="sxs-lookup"><span data-stu-id="e4ee9-103">Listening on a Socket</span></span>

<span data-ttu-id="e4ee9-104">Une fois que le socket est lié à une adresse IP et à un port sur le système, le serveur doit ensuite écouter cette adresse IP et ce port pour les demandes de connexion entrante.</span><span class="sxs-lookup"><span data-stu-id="e4ee9-104">After the socket is bound to an IP address and port on the system, the server must then listen on that IP address and port for incoming connection requests.</span></span>

## <a name="to-listen-on-a-socket"></a><span data-ttu-id="e4ee9-105">Pour écouter sur un socket</span><span class="sxs-lookup"><span data-stu-id="e4ee9-105">To listen on a socket</span></span>

<span data-ttu-id="e4ee9-106">Appelez la fonction [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) , en passant comme paramètres le socket créé et une valeur pour le *backlog*, longueur maximale de la file d’attente des connexions en attente à accepter.</span><span class="sxs-lookup"><span data-stu-id="e4ee9-106">Call the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function, passing as parameters the created socket and a value for the *backlog*, maximum length of the queue of pending connections to accept.</span></span> <span data-ttu-id="e4ee9-107">Dans cet exemple, le paramètre *backlog* a été défini sur **SOMAXCONN**.</span><span class="sxs-lookup"><span data-stu-id="e4ee9-107">In this example, the *backlog* parameter was set to **SOMAXCONN**.</span></span> <span data-ttu-id="e4ee9-108">Cette valeur est une constante spéciale qui indique au fournisseur Winsock pour que ce Socket autorise un nombre maximal raisonnable de connexions en attente dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="e4ee9-108">This value is a special constant that instructs the Winsock provider for this socket to allow a maximum reasonable number of pending connections in the queue.</span></span> <span data-ttu-id="e4ee9-109">Vérifiez la valeur de retour pour les erreurs générales.</span><span class="sxs-lookup"><span data-stu-id="e4ee9-109">Check the return value for general errors.</span></span>


```C++
if ( listen( ListenSocket, SOMAXCONN ) == SOCKET_ERROR ) {
    printf( "Listen failed with error: %ld\n", WSAGetLastError() );
    closesocket(ListenSocket);
    WSACleanup();
    return 1;
}
```



<span data-ttu-id="e4ee9-110">Étape suivante : [accepter une connexion](accepting-a-connection.md)</span><span class="sxs-lookup"><span data-stu-id="e4ee9-110">Next Step: [Accepting a Connection](accepting-a-connection.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4ee9-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e4ee9-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4ee9-112">Prise en main avec Winsock</span><span class="sxs-lookup"><span data-stu-id="e4ee9-112">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="e4ee9-113">Application de serveur Winsock</span><span class="sxs-lookup"><span data-stu-id="e4ee9-113">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="e4ee9-114">Liaison d’un socket</span><span class="sxs-lookup"><span data-stu-id="e4ee9-114">Binding a Socket</span></span>](binding-a-socket.md)
</dt> </dl>

 

 



