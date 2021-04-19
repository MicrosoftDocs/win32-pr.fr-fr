---
title: Itinéraires et le meilleur itinéraire
description: Un itinéraire est un \ 0034 ; chemin réseau \ 0034 ; à une destination associée à un certain coût. Le coût est représenté par sa préférence administrative et sa métrique propre au protocole. Les itinéraires avec des coûts inférieurs sont préférés sur tous les autres itinéraires.
ms.assetid: c5a75308-42da-4ef9-a712-9987c87eef84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd55ec1188383f4cdef55511aae7a9c2cf59303
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510228"
---
# <a name="routes-and-the-best-route"></a><span data-ttu-id="10cb2-105">Itinéraires et le meilleur itinéraire</span><span class="sxs-lookup"><span data-stu-id="10cb2-105">Routes and the Best Route</span></span>

<span data-ttu-id="10cb2-106">Un itinéraire est un « chemin d’accès réseau » vers une destination qui est associée à un certain coût.</span><span class="sxs-lookup"><span data-stu-id="10cb2-106">A route is a "network path" to a destination that has a certain cost associated with it.</span></span> <span data-ttu-id="10cb2-107">Le coût est représenté par sa préférence administrative et sa métrique propre au protocole.</span><span class="sxs-lookup"><span data-stu-id="10cb2-107">The cost is represented by its administrative preference and its protocol-specific metric.</span></span> <span data-ttu-id="10cb2-108">Les itinéraires avec des coûts inférieurs sont préférés sur tous les autres itinéraires.</span><span class="sxs-lookup"><span data-stu-id="10cb2-108">Routes with lower costs are preferred over all other routes.</span></span>

<span data-ttu-id="10cb2-109">Une entrée d’itinéraire dans la table de routage comprend les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="10cb2-109">A route entry in the routing table includes:</span></span>

-   <span data-ttu-id="10cb2-110">Handle vers la destination</span><span class="sxs-lookup"><span data-stu-id="10cb2-110">A handle to the destination</span></span>
-   <span data-ttu-id="10cb2-111">Propriétaire de cet itinéraire</span><span class="sxs-lookup"><span data-stu-id="10cb2-111">The owner of this route</span></span>
-   <span data-ttu-id="10cb2-112">Voisin (homologue) qui a fourni les informations de routage</span><span class="sxs-lookup"><span data-stu-id="10cb2-112">The neighbor (peer) that provided the route information</span></span>
-   <span data-ttu-id="10cb2-113">Indicateurs associés à l’état de l’itinéraire</span><span class="sxs-lookup"><span data-stu-id="10cb2-113">Flags associated with the state of the route</span></span>
-   <span data-ttu-id="10cb2-114">Indicateurs associés à l’itinéraire</span><span class="sxs-lookup"><span data-stu-id="10cb2-114">Flags associated with the route</span></span>
-   <span data-ttu-id="10cb2-115">La préférence et la métrique de l’itinéraire</span><span class="sxs-lookup"><span data-stu-id="10cb2-115">The preference and metric for the route</span></span>
-   <span data-ttu-id="10cb2-116">Liste des vues auxquelles l’itinéraire appartient</span><span class="sxs-lookup"><span data-stu-id="10cb2-116">The list of views to which the route belongs</span></span>
-   <span data-ttu-id="10cb2-117">Informations privées pour le propriétaire de l’itinéraire</span><span class="sxs-lookup"><span data-stu-id="10cb2-117">Information that is private to the owner of the route</span></span>
-   <span data-ttu-id="10cb2-118">Liste des tronçons suivants utilisés pour atteindre la destination</span><span class="sxs-lookup"><span data-stu-id="10cb2-118">A list of next hops used to reach the destination</span></span>

<span data-ttu-id="10cb2-119">Les valeurs suivantes, prises ensemble, identifient de façon unique un itinéraire dans la table de routage :</span><span class="sxs-lookup"><span data-stu-id="10cb2-119">The following values, taken together, uniquely identify a route in the routing table:</span></span>

-   <span data-ttu-id="10cb2-120">Réseau de destination</span><span class="sxs-lookup"><span data-stu-id="10cb2-120">The destination network</span></span>
-   <span data-ttu-id="10cb2-121">Propriétaire de l’itinéraire</span><span class="sxs-lookup"><span data-stu-id="10cb2-121">The owner of the route</span></span>
-   <span data-ttu-id="10cb2-122">Voisin ayant fourni l’itinéraire</span><span class="sxs-lookup"><span data-stu-id="10cb2-122">The neighbor who supplied the route</span></span>

## <a name="metrics-and-preference"></a><span data-ttu-id="10cb2-123">Métriques et préférences</span><span class="sxs-lookup"><span data-stu-id="10cb2-123">Metrics and Preference</span></span>

<span data-ttu-id="10cb2-124">Chaque itinéraire a une préférence administrative (spécifiée par la stratégie de routage) et une mesure dépendante du client.</span><span class="sxs-lookup"><span data-stu-id="10cb2-124">Each route has an administrative preference (specified by the routing policy), and a client-dependent metric.</span></span> <span data-ttu-id="10cb2-125">Le gestionnaire de tables de routage utilise ces informations pour déterminer quel itinéraire est le meilleur itinéraire vers une destination.</span><span class="sxs-lookup"><span data-stu-id="10cb2-125">The routing table manager uses this information to determine which route is the better route to a destination.</span></span> <span data-ttu-id="10cb2-126">Les itinéraires avec une préférence inférieure sont de meilleurs itinéraires (l’un étant le plus bas, et par conséquent le meilleur).</span><span class="sxs-lookup"><span data-stu-id="10cb2-126">Routes with lower preference are better routes (one being lowest, and therefore best).</span></span> <span data-ttu-id="10cb2-127">Si deux itinéraires ont la même préférence, l’itinéraire avec la métrique inférieure est le meilleur itinéraire.</span><span class="sxs-lookup"><span data-stu-id="10cb2-127">If two routes have the same preference, the route with the lower metric is the better route.</span></span>

<span data-ttu-id="10cb2-128">Normalement, la préférence d’un itinéraire est déterminée par la préférence du client qui a ajouté l’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="10cb2-128">Normally, the preference of a route is determined by the preference of the client that added the route.</span></span> <span data-ttu-id="10cb2-129">Toutefois, pour tous les itinéraires ajoutés à l’aide de l’outil de gestion Netsh.exe, vous pouvez spécifier une valeur de préférence pour chaque itinéraire.</span><span class="sxs-lookup"><span data-stu-id="10cb2-129">However, for any routes added using the Netsh.exe management tool, a preference value can be specified on a per-route basis.</span></span>

<span data-ttu-id="10cb2-130">La préférence est normalement utilisée pour indiquer la priorité entre les clients.</span><span class="sxs-lookup"><span data-stu-id="10cb2-130">Preference is normally used to indicate priority between clients.</span></span> <span data-ttu-id="10cb2-131">Par exemple, un administrateur peut attribuer à OSPF une préférence inférieure à celle de RIP.</span><span class="sxs-lookup"><span data-stu-id="10cb2-131">For example, an administrator can assign OSPF a lower (better) preference than RIP.</span></span> <span data-ttu-id="10cb2-132">Dans ce cas, les itinéraires OSPF sont préférables aux itinéraires RIP.</span><span class="sxs-lookup"><span data-stu-id="10cb2-132">In this case, OSPF routes are preferable to RIP routes.</span></span>

 

 




