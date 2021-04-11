---
title: Récupération des informations
description: RTMv2 permet à un client de récupérer les informations référencées par un handle donné à l’aide des fonctions RtmGetEntityInfo, RtmGetDestInfo, RtmGetRouteInfo et RtmGetNextHopInfo.
ms.assetid: a3fc2020-eac4-40a1-9a6e-6eaa2bcc582c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058a87c9463011aec55b0c6c8c0574ff1e013f23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190851"
---
# <a name="retrieving-information"></a><span data-ttu-id="85f84-103">Récupération des informations</span><span class="sxs-lookup"><span data-stu-id="85f84-103">Retrieving Information</span></span>

<span data-ttu-id="85f84-104">RTMv2 permet à un client de récupérer les informations référencées par un handle donné à l’aide des fonctions [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo)et [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) .</span><span class="sxs-lookup"><span data-stu-id="85f84-104">RTMv2 allows a client to retrieve the information referred to by a given handle using the [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo), and [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) functions.</span></span>

<span data-ttu-id="85f84-105">Ces appels de fonction ont des fonctions correspondantes ([**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo), [**RtmReleaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)) pour libérer les handles associés à la structure d’informations retournée par le gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="85f84-105">These function calls have corresponding functions ([**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo), [**RtmReleaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)) to release the handles associated with the information structure returned by the routing table manager.</span></span>

> [!Note]  
> <span data-ttu-id="85f84-106">Les informations pour les clients sont disponibles uniquement dans la famille d’adresses et d’instances actuelles.</span><span class="sxs-lookup"><span data-stu-id="85f84-106">Information for clients is available only in the current instance and address family.</span></span>

 

<span data-ttu-id="85f84-107">Pour obtenir un exemple de code qui montre comment utiliser ces fonctions, consultez [Rechercher le meilleur itinéraire](search-for-the-best-route.md).</span><span class="sxs-lookup"><span data-stu-id="85f84-107">For sample code that shows how to use these functions, see [Search For the Best Route](search-for-the-best-route.md).</span></span>

## <a name="using-rtmgetexactmatchroute-and-rtmgetexactmatchdestination"></a><span data-ttu-id="85f84-108">Utilisation de RtmGetExactMatchRoute et RtmGetExactMatchDestination</span><span class="sxs-lookup"><span data-stu-id="85f84-108">Using RtmGetExactMatchRoute and RtmGetExactMatchDestination</span></span>

<span data-ttu-id="85f84-109">Les fonctions [**RtmGetExactMatchRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute) et [**RtmGetExactMatchDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination) sont utilisées par les clients pour rechercher un itinéraire ou une destination spécifique.</span><span class="sxs-lookup"><span data-stu-id="85f84-109">The [**RtmGetExactMatchRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute) and [**RtmGetExactMatchDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination) functions are used by clients to find a specific route or destination.</span></span> <span data-ttu-id="85f84-110">Ces fonctions permettent de gagner du temps en procédant au travail de comparaison pour le client.</span><span class="sxs-lookup"><span data-stu-id="85f84-110">These functions save time by doing the comparison work for the client.</span></span>

<span data-ttu-id="85f84-111">Par exemple, lorsque RIP met à jour un itinéraire, RIP doit conserver les anciennes informations de métriques.</span><span class="sxs-lookup"><span data-stu-id="85f84-111">For example, when RIP updates a route, RIP must retain the old metric information.</span></span> <span data-ttu-id="85f84-112">RIP recherche l’itinéraire et ses informations.</span><span class="sxs-lookup"><span data-stu-id="85f84-112">RIP searches for the route and its information.</span></span> <span data-ttu-id="85f84-113">Ensuite, RIP peut copier les informations et mettre à jour l’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="85f84-113">Then RIP can copy the information and update the route.</span></span>

## <a name="using-rtmgetmostspecificdestination"></a><span data-ttu-id="85f84-114">Utilisation de RtmGetMostSpecificDestination</span><span class="sxs-lookup"><span data-stu-id="85f84-114">Using RtmGetMostSpecificDestination</span></span>

<span data-ttu-id="85f84-115">La fonction [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination) est utilisée pour localiser la destination qui correspond le mieux au préfixe réseau spécifié.</span><span class="sxs-lookup"><span data-stu-id="85f84-115">The [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination) function is used to locate the destination that best matches the specified network prefix.</span></span>

