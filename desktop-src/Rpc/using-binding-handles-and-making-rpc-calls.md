---
title: Utilisation de handles de liaison et exécution d’appels RPC
description: Une erreur courante entre les programmeurs RPC consiste à gérer toutes les exceptions.
ms.assetid: 5b452129-4060-49f9-9400-8585fb5714a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b285fc3030b92e2616c850bf79c73e37f0341c9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728852"
---
# <a name="using-binding-handles-and-making-rpc-calls"></a><span data-ttu-id="1a3ef-103">Utilisation de handles de liaison et exécution d’appels RPC</span><span class="sxs-lookup"><span data-stu-id="1a3ef-103">Using Binding Handles and Making RPC Calls</span></span>

<span data-ttu-id="1a3ef-104">Une erreur courante entre les programmeurs RPC consiste à gérer toutes les exceptions.</span><span class="sxs-lookup"><span data-stu-id="1a3ef-104">A common mistake among RPC programmers is handling all exceptions.</span></span> <span data-ttu-id="1a3ef-105">De nombreux programmeurs structurent leurs handles d’exception comme suit :</span><span class="sxs-lookup"><span data-stu-id="1a3ef-105">Many programmers structure their exception handles like the following:</span></span>

``` syntax
    RpcTryExcept
        {
        RemoteSample();
        }
    RpcExcept(1)
        {
        log an error or do something else
        }
    RpcEndExcept
```

<span data-ttu-id="1a3ef-106">Le problème avec ce gestionnaire est qu’il intercepte toutes les erreurs, y compris les erreurs dans le programme client.</span><span class="sxs-lookup"><span data-stu-id="1a3ef-106">The problem with this handler is that it catches all errors, including errors in the client program.</span></span> <span data-ttu-id="1a3ef-107">L’interception des erreurs dans le programme client rend le débogage plus difficile.</span><span class="sxs-lookup"><span data-stu-id="1a3ef-107">Catching errors in the client program makes debugging more difficult.</span></span> <span data-ttu-id="1a3ef-108">La façon correcte de structurer un gestionnaire d’exceptions est la suivante :</span><span class="sxs-lookup"><span data-stu-id="1a3ef-108">The proper way to structure an exception handler is the following:</span></span>

``` syntax
    RpcTryExcept
        {
        RemoteSample();
        }
    // Return "non-fatal" errors to clients.  Catching fatal errors
    // makes it harder to debug.
    RpcExcept( ( ( (RpcExceptionCode() != STATUS_ACCESS_VIOLATION) &&
                   (RpcExceptionCode() != STATUS_POSSIBLE_DEADLOCK) &&
                   (RpcExceptionCode() != STATUS_INSTRUCTION_MISALIGNMENT) &&
                   (RpcExceptionCode() != STATUS_DATATYPE_MISALIGNMENT) &&
                   (RpcExceptionCode() != STATUS_PRIVILEGED_INSTRUCTION) &&
                   (RpcExceptionCode() != STATUS_ILLEGAL_INSTRUCTION) &&
                   (RpcExceptionCode() != STATUS_BREAKPOINT) &&
                   (RpcExceptionCode() != STATUS_STACK_OVERFLOW) &&
                   (RpcExceptionCode() != STATUS_HANDLE_NOT_CLOSABLE) &&
                   (RpcExceptionCode() != STATUS_IN_PAGE_ERROR) &&
                   (RpcExceptionCode() != STATUS_ASSERTION_FAILURE) &&
                   (RpcExceptionCode() != STATUS_STACK_BUFFER_OVERRUN) &&
                   (RpcExceptionCode() != STATUS_GUARD_PAGE_VIOLATION)
                    )
                    ? EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH ) )
        {
        log an error or do something else
        }
    RpcEndExcept
```

<span data-ttu-id="1a3ef-109">Ce gestionnaire d’exceptions présente l’avantage de permettre une certaine plage d’erreurs via.</span><span class="sxs-lookup"><span data-stu-id="1a3ef-109">This exception handler has the advantage of letting a certain range of errors through.</span></span> <span data-ttu-id="1a3ef-110">Ces erreurs ne sont jamais retournées par le serveur, car elles indiquent un problème côté client.</span><span class="sxs-lookup"><span data-stu-id="1a3ef-110">These errors will never be returned by the server, because they indicate a client side problem.</span></span>

<span data-ttu-id="1a3ef-111">En outre, il est recommandé d’utiliser le **\[** [ \_ \_ handle de contexte strict](/windows/desktop/Midl/strict-context-handle) **\]** et les attributs de **\[** [ \_ \_ \_ handle de contexte stricts](/windows/desktop/Midl/type-strict-context-handle) **\]** pour garantir que la durée d’exécution RPC crée un handle de contexte sur une interface qui peut être passée comme argument uniquement aux méthodes de cette interface.</span><span class="sxs-lookup"><span data-stu-id="1a3ef-111">Additionally, the use of the **\[**[strict\_context\_handle](/windows/desktop/Midl/strict-context-handle)**\]** and **\[**[type\_strict\_context\_handle](/windows/desktop/Midl/type-strict-context-handle)**\]** attributes are recommended to ensure the RPC run time creates a context handle on one interface that can be passed as an argument only to methods of that interface.</span></span> <span data-ttu-id="1a3ef-112">Cela empêchera les défaillances du serveur qui se produisent lorsque des handles de contexte sont ouverts et passés entre différentes interfaces qui existent au sein du même processus.</span><span class="sxs-lookup"><span data-stu-id="1a3ef-112">Doing so will prevent server failures that occur when context handles are opened and passed between different interfaces that exist within the same process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a3ef-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1a3ef-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a3ef-114">\_handle de contexte strict \_</span><span class="sxs-lookup"><span data-stu-id="1a3ef-114">strict\_context\_handle</span></span>](/windows/desktop/Midl/strict-context-handle)
</dt> <dt>

[<span data-ttu-id="1a3ef-115">\_handle de \_ contexte \_ strict de type</span><span class="sxs-lookup"><span data-stu-id="1a3ef-115">type\_strict\_context\_handle</span></span>](/windows/desktop/Midl/type-strict-context-handle)
</dt> </dl>

 

 