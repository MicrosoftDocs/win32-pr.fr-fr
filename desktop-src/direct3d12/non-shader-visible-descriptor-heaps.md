---
title: Tas du descripteur non visible par le nuanceur
description: Certains tas de descripteurs ne peuvent pas être référencés par des nuanceurs par le biais de tables de descripteurs, mais ils existent pour aider l’application à mettre en attente les descripteurs avant l’enregistrement d’une liste de commandes ou parce qu’aucun tas visible par le nuanceur n’est requis.
ms.assetid: 85934873-8889-4564-A717-28A00614B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d51d30c7a99250ee0842b79d76ccebb6150bcf9a
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343454"
---
# <a name="non-shader-visible-descriptor-heaps"></a><span data-ttu-id="fe5aa-103">Tas du descripteur non visible par le nuanceur</span><span class="sxs-lookup"><span data-stu-id="fe5aa-103">Non Shader Visible Descriptor Heaps</span></span>

<span data-ttu-id="fe5aa-104">Certains tas de descripteurs ne peuvent pas être référencés par des nuanceurs par le biais de tables de descripteurs, mais ils existent pour aider l’application à mettre en attente les descripteurs avant l’enregistrement d’une liste de commandes ou parce qu’aucun tas visible par le nuanceur n’est requis.</span><span class="sxs-lookup"><span data-stu-id="fe5aa-104">Some descriptor heaps cannot be referenced by shaders through descriptor tables, but exist either to assist the app in staging the descriptors prior to recording a command list or because no shader-visible heap is required.</span></span>

