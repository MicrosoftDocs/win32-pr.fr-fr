---
title: Utilisation de méthodes
description: Lorsqu’un client s’inscrit auprès du gestionnaire de tables de routage, il peut exporter un ensemble de méthodes. Ces méthodes sont utilisées par d’autres clients pour obtenir des informations spécifiques au client. Les méthodes permettent une communication privée entre les clients du gestionnaire de tables de routage.
ms.assetid: 6d984a02-d005-43ad-81c4-968ae9c1a105
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33bd895fbb3f8f54224522786b5794c5c6c57a9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940045"
---
# <a name="using-methods"></a><span data-ttu-id="e310e-105">Utilisation de méthodes</span><span class="sxs-lookup"><span data-stu-id="e310e-105">Using Methods</span></span>

<span data-ttu-id="e310e-106">Lorsqu’un client s’inscrit auprès du gestionnaire de tables de routage, il peut exporter un ensemble de méthodes.</span><span class="sxs-lookup"><span data-stu-id="e310e-106">When a client registers with the routing table manager, it can export a set of methods.</span></span> <span data-ttu-id="e310e-107">Ces méthodes sont utilisées par d’autres clients pour obtenir des informations spécifiques au client.</span><span class="sxs-lookup"><span data-stu-id="e310e-107">These methods are used by other clients to obtain client-specific information.</span></span> <span data-ttu-id="e310e-108">Les méthodes permettent une communication privée entre les clients du gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="e310e-108">Methods enable private communication between clients of the routing table manager.</span></span>

<span data-ttu-id="e310e-109">Un client peut obtenir la liste des méthodes exportées par un autre client.</span><span class="sxs-lookup"><span data-stu-id="e310e-109">A client can obtain the list of methods exported by another client.</span></span> <span data-ttu-id="e310e-110">Le client appelle la fonction [**RtmGetEntityMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods) , en fournissant le handle du client cible.</span><span class="sxs-lookup"><span data-stu-id="e310e-110">The client calls the [**RtmGetEntityMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods) function, supplying the target client's handle.</span></span>

<span data-ttu-id="e310e-111">Chaque méthode exportée par un client est identifiée de manière unique par son identificateur de méthode.</span><span class="sxs-lookup"><span data-stu-id="e310e-111">Each method exported by a client is uniquely identified by its method identifier.</span></span> <span data-ttu-id="e310e-112">Chaque client peut exporter jusqu’à 32 méthodes.</span><span class="sxs-lookup"><span data-stu-id="e310e-112">Each client can export up to 32 methods.</span></span> <span data-ttu-id="e310e-113">Chaque méthode correspond à un bit défini dans le membre **methodType** de la structure de la méthode d' [**exportation d' \_ entité \_ \_ RTM**](/windows/win32/api/rtmv2/nc-rtmv2-_entity_method) .</span><span class="sxs-lookup"><span data-stu-id="e310e-113">Each method corresponds to a bit set in the **MethodType** member of the [**RTM\_ENTITY\_EXPORT\_METHOD**](/windows/win32/api/rtmv2/nc-rtmv2-_entity_method) structure.</span></span> <span data-ttu-id="e310e-114">Pour appeler plusieurs méthodes, le client doit exécuter un ou logique des identificateurs pour ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e310e-114">To invoke multiple methods, the client should perform a logical OR of the identifiers for those methods.</span></span> <span data-ttu-id="e310e-115">La syntaxe et la sémantique des structures d’entrée et de sortie pour chaque protocole doivent être spécifiées lors de l’implémentation du protocole.</span><span class="sxs-lookup"><span data-stu-id="e310e-115">The syntax and semantics of input and output structures for each protocol must be specified when the protocol is implemented.</span></span>

> [!Note]  
> <span data-ttu-id="e310e-116">Les valeurs d’identificateur de méthode qui correspondent à un bit défini dans la moitié inférieure du membre **methodType** (les 16 bits inférieurs) sont réservées par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e310e-116">Method identifier values that correspond to a bit set in the lower half of the **MethodType** member (the lower 16 bits) are reserved by Microsoft.</span></span>

 

<span data-ttu-id="e310e-117">Pour appeler la méthode d’un second client, un client appelle la fonction [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) .</span><span class="sxs-lookup"><span data-stu-id="e310e-117">To invoke a second client's method, a client calls the [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) function.</span></span> <span data-ttu-id="e310e-118">Le gestionnaire de table de routage arbitre toutes les demandes pour appeler les méthodes d’un client.</span><span class="sxs-lookup"><span data-stu-id="e310e-118">The routing table manager arbitrates all requests to invoke a client's methods.</span></span> <span data-ttu-id="e310e-119">Le gestionnaire de tables de routage effectue deux fonctions lorsqu’il arbitre entre les clients :</span><span class="sxs-lookup"><span data-stu-id="e310e-119">The routing table manager performs two functions when it arbitrates between clients:</span></span>

-   <span data-ttu-id="e310e-120">Empêcher le second client d’appeler une méthode pour un client qui annule l’inscription.</span><span class="sxs-lookup"><span data-stu-id="e310e-120">Preventing the second client from invoking a method for a client that is unregistering.</span></span>
-   <span data-ttu-id="e310e-121">Maintien d’une demande d’appel lorsque les méthodes sont bloquées et autoriser la poursuite de la demande lorsque les méthodes sont débloquées.</span><span class="sxs-lookup"><span data-stu-id="e310e-121">Holding an "invoke" request when methods are blocked, and allowing the request to continue when the methods are unblocked.</span></span>

<span data-ttu-id="e310e-122">Si un client doit empêcher d’autres clients d’exécuter ses méthodes, le client peut appeler [**RtmBlockMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods).</span><span class="sxs-lookup"><span data-stu-id="e310e-122">If a client must prevent other clients from executing its methods, the client can call [**RtmBlockMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods).</span></span> <span data-ttu-id="e310e-123">Le gestionnaire de table de routage n’autorise pas le traitement d’un appel à [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) tant que le client n’a pas débloqué ses méthodes.</span><span class="sxs-lookup"><span data-stu-id="e310e-123">The routing table manager will not allow a call to [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) to be processed until the client unblocks its methods again.</span></span>

<span data-ttu-id="e310e-124">En général, les clients bloquent les méthodes lors de l’apport de modifications aux données privées échangées entre les clients.</span><span class="sxs-lookup"><span data-stu-id="e310e-124">Clients typically block methods when making changes to the private data that is exchanged between clients.</span></span> <span data-ttu-id="e310e-125">Les méthodes de blocage sont une action facultative.</span><span class="sxs-lookup"><span data-stu-id="e310e-125">Blocking methods is an optional action.</span></span> <span data-ttu-id="e310e-126">Un client peut également utiliser des verrous internes pour empêcher d’autres clients d’appeler des méthodes.</span><span class="sxs-lookup"><span data-stu-id="e310e-126">A client can also use internal locks to prevent other clients from invoking methods.</span></span>

<span data-ttu-id="e310e-127">Pour obtenir un exemple de code qui montre comment utiliser ces fonctions, consultez [obtenir et appeler les méthodes exportées pour un client](obtain-and-call-the-exported-methods-for-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="e310e-127">For sample code that shows how to use these functions, see [Obtain and Call the Exported Methods for a Client](obtain-and-call-the-exported-methods-for-a-client.md).</span></span>

 

 




