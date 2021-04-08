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
# <a name="using-binding-handles-and-making-rpc-calls"></a>Utilisation de handles de liaison et exécution d’appels RPC

Une erreur courante entre les programmeurs RPC consiste à gérer toutes les exceptions. De nombreux programmeurs structurent leurs handles d’exception comme suit :

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

Le problème avec ce gestionnaire est qu’il intercepte toutes les erreurs, y compris les erreurs dans le programme client. L’interception des erreurs dans le programme client rend le débogage plus difficile. La façon correcte de structurer un gestionnaire d’exceptions est la suivante :

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

Ce gestionnaire d’exceptions présente l’avantage de permettre une certaine plage d’erreurs via. Ces erreurs ne sont jamais retournées par le serveur, car elles indiquent un problème côté client.

En outre, il est recommandé d’utiliser le **\[** [ \_ \_ handle de contexte strict](/windows/desktop/Midl/strict-context-handle) **\]** et les attributs de **\[** [ \_ \_ \_ handle de contexte stricts](/windows/desktop/Midl/type-strict-context-handle) **\]** pour garantir que la durée d’exécution RPC crée un handle de contexte sur une interface qui peut être passée comme argument uniquement aux méthodes de cette interface. Cela empêchera les défaillances du serveur qui se produisent lorsque des handles de contexte sont ouverts et passés entre différentes interfaces qui existent au sein du même processus.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[\_handle de contexte strict \_](/windows/desktop/Midl/strict-context-handle)
</dt> <dt>

[\_handle de \_ contexte \_ strict de type](/windows/desktop/Midl/type-strict-context-handle)
</dt> </dl>

 

 