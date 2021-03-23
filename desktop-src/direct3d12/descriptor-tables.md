---
title: Tables de descripteurs
description: Une table de descripteur est logiquement un tableau de descripteurs.
ms.assetid: 5faf294f-acd5-4b39-92f4-1d6b2abe3040
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10414f8458006029f3279203e949b43410911fd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104621"
---
# <a name="descriptor-tables"></a><span data-ttu-id="3613c-103">Tables de descripteurs</span><span class="sxs-lookup"><span data-stu-id="3613c-103">Descriptor Tables</span></span>

<span data-ttu-id="3613c-104">Une table de descripteur est logiquement un tableau de descripteurs.</span><span class="sxs-lookup"><span data-stu-id="3613c-104">A descriptor table is logically an array of descriptors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3613c-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="3613c-105">In this section</span></span>



| <span data-ttu-id="3613c-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="3613c-106">Topic</span></span>                                                                                 | <span data-ttu-id="3613c-107">Description</span><span class="sxs-lookup"><span data-stu-id="3613c-107">Description</span></span>                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3613c-108">Vue d’ensemble des tables de descripteurs</span><span class="sxs-lookup"><span data-stu-id="3613c-108">Descriptor Tables Overview</span></span>](descriptor-tables-overview.md)<br/>               | <span data-ttu-id="3613c-109">Chaque table de descripteur stocke des descripteurs d’un ou plusieurs types-SRVs, UAVe, CBVs et échantillonneurs.</span><span class="sxs-lookup"><span data-stu-id="3613c-109">Each descriptor table stores descriptors of one or more types - SRVs, UAVe, CBVs, and Samplers.</span></span> <span data-ttu-id="3613c-110">Une table de descripteurs n’est pas une allocation de mémoire ; Il s’agit simplement d’un décalage et d’une longueur dans un tas de descripteur.</span><span class="sxs-lookup"><span data-stu-id="3613c-110">A descriptor table is not an allocation of memory; it is simply an offset and length into a descriptor heap.</span></span><br/> |
| [<span data-ttu-id="3613c-111">Utilisation de tables de descripteurs</span><span class="sxs-lookup"><span data-stu-id="3613c-111">Using Descriptor Tables</span></span>](using-descriptor-tables.md)<br/>                     | <span data-ttu-id="3613c-112">Les tables de descripteurs, chacune identifiant une plage dans un tas de descripteur, sont liées aux emplacements définis par la signature racine actuelle dans une liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="3613c-112">Descriptor tables, each identifying a range in a descriptor heap, are bound at slots defined by the current root signature on a command list.</span></span> <br/>                                                               |
| [<span data-ttu-id="3613c-113">Utilisation avancée des tables de descripteurs</span><span class="sxs-lookup"><span data-stu-id="3613c-113">Advanced Use of Descriptor Tables</span></span>](advanced-use-of-descriptor-tables.md)<br/> | <span data-ttu-id="3613c-114">Les sections suivantes fournissent des informations sur l’utilisation avancée des tables de descripteurs.</span><span class="sxs-lookup"><span data-stu-id="3613c-114">The following sections provide information about the advanced use of descriptor tables.</span></span><br/>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="3613c-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3613c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3613c-116">Tas de descripteurs</span><span class="sxs-lookup"><span data-stu-id="3613c-116">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> <dt>

[<span data-ttu-id="3613c-117">Liaison de ressource</span><span class="sxs-lookup"><span data-stu-id="3613c-117">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="3613c-118">Signatures racines</span><span class="sxs-lookup"><span data-stu-id="3613c-118">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 





