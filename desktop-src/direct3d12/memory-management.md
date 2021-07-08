---
title: Gestion de la mémoire dans Direct3D 12
description: Le passage à D3D12 implique une synchronisation et une gestion appropriées de la résidence en mémoire.
ms.assetid: 94D47EBB-8060-49F6-A1FF-8B7B98AD5363
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b8091c2893f8906fe2ab5baadbf1288a1474cd
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481804"
---
# <a name="memory-management-in-direct3d-12"></a><span data-ttu-id="35a99-103">Gestion de la mémoire dans Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="35a99-103">Memory Management in Direct3D 12</span></span>

<span data-ttu-id="35a99-104">Le passage à D3D12 implique une synchronisation et une gestion appropriées de la résidence en mémoire.</span><span class="sxs-lookup"><span data-stu-id="35a99-104">Moving to D3D12 involves doing proper synchronization and management of memory residency.</span></span> <span data-ttu-id="35a99-105">La gestion de la résidence en mémoire signifie qu’une plus grande synchronisation doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="35a99-105">Managing memory residency means even more synchronization must be done.</span></span> <span data-ttu-id="35a99-106">Cette section traite des stratégies de gestion de la mémoire et de la sous-allocation au sein des tas et des mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="35a99-106">This section covers memory management strategies, and suballocation within heaps and buffers.</span></span>

-   [<span data-ttu-id="35a99-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="35a99-107">In this section</span></span>](#in-this-section)
-   [<span data-ttu-id="35a99-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="35a99-108">Related topics</span></span>](#related-topics)

## <a name="in-this-section"></a><span data-ttu-id="35a99-109">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="35a99-109">In this section</span></span>



| <span data-ttu-id="35a99-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="35a99-110">Topic</span></span>                                                                       | <span data-ttu-id="35a99-111">Description</span><span class="sxs-lookup"><span data-stu-id="35a99-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35a99-112">Stratégies de gestion de la mémoire</span><span class="sxs-lookup"><span data-stu-id="35a99-112">Memory Management Strategies</span></span>](memory-management-strategies.md)<br/> | <span data-ttu-id="35a99-113">Un gestionnaire de mémoire pour Direct3D 12 peut être très compliqué rapidement avec les différents niveaux de prise en charge, pour les adaptateurs UMA ou discrets (non-UMA) et avec un large éventail de différences d’architecture entre les adaptateurs GPU.</span><span class="sxs-lookup"><span data-stu-id="35a99-113">A memory manager for Direct3D 12 could get very complicated quickly with all the different tiers of support, for UMA or discrete (non-UMA) adapters, and with a considerable range of architecture differences between GPU adapters.</span></span><br/> <span data-ttu-id="35a99-114">La stratégie recommandée pour la gestion de la mémoire Direct3D 12, décrite dans cette section, est « classification, budget et flux ».</span><span class="sxs-lookup"><span data-stu-id="35a99-114">The recommended strategy for Direct3D 12 memory management , described in this section, is "classify, budget and stream".</span></span><br/> |
| [<span data-ttu-id="35a99-115">Sous-allocation au sein des tampons</span><span class="sxs-lookup"><span data-stu-id="35a99-115">Suballocation Within Buffers</span></span>](large-buffers.md)<br/>                | <span data-ttu-id="35a99-116">Les mémoires tampons disposent de toutes les fonctionnalités nécessaires dans D3D12 pour les applications afin de transférer une grande plage de données temporaires du processeur vers le GPU.</span><span class="sxs-lookup"><span data-stu-id="35a99-116">Buffers have all the features necessary in D3D12 for applications to transfer a large range of transient data from the CPU to the GPU.</span></span> <span data-ttu-id="35a99-117">Cette section aborde les quatre scénarios courants d’utilisation et de gestion des ressources et des mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="35a99-117">This section covers four common scenarios for the use and management of resources and buffers.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="35a99-118">Sous-allocation au sein des tas</span><span class="sxs-lookup"><span data-stu-id="35a99-118">Suballocation Within Heaps</span></span>](suballocation-within-heaps.md)<br/>     | <span data-ttu-id="35a99-119">Les tas de ressources transfèrent les données de l’UC vers le GPU (chargement) et du GPU vers le processeur (lecture en retour).</span><span class="sxs-lookup"><span data-stu-id="35a99-119">Resource heaps transfer data from the CPU to the GPU (upload), and from the GPU to the CPU (read back).</span></span> <br/>                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="35a99-120">Résidence</span><span class="sxs-lookup"><span data-stu-id="35a99-120">Residency</span></span>](residency.md)<br/>                                       | <span data-ttu-id="35a99-121">Un objet est considéré comme *résident* lorsqu’il est accessible par le GPU.</span><span class="sxs-lookup"><span data-stu-id="35a99-121">An object is considered to be *resident* when it is accessible by the GPU.</span></span><br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="35a99-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="35a99-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35a99-123">Guide de programmation de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="35a99-123">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="35a99-124">Liaison de ressource</span><span class="sxs-lookup"><span data-stu-id="35a99-124">Resource Binding</span></span>](resource-binding.md)
</dt> </dl>

 

 





