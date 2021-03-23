---
title: Utilisation de barrières de ressources pour synchroniser les États des ressources dans Direct3D 12
description: Pour réduire l’utilisation globale du processeur et activer le traitement multithread et le prétraitement des pilotes, Direct3D 12 déplace la responsabilité de la gestion de l’État par ressource du pilote Graphics vers l’application.
ms.assetid: 3AB3BF34-433C-400B-921A-55B23CCDA44F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c766f18e85ab8acc2ed0afad8e680d566a723a68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104548597"
---
# <a name="using-resource-barriers-to-synchronize-resource-states-in-direct3d-12"></a><span data-ttu-id="68e62-103">Utilisation de barrières de ressources pour synchroniser les États des ressources dans Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="68e62-103">Using Resource Barriers to Synchronize Resource States in Direct3D 12</span></span>

<span data-ttu-id="68e62-104">Pour réduire l’utilisation globale du processeur et activer le traitement multithread et le prétraitement des pilotes, Direct3D 12 déplace la responsabilité de la gestion de l’État par ressource du pilote Graphics vers l’application.</span><span class="sxs-lookup"><span data-stu-id="68e62-104">To reduce overall CPU usage and enable driver multi-threading and pre-processing, Direct3D 12 moves the responsibility of per-resource state management from the graphics driver to the application.</span></span> <span data-ttu-id="68e62-105">Un exemple d’État par ressource est de savoir si une ressource de texture est actuellement accessible par le biais d’un nuanceur Affichage des ressources ou en tant que vue de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="68e62-105">An example of per-resource state is whether a texture resource is currently being accessed as through a Shader Resource View or as a Render Target View.</span></span> <span data-ttu-id="68e62-106">Dans Direct3D 11, les pilotes devaient suivre cet État en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="68e62-106">In Direct3D 11, drivers were required to track this state in the background.</span></span> <span data-ttu-id="68e62-107">Cela s’avère coûteux du point de vue de l’UC et complique de manière significative tout type de conception multithread.</span><span class="sxs-lookup"><span data-stu-id="68e62-107">This is expensive from a CPU perspective and significantly complicates any sort of multi-threaded design.</span></span> <span data-ttu-id="68e62-108">Dans Microsoft Direct3D 12, la majeure partie de l’État par ressource est gérée par l’application avec une seule API, [**ID3D12GraphicsCommandList :: ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span><span class="sxs-lookup"><span data-stu-id="68e62-108">In Microsoft Direct3D 12, most per-resource state is managed by the application with a single API, [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span>

-   [<span data-ttu-id="68e62-109">Utilisation de l’API ResourceBarrier pour gérer l’État par ressource</span><span class="sxs-lookup"><span data-stu-id="68e62-109">Using the ResourceBarrier API to manage per-resource state</span></span>](#using-the-resourcebarrier-api-to-manage-per-resource-state)
    -   [<span data-ttu-id="68e62-110">États des ressources</span><span class="sxs-lookup"><span data-stu-id="68e62-110">Resource states</span></span>](#using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
    -   [<span data-ttu-id="68e62-111">États initiaux pour les ressources</span><span class="sxs-lookup"><span data-stu-id="68e62-111">Initial states for resources</span></span>](#initial-states-for-resources)
    -   [<span data-ttu-id="68e62-112">Restrictions relatives à l’état des ressources en lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="68e62-112">Read/write resource state restrictions</span></span>](#readwrite-resource-state-restrictions)
    -   [<span data-ttu-id="68e62-113">États des ressources pour la présentation des mémoires tampons d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="68e62-113">Resource states for presenting back buffers</span></span>](#resource-states-for-presenting-back-buffers)
    -   [<span data-ttu-id="68e62-114">Rejet des ressources</span><span class="sxs-lookup"><span data-stu-id="68e62-114">Discarding resources</span></span>](#discarding-resources)
-   [<span data-ttu-id="68e62-115">Transitions d’État implicites</span><span class="sxs-lookup"><span data-stu-id="68e62-115">Implicit State Transitions</span></span>](#implicit-state-transitions)
    -   [<span data-ttu-id="68e62-116">Promotion de l’État commun</span><span class="sxs-lookup"><span data-stu-id="68e62-116">Common state promotion</span></span>](#common-state-promotion)
    -   [<span data-ttu-id="68e62-117">État d’atténuation commun</span><span class="sxs-lookup"><span data-stu-id="68e62-117">State decay to common</span></span>](#state-decay-to-common)
    -   [<span data-ttu-id="68e62-118">Impact sur les performances</span><span class="sxs-lookup"><span data-stu-id="68e62-118">Performance implications</span></span>](#performance-implications)
-   [<span data-ttu-id="68e62-119">Fractionner les barrières</span><span class="sxs-lookup"><span data-stu-id="68e62-119">Split Barriers</span></span>](#split-barriers)
-   [<span data-ttu-id="68e62-120">Exemple de scénario de cloisonnement de ressources</span><span class="sxs-lookup"><span data-stu-id="68e62-120">Resource barrier example scenario</span></span>](#resource-barrier-example-scenario)
-   [<span data-ttu-id="68e62-121">Exemple de promotion et d’atténuation de l’État commun</span><span class="sxs-lookup"><span data-stu-id="68e62-121">Common state promotion and decay sample</span></span>](#common-state-promotion-and-decay-sample)
-   [<span data-ttu-id="68e62-122">Exemple de barrières divisées</span><span class="sxs-lookup"><span data-stu-id="68e62-122">Example of split barriers</span></span>](#example-of-split-barriers)
-   [<span data-ttu-id="68e62-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="68e62-123">Related topics</span></span>](#related-topics)

## <a name="using-the-resourcebarrier-api-to-manage-per-resource-state"></a><span data-ttu-id="68e62-124">Utilisation de l’API ResourceBarrier pour gérer l’État par ressource</span><span class="sxs-lookup"><span data-stu-id="68e62-124">Using the ResourceBarrier API to manage per-resource state</span></span>

<span data-ttu-id="68e62-125">[**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) notifie le pilote graphique des situations dans lesquelles le pilote peut avoir besoin de synchroniser plusieurs accès à la mémoire dans laquelle une ressource est stockée.</span><span class="sxs-lookup"><span data-stu-id="68e62-125">[**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) notifies the graphics driver of situations in which the driver may need to synchronize multiple accesses to the memory in which a resource is stored.</span></span> <span data-ttu-id="68e62-126">La méthode est appelée avec une ou plusieurs structures de description de la barrière des ressources qui indiquent le type de cloisonnement des ressources déclaré.</span><span class="sxs-lookup"><span data-stu-id="68e62-126">The method is called with one or more resource barrier description structures indicating the type of resource barrier being declared.</span></span>

<span data-ttu-id="68e62-127">Il existe trois types de barrières des ressources :</span><span class="sxs-lookup"><span data-stu-id="68e62-127">There are three types of resource barriers:</span></span>

-   <span data-ttu-id="68e62-128">**Transition barrière** : une barrière de transition indique qu’un ensemble de sous-ressources est en transition entre différentes utilisations.</span><span class="sxs-lookup"><span data-stu-id="68e62-128">**Transition barrier** - A transition barrier indicates that a set of subresources transition between different usages.</span></span> <span data-ttu-id="68e62-129">Une structure de [**barrière de \_ transition de ressource \_ \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) est utilisée pour spécifier la sous-ressource qui est en transition, ainsi que les États *avant* et *après* de la sous-ressource.</span><span class="sxs-lookup"><span data-stu-id="68e62-129">A [**D3D12\_RESOURCE\_TRANSITION\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) structure is used to specify the subresource that is transitioning as well as the *before* and *after* states of the subresource.</span></span>

    <span data-ttu-id="68e62-130">Le système vérifie que les transitions de sous-ressources dans une liste de commandes sont cohérentes avec les transitions précédentes dans la même liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="68e62-130">The system verifies that subresource transitions in a command list are consistent with previous transitions in the same command list.</span></span> <span data-ttu-id="68e62-131">La couche de débogage suit plus en détail l’état des sous-ressources pour trouver d’autres erreurs, mais cette validation est conservatrice et non exhaustive.</span><span class="sxs-lookup"><span data-stu-id="68e62-131">The debug layer further tracks subresource state to find other errors however this validation is conservative and not exhaustive.</span></span>

    <span data-ttu-id="68e62-132">Notez que vous pouvez utiliser l' \_ \_ indicateur de ressource D3D12 \_ de tous les sous- \_ ressources pour spécifier que toutes les sous-ressources d’une ressource sont en cours de transition.</span><span class="sxs-lookup"><span data-stu-id="68e62-132">Note that you can use the D3D12\_RESOURCE\_BARRIER\_ALL\_SUBRESOURCES flag to specify that all subresources within a resource are being transitioned.</span></span>

-   <span data-ttu-id="68e62-133">**Barrière d’alias** : une barrière d’alias indique une transition entre les utilisations de deux ressources différentes qui ont des mappages qui se chevauchent dans le même tas.</span><span class="sxs-lookup"><span data-stu-id="68e62-133">**Aliasing barrier** - An aliasing barrier indicates a transition between usages of two different resources which have overlapping mappings into the same heap.</span></span> <span data-ttu-id="68e62-134">Cela s’applique aux ressources réservées et placées.</span><span class="sxs-lookup"><span data-stu-id="68e62-134">This applies to both reserved and placed resources.</span></span> <span data-ttu-id="68e62-135">Une structure de [**barrière d' \_ alias des ressources \_ \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) est utilisée pour spécifier la ressource *avant* et la ressource *après* .</span><span class="sxs-lookup"><span data-stu-id="68e62-135">A [**D3D12\_RESOURCE\_ALIASING\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) structure is used to specify both the *before* resource and the *after* resource.</span></span>

    <span data-ttu-id="68e62-136">Notez qu’une ou les deux ressources peuvent avoir la valeur NULL, ce qui indique qu’une ressource en mosaïque peut provoquer des alias.</span><span class="sxs-lookup"><span data-stu-id="68e62-136">Note that one or both resources can be NULL, which indicates that any tiled resource could cause aliasing.</span></span> <span data-ttu-id="68e62-137">Pour plus d’informations sur l’utilisation des ressources en mosaïque, consultez [ressources](../direct3d11/tiled-resources.md) en mosaïque et [ressources en mosaïque de volume](volume-tiled-resources.md).</span><span class="sxs-lookup"><span data-stu-id="68e62-137">For more information about using tiled resources, see [Tiled resources](../direct3d11/tiled-resources.md) and [Volume Tiled Resources](volume-tiled-resources.md).</span></span>

-   <span data-ttu-id="68e62-138">**Barrière de vue d’accès non triée (UAV)** : une barrière UAV indique que tous les accès UAV, à la fois en lecture ou en écriture, à une ressource particulière doivent se terminer entre tous les futurs accès UAV, en lecture ou en écriture.</span><span class="sxs-lookup"><span data-stu-id="68e62-138">**Unordered access view (UAV) barrier** - A UAV barrier indicates that all UAV accesses, both read or write, to a particular resource must complete between any future UAV accesses, both read or write.</span></span> <span data-ttu-id="68e62-139">Il n’est pas nécessaire pour une application de placer une barrière UAV entre deux appels de dessin ou de distribution qui lisent uniquement à partir d’un UAV.</span><span class="sxs-lookup"><span data-stu-id="68e62-139">It's not necessary for an app to put a UAV barrier between two draw or dispatch calls that only read from a UAV.</span></span> <span data-ttu-id="68e62-140">En outre, il n’est pas nécessaire de placer une barrière UAV entre deux appels de dessin ou de distribution qui écrivent dans le même UAV si l’application sait qu’il est possible d’exécuter l’accès UAV dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="68e62-140">Also, it's not necessary to put a UAV barrier between two draw or dispatch calls that write to the same UAV if the application knows that it is safe to execute the UAV access in any order.</span></span> <span data-ttu-id="68e62-141">Une structure de [**\_ \_ \_ barrière UAV de ressource D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) est utilisée pour spécifier la ressource UAV à laquelle s’applique le cloisonnement.</span><span class="sxs-lookup"><span data-stu-id="68e62-141">A [**D3D12\_RESOURCE\_UAV\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) structure is used to specify the UAV resource to which the barrier applies.</span></span> <span data-ttu-id="68e62-142">L’application peut spécifier la valeur NULL pour le UAV du cloisonnement, ce qui indique que tout accès UAV peut nécessiter le cloisonnement.</span><span class="sxs-lookup"><span data-stu-id="68e62-142">The application can specify NULL for the barrier's UAV, which indicates that any UAV access could require the barrier.</span></span>

<span data-ttu-id="68e62-143">Quand [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) est appelé avec un tableau de descriptions de cloisonnement de ressources, l’API se comporte comme si elle était appelée une fois pour chaque élément, dans l’ordre dans lequel elles ont été fournies.</span><span class="sxs-lookup"><span data-stu-id="68e62-143">When [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) is called with an array of resource barrier descriptions, the API behaves as if it was called once for each element, in the order in which they were supplied.</span></span>

<span data-ttu-id="68e62-144">À un moment donné, une sous-ressource se trouve dans un seul État, déterminé par l’ensemble des indicateurs d' [**\_ \_ États de ressource D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) fournis à [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span><span class="sxs-lookup"><span data-stu-id="68e62-144">At any given time, a subresource is in exactly one state, determined by the set of [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) flags supplied to [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span> <span data-ttu-id="68e62-145">L’application doit s’assurer que les États *Before* et *after* des appels consécutifs à **ResourceBarrier** conviennent.</span><span class="sxs-lookup"><span data-stu-id="68e62-145">The application must ensure that the *before* and *after* states of consecutive calls to **ResourceBarrier** agree.</span></span>

> [!TIP]
>
> <span data-ttu-id="68e62-146">Dans la mesure du possible, les applications doivent regrouper plusieurs transitions dans un seul appel d’API.</span><span class="sxs-lookup"><span data-stu-id="68e62-146">Applications should batch multiple transitions into one API call wherever possible.</span></span>

 

### <a name="resource-states"></a><span data-ttu-id="68e62-147">États des ressources</span><span class="sxs-lookup"><span data-stu-id="68e62-147">Resource states</span></span>

<span data-ttu-id="68e62-148">Pour obtenir la liste complète des États des ressources qu’une ressource peut passer d’une ressource à l’autre, consultez la rubrique de référence pour l’énumération des [**\_ \_ États des ressources D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) .</span><span class="sxs-lookup"><span data-stu-id="68e62-148">For the complete list of resource states that a resource can transition between, see the reference topic for the [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) enumeration.</span></span>

<span data-ttu-id="68e62-149">Pour les cloisonnements de ressources fractionnées, consultez également les [**\_ indicateurs de \_ barrière \_ de ressources D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).</span><span class="sxs-lookup"><span data-stu-id="68e62-149">For split resource barriers, also refer to [**D3D12\_RESOURCE\_BARRIER\_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).</span></span>

### <a name="initial-states-for-resources"></a><span data-ttu-id="68e62-150">États initiaux pour les ressources</span><span class="sxs-lookup"><span data-stu-id="68e62-150">Initial states for resources</span></span>

<span data-ttu-id="68e62-151">Les ressources peuvent être créées avec n’importe quel état initial spécifié par l’utilisateur (valide pour la description de la ressource), avec les exceptions suivantes :</span><span class="sxs-lookup"><span data-stu-id="68e62-151">Resources may be created with any user-specified initial state (valid for the resource description), with the following exceptions:</span></span>

-   <span data-ttu-id="68e62-152">Le chargement des segments de mémoire doit commencer dans la lecture générique état de la ressource State D3D12 \_ \_ \_ \_ qui est une combinaison or au niveau du bit :</span><span class="sxs-lookup"><span data-stu-id="68e62-152">Upload heaps must start out in the state D3D12\_RESOURCE\_STATE\_GENERIC\_READ which is a bitwise OR combination of:</span></span>
    -   <span data-ttu-id="68e62-153">\_ \_ Sommet de l’état de la ressource D3D12 \_ \_ et \_ \_ mémoire tampon constante</span><span class="sxs-lookup"><span data-stu-id="68e62-153">D3D12\_RESOURCE\_STATE\_VERTEX\_AND\_CONSTANT\_BUFFER</span></span>
    -   <span data-ttu-id="68e62-154">\_ \_ \_ Mémoire tampon d’index d’état de ressource D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="68e62-154">D3D12\_RESOURCE\_STATE\_INDEX\_BUFFER</span></span>
    -   <span data-ttu-id="68e62-155">SOURCE de copie de l' \_ \_ État de la ressource D3D12 \_ \_</span><span class="sxs-lookup"><span data-stu-id="68e62-155">D3D12\_RESOURCE\_STATE\_COPY\_SOURCE</span></span>
    -   <span data-ttu-id="68e62-156">\_Ressource du \_ \_ \_ \_ nuanceur de non-pixel \_ de l’état de ressource D3D12</span><span class="sxs-lookup"><span data-stu-id="68e62-156">D3D12\_RESOURCE\_STATE\_NON\_PIXEL\_SHADER\_RESOURCE</span></span>
    -   <span data-ttu-id="68e62-157">\_Ressource de \_ \_ \_ nuanceur de pixels d’état de ressource D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="68e62-157">D3D12\_RESOURCE\_STATE\_PIXEL\_SHADER\_RESOURCE</span></span>
    -   <span data-ttu-id="68e62-158">\_ \_ \_ Argument indirect de l’état de la ressource D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="68e62-158">D3D12\_RESOURCE\_STATE\_INDIRECT\_ARGUMENT</span></span>
-   <span data-ttu-id="68e62-159">Les segments de mémoire readback doivent démarrer dans l’état de la copie de destination de l’état de la \_ ressource D3D12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="68e62-159">Readback heaps must start out in the D3D12\_RESOURCE\_STATE\_COPY\_DEST state.</span></span>
-   <span data-ttu-id="68e62-160">Les mémoires tampons d’annulation de chaîne de permutation commencent automatiquement par l' \_ État commun de l’état de ressource D3D12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="68e62-160">Swap chain back buffers automatically start out in the D3D12\_RESOURCE\_STATE\_COMMON state.</span></span>

<span data-ttu-id="68e62-161">Pour qu’un segment de mémoire puisse être la cible d’une opération de copie GPU, le tas doit d’abord être transféré à l’état de copie de destination de l’état de la \_ ressource D3D12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="68e62-161">Before a heap can be the target of a GPU copy operation, normally the heap must first be transitioned to the D3D12\_RESOURCE\_STATE\_COPY\_DEST state.</span></span> <span data-ttu-id="68e62-162">Toutefois, les ressources créées sur les tas de chargement doivent commencer dans et ne peuvent pas être modifiées à partir de l' \_ État de lecture générique puisque seul l’UC est en cours d’écriture.</span><span class="sxs-lookup"><span data-stu-id="68e62-162">However, resources created on UPLOAD heaps must start in and cannot change from the GENERIC\_READ state since only the CPU will be doing writing.</span></span> <span data-ttu-id="68e62-163">À l’inverse, les ressources validées créées dans des segments de mémoire READBACK doivent démarrer dans et ne peuvent pas changer à partir de l’état de copie de \_ destination.</span><span class="sxs-lookup"><span data-stu-id="68e62-163">Conversely, committed resources created in READBACK heaps must start in and cannot change from the COPY\_DEST state.</span></span>

### <a name="readwrite-resource-state-restrictions"></a><span data-ttu-id="68e62-164">Restrictions relatives à l’état des ressources en lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="68e62-164">Read/write resource state restrictions</span></span>

<span data-ttu-id="68e62-165">Les bits d’utilisation de l’état des ressources qui sont utilisés pour décrire un état de ressource sont divisés en États en lecture seule et en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="68e62-165">The resource state usage bits that are used to describe a resource state are divided into read-only and read/write states.</span></span> <span data-ttu-id="68e62-166">La rubrique de référence pour [**les \_ \_ États de ressource D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) indique le niveau d’accès en lecture/écriture pour chaque bit de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="68e62-166">The reference topic for the [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) indicates the read/write access level for each bit in the enumeration.</span></span>

<span data-ttu-id="68e62-167">Au maximum, un seul bit de lecture/écriture peut être défini pour n’importe quelle ressource.</span><span class="sxs-lookup"><span data-stu-id="68e62-167">At most, only one read/write bit can be set for any resource.</span></span> <span data-ttu-id="68e62-168">Si un bit d’écriture est défini, aucun bit en lecture seule ne peut être défini pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="68e62-168">If a write bit is set, then no read-only bit may be set for that resource.</span></span> <span data-ttu-id="68e62-169">Si aucun bit d’écriture n’est défini, vous pouvez définir n’importe quel nombre de bits de lecture.</span><span class="sxs-lookup"><span data-stu-id="68e62-169">If no write bit is set, then any number of read bits may be set.</span></span>

### <a name="resource-states-for-presenting-back-buffers"></a><span data-ttu-id="68e62-170">États des ressources pour la présentation des mémoires tampons d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="68e62-170">Resource states for presenting back buffers</span></span>

<span data-ttu-id="68e62-171">Avant qu’une mémoire tampon d’arrière-plan ne soit présentée, elle doit être dans l' \_ État commun de l’état de ressource D3D12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="68e62-171">Before a back buffer is presented, it must be in the D3D12\_RESOURCE\_STATE\_COMMON state.</span></span> <span data-ttu-id="68e62-172">Notez que l’état de ressource D3D12 de l’état \_ \_ de ressource \_ présent est un synonyme de l' \_ État de ressource D3D12 \_ \_ commun et qu’ils ont tous les deux la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="68e62-172">Note, the resource state D3D12\_RESOURCE\_STATE\_PRESENT is a synonym for D3D12\_RESOURCE\_STATE\_COMMON, and they both have a value of 0.</span></span> <span data-ttu-id="68e62-173">Si [**IDXGISwapChain ::P renvoyée**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (ou [**IDXGISwapChain1 ::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) est appelé sur une ressource qui n’est pas actuellement dans cet État, un avertissement de couche de débogage est émis.</span><span class="sxs-lookup"><span data-stu-id="68e62-173">If [**IDXGISwapChain::Present**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (or [**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) is called on a resource that is not currently in this state, a debug layer warning is emitted.</span></span>

### <a name="discarding-resources"></a><span data-ttu-id="68e62-174">Rejet des ressources</span><span class="sxs-lookup"><span data-stu-id="68e62-174">Discarding resources</span></span>

<span data-ttu-id="68e62-175">Toutes les sous-ressources d’une ressource doivent se trouver dans l’état de la cible de rendu \_ , ou en \_ lecture seule, pour les cibles de rendu/les ressources de stencil de profondeur, lorsque [**ID3D12GraphicsCommandList ::D iscardresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) est appelée.</span><span class="sxs-lookup"><span data-stu-id="68e62-175">All subresources in a resource must be in the RENDER\_TARGET state, or DEPTH\_WRITE state, for render targets/depth-stencil resources respectively, when [**ID3D12GraphicsCommandList::DiscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) is called.</span></span>

## <a name="implicit-state-transitions"></a><span data-ttu-id="68e62-176">Transitions d’État implicites</span><span class="sxs-lookup"><span data-stu-id="68e62-176">Implicit State Transitions</span></span>

<span data-ttu-id="68e62-177">Les ressources peuvent uniquement être « promues » en dehors de l' \_ État de ressource D3D12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="68e62-177">Resources can only be "promoted" out of D3D12\_RESOURCE\_STATE\_COMMON.</span></span> <span data-ttu-id="68e62-178">De même, les ressources ne sont que de la « atténuation » de l' \_ État de ressource D3D12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="68e62-178">Similarly, resources will only "decay" to D3D12\_RESOURCE\_STATE\_COMMON.</span></span>

### <a name="common-state-promotion"></a><span data-ttu-id="68e62-179">Promotion de l’État commun</span><span class="sxs-lookup"><span data-stu-id="68e62-179">Common state promotion</span></span>

<span data-ttu-id="68e62-180">Toutes les ressources de mémoire tampon et les textures avec l' \_ indicateur de ressource D3D12 \_ autoriser l' \_ \_ \_ ensemble d’indicateurs d’accès simultané sont promues implicitement de \_ l’état de ressource D3D12 \_ \_ commun à l’état approprié lors du premier accès GPU, y compris la \_ lecture générique pour couvrir tout scénario de lecture.</span><span class="sxs-lookup"><span data-stu-id="68e62-180">All buffer resources as well as textures with the D3D12\_RESOURCE\_FLAG\_ALLOW\_SIMULTANEOUS\_ACCESS flag set are implicitly promoted from D3D12\_RESOURCE\_STATE\_COMMON to the relevant state on first GPU access, including GENERIC\_READ to cover any read scenario.</span></span> <span data-ttu-id="68e62-181">Toutes les ressources de l’État commun sont accessibles comme si elles étaient dans un État unique avec</span><span class="sxs-lookup"><span data-stu-id="68e62-181">Any resource in the COMMON state can be accessed as through it were in a single state with</span></span>

<dl> <span data-ttu-id="68e62-182">1 indicateur d’écriture, ou</span><span class="sxs-lookup"><span data-stu-id="68e62-182">1 WRITE flag, or</span></span>  
<span data-ttu-id="68e62-183">1 ou plusieurs indicateurs de lecture</span><span class="sxs-lookup"><span data-stu-id="68e62-183">1 or more READ flags</span></span>  
</dl>

<span data-ttu-id="68e62-184">Les ressources peuvent être promues à partir de l’État commun en fonction du tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="68e62-184">Resources can be promoted from the COMMON state based on the following table:</span></span>



| <span data-ttu-id="68e62-185">Indicateur d’État</span><span class="sxs-lookup"><span data-stu-id="68e62-185">State flag</span></span>                    | <span data-ttu-id="68e62-186">État pouvant être promu</span><span class="sxs-lookup"><span data-stu-id="68e62-186">Promotable State</span></span>                             |                                      |
|-------------------------------|----------------------------------------------|--------------------------------------|
|                               | <span data-ttu-id="68e62-187">**Mémoires tampons et Simultaneous-Access textures**</span><span class="sxs-lookup"><span data-stu-id="68e62-187">**Buffers and Simultaneous-Access Textures**</span></span> | <span data-ttu-id="68e62-188">**Textures à accès non simultané**</span><span class="sxs-lookup"><span data-stu-id="68e62-188">**Non-Simultaneous-Access Textures**</span></span> |
| <span data-ttu-id="68e62-189">\_mémoire tampon de vertex et \_ constante \_</span><span class="sxs-lookup"><span data-stu-id="68e62-189">VERTEX\_AND\_CONSTANT\_BUFFER</span></span> | <span data-ttu-id="68e62-190">Oui</span><span class="sxs-lookup"><span data-stu-id="68e62-190">Yes</span></span>                                          | <span data-ttu-id="68e62-191">Non</span><span class="sxs-lookup"><span data-stu-id="68e62-191">No</span></span>                                   |
| <span data-ttu-id="68e62-192">\_mémoire tampon d’index</span><span class="sxs-lookup"><span data-stu-id="68e62-192">INDEX\_BUFFER</span></span>                 | <span data-ttu-id="68e62-193">Oui</span><span class="sxs-lookup"><span data-stu-id="68e62-193">Yes</span></span>                                          | <span data-ttu-id="68e62-194">Non</span><span class="sxs-lookup"><span data-stu-id="68e62-194">No</span></span>                                   |
| <span data-ttu-id="68e62-195">cible de rendu \_</span><span class="sxs-lookup"><span data-stu-id="68e62-195">RENDER\_TARGET</span></span>                | <span data-ttu-id="68e62-196">Oui</span><span class="sxs-lookup"><span data-stu-id="68e62-196">Yes</span></span>                                          | <span data-ttu-id="68e62-197">Non</span><span class="sxs-lookup"><span data-stu-id="68e62-197">No</span></span>                                   |
| <span data-ttu-id="68e62-198">accès non ordonné \_</span><span class="sxs-lookup"><span data-stu-id="68e62-198">UNORDERED\_ACCESS</span></span>             | <span data-ttu-id="68e62-199">Oui</span><span class="sxs-lookup"><span data-stu-id="68e62-199">Yes</span></span>                                          | <span data-ttu-id="68e62-200">Non</span><span class="sxs-lookup"><span data-stu-id="68e62-200">No</span></span>                                   |
| <span data-ttu-id="68e62-201">écriture de profondeur \_</span><span class="sxs-lookup"><span data-stu-id="68e62-201">DEPTH\_WRITE</span></span>                  | <span data-ttu-id="68e62-202">º<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="68e62-202">No<sup>\*</sup></span></span>                              | <span data-ttu-id="68e62-203">No</span><span class="sxs-lookup"><span data-stu-id="68e62-203">No</span></span>                                   |
| <span data-ttu-id="68e62-204">lecture de profondeur \_</span><span class="sxs-lookup"><span data-stu-id="68e62-204">DEPTH\_READ</span></span>                   | <span data-ttu-id="68e62-205">º<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="68e62-205">No<sup>\*</sup></span></span>                              | <span data-ttu-id="68e62-206">No</span><span class="sxs-lookup"><span data-stu-id="68e62-206">No</span></span>                                   |
| <span data-ttu-id="68e62-207">\_ressource de \_ nuanceur non pixel \_</span><span class="sxs-lookup"><span data-stu-id="68e62-207">NON\_PIXEL\_SHADER\_RESOURCE</span></span>  | <span data-ttu-id="68e62-208">Oui</span><span class="sxs-lookup"><span data-stu-id="68e62-208">Yes</span></span>                                          | <span data-ttu-id="68e62-209">Oui</span><span class="sxs-lookup"><span data-stu-id="68e62-209">Yes</span></span>                                  |
| <span data-ttu-id="68e62-210">\_ressource de nuanceur de pixels \_</span><span class="sxs-lookup"><span data-stu-id="68e62-210">PIXEL\_SHADER\_RESOURCE</span></span>       | <span data-ttu-id="68e62-211">Oui</span><span class="sxs-lookup"><span data-stu-id="68e62-211">Yes</span></span>                                          | <span data-ttu-id="68e62-212">Oui</span><span class="sxs-lookup"><span data-stu-id="68e62-212">Yes</span></span>                                  |
| <span data-ttu-id="68e62-213">DIFFUSER \_ en continu</span><span class="sxs-lookup"><span data-stu-id="68e62-213">STREAM\_OUT</span></span>                   | <span data-ttu-id="68e62-214">Oui</span><span class="sxs-lookup"><span data-stu-id="68e62-214">Yes</span></span>                                          | <span data-ttu-id="68e62-215">Non</span><span class="sxs-lookup"><span data-stu-id="68e62-215">No</span></span>                                   |
| <span data-ttu-id="68e62-216">\_argument indirect</span><span class="sxs-lookup"><span data-stu-id="68e62-216">INDIRECT\_ARGUMENT</span></span>            | <span data-ttu-id="68e62-217">Oui</span><span class="sxs-lookup"><span data-stu-id="68e62-217">Yes</span></span>                                          | <span data-ttu-id="68e62-218">Non</span><span class="sxs-lookup"><span data-stu-id="68e62-218">No</span></span>                                   |
| <span data-ttu-id="68e62-219">COPIER la \_ dest.</span><span class="sxs-lookup"><span data-stu-id="68e62-219">COPY\_DEST</span></span>                    | <span data-ttu-id="68e62-220">Oui</span><span class="sxs-lookup"><span data-stu-id="68e62-220">Yes</span></span>                                          | <span data-ttu-id="68e62-221">Oui</span><span class="sxs-lookup"><span data-stu-id="68e62-221">Yes</span></span>                                  |
| <span data-ttu-id="68e62-222">COPIER la \_ source</span><span class="sxs-lookup"><span data-stu-id="68e62-222">COPY\_SOURCE</span></span>                  | <span data-ttu-id="68e62-223">Oui</span><span class="sxs-lookup"><span data-stu-id="68e62-223">Yes</span></span>                                          | <span data-ttu-id="68e62-224">Oui</span><span class="sxs-lookup"><span data-stu-id="68e62-224">Yes</span></span>                                  |
| <span data-ttu-id="68e62-225">RÉSOUDRE la \_ dest.</span><span class="sxs-lookup"><span data-stu-id="68e62-225">RESOLVE\_DEST</span></span>                 | <span data-ttu-id="68e62-226">Oui</span><span class="sxs-lookup"><span data-stu-id="68e62-226">Yes</span></span>                                          | <span data-ttu-id="68e62-227">Non</span><span class="sxs-lookup"><span data-stu-id="68e62-227">No</span></span>                                   |
| <span data-ttu-id="68e62-228">RÉSOUDRE la \_ source</span><span class="sxs-lookup"><span data-stu-id="68e62-228">RESOLVE\_SOURCE</span></span>               | <span data-ttu-id="68e62-229">Oui</span><span class="sxs-lookup"><span data-stu-id="68e62-229">Yes</span></span>                                          | <span data-ttu-id="68e62-230">Non</span><span class="sxs-lookup"><span data-stu-id="68e62-230">No</span></span>                                   |
| <span data-ttu-id="68e62-231">PRÉDICATION</span><span class="sxs-lookup"><span data-stu-id="68e62-231">PREDICATION</span></span>                   | <span data-ttu-id="68e62-232">Oui</span><span class="sxs-lookup"><span data-stu-id="68e62-232">Yes</span></span>                                          | <span data-ttu-id="68e62-233">Non</span><span class="sxs-lookup"><span data-stu-id="68e62-233">No</span></span>                                   |



 

<span data-ttu-id="68e62-234"><sup>\*</sup>Les ressources de stencil de profondeur doivent être des textures d’accès non simultanées et ne peuvent donc jamais être promues implicitement.</span><span class="sxs-lookup"><span data-stu-id="68e62-234"><sup>\*</sup>Depth-stencil resources must be non-simultaneous-access textures and thus can never be implicitly promoted.</span></span>

<span data-ttu-id="68e62-235">Quand cet accès se produit, la promotion agit comme une barrière de ressources implicite.</span><span class="sxs-lookup"><span data-stu-id="68e62-235">When this access occurs the promotion acts like an implicit resource barrier.</span></span> <span data-ttu-id="68e62-236">Pour les accès suivants, les barrières des ressources sont nécessaires pour modifier l’état des ressources si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="68e62-236">For subsequent accesses, resource barriers will be required to change the resource state if necessary.</span></span> <span data-ttu-id="68e62-237">Notez que la promotion d’un état de lecture promu en un état de lecture multiple est valide, mais ce n’est pas le cas pour les États d’écriture.</span><span class="sxs-lookup"><span data-stu-id="68e62-237">Note that promotion from one promoted read state into multiple read state is valid, but this is not the case for write states.</span></span>  
<span data-ttu-id="68e62-238">Par exemple, si une ressource de l’État commun est promue en \_ ressource de nuanceur \_ de pixels dans un appel de dessin, elle peut toujours être promue en NON_PIXEL \_ ressource de nuanceur \_ | \_ \_ Ressource de nuanceur de pixels dans un autre appel de dessin.</span><span class="sxs-lookup"><span data-stu-id="68e62-238">For example, if a resource in the common state is promoted to PIXEL\_SHADER\_RESOURCE in a Draw call, it can still be promoted to NON_PIXEL\_SHADER\_RESOURCE | PIXEL\_SHADER\_RESOURCE in another Draw call.</span></span> <span data-ttu-id="68e62-239">Toutefois, s’il est utilisé dans une opération d’écriture, telle qu’une destination de copie, barrière de transition d’état de ressource par rapport aux États de lecture promus combinés, ici NON_PIXEL \_ ressource de nuanceur \_ | La \_ \_ ressource de nuanceur de pixels, pour copier la \_ destination, est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="68e62-239">However, if it is used in a write operation, such as a copy destination, a resource state transition barrier from the combined promoted read states, here NON_PIXEL\_SHADER\_RESOURCE | PIXEL\_SHADER\_RESOURCE, to COPY\_DEST is needed.</span></span>  
<span data-ttu-id="68e62-240">De même, si elle est promue de commun à copie de \_ destination, un cloisonnement est toujours nécessaire pour effectuer la transition de la destination de copie \_ à la cible de rendu \_ .</span><span class="sxs-lookup"><span data-stu-id="68e62-240">Similarly, if promoted from COMMON to COPY\_DEST, a barrier is still required to transition from COPY\_DEST to RENDER\_TARGET.</span></span>

<span data-ttu-id="68e62-241">Notez que la promotion de l’État commun est « gratuite » en ce qu’il n’est pas nécessaire que le GPU exécute des attentes de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="68e62-241">Note that common state promotion is "free" in that there is no need for the GPU to perform any synchronization waits.</span></span> <span data-ttu-id="68e62-242">La promotion représente le fait que les ressources dans l’État commun ne doivent pas nécessiter d’autres opérations GPU ou un suivi des pilotes pour prendre en charge certains accès.</span><span class="sxs-lookup"><span data-stu-id="68e62-242">The promotion represents the fact that resources in the COMMON state should not require additional GPU work or driver tracking to support certain accesses.</span></span>

### <a name="state-decay-to-common"></a><span data-ttu-id="68e62-243">État d’atténuation commun</span><span class="sxs-lookup"><span data-stu-id="68e62-243">State decay to common</span></span>

<span data-ttu-id="68e62-244">Le retournement de la promotion de l’État commun est la désintégration de l' \_ État de ressource D3D12 \_ \_ courant.</span><span class="sxs-lookup"><span data-stu-id="68e62-244">The flip-side of common state promotion is decay back to D3D12\_RESOURCE\_STATE\_COMMON.</span></span> <span data-ttu-id="68e62-245">Les ressources qui répondent à certaines exigences sont considérées comme sans État et retournent efficacement à l’État commun lorsque l’exécution d’une opération [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) est terminée.</span><span class="sxs-lookup"><span data-stu-id="68e62-245">Resources that meet certain requirements are considered to be stateless and effectively return to the common state when the GPU finishes execution of an [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) operation.</span></span> <span data-ttu-id="68e62-246">La désintégration n’a pas lieu entre les listes de commandes exécutées ensemble dans le même appel **ExecuteCommandLists** .</span><span class="sxs-lookup"><span data-stu-id="68e62-246">Decay does not occur between command lists executed together in the same **ExecuteCommandLists** call.</span></span>

<span data-ttu-id="68e62-247">Les ressources suivantes s’atténueront quand une opération [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) sera effectuée sur le GPU :</span><span class="sxs-lookup"><span data-stu-id="68e62-247">The following resources will decay when an [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) operation is completed on the GPU:</span></span>

-   <span data-ttu-id="68e62-248">Ressources faisant l’objet d’un accès sur une file d’attente de copie, *ou*</span><span class="sxs-lookup"><span data-stu-id="68e62-248">Resources being accessed on a Copy queue, *or*</span></span>
-   <span data-ttu-id="68e62-249">Des ressources de mémoire tampon sur n’importe quel type de file d’attente, *ou*</span><span class="sxs-lookup"><span data-stu-id="68e62-249">Buffer resources on any queue type, *or*</span></span>
-   <span data-ttu-id="68e62-250">Les ressources de texture sur tout type de file d’attente qui ont l' \_ indicateur de ressource D3D12 autoriser l’ensemble d’indicateurs d' \_ \_ \_ \_ accès simultané, *ou*</span><span class="sxs-lookup"><span data-stu-id="68e62-250">Texture resources on any queue type that have the D3D12\_RESOURCE\_FLAG\_ALLOW\_SIMULTANEOUS\_ACCESS flag set, *or*</span></span>
-   <span data-ttu-id="68e62-251">Toute ressource promue implicitement en état lecture seule.</span><span class="sxs-lookup"><span data-stu-id="68e62-251">Any resource implicitly promoted to a read-only state.</span></span>

<span data-ttu-id="68e62-252">À l’instar de la promotion de l’État commun, la désintégration est gratuite dans le fait qu’aucune synchronisation supplémentaire n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="68e62-252">Like common state promotion, the decay is free in that no additional synchronization is needed.</span></span> <span data-ttu-id="68e62-253">La combinaison de la promotion et de la dégradation de l’État commun permet d’éliminer de nombreuses transitions [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) inutiles.</span><span class="sxs-lookup"><span data-stu-id="68e62-253">Combining common state promotion and decay can help to eliminate many unnecessary [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions.</span></span> <span data-ttu-id="68e62-254">Dans certains cas, cela peut apporter des améliorations significatives en matière de performances.</span><span class="sxs-lookup"><span data-stu-id="68e62-254">In some cases, this can provide significant performance improvements.</span></span>

<span data-ttu-id="68e62-255">Les mémoires tampons et les ressources de Simultaneous-Access sont réaffectées à l’État commun, qu’elles aient été explicitement migrées à l’aide de barrières de ressources ou qu’elles soient promues implicitement.</span><span class="sxs-lookup"><span data-stu-id="68e62-255">Buffers and Simultaneous-Access resources will decay to the common state regardless of whether they were explicitly transitioned using resource barriers or implicitly promoted.</span></span>

### <a name="performance-implications"></a><span data-ttu-id="68e62-256">Impact sur les performances</span><span class="sxs-lookup"><span data-stu-id="68e62-256">Performance implications</span></span>

<span data-ttu-id="68e62-257">Lors de l’enregistrement de transitions [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) explicites sur des ressources dans l’État commun, il est correct d’utiliser l’état de \_ ressource D3D12 \_ \_ commun ou tout état pouvant être promu en tant que valeur de la *forêt* dans la structure de barrière de transition de \_ ressource D3D12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="68e62-257">When recording explicit [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions on resources in the common state, it is correct to use either D3D12\_RESOURCE\_STATE\_COMMON or any promotable state as the *BeforeState* value in the D3D12\_RESOURCE\_TRANSITION\_BARRIER structure.</span></span> <span data-ttu-id="68e62-258">Cela permet une gestion d’État traditionnelle qui ignore la désintégration automatique des mémoires tampons et des textures à accès simultané.</span><span class="sxs-lookup"><span data-stu-id="68e62-258">This allows traditional state management that ignores automatic decay of buffers and simultaneous-access textures.</span></span> <span data-ttu-id="68e62-259">Cela peut cependant ne pas être souhaitable, car l’évitement des appels **ResourceBarrier** de transition avec les ressources connues comme étant dans l’État commun peut améliorer les performances de manière significative.</span><span class="sxs-lookup"><span data-stu-id="68e62-259">This may not be desirable though, as avoiding transition **ResourceBarrier** calls with resources known to be in the common state can significantly improve performance.</span></span> <span data-ttu-id="68e62-260">Les barrières des ressources peuvent être onéreuses.</span><span class="sxs-lookup"><span data-stu-id="68e62-260">Resource barriers can be expensive.</span></span> <span data-ttu-id="68e62-261">Ils sont conçus pour forcer les vidages du cache, les modifications de la disposition de la mémoire et d’autres synchronisations qui peuvent ne pas être nécessaires pour les ressources qui sont déjà dans l’État commun.</span><span class="sxs-lookup"><span data-stu-id="68e62-261">They are designed to force cache flushes, memory layout changes and other synchronization that may not be necessary for resources already in the common state.</span></span> <span data-ttu-id="68e62-262">Une liste de commandes qui utilise une barrière de ressources d’un État non commun à un autre État non courant sur une ressource actuellement en état commun peut entraîner une surcharge importante.</span><span class="sxs-lookup"><span data-stu-id="68e62-262">A command list that uses a resource barrier from a non-common state to another non-common state on a resource currently in the common state can introduce a lot of unneeded overhead.</span></span>

<span data-ttu-id="68e62-263">Évitez également les transitions [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) explicites vers l' \_ État de ressource D3D12 \_ \_ courant, sauf si cela est absolument nécessaire (par exemple, l’accès suivant se trouve dans une file d’attente de commandes de copie qui nécessite une ressource commençant dans l’État commun).</span><span class="sxs-lookup"><span data-stu-id="68e62-263">Also, avoid explicit [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions to D3D12\_RESOURCE\_STATE\_COMMON unless absolutely necessary (e.g. the next access is on a COPY command queue which requires a resources begin in the common state).</span></span> <span data-ttu-id="68e62-264">Une transition excessive vers l’État commun peut ralentir considérablement les performances du GPU.</span><span class="sxs-lookup"><span data-stu-id="68e62-264">Excessive transitions to the common state can dramatically slow down GPU performance.</span></span>

<span data-ttu-id="68e62-265">En résumé, essayez de vous appuyer sur la promotion et la désintégration de l’État commun chaque fois que sa sémantique vous permet de quitter sans émettre d’appels [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) .</span><span class="sxs-lookup"><span data-stu-id="68e62-265">In summary, try to rely on common state promotion and decay whenever its semantics let you get away without issuing [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) calls.</span></span>

## <a name="split-barriers"></a><span data-ttu-id="68e62-266">Fractionner les barrières</span><span class="sxs-lookup"><span data-stu-id="68e62-266">Split Barriers</span></span>

<span data-ttu-id="68e62-267">Un cloisonnement de transition de ressource avec l’indicateur de barrière de ressources D3D12 de \_ \_ \_ \_ début \_ uniquement commence une barrière de fractionnement et le cloisonnement de transition est dit en attente.</span><span class="sxs-lookup"><span data-stu-id="68e62-267">A resource transition barrier with the D3D12\_RESOURCE\_BARRIER\_FLAG\_BEGIN\_ONLY flag begins a split barrier and the transition barrier is said to be pending.</span></span> <span data-ttu-id="68e62-268">Alors que le cloisonnement est en attente, la ressource (Sub) ne peut pas être lue ou écrite par le GPU.</span><span class="sxs-lookup"><span data-stu-id="68e62-268">While the barrier is pending the (sub)resource cannot be read or written by the GPU.</span></span> <span data-ttu-id="68e62-269">La seule barrière de transition légale qui peut être appliquée à une ressource (Sub) avec un cloisonnement en attente est l’une avec les mêmes États *avant* et *après* et l’indicateur de barrière de la \_ ressource D3D12 \_ \_ \_ End \_ only, lequel entrave termine la transition en attente.</span><span class="sxs-lookup"><span data-stu-id="68e62-269">The only legal transition barrier that can be applied to a (sub)resource with a pending barrier is one with the same *before* and *after* states and the D3D12\_RESOURCE\_BARRIER\_FLAG\_END\_ONLY flag, which barrier completes the pending transition.</span></span>

<span data-ttu-id="68e62-270">Les barrières fractionnées fournissent des indications au GPU qu’une ressource dans l’état *a* sera ensuite utilisée dans l’état *B* ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="68e62-270">Split barriers provide hints to the GPU that a resource in state *A* will next be used in state *B* sometime later.</span></span> <span data-ttu-id="68e62-271">Cela donne au GPU la possibilité d’optimiser la charge de travail de transition, ce qui peut réduire ou éliminer les blocages d’exécution.</span><span class="sxs-lookup"><span data-stu-id="68e62-271">This gives the GPU the option to optimize the transition workload, possibly reducing or eliminating execution stalls.</span></span> <span data-ttu-id="68e62-272">L’émission de la barrière de fin uniquement garantit que toutes les tâches de transition GPU sont terminées avant de passer à la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="68e62-272">Issuing the end-only barrier guarantees that all GPU transition work is finished before moving onto the next command.</span></span>

<span data-ttu-id="68e62-273">L’utilisation de cloisonnements peut contribuer à améliorer les performances, en particulier dans les scénarios impliquant plusieurs moteurs ou lorsque les ressources sont en cours de lecture/écriture dans une ou plusieurs listes de commandes.</span><span class="sxs-lookup"><span data-stu-id="68e62-273">Using split barriers can help to improve performance, especially in multi-engine scenarios or where resources are read/write transitioned sparsely throughout one or more command lists.</span></span>

## <a name="resource-barrier-example-scenario"></a><span data-ttu-id="68e62-274">Exemple de scénario de cloisonnement de ressources</span><span class="sxs-lookup"><span data-stu-id="68e62-274">Resource barrier example scenario</span></span>

<span data-ttu-id="68e62-275">Les extraits de code suivants illustrent l’utilisation de la méthode [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) dans un exemple de Multi-Threading.</span><span class="sxs-lookup"><span data-stu-id="68e62-275">The following snippets show the use of the [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) method in a multi-threading sample.</span></span>

<span data-ttu-id="68e62-276">Création de la vue du stencil de profondeur, transition vers un état accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="68e62-276">Creating the depth stencil view, transitioning it to a writeable state.</span></span>


```C++
// Create the depth stencil.
{
    CD3DX12_RESOURCE_DESC shadowTextureDesc(
        D3D12_RESOURCE_DIMENSION_TEXTURE2D,
        0,
        static_cast<UINT>(m_viewport.Width), 
        static_cast<UINT>(m_viewport.Height), 
        1,
        1,
        DXGI_FORMAT_D32_FLOAT,
        1, 
        0,
        D3D12_TEXTURE_LAYOUT_UNKNOWN,
        D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL | D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE);

    D3D12_CLEAR_VALUE clearValue;    // Performance tip: Tell the runtime at resource creation the desired clear value.
    clearValue.Format = DXGI_FORMAT_D32_FLOAT;
    clearValue.DepthStencil.Depth = 1.0f;
    clearValue.DepthStencil.Stencil = 0;

    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &shadowTextureDesc,
        D3D12_RESOURCE_STATE_DEPTH_WRITE,
        &clearValue,
        IID_PPV_ARGS(&m_depthStencil)));

    // Create the depth stencil view.
    m_device->CreateDepthStencilView(m_depthStencil.Get(), nullptr, m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
}
```



<span data-ttu-id="68e62-277">Création de la vue de mémoire tampon de vertex, en la remplaçant d’un État commun à une destination, puis d’une destination à un état de lecture générique.</span><span class="sxs-lookup"><span data-stu-id="68e62-277">Creating the vertex buffer view, first changing it from a common state to a destination, then from a destination to a generic readable state.</span></span>


```C++
// Create the vertex buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_vertexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the vertex buffer.
        D3D12_SUBRESOURCE_DATA vertexData = {};
        vertexData.pData = pAssetData + SampleAssets::VertexDataOffset;
        vertexData.RowPitch = SampleAssets::VertexDataSize;
        vertexData.SlicePitch = vertexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy vertex buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_vertexBuffer.Get(), m_vertexBufferUpload.Get(), 0, 0, 1, &vertexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_vertexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER));

        PIXEndEvent(commandList.Get());
    }
```



<span data-ttu-id="68e62-278">Création de la vue de la mémoire tampon d’index, première modification d’un État commun à une destination, puis d’une destination à un état de lecture générique.</span><span class="sxs-lookup"><span data-stu-id="68e62-278">Creating the index buffer view, first changing it from a common state to a destination, then from a destination to a generic readable state.</span></span>


```C++
// Create the index buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_indexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_indexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the index buffer.
        D3D12_SUBRESOURCE_DATA indexData = {};
        indexData.pData = pAssetData + SampleAssets::IndexDataOffset;
        indexData.RowPitch = SampleAssets::IndexDataSize;
        indexData.SlicePitch = indexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy index buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_indexBuffer.Get(), m_indexBufferUpload.Get(), 0, 0, 1, &indexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_indexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_INDEX_BUFFER));

        PIXEndEvent(commandList.Get());
    }

    // Initialize the index buffer view.
    m_indexBufferView.BufferLocation = m_indexBuffer->GetGPUVirtualAddress();
    m_indexBufferView.SizeInBytes = SampleAssets::IndexDataSize;
    m_indexBufferView.Format = SampleAssets::StandardIndexFormat;
}
```



<span data-ttu-id="68e62-279">Création de textures et de vues de ressources de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="68e62-279">Creating textures and shader resource views.</span></span> <span data-ttu-id="68e62-280">La texture passe d’un État commun à une destination, puis d’une destination à une ressource de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="68e62-280">The texture is changed from a common state to a destination, and then from a destination to a pixel shader resource.</span></span>


```C++
    // Create each texture and SRV descriptor.
    const UINT srvCount = _countof(SampleAssets::Textures);
    PIXBeginEvent(commandList.Get(), 0, L"Copy diffuse and normal texture data to default resources...");
    for (int i = 0; i < srvCount; i++)
    {
        // Describe and create a Texture2D.
        const SampleAssets::TextureResource &tex = SampleAssets::Textures[i];
        CD3DX12_RESOURCE_DESC texDesc(
            D3D12_RESOURCE_DIMENSION_TEXTURE2D,
            0,
            tex.Width, 
            tex.Height, 
            1,
            static_cast<UINT16>(tex.MipLevels),
            tex.Format,
            1, 
            0,
            D3D12_TEXTURE_LAYOUT_UNKNOWN,
            D3D12_RESOURCE_FLAG_NONE);

        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
            D3D12_HEAP_FLAG_NONE,
            &texDesc,
            D3D12_RESOURCE_STATE_COPY_DEST,
            nullptr,
            IID_PPV_ARGS(&m_textures[i])));

        {
            const UINT subresourceCount = texDesc.DepthOrArraySize * texDesc.MipLevels;
            UINT64 uploadBufferSize = GetRequiredIntermediateSize(m_textures[i].Get(), 0, subresourceCount);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
                D3D12_HEAP_FLAG_NONE,
                &CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize),
                D3D12_RESOURCE_STATE_GENERIC_READ,
                nullptr,
                IID_PPV_ARGS(&m_textureUploads[i])));

            // Copy data to the intermediate upload heap and then schedule a copy 
            // from the upload heap to the Texture2D.
            D3D12_SUBRESOURCE_DATA textureData = {};
            textureData.pData = pAssetData + tex.Data->Offset;
            textureData.RowPitch = tex.Data->Pitch;
            textureData.SlicePitch = tex.Data->Size;

            UpdateSubresources(commandList.Get(), m_textures[i].Get(), m_textureUploads[i].Get(), 0, 0, subresourceCount, &textureData);
            commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_textures[i].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
        }

        // Describe and create an SRV.
        D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
        srvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
        srvDesc.Format = tex.Format;
        srvDesc.Texture2D.MipLevels = tex.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = 0;
        srvDesc.Texture2D.ResourceMinLODClamp = 0.0f;
        m_device->CreateShaderResourceView(m_textures[i].Get(), &srvDesc, cbvSrvHandle);

        // Move to the next descriptor slot.
        cbvSrvHandle.Offset(cbvSrvDescriptorSize);
    }
```



<span data-ttu-id="68e62-281">Début d’un frame ; elle utilise non seulement [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) pour indiquer que la mémoire tampon de mise en mémoire tampon doit être utilisée comme cible de rendu, mais elle initialise également la ressource de frame (qui appelle **ResourceBarrier** sur la mémoire tampon du stencil de profondeur).</span><span class="sxs-lookup"><span data-stu-id="68e62-281">Beginning a frame; this not only uses [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) to indicate that the backbuffer is to be used as a render target, but also initializes the frame resource (which calls **ResourceBarrier** on the depth stencil buffer).</span></span>


```C++
// Assemble the CommandListPre command list.
void D3D12Multithreading::BeginFrame()
{
    m_pCurrentFrameResource->Init();

    // Indicate that the back buffer will be used as a render target.
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    // Clear the render target and depth stencil.
    const float clearColor[] = { 0.0f, 0.0f, 0.0f, 1.0f };
    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearDepthStencilView(m_dsvHeap->GetCPUDescriptorHandleForHeapStart(), D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPre]->Close());
}

// Assemble the CommandListMid command list.
void D3D12Multithreading::MidFrame()
{
    // Transition our shadow map from the shadow pass to readable in the scene pass.
    m_pCurrentFrameResource->SwapBarriers();

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListMid]->Close());
}
```



<span data-ttu-id="68e62-282">Fin d’un frame, indiquant que la mémoire tampon d’arrière-plan est maintenant utilisée.</span><span class="sxs-lookup"><span data-stu-id="68e62-282">Ending a frame, indicating the back buffer is now used to present.</span></span>


```C++
// Assemble the CommandListPost command list.
void D3D12Multithreading::EndFrame()
{
    m_pCurrentFrameResource->Finish();

    // Indicate that the back buffer will now be used to present.
    m_pCurrentFrameResource->m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPost]->Close());
}
```



<span data-ttu-id="68e62-283">L’initialisation d’une ressource Frame, appelée au début d’un frame, fait passer la mémoire tampon du stencil de profondeur à l’État inscriptible.</span><span class="sxs-lookup"><span data-stu-id="68e62-283">Initializing a frame resource, called when beginning a frame, transitions the depth stencil buffer to writeable.</span></span>


```C++
void FrameResource::Init()
{
    // Reset the command allocators and lists for the main thread.
    for (int i = 0; i < CommandListCount; i++)
    {
        ThrowIfFailed(m_commandAllocators[i]->Reset());
        ThrowIfFailed(m_commandLists[i]->Reset(m_commandAllocators[i].Get(), m_pipelineState.Get()));
    }

    // Clear the depth stencil buffer in preparation for rendering the shadow map.
    m_commandLists[CommandListPre]->ClearDepthStencilView(m_shadowDepthView, D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    // Reset the worker command allocators and lists.
    for (int i = 0; i < NumContexts; i++)
    {
        ThrowIfFailed(m_shadowCommandAllocators[i]->Reset());
        ThrowIfFailed(m_shadowCommandLists[i]->Reset(m_shadowCommandAllocators[i].Get(), m_pipelineStateShadowMap.Get()));

        ThrowIfFailed(m_sceneCommandAllocators[i]->Reset());
        ThrowIfFailed(m_sceneCommandLists[i]->Reset(m_sceneCommandAllocators[i].Get(), m_pipelineState.Get()));
    }
}
```



<span data-ttu-id="68e62-284">Les barrières sont échangées en milieu de trame, ce qui permet de faire passer le mappage des ombres de l’état accessible en lecture.</span><span class="sxs-lookup"><span data-stu-id="68e62-284">Barriers are swapped mid-frame, transitioning the shadow map from writeable to readable.</span></span>


```C++
void FrameResource::SwapBarriers()
{
    // Transition the shadow map from writeable to readable.
    m_commandLists[CommandListMid]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_DEPTH_WRITE, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
}
```



<span data-ttu-id="68e62-285">La méthode Finish est appelée lorsqu’une image est terminée, ce qui fait passer le mappage de l’ombre à un État commun.</span><span class="sxs-lookup"><span data-stu-id="68e62-285">Finish is called when a frame is ended, transitioning the shadow map to a common state.</span></span>


```C++
void FrameResource::Finish()
{
    m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE, D3D12_RESOURCE_STATE_DEPTH_WRITE));
}
```



## <a name="common-state-promotion-and-decay-sample"></a><span data-ttu-id="68e62-286">Exemple de promotion et d’atténuation de l’État commun</span><span class="sxs-lookup"><span data-stu-id="68e62-286">Common state promotion and decay sample</span></span>

``` syntax
    // Create a buffer resource using D3D12_RESOURCE_STATE_COMMON as the init state
    ID3D12Resource *pResource;
    CreateCommittedVertexBufferInCommonState(1024, &pResource);

    // Copy data to the buffer without the need for a barrier.
    // Promotes pResource state to D3D12_RESOURCE_STATE_COPY_DEST.
    pCommandList->CopyBufferRegion(pResource, 0, pOtherResource, 0, 1024); 

    // To use pResource as a vertex buffer a transition barrier is needed.
    // Note the StateBefore is D3D12_RESOURCE_STATE_COPY_DEST.
    D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TYPE_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_FLAG_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COPY_DEST;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    // Use pResource as a vertex buffer
    D3D12_VERTEX_BUFFER_VIEW vbView;
    vbView.BufferLocation = pResource->GetGPUVirtualAddress();
    vbView.SizeInBytes = 1024;
    vbView.StrideInBytes = sizeof(MyVertex);

    pCommandList->IASetVertexBuffers(0, 1, &vbView);
    pCommandList->Draw();

    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 
    pCommandList->Reset(pAllocator, pPipelineState);

    // Since the reset command list will be executed in a separate call to 
    // ExecuteCommandLists, the previous state of pResource
    // will have decayed to D3D12_RESOURCE_STATE_COMMON so, again, no barrier is needed
    pCommandList->CopyBufferRegion(pResource, 0, pDifferentResource, 0, 1024);

    FinishRecordingCommandList(pCommandList);
    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 

    WaitForQueue(pCommandQueue);

    // The previous ExecuteCommandLists call has finished so 
    // pResource has decayed to D3D12_RESOURCE_STATE_COMMON
```

## <a name="example-of-split-barriers"></a><span data-ttu-id="68e62-287">Exemple de barrières divisées</span><span class="sxs-lookup"><span data-stu-id="68e62-287">Example of split barriers</span></span>

<span data-ttu-id="68e62-288">L’exemple suivant montre comment utiliser une barrière Split pour réduire les blocages de pipeline.</span><span class="sxs-lookup"><span data-stu-id="68e62-288">The following example shows how to use a split barrier to reduce pipeline stalls.</span></span> <span data-ttu-id="68e62-289">Le code qui suit n’utilise pas de barrières divisées :</span><span class="sxs-lookup"><span data-stu-id="68e62-289">The code that follows does not use split barriers:</span></span>

``` syntax
 D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource
    OtherStuff(); // .. other gpu work

    // Transition pResource to PIXEL_SHADER_RESOURCE
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    Read(pResource); // ... read from pResource
```

<span data-ttu-id="68e62-290">Le code suivant utilise des barrières divisées :</span><span class="sxs-lookup"><span data-stu-id="68e62-290">The following code uses split barriers:</span></span>

``` syntax
D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource

    // Done writing to pResource. Start barrier to PIXEL_SHADER_RESOURCE and
    // then do other work
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_BEGIN_ONLY;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    OtherStuff(); // .. other gpu work

    // Need to read from pResource so end barrier
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_END_ONLY;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    Read(pResource); // ... read from pResource
```

## <a name="related-topics"></a><span data-ttu-id="68e62-291">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="68e62-291">Related topics</span></span>

[<span data-ttu-id="68e62-292">Didacticiels vidéo sur DirectX Advanced Learning : barrières des ressources et suivi de l’État</span><span class="sxs-lookup"><span data-stu-id="68e62-292">DirectX advanced learning video tutorials : Resource Barriers and State Tracking</span></span>](https://www.youtube.com/watch?v=nmB2XMasz2o)

[<span data-ttu-id="68e62-293">Synchronisation multi-moteur</span><span class="sxs-lookup"><span data-stu-id="68e62-293">Multi-engine synchronization</span></span>](./user-mode-heap-synchronization.md)

[<span data-ttu-id="68e62-294">Envoi de travail dans Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="68e62-294">Work Submission in Direct3D 12</span></span>](command-queues-and-command-lists.md)

[<span data-ttu-id="68e62-295">Examiner les barrières de l’état des ressources D3D12</span><span class="sxs-lookup"><span data-stu-id="68e62-295">A Look Inside D3D12 Resource State Barriers</span></span>](https://devblogs.microsoft.com/directx/a-look-inside-d3d12-resource-state-barriers/)

