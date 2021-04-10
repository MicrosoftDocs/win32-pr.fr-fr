---
title: Indicateurs de tronçon suivant
description: Indicateurs de tronçon suivant
ms.assetid: e4c7e9ea-21f5-491a-b005-1ef1a457cb80
keywords:
- Suivant
- Indicateurs de tronçon suivant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd672c9b083e47c3d0a7419d03ab890c1037ce5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029696"
---
# <a name="next-hop-flags"></a><span data-ttu-id="66fd7-105">Indicateurs de tronçon suivant</span><span class="sxs-lookup"><span data-stu-id="66fd7-105">Next Hop Flags</span></span>

## <a name="next-hop-state-flags"></a><span data-ttu-id="66fd7-106">Indicateurs d’état de tronçon suivant</span><span class="sxs-lookup"><span data-stu-id="66fd7-106">Next Hop State Flags</span></span>



| <span data-ttu-id="66fd7-107">Constante</span><span class="sxs-lookup"><span data-stu-id="66fd7-107">Constant</span></span>                     | <span data-ttu-id="66fd7-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="66fd7-108">Value</span></span> | <span data-ttu-id="66fd7-109">Description</span><span class="sxs-lookup"><span data-stu-id="66fd7-109">Description</span></span>                              |
|------------------------------|-------|------------------------------------------|
| <span data-ttu-id="66fd7-110">État du tronçon de la version RTM \_ \_ \_ créé</span><span class="sxs-lookup"><span data-stu-id="66fd7-110">RTM\_NEXTHOP\_STATE\_CREATED</span></span> | <span data-ttu-id="66fd7-111">0</span><span class="sxs-lookup"><span data-stu-id="66fd7-111">0</span></span>     | <span data-ttu-id="66fd7-112">Indique que le tronçon suivant a été créé.</span><span class="sxs-lookup"><span data-stu-id="66fd7-112">Indicates that the next hop was created.</span></span> |
| <span data-ttu-id="66fd7-113">État du tronçon de la version RTM \_ \_ \_ supprimé</span><span class="sxs-lookup"><span data-stu-id="66fd7-113">RTM\_NEXTHOP\_STATE\_DELETED</span></span> | <span data-ttu-id="66fd7-114">1</span><span class="sxs-lookup"><span data-stu-id="66fd7-114">1</span></span>     | <span data-ttu-id="66fd7-115">Indique que le tronçon suivant a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="66fd7-115">Indicates that the next hop was deleted.</span></span> |



 

## <a name="next-hop-flags"></a><span data-ttu-id="66fd7-116">Indicateurs de tronçon suivant</span><span class="sxs-lookup"><span data-stu-id="66fd7-116">Next Hop Flags</span></span>



| <span data-ttu-id="66fd7-117">Constante</span><span class="sxs-lookup"><span data-stu-id="66fd7-117">Constant</span></span>                    | <span data-ttu-id="66fd7-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="66fd7-118">Value</span></span>  | <span data-ttu-id="66fd7-119">Description</span><span class="sxs-lookup"><span data-stu-id="66fd7-119">Description</span></span>                                                                                                                                           |
|-----------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66fd7-120">\_indicateurs tronçons RTM \_ \_ distants</span><span class="sxs-lookup"><span data-stu-id="66fd7-120">RTM\_NEXTHOP\_FLAGS\_REMOTE</span></span> | <span data-ttu-id="66fd7-121">0x0001</span><span class="sxs-lookup"><span data-stu-id="66fd7-121">0x0001</span></span> | <span data-ttu-id="66fd7-122">Ce tronçon suivant pointe vers une destination distante qui n’est pas directement accessible.</span><span class="sxs-lookup"><span data-stu-id="66fd7-122">This next hop points to a remote destination that is not directly reachable.</span></span> <span data-ttu-id="66fd7-123">Pour obtenir le chemin d’accès complet, le client doit effectuer une recherche récursive.</span><span class="sxs-lookup"><span data-stu-id="66fd7-123">To obtain the complete path, the client must perform a recursive lookup.</span></span> |
| <span data-ttu-id="66fd7-124">\_indicateurs de tronçons de \_ \_ la version RTM</span><span class="sxs-lookup"><span data-stu-id="66fd7-124">RTM\_NEXTHOP\_FLAGS\_DOWN</span></span>   | <span data-ttu-id="66fd7-125">0x0002</span><span class="sxs-lookup"><span data-stu-id="66fd7-125">0x0002</span></span> | <span data-ttu-id="66fd7-126">Cet indicateur est réservé à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="66fd7-126">This flag is reserved for future use.</span></span>                                                                                                                 |



 

## <a name="next-hop-added"></a><span data-ttu-id="66fd7-127">Tronçon suivant ajouté</span><span class="sxs-lookup"><span data-stu-id="66fd7-127">Next Hop Added</span></span>



| <span data-ttu-id="66fd7-128">Constante</span><span class="sxs-lookup"><span data-stu-id="66fd7-128">Constant</span></span>                  | <span data-ttu-id="66fd7-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="66fd7-129">Value</span></span> | <span data-ttu-id="66fd7-130">Description</span><span class="sxs-lookup"><span data-stu-id="66fd7-130">Description</span></span>                 |
|---------------------------|-------|-----------------------------|
| <span data-ttu-id="66fd7-131">\_ \_ nouvelle modification du tronçon RTM \_</span><span class="sxs-lookup"><span data-stu-id="66fd7-131">RTM\_NEXTHOP\_CHANGE\_NEW</span></span> | <span data-ttu-id="66fd7-132">0x01</span><span class="sxs-lookup"><span data-stu-id="66fd7-132">0x01</span></span>  | <span data-ttu-id="66fd7-133">Un nouveau tronçon suivant a été créé.</span><span class="sxs-lookup"><span data-stu-id="66fd7-133">A new next hop was created.</span></span> |



 

 

 




