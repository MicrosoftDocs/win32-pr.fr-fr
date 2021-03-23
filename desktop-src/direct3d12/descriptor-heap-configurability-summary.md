---
title: Résumé de la configuration du tas de descripteurs
description: Le tableau suivant récapitule les informations sur la prise en charge des tas et des tas visibles non-nuanceur.
ms.assetid: DF266915-6224-4FFB-BE3E-34A44F7318DD
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ce6718e95b774f83d25a84476616643c77c119
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104625"
---
# <a name="descriptor-heap-configurability-summary"></a><span data-ttu-id="bc2d8-103">Résumé de la configuration du tas de descripteurs</span><span class="sxs-lookup"><span data-stu-id="bc2d8-103">Descriptor Heap Configurability Summary</span></span>

<span data-ttu-id="bc2d8-104">Le tableau suivant récapitule les informations sur la prise en charge des tas et des tas visibles non-nuanceur.</span><span class="sxs-lookup"><span data-stu-id="bc2d8-104">The following table summarizes information about Shader and non-Shader visible heap support.</span></span>



|                               | <span data-ttu-id="bc2d8-105">Tas du descripteur visible du nuanceur</span><span class="sxs-lookup"><span data-stu-id="bc2d8-105">Shader Visible Descriptor Heap</span></span>                                                 | <span data-ttu-id="bc2d8-106">Tas du descripteur visible non-nuanceur</span><span class="sxs-lookup"><span data-stu-id="bc2d8-106">Non Shader Visible Descriptor Heap</span></span>                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc2d8-107">Types de tas pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc2d8-107">Heap Types Supported</span></span>          | <span data-ttu-id="bc2d8-108">CBV \_ SRV \_ UAV, échantillonneur</span><span class="sxs-lookup"><span data-stu-id="bc2d8-108">CBV\_SRV\_UAV, Sampler</span></span>                                                         | <span data-ttu-id="bc2d8-109">Tous</span><span class="sxs-lookup"><span data-stu-id="bc2d8-109">All</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="bc2d8-110">Propriétés de la page UC prises en charge</span><span class="sxs-lookup"><span data-stu-id="bc2d8-110">CPU Page Properties Supported</span></span> | <span data-ttu-id="bc2d8-111">NON \_ disponible, combinaison d’écriture \_</span><span class="sxs-lookup"><span data-stu-id="bc2d8-111">NOT\_AVAILABLE, WRITE\_COMBINE</span></span>                                                 | <span data-ttu-id="bc2d8-112">ÉCRITURE \_ différée</span><span class="sxs-lookup"><span data-stu-id="bc2d8-112">WRITE\_BACK</span></span>                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="bc2d8-113">Gestion de la résidence par application</span><span class="sxs-lookup"><span data-stu-id="bc2d8-113">Residency Management By App</span></span>   | <span data-ttu-id="bc2d8-114">Oui, l’application est responsable</span><span class="sxs-lookup"><span data-stu-id="bc2d8-114">Yes, app responsible</span></span>                                                           | <span data-ttu-id="bc2d8-115">Non applicable (pas de GPU visible).</span><span class="sxs-lookup"><span data-stu-id="bc2d8-115">Not applicable (not GPU visible).</span></span>                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="bc2d8-116">Prise en charge des modifications de descripteur</span><span class="sxs-lookup"><span data-stu-id="bc2d8-116">Descriptor Edit Support</span></span>       | <span data-ttu-id="bc2d8-117">Destination de copie uniquement, via la mise à jour de la liste de commandes et/ou la copie de l’UC si l’UC est visible.</span><span class="sxs-lookup"><span data-stu-id="bc2d8-117">Copy destination only, via command list update and/or CPU copy if CPU visible.</span></span> | <span data-ttu-id="bc2d8-118">Lecture et écriture de l’UC uniquement.</span><span class="sxs-lookup"><span data-stu-id="bc2d8-118">CPU read and write only.</span></span> <span data-ttu-id="bc2d8-119">Aucun accès direct au GPU.</span><span class="sxs-lookup"><span data-stu-id="bc2d8-119">No direct GPU access.</span></span> <span data-ttu-id="bc2d8-120">Peut être utilisé pour la copie de l’UC immédiate (en tant que source et destination).</span><span class="sxs-lookup"><span data-stu-id="bc2d8-120">Can be used for immediate CPU copying (as a source and destination).</span></span> <span data-ttu-id="bc2d8-121">Peut être utilisé en tant que source de mise à jour dans une liste de commandes : copie les descripteurs dans le stockage de la liste de commandes lors de l’enregistrement de la liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="bc2d8-121">Can be used as an update source on a command list – this will copy the descriptors into command list storage during command list record.</span></span> <span data-ttu-id="bc2d8-122">Lors de l’exécution, la copie stockée est copiée vers la destination, qui doit être un tas visible par le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="bc2d8-122">On execution, the stored copy will get copied to the destination, which must be a shader visible heap.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="bc2d8-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc2d8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc2d8-124">Tas de descripteurs</span><span class="sxs-lookup"><span data-stu-id="bc2d8-124">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