<span data-ttu-id="85f84-116">Par exemple, le gestionnaire de groupe de multidiffusion utilise cette fonction pour effectuer une vérification de transfert de chemin inverse (RPF) sur une seule adresse.</span><span class="sxs-lookup"><span data-stu-id="85f84-116">For example, the multicast group manager uses this function to perform a reverse-path-forwarding (RPF) check on a single address.</span></span> <span data-ttu-id="85f84-117">La fonction peut également être utilisée pour rechercher le tronçon suivant local pour un tronçon suivant distant donné.</span><span class="sxs-lookup"><span data-stu-id="85f84-117">The function can also be used to find the local next hop for a given remote next hop.</span></span>

<span data-ttu-id="85f84-118">Pour obtenir un exemple de code qui montre comment utiliser ces fonctions, consultez [Rechercher des itinéraires à l’aide d’une arborescence de préfixe](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md) et [recherchez le meilleur itinéraire](search-for-the-best-route.md).</span><span class="sxs-lookup"><span data-stu-id="85f84-118">For sample code that shows how to use these functions, see [Search for Routes Using a Prefix Tree](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md) and [Search For the Best Route](search-for-the-best-route.md).</span></span>

## <a name="using-rtmgetlessspecificdestination"></a><span data-ttu-id="85f84-119">Utilisation de RtmGetLessSpecificDestination</span><span class="sxs-lookup"><span data-stu-id="85f84-119">Using RtmGetLessSpecificDestination</span></span>

<span data-ttu-id="85f84-120">La fonction [**RtmGetLessSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination) est utilisée pour localiser la destination qui correspond à la meilleure correspondance pour le préfixe réseau spécifié.</span><span class="sxs-lookup"><span data-stu-id="85f84-120">The [**RtmGetLessSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination) function is used to locate the destination that is the next-best match for the specified network prefix.</span></span> <span data-ttu-id="85f84-121">Cette fonction peut être appelée à plusieurs reprises pour retourner la correspondance suivante moins spécifique, jusqu’à ce qu’il n’y ait plus de destinations.</span><span class="sxs-lookup"><span data-stu-id="85f84-121">This function can be called repeatedly to return the next successive less-specific match, until no more destinations match.</span></span>

<span data-ttu-id="85f84-122">Cette fonction est appelée après un appel à [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination).</span><span class="sxs-lookup"><span data-stu-id="85f84-122">This function is called after a call to [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination).</span></span>

<span data-ttu-id="85f84-123">Pour obtenir un exemple de code illustrant l’utilisation de ces fonctions, consultez [Rechercher des itinéraires à l’aide d’une arborescence de préfixe](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md).</span><span class="sxs-lookup"><span data-stu-id="85f84-123">For sample code that illustrates how to use these functions, see [Search for Routes Using a Prefix Tree](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md).</span></span>

## <a name="using-rtmisbestroute"></a><span data-ttu-id="85f84-124">Utilisation de RtmIsBestRoute</span><span class="sxs-lookup"><span data-stu-id="85f84-124">Using RtmIsBestRoute</span></span>

<span data-ttu-id="85f84-125">La fonction [**RtmIsBestRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute) permet à un client de déterminer rapidement si un itinéraire particulier est le meilleur itinéraire vers une destination.</span><span class="sxs-lookup"><span data-stu-id="85f84-125">The [**RtmIsBestRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute) function enables a client to quickly find out whether or not a particular route is the best route to a destination.</span></span> <span data-ttu-id="85f84-126">Par exemple, un client peut avoir besoin de stocker un itinéraire particulier uniquement s’il s’agit du meilleur itinéraire.</span><span class="sxs-lookup"><span data-stu-id="85f84-126">For example, a client may need to store a particular route only if it is the best route.</span></span> <span data-ttu-id="85f84-127">Par conséquent, le client peut appeler cette fonction, au lieu d’énumérer tous les itinéraires et d’effectuer la comparaison elle-même.</span><span class="sxs-lookup"><span data-stu-id="85f84-127">Therefore, the client can call this function, instead of enumerating all routes and making the comparison itself.</span></span>

 

 




