---
title: Tas de descripteurs non visibles par le nuanceur
description: Certains tas de descripteurs ne peuvent pas être référencés par des nuanceurs par le biais de tables de descripteurs, mais ils existent pour aider l’application à mettre en attente les descripteurs avant l’enregistrement d’une liste de commandes ou parce qu’aucun tas visible par le nuanceur n’est requis.
ms.assetid: 85934873-8889-4564-A717-28A00614B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 894640cde142f1241b088518ba7140ffb9405152
ms.sourcegitcommit: 015fb35e736a235d3c9becff1f6832a0965b4303
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548521"
---
# <a name="non-shader-visible-descriptor-heaps"></a><span data-ttu-id="c7bcc-103">Tas de descripteurs non visibles par le nuanceur</span><span class="sxs-lookup"><span data-stu-id="c7bcc-103">Non Shader Visible Descriptor Heaps</span></span>

<span data-ttu-id="c7bcc-104">Certains tas de descripteurs ne peuvent pas être référencés par des nuanceurs par le biais de tables de descripteurs, mais ils existent pour aider l’application à mettre en attente les descripteurs avant l’enregistrement d’une liste de commandes ou parce qu’aucun tas visible par le nuanceur n’est requis.</span><span class="sxs-lookup"><span data-stu-id="c7bcc-104">Some descriptor heaps cannot be referenced by shaders through descriptor tables, but exist either to assist the app in staging the descriptors prior to recording a command list or because no shader-visible heap is required.</span></span>

