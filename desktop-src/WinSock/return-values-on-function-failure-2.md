---
description: L' \_ erreur de socket de constante de manifeste est fournie pour vérifier l’échec de la fonction. Bien que l’utilisation de cette constante ne soit pas obligatoire, elle est recommandée. L’exemple suivant illustre l’utilisation de la constante d' \_ erreur de Socket.
ms.assetid: b46203dc-5666-413b-90fe-8432318f3037
title: Valeurs de retour en cas d’échec de la fonction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94280d47d705833528c03c0d98a4a31232a0c6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202185"
---
# <a name="return-values-on-function-failure"></a><span data-ttu-id="c8e09-105">Valeurs de retour en cas d’échec de la fonction</span><span class="sxs-lookup"><span data-stu-id="c8e09-105">Return Values on Function Failure</span></span>

<span data-ttu-id="c8e09-106">L’erreur de **socket \_** de constante de manifeste est fournie pour vérifier l’échec de la fonction.</span><span class="sxs-lookup"><span data-stu-id="c8e09-106">The manifest constant **SOCKET\_ERROR** is provided for checking function failure.</span></span> <span data-ttu-id="c8e09-107">Bien que l’utilisation de cette constante ne soit pas obligatoire, elle est recommandée.</span><span class="sxs-lookup"><span data-stu-id="c8e09-107">Although use of this constant is not mandatory, it is recommended.</span></span> <span data-ttu-id="c8e09-108">L’exemple suivant illustre l’utilisation de la constante **d' \_ erreur de socket** .</span><span class="sxs-lookup"><span data-stu-id="c8e09-108">The following example illustrates the use of the **SOCKET\_ERROR** constant.</span></span>

<span data-ttu-id="c8e09-109">Style BSD classique (ne fonctionne pas sur Windows)</span><span class="sxs-lookup"><span data-stu-id="c8e09-109">Typical BSD Style (will not work on Windows)</span></span>


```C++
        r = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (r == -1     /* or r < 0 */
            && errno == EWOULDBLOCK) {
            printf("recv failed with error: EWOULDBLOCK\n");
        }    
```



<span data-ttu-id="c8e09-110">Style Windows</span><span class="sxs-lookup"><span data-stu-id="c8e09-110">Windows Style</span></span>


```C++
        iResult = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (iResult == SOCKET_ERROR ) {
            iError = WSAGetLastError();
            if (iError == WSAEWOULDBLOCK)
                printf("recv failed with error: WSAEWOULDBLOCK\n");
            else
                printf("recv failed with error: %ld\n", iError);

            closesocket(ClientSocket);
            WSACleanup();
            return 1;
        }    
```



## <a name="related-topics"></a><span data-ttu-id="c8e09-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c8e09-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8e09-112">Codes d’erreur-errno, h \_ errno et WSAGetLastError</span><span class="sxs-lookup"><span data-stu-id="c8e09-112">Error Codes - errno, h\_errno and WSAGetLastError</span></span>](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
</dt> <dt>

[<span data-ttu-id="c8e09-113">Gestion des erreurs Winsock</span><span class="sxs-lookup"><span data-stu-id="c8e09-113">Handling Winsock Errors</span></span>](handling-winsock-errors.md)
</dt> <dt>

[<span data-ttu-id="c8e09-114">Portage d’applications de socket vers Winsock</span><span class="sxs-lookup"><span data-stu-id="c8e09-114">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="c8e09-115">Considérations sur la programmation Winsock</span><span class="sxs-lookup"><span data-stu-id="c8e09-115">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="c8e09-116">Codes d’erreur de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="c8e09-116">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