-   [<span data-ttu-id="fe5aa-105">Affichages non visibles</span><span class="sxs-lookup"><span data-stu-id="fe5aa-105">Non-visible views</span></span>](#non-visible-views)
-   [<span data-ttu-id="fe5aa-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="fe5aa-106">Summary</span></span>](#summary)
-   [<span data-ttu-id="fe5aa-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe5aa-107">Related topics</span></span>](#related-topics)

## <a name="non-visible-views"></a><span data-ttu-id="fe5aa-108">Affichages non visibles</span><span class="sxs-lookup"><span data-stu-id="fe5aa-108">Non-visible views</span></span>

<span data-ttu-id="fe5aa-109">Tous les tas de descripteurs, y compris les tas de descripteurs accessibles aux nuanceurs décrits précédemment, peuvent être manipulés par les listes d’UC et/ou de commandes selon les propriétés du pool de mémoire et de l’accès au processeur que l’application sélectionne pour un tas de descripteur.</span><span class="sxs-lookup"><span data-stu-id="fe5aa-109">All descriptor heaps, including the shader accessible descriptor heaps described previously, can be manipulated by the CPU and/or command lists depending on the memory pool and CPU access properties the application selects for a descriptor heap.</span></span>

<span data-ttu-id="fe5aa-110">Pour les [tas de descripteurs visibles du nuanceur](shader-visible-descriptor-heaps.md), la raison évidente de refuser l’accès du nuanceur à ces tas de descripteurs est lorsqu’ils sont en cours d’installation.</span><span class="sxs-lookup"><span data-stu-id="fe5aa-110">For [Shader Visible Descriptor Heaps](shader-visible-descriptor-heaps.md), the obvious reason to deny shader access to these descriptor heaps is while they are being staged.</span></span> <span data-ttu-id="fe5aa-111">Ces tas sont alors rendus visibles par le Shader et accessibles via les tables de descripteurs au moment de l’exécution de la liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="fe5aa-111">Then these heaps are made shader-visible, and accessed via descriptor tables at command list execution.</span></span> <span data-ttu-id="fe5aa-112">Toutefois, il n’est pas nécessaire de préparer les tas visibles par le nuanceur, ils peuvent être remplis directement.</span><span class="sxs-lookup"><span data-stu-id="fe5aa-112">However, there is no requirement to stage shader-visible heaps, they can be populated directly.</span></span>

<span data-ttu-id="fe5aa-113">D’autres descripteurs sont liés au pipeline en faisant en sorte que leur contenu soit enregistré directement dans la liste des commandes.</span><span class="sxs-lookup"><span data-stu-id="fe5aa-113">Other descriptors get bound to the pipeline by having their contents recorded directly into the command list.</span></span> <span data-ttu-id="fe5aa-114">Ces descripteurs servent uniquement à traduire les paramètres de vue au moment de l’enregistrement de la liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="fe5aa-114">These descriptors only serve to translate the view parameters at command list record time.</span></span> <span data-ttu-id="fe5aa-115">Ces tas sont toujours visibles non-nuanceur et contiennent les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="fe5aa-115">These heaps are always non-shader visible and contain the following.</span></span>

-   <span data-ttu-id="fe5aa-116">Affichages des cibles de rendu (RTVs)</span><span class="sxs-lookup"><span data-stu-id="fe5aa-116">Render Target Views (RTVs)</span></span>
-   <span data-ttu-id="fe5aa-117">Vues du stencil de profondeur (DSV)</span><span class="sxs-lookup"><span data-stu-id="fe5aa-117">Depth Stencil Views (DSVs)</span></span>

<span data-ttu-id="fe5aa-118">Les vues de mémoire tampon d’index (IBVs), les vues de mémoire tampon de vertex (VBVs) et les vues de sortie de flux (SOVs) sont passées directement aux méthodes d’API, et ne possèdent pas de types de tas spécifiques.</span><span class="sxs-lookup"><span data-stu-id="fe5aa-118">Index Buffer Views (IBVs), Vertex Buffer Views (VBVs), and Stream Output Views (SOVs) are passed directly to API methods, are do not have specific heap types.</span></span>

<span data-ttu-id="fe5aa-119">Après l’enregistrement dans la liste de commandes (avec un appel tel que [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets), par exemple), la mémoire utilisée pour stocker les descripteurs pour cet appel est immédiatement disponible pour une réutilisation après l’appel.</span><span class="sxs-lookup"><span data-stu-id="fe5aa-119">After recording into the command list (with a call such as [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets), for example) the memory used to hold the descriptors for this call is immediately available for re-use after the call.</span></span>

<span data-ttu-id="fe5aa-120">Même les tables de descripteur ont des options dans lesquelles une application peut permettre à l’implémentation de choisir d’enregistrer le contenu de la table dans l’enregistrement de la liste de commandes (plutôt que de déréférencer le pointeur de table au moment de l’exécution).</span><span class="sxs-lookup"><span data-stu-id="fe5aa-120">Even descriptor tables have options where an app can allow the implementation to choose to record the table contents at command list recording (rather than dereference the table pointer at execution).</span></span>

## <a name="summary"></a><span data-ttu-id="fe5aa-121">Résumé</span><span class="sxs-lookup"><span data-stu-id="fe5aa-121">Summary</span></span>



|                   | <span data-ttu-id="fe5aa-122">Nuanceur visible, UC en écriture seule</span><span class="sxs-lookup"><span data-stu-id="fe5aa-122">Shader visible, CPU write only</span></span>                                   | <span data-ttu-id="fe5aa-123">Non-nuanceur visible, lecture/écriture de l’UC</span><span class="sxs-lookup"><span data-stu-id="fe5aa-123">Non-shader visible, CPU read/write</span></span>                                       |
|-------------------|------------------------------------|----------------------------------------|
| <span data-ttu-id="fe5aa-124">**CBV, SRV, UAV**</span><span class="sxs-lookup"><span data-stu-id="fe5aa-124">**CBV, SRV, UAV**</span></span> | <span data-ttu-id="fe5aa-125">oui</span><span class="sxs-lookup"><span data-stu-id="fe5aa-125">yes</span></span>                                | <span data-ttu-id="fe5aa-126">oui</span><span class="sxs-lookup"><span data-stu-id="fe5aa-126">yes</span></span>                                    |
| <span data-ttu-id="fe5aa-127">**ÉCHANTILLONNEUR**</span><span class="sxs-lookup"><span data-stu-id="fe5aa-127">**SAMPLER**</span></span>       | <span data-ttu-id="fe5aa-128">oui</span><span class="sxs-lookup"><span data-stu-id="fe5aa-128">yes</span></span>                                | <span data-ttu-id="fe5aa-129">oui</span><span class="sxs-lookup"><span data-stu-id="fe5aa-129">yes</span></span>                                    |
| <span data-ttu-id="fe5aa-130">**Retour au fournisseur**</span><span class="sxs-lookup"><span data-stu-id="fe5aa-130">**RTV**</span></span>           | <span data-ttu-id="fe5aa-131">non</span><span class="sxs-lookup"><span data-stu-id="fe5aa-131">no</span></span>                                 | <span data-ttu-id="fe5aa-132">oui</span><span class="sxs-lookup"><span data-stu-id="fe5aa-132">yes</span></span>                                    |
| <span data-ttu-id="fe5aa-133">**VUE**</span><span class="sxs-lookup"><span data-stu-id="fe5aa-133">**DSV**</span></span>           | <span data-ttu-id="fe5aa-134">non</span><span class="sxs-lookup"><span data-stu-id="fe5aa-134">no</span></span>                                 | <span data-ttu-id="fe5aa-135">oui</span><span class="sxs-lookup"><span data-stu-id="fe5aa-135">yes</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="fe5aa-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe5aa-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe5aa-137">Tas de descripteurs</span><span class="sxs-lookup"><span data-stu-id="fe5aa-137">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




