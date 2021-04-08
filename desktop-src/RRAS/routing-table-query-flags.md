---
title: Indicateurs de requête de table de routage
description: Utilisez ces constantes pour les requêtes de table de routeur.
ms.assetid: 345a8edc-c2aa-483e-8685-15a692bbfd56
keywords:
- Indicateurs de requête de table de routage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37ab647efb192e29aae421e02bef1dec065e3b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840910"
---
# <a name="routing-table-query-flags"></a><span data-ttu-id="a6bfd-104">Indicateurs de requête de table de routage</span><span class="sxs-lookup"><span data-stu-id="a6bfd-104">Routing Table Query Flags</span></span>

<span data-ttu-id="a6bfd-105">Utilisez ces constantes pour les requêtes de table de routeur.</span><span class="sxs-lookup"><span data-stu-id="a6bfd-105">Use these constants for router table queries.</span></span>



| <span data-ttu-id="a6bfd-106">Constante</span><span class="sxs-lookup"><span data-stu-id="a6bfd-106">Constant</span></span>              | <span data-ttu-id="a6bfd-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6bfd-107">Value</span></span>      | <span data-ttu-id="a6bfd-108">Description</span><span class="sxs-lookup"><span data-stu-id="a6bfd-108">Description</span></span>                                                                |
|-----------------------|------------|----------------------------------------------------------------------------|
| <span data-ttu-id="a6bfd-109">\_correspondance RTM \_ aucune</span><span class="sxs-lookup"><span data-stu-id="a6bfd-109">RTM\_MATCH\_NONE</span></span>      | <span data-ttu-id="a6bfd-110">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6bfd-110">0x00000000</span></span> | <span data-ttu-id="a6bfd-111">Correspond à aucun des critères ; tous les itinéraires pour la destination sont retournés.</span><span class="sxs-lookup"><span data-stu-id="a6bfd-111">Matches none of the criteria; all routes for the destination are returned.</span></span> |
| <span data-ttu-id="a6bfd-112">\_propriétaire de correspondance RTM \_</span><span class="sxs-lookup"><span data-stu-id="a6bfd-112">RTM\_MATCH\_OWNER</span></span>     | <span data-ttu-id="a6bfd-113">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a6bfd-113">0x00000001</span></span> | <span data-ttu-id="a6bfd-114">Correspond aux itinéraires ayant le même propriétaire.</span><span class="sxs-lookup"><span data-stu-id="a6bfd-114">Matches routes with same owner.</span></span>                                            |
| <span data-ttu-id="a6bfd-115">RTM \_ match \_ voisin</span><span class="sxs-lookup"><span data-stu-id="a6bfd-115">RTM\_MATCH\_NEIGHBOUR</span></span> | <span data-ttu-id="a6bfd-116">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a6bfd-116">0x00000002</span></span> | <span data-ttu-id="a6bfd-117">Met en correspondance les itinéraires avec le même voisin.</span><span class="sxs-lookup"><span data-stu-id="a6bfd-117">Matches routes with the same neighbor.</span></span>                                     |
| <span data-ttu-id="a6bfd-118">\_correspondance RTM \_ Préférences</span><span class="sxs-lookup"><span data-stu-id="a6bfd-118">RTM\_MATCH\_PREF</span></span>      | <span data-ttu-id="a6bfd-119">0x00000004</span><span class="sxs-lookup"><span data-stu-id="a6bfd-119">0x00000004</span></span> | <span data-ttu-id="a6bfd-120">Correspond aux itinéraires qui ont la même préférence.</span><span class="sxs-lookup"><span data-stu-id="a6bfd-120">Matches routes that have the same preference.</span></span>                              |
| <span data-ttu-id="a6bfd-121">version RTM \_ match \_ NEXTHOP</span><span class="sxs-lookup"><span data-stu-id="a6bfd-121">RTM\_MATCH\_NEXTHOP</span></span>   | <span data-ttu-id="a6bfd-122">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a6bfd-122">0x00000008</span></span> | <span data-ttu-id="a6bfd-123">Correspond aux itinéraires qui ont le même tronçon suivant.</span><span class="sxs-lookup"><span data-stu-id="a6bfd-123">Matches routes that have the same next hop.</span></span>                                |
| <span data-ttu-id="a6bfd-124">\_interface de correspondance RTM \_</span><span class="sxs-lookup"><span data-stu-id="a6bfd-124">RTM\_MATCH\_INTERFACE</span></span> | <span data-ttu-id="a6bfd-125">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6bfd-125">0x00000010</span></span> | <span data-ttu-id="a6bfd-126">Correspond aux itinéraires qui se trouvent sur la même interface.</span><span class="sxs-lookup"><span data-stu-id="a6bfd-126">Matches routes that are on the same interface.</span></span>                             |
| <span data-ttu-id="a6bfd-127">mise en \_ correspondance RTM \_ complète</span><span class="sxs-lookup"><span data-stu-id="a6bfd-127">RTM\_MATCH\_FULL</span></span>      | <span data-ttu-id="a6bfd-128">0x0000FFFF</span><span class="sxs-lookup"><span data-stu-id="a6bfd-128">0x0000FFFF</span></span> | <span data-ttu-id="a6bfd-129">Met en correspondance les itinéraires avec tous les critères.</span><span class="sxs-lookup"><span data-stu-id="a6bfd-129">Matches routes with all criteria.</span></span>                                          |
| <span data-ttu-id="a6bfd-130">\_meilleur \_ protocole RTM</span><span class="sxs-lookup"><span data-stu-id="a6bfd-130">RTM\_BEST\_PROTOCOL</span></span>   | <span data-ttu-id="a6bfd-131">0</span><span class="sxs-lookup"><span data-stu-id="a6bfd-131">0</span></span>          | <span data-ttu-id="a6bfd-132">Retourne un itinéraire quel que soit le protocole qui le possède.</span><span class="sxs-lookup"><span data-stu-id="a6bfd-132">Returns a route regardless of which protocol owns it.</span></span>                      |
| <span data-ttu-id="a6bfd-133">RTM \_ ce \_ protocole</span><span class="sxs-lookup"><span data-stu-id="a6bfd-133">RTM\_THIS\_PROTOCOL</span></span>   | <span data-ttu-id="a6bfd-134">~0</span><span class="sxs-lookup"><span data-stu-id="a6bfd-134">~0</span></span>         | <span data-ttu-id="a6bfd-135">Retourne le meilleur itinéraire pour le protocole appelant.</span><span class="sxs-lookup"><span data-stu-id="a6bfd-135">Returns the best route for the calling protocol.</span></span>                           |



 

 

 




