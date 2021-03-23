---
title: Tas de descripteurs
description: Un tas de descripteur est une collection d’allocations contiguës de descripteurs, une allocation pour chaque descripteur.
ms.assetid: 04d3facf-21ec-45ca-ad9b-78fdcddc7136
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f19821cff5e8730c376e5c80fef07e67974d31d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103977"
---
# <a name="descriptor-heaps"></a><span data-ttu-id="24da9-103">Tas de descripteurs</span><span class="sxs-lookup"><span data-stu-id="24da9-103">Descriptor Heaps</span></span>

<span data-ttu-id="24da9-104">Un tas de descripteur est une collection d’allocations contiguës de descripteurs, une allocation pour chaque descripteur.</span><span class="sxs-lookup"><span data-stu-id="24da9-104">A descriptor heap is a collection of contiguous allocations of descriptors, one allocation for every descriptor.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="24da9-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="24da9-105">In this section</span></span>



| <span data-ttu-id="24da9-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="24da9-106">Topic</span></span>                                                                                             | <span data-ttu-id="24da9-107">Description</span><span class="sxs-lookup"><span data-stu-id="24da9-107">Description</span></span>                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="24da9-108">Vue d’ensemble des tas de descripteurs</span><span class="sxs-lookup"><span data-stu-id="24da9-108">Descriptor Heaps Overview</span></span>](descriptor-heaps-overview.md)<br/>                             | <span data-ttu-id="24da9-109">Les tas de descripteurs contiennent de nombreux types d’objets qui ne font pas partie d’un objet d’État du pipeline (PSO), tels que les vues des ressources de nuanceur (SRVs), les vues d’accès non ordonnées (UAVs), les vues de mémoire tampon constante (CBVs) et les échantillonneurs.</span><span class="sxs-lookup"><span data-stu-id="24da9-109">Descriptor heaps contain many object types that are not part of a Pipeline State Object (PSO), such as Shader Resource Views (SRVs), Unordered Access Views (UAVs), Constant Buffer Views (CBVs), and Samplers.</span></span> <br/>                |
| [<span data-ttu-id="24da9-110">Niveaux matériels</span><span class="sxs-lookup"><span data-stu-id="24da9-110">Hardware Tiers</span></span>](hardware-support.md)<br/>                                                 | <span data-ttu-id="24da9-111">Les niveaux de matériel du niveau 1 au niveau 3 ont des ressources accrues disponibles pour le pipeline.</span><span class="sxs-lookup"><span data-stu-id="24da9-111">The levels of hardware from Tier 1 to Tier 3 have increasing resources available to the pipeline.</span></span> <br/>                                                                                                                              |
| [<span data-ttu-id="24da9-112">Tas du descripteur visible par le nuanceur</span><span class="sxs-lookup"><span data-stu-id="24da9-112">Shader Visible Descriptor Heaps</span></span>](shader-visible-descriptor-heaps.md)<br/>                 | <span data-ttu-id="24da9-113">Les tas de descripteurs visibles du nuanceur, sont des tas de descripteurs qui peuvent être référencés par des nuanceurs par le biais de tables de descripteurs.</span><span class="sxs-lookup"><span data-stu-id="24da9-113">Shader visible descriptor heaps, are descriptor heaps that can be referenced by shaders through descriptor tables.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="24da9-114">Tas de descripteurs non visibles par le nuanceur</span><span class="sxs-lookup"><span data-stu-id="24da9-114">Non Shader Visible Descriptor Heaps</span></span>](non-shader-visible-descriptor-heaps.md)<br/>         | <span data-ttu-id="24da9-115">Certains tas de descripteurs ne peuvent pas être référencés par des nuanceurs par le biais de tables de descripteurs, mais ils existent pour aider l’application à mettre en attente les descripteurs avant l’enregistrement d’une liste de commandes ou parce qu’aucun tas visible par le nuanceur n’est requis.</span><span class="sxs-lookup"><span data-stu-id="24da9-115">Some descriptor heaps cannot be referenced by shaders through descriptor tables, but exist either to assist the app in staging the descriptors prior to recording a command list or because no shader-visible heap is required.</span></span><br/> |
| [<span data-ttu-id="24da9-116">Création de tas de descripteurs</span><span class="sxs-lookup"><span data-stu-id="24da9-116">Creating Descriptor Heaps</span></span>](creating-descriptor-heaps.md)<br/>                             | <span data-ttu-id="24da9-117">Pour créer et configurer un tas de descripteur, vous devez sélectionner un type de tas de descripteur, déterminer le nombre de descripteurs qu’il contient et définir des indicateurs qui indiquent s’il est visible par l’UC et/ou nuanceur visible.</span><span class="sxs-lookup"><span data-stu-id="24da9-117">To create and configure a descriptor heap, you must select a descriptor heap type, determine how many descriptors it contains, and set flags that indicate whether it is CPU visible and/or shader visible.</span></span> <br/>                    |
| [<span data-ttu-id="24da9-118">Définition et remplissage des tas de descripteurs</span><span class="sxs-lookup"><span data-stu-id="24da9-118">Setting and Populating Descriptor Heaps</span></span>](setting-descriptor-heaps.md)<br/>                | <span data-ttu-id="24da9-119">Les types de tas de descripteur qui peuvent être définis sur une liste de commandes sont ceux qui contiennent des descripteurs pour lesquels les tables de descripteurs peuvent être utilisées (au plus une de chacune à la fois).</span><span class="sxs-lookup"><span data-stu-id="24da9-119">The descriptor heap types that can be set on a command list are those that contain descriptors for which descriptor tables can be used (at most one of each at a time).</span></span> <br/>                                                        |
| [<span data-ttu-id="24da9-120">Résumé de la configuration du tas de descripteurs</span><span class="sxs-lookup"><span data-stu-id="24da9-120">Descriptor Heap Configurability Summary</span></span>](descriptor-heap-configurability-summary.md)<br/> | <span data-ttu-id="24da9-121">Le tableau suivant récapitule les informations sur la prise en charge des tas et des tas visibles non-nuanceur.</span><span class="sxs-lookup"><span data-stu-id="24da9-121">The following table summarizes information about Shader and non-Shader visible heap support.</span></span><br/>                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="24da9-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="24da9-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24da9-123">Descripteurs</span><span class="sxs-lookup"><span data-stu-id="24da9-123">Descriptors</span></span>](descriptors.md)
</dt> <dt>

[<span data-ttu-id="24da9-124">Tables de descripteurs</span><span class="sxs-lookup"><span data-stu-id="24da9-124">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> <dt>

[<span data-ttu-id="24da9-125">**ID3D12DescriptorHeap**</span><span class="sxs-lookup"><span data-stu-id="24da9-125">**ID3D12DescriptorHeap**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)
</dt> <dt>

[<span data-ttu-id="24da9-126">Liaison de ressource</span><span class="sxs-lookup"><span data-stu-id="24da9-126">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="24da9-127">Signatures racines</span><span class="sxs-lookup"><span data-stu-id="24da9-127">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 