-   [<span data-ttu-id="c7bcc-105">Affichages non visibles</span><span class="sxs-lookup"><span data-stu-id="c7bcc-105">Non-visible views</span></span>](#non-visible-views)
-   [<span data-ttu-id="c7bcc-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="c7bcc-106">Summary</span></span>](#summary)
-   [<span data-ttu-id="c7bcc-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c7bcc-107">Related topics</span></span>](#related-topics)

## <a name="non-visible-views"></a><span data-ttu-id="c7bcc-108">Affichages non visibles</span><span class="sxs-lookup"><span data-stu-id="c7bcc-108">Non-visible views</span></span>

<span data-ttu-id="c7bcc-109">Tous les tas de descripteurs, y compris les tas de descripteurs accessibles aux nuanceurs décrits précédemment, peuvent être manipulés par les listes d’UC et/ou de commandes selon les propriétés du pool de mémoire et de l’accès au processeur que l’application sélectionne pour un tas de descripteur.</span><span class="sxs-lookup"><span data-stu-id="c7bcc-109">All descriptor heaps, including the shader accessible descriptor heaps described previously, can be manipulated by the CPU and/or command lists depending on the memory pool and CPU access properties the application selects for a descriptor heap.</span></span>

<span data-ttu-id="c7bcc-110">Pour les [tas de descripteurs visibles du nuanceur](shader-visible-descriptor-heaps.md), la raison évidente de refuser l’accès du nuanceur à ces tas de descripteurs est lorsqu’ils sont en cours d’installation.</span><span class="sxs-lookup"><span data-stu-id="c7bcc-110">For [Shader Visible Descriptor Heaps](shader-visible-descriptor-heaps.md), the obvious reason to deny shader access to these descriptor heaps is while they are being staged.</span></span> <span data-ttu-id="c7bcc-111">Ces tas sont alors rendus visibles par le Shader et accessibles via les tables de descripteurs au moment de l’exécution de la liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="c7bcc-111">Then these heaps are made shader-visible, and accessed via descriptor tables at command list execution.</span></span> <span data-ttu-id="c7bcc-112">Toutefois, il n’est pas nécessaire de préparer les tas visibles par le nuanceur, ils peuvent être remplis directement.</span><span class="sxs-lookup"><span data-stu-id="c7bcc-112">However, there is no requirement to stage shader-visible heaps, they can be populated directly.</span></span>

<span data-ttu-id="c7bcc-113">D’autres descripteurs sont liés au pipeline en faisant en sorte que leur contenu soit enregistré directement dans la liste des commandes.</span><span class="sxs-lookup"><span data-stu-id="c7bcc-113">Other descriptors get bound to the pipeline by having their contents recorded directly into the command list.</span></span> <span data-ttu-id="c7bcc-114">Ces descripteurs servent uniquement à traduire les paramètres de vue au moment de l’enregistrement de la liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="c7bcc-114">These descriptors only serve to translate the view parameters at command list record time.</span></span> <span data-ttu-id="c7bcc-115">Ces tas sont toujours visibles non-nuanceur et contiennent les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="c7bcc-115">These heaps are always non-shader visible and contain the following.</span></span>

-   <span data-ttu-id="c7bcc-116">Affichages des cibles de rendu (RTVs)</span><span class="sxs-lookup"><span data-stu-id="c7bcc-116">Render Target Views (RTVs)</span></span>
-   <span data-ttu-id="c7bcc-117">Vues du stencil de profondeur (DSV)</span><span class="sxs-lookup"><span data-stu-id="c7bcc-117">Depth Stencil Views (DSVs)</span></span>

<span data-ttu-id="c7bcc-118">Les vues de mémoire tampon d’index (IBVs), les vues de mémoire tampon de vertex (VBVs) et les vues de sortie de flux (SOVs) sont passées directement aux méthodes d’API, et ne possèdent pas de types de tas spécifiques.</span><span class="sxs-lookup"><span data-stu-id="c7bcc-118">Index Buffer Views (IBVs), Vertex Buffer Views (VBVs), and Stream Output Views (SOVs) are passed directly to API methods, are do not have specific heap types.</span></span>

<span data-ttu-id="c7bcc-119">Après l’enregistrement dans la liste de commandes (avec un appel tel que [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets), par exemple), la mémoire utilisée pour stocker les descripteurs pour cet appel est immédiatement disponible pour une réutilisation après l’appel.</span><span class="sxs-lookup"><span data-stu-id="c7bcc-119">After recording into the command list (with a call such as [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets), for example) the memory used to hold the descriptors for this call is immediately available for re-use after the call.</span></span>

<span data-ttu-id="c7bcc-120">Même les tables de descripteur ont des options dans lesquelles une application peut permettre à l’implémentation de choisir d’enregistrer le contenu de la table dans l’enregistrement de la liste de commandes (plutôt que de déréférencer le pointeur de table au moment de l’exécution).</span><span class="sxs-lookup"><span data-stu-id="c7bcc-120">Even descriptor tables have options where an app can allow the implementation to choose to record the table contents at command list recording (rather than dereference the table pointer at execution).</span></span>

## <a name="summary"></a><span data-ttu-id="c7bcc-121">Résumé</span><span class="sxs-lookup"><span data-stu-id="c7bcc-121">Summary</span></span>



|                   |                                    |                                        |
|-------------------|------------------------------------|----------------------------------------|
|                   | <span data-ttu-id="c7bcc-122">**nuanceur visible, UC en écriture seule**</span><span class="sxs-lookup"><span data-stu-id="c7bcc-122">**shader visible, CPU write only**</span></span> | <span data-ttu-id="c7bcc-123">**non-nuanceur visible, lecture/écriture de l’UC**</span><span class="sxs-lookup"><span data-stu-id="c7bcc-123">**non-shader visible, CPU read/write**</span></span> |
| <span data-ttu-id="c7bcc-124">**CBV, SRV, UAV**</span><span class="sxs-lookup"><span data-stu-id="c7bcc-124">**CBV, SRV, UAV**</span></span> | <span data-ttu-id="c7bcc-125">Oui</span><span class="sxs-lookup"><span data-stu-id="c7bcc-125">yes</span></span>                                | <span data-ttu-id="c7bcc-126">Oui</span><span class="sxs-lookup"><span data-stu-id="c7bcc-126">yes</span></span>                                    |
| <span data-ttu-id="c7bcc-127">**ÉCHANTILLONNEUR**</span><span class="sxs-lookup"><span data-stu-id="c7bcc-127">**SAMPLER**</span></span>       | <span data-ttu-id="c7bcc-128">Oui</span><span class="sxs-lookup"><span data-stu-id="c7bcc-128">yes</span></span>                                | <span data-ttu-id="c7bcc-129">Oui</span><span class="sxs-lookup"><span data-stu-id="c7bcc-129">yes</span></span>                                    |
| <span data-ttu-id="c7bcc-130">**Retour au fournisseur**</span><span class="sxs-lookup"><span data-stu-id="c7bcc-130">**RTV**</span></span>           | <span data-ttu-id="c7bcc-131">non</span><span class="sxs-lookup"><span data-stu-id="c7bcc-131">no</span></span>                                 | <span data-ttu-id="c7bcc-132">Oui</span><span class="sxs-lookup"><span data-stu-id="c7bcc-132">yes</span></span>                                    |
| <span data-ttu-id="c7bcc-133">**VUE**</span><span class="sxs-lookup"><span data-stu-id="c7bcc-133">**DSV**</span></span>           | <span data-ttu-id="c7bcc-134">non</span><span class="sxs-lookup"><span data-stu-id="c7bcc-134">no</span></span>                                 | <span data-ttu-id="c7bcc-135">Oui</span><span class="sxs-lookup"><span data-stu-id="c7bcc-135">yes</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="c7bcc-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c7bcc-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7bcc-137">Tas de descripteurs</span><span class="sxs-lookup"><span data-stu-id="c7bcc-137">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




