---
title: Ordre de causalité des appels asynchrones
description: Dans une application RPC asynchrone, il est possible pour un thread client d’effectuer un deuxième appel asynchrone sur un handle de liaison avant la fin d’un appel antérieur effectué sur ce handle.
ms.assetid: 69beb3a4-39ae-4e3f-bb7d-31519278334d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 754ae4733e5a3936bdd28fef72b9560fb9c9dfcd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029131"
---
# <a name="causal-ordering-of-asynchronous-calls"></a><span data-ttu-id="05482-103">Ordre de causalité des appels asynchrones</span><span class="sxs-lookup"><span data-stu-id="05482-103">Causal Ordering of Asynchronous Calls</span></span>

<span data-ttu-id="05482-104">Dans une application RPC asynchrone, il est possible pour un thread client d’effectuer un deuxième appel asynchrone sur un handle de liaison avant la fin d’un appel antérieur effectué sur ce handle.</span><span class="sxs-lookup"><span data-stu-id="05482-104">In an asynchronous RPC application, it is possible for a client thread to make a second asynchronous call on a binding handle before an earlier call made on that handle has completed.</span></span> <span data-ttu-id="05482-105">La bibliothèque Runtime RPC gère cette situation comme suit :</span><span class="sxs-lookup"><span data-stu-id="05482-105">The RPC run-time library handles this situation as follows:</span></span>

-   <span data-ttu-id="05482-106">Le mécanisme RPC asynchrone garantit que les appels asynchrones effectués sur le même handle de liaison, sur le même thread, au même niveau de sécurité, sont distribués dans l’ordre dans lequel ils ont été créés.</span><span class="sxs-lookup"><span data-stu-id="05482-106">The asynchronous RPC mechanism guarantees that asynchronous calls made on the same binding handle, on the same thread, at the same security level, are dispatched in the order they were made.</span></span> <span data-ttu-id="05482-107">L’exécution réelle des appels peut se produire dans le désordre.</span><span class="sxs-lookup"><span data-stu-id="05482-107">Actual execution of the calls may occur out of order.</span></span>
-   <span data-ttu-id="05482-108">Comme pour les appels synchrones, les appels de procédure distante asynchrones de différents threads clients s’exécutent simultanément.</span><span class="sxs-lookup"><span data-stu-id="05482-108">As with synchronous calls, asynchronous remote procedure calls from different client threads execute simultaneously.</span></span>
-   <span data-ttu-id="05482-109">Si un appel asynchrone à partir d’une application cliente est suivi d’un ou de plusieurs appels synchrones, l’appel asynchrone peut s’exécuter pendant l’exécution des appels synchrones.</span><span class="sxs-lookup"><span data-stu-id="05482-109">If an asynchronous call from a client application is followed by one or more synchronous calls, the asynchronous call can execute while the synchronous calls are executing.</span></span> <span data-ttu-id="05482-110">Quel que soit l’état de l’appel asynchrone, les appels synchrones sont exécutés dans l’ordre dans lequel ils sont reçus par le serveur.</span><span class="sxs-lookup"><span data-stu-id="05482-110">Regardless of the status of the asynchronous call, the synchronous calls are executed in the order in which they are received by the server.</span></span>
-   <span data-ttu-id="05482-111">Si une application cliente sélectionne le classement non causalité pour un handle de liaison particulier, elle désactive la sérialisation pour ce handle.</span><span class="sxs-lookup"><span data-stu-id="05482-111">If a client application selects noncausal ordering for a particular binding handle, it disables serialization for that handle.</span></span> <span data-ttu-id="05482-112">Les applications activent le classement sans causalité en appelant [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) avec le paramètre *option* défini sur \_ liaison RPC C opt not \_ \_ \_ causalité et le paramètre *OptionValue* défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="05482-112">Applications enable noncausal ordering by calling [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) with the *Option* parameter set to RPC\_C\_OPT\_BINDING\_NONCAUSAL and the *OptionValue* parameter set to **TRUE**.</span></span> <span data-ttu-id="05482-113">Pour plus d’informations, consultez [constantes d’option de liaison](binding-option-constants.md).</span><span class="sxs-lookup"><span data-stu-id="05482-113">For details, see [Binding Option Constants](binding-option-constants.md).</span></span>

 

 




