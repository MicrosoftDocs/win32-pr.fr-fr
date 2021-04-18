---
title: Ajouter et mettre à jour des itinéraires à l’aide de RtmAddRouteToDest
description: La fonction RtmAddRouteToDest est utilisée pour ajouter de nouveaux itinéraires et mettre à jour des itinéraires existants pour une destination. Les procédures suivantes expliquent les deux cas. L’exemple de code suivant montre comment implémenter la première procédure.
ms.assetid: 17a04511-69f8-4e50-993c-0e558ee72184
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd3594aee054e6815094834bedbc1aae158fc4e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512257"
---
# <a name="add-and-update-routes-using-rtmaddroutetodest"></a><span data-ttu-id="b9659-105">Ajouter et mettre à jour des itinéraires à l’aide de RtmAddRouteToDest</span><span class="sxs-lookup"><span data-stu-id="b9659-105">Add and Update Routes Using RtmAddRouteToDest</span></span>

<span data-ttu-id="b9659-106">La fonction [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) est utilisée pour ajouter de nouveaux itinéraires et mettre à jour des itinéraires existants pour une destination.</span><span class="sxs-lookup"><span data-stu-id="b9659-106">The function [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) is used to add new routes and update existing routes for a destination.</span></span> <span data-ttu-id="b9659-107">Les procédures suivantes expliquent les deux cas.</span><span class="sxs-lookup"><span data-stu-id="b9659-107">The following procedures explain both cases.</span></span> <span data-ttu-id="b9659-108">L’exemple de code suivant montre comment implémenter la première procédure.</span><span class="sxs-lookup"><span data-stu-id="b9659-108">The sample code that follows shows how to implement the first procedure.</span></span>

<span data-ttu-id="b9659-109">**Pour ajouter un itinéraire, le client doit effectuer les étapes suivantes**</span><span class="sxs-lookup"><span data-stu-id="b9659-109">**To add a route, the client should take the following steps**</span></span>

1.  <span data-ttu-id="b9659-110">Si le client a déjà mis en cache le descripteur de saut suivant, passez à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="b9659-110">If the client has already cached the next-hop handle, go to step 4.</span></span>
2.  <span data-ttu-id="b9659-111">Créez une structure d' [**\_ \_ informations de tronçon RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) et remplissez-la avec les informations appropriées.</span><span class="sxs-lookup"><span data-stu-id="b9659-111">Create an [**RTM\_NEXTHOP\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) structure and fill it with the appropriate information.</span></span>
3.  <span data-ttu-id="b9659-112">Ajoutez le tronçon suivant à la table de routage en appelant [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop).</span><span class="sxs-lookup"><span data-stu-id="b9659-112">Add the next hop to the routing table by calling [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop).</span></span> <span data-ttu-id="b9659-113">Le gestionnaire de tables de routage retourne un handle vers le tronçon suivant.</span><span class="sxs-lookup"><span data-stu-id="b9659-113">The routing table manager returns a handle to the next hop.</span></span> <span data-ttu-id="b9659-114">Si le tronçon suivant existe déjà, la table de routage n’ajoute pas le tronçon suivant. au lieu de cela, elle retourne le handle vers le tronçon suivant.</span><span class="sxs-lookup"><span data-stu-id="b9659-114">If the next hop already exists, the routing table does not add the next hop; instead it returns the handle to the next hop.</span></span>
4.  <span data-ttu-id="b9659-115">Créez une structure d' [**\_ \_ informations d’itinéraire RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) et remplissez-la avec les informations appropriées, y compris le descripteur de saut suivant renvoyé par le gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="b9659-115">Create an [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure and fill it with the appropriate information, including the next-hop handle returned by the routing table manager.</span></span>
5.  <span data-ttu-id="b9659-116">Ajoutez l’itinéraire à la table de routage en appelant [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest).</span><span class="sxs-lookup"><span data-stu-id="b9659-116">Add the route to the routing table by calling [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest).</span></span> <span data-ttu-id="b9659-117">Le gestionnaire de tables de routage compare le nouvel itinéraire aux itinéraires qui se trouvent déjà dans la table de routage.</span><span class="sxs-lookup"><span data-stu-id="b9659-117">The routing table manager compares the new route to the routes that are already in the routing table.</span></span> <span data-ttu-id="b9659-118">Deux itinéraires sont égaux si toutes les conditions suivantes sont remplies :</span><span class="sxs-lookup"><span data-stu-id="b9659-118">Two routes are equal if all of the following conditions are true:</span></span>

    -   <span data-ttu-id="b9659-119">L’itinéraire est ajouté à la même destination.</span><span class="sxs-lookup"><span data-stu-id="b9659-119">The route is being added to the same destination.</span></span>
    -   <span data-ttu-id="b9659-120">L’itinéraire est ajouté par le même client que celui spécifié par le membre **propriétaire** de la structure d' [**\_ \_ informations d’itinéraire RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) .</span><span class="sxs-lookup"><span data-stu-id="b9659-120">The route is being added by the same client as specified by the **Owner** member of the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure.</span></span>
    -   <span data-ttu-id="b9659-121">L’itinéraire est publié par le même voisin que celui spécifié par le membre **voisin** de la structure d' [**\_ \_ informations d’itinéraire RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) .</span><span class="sxs-lookup"><span data-stu-id="b9659-121">The route is advertised by the same neighbor as specified by the **Neighbor** member of the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure.</span></span>

    <span data-ttu-id="b9659-122">Si l’itinéraire existe, le gestionnaire de tables de routage retourne le descripteur à l’itinéraire existant.</span><span class="sxs-lookup"><span data-stu-id="b9659-122">If the route exists, the routing table manager returns the handle to the existing route.</span></span> <span data-ttu-id="b9659-123">Dans le cas contraire, le gestionnaire de tables de routage ajoute l’itinéraire et retourne le descripteur au nouvel itinéraire.</span><span class="sxs-lookup"><span data-stu-id="b9659-123">Otherwise, the routing table manager adds the route and returns the handle to the new route.</span></span>

    <span data-ttu-id="b9659-124">Le client peut définir le *paramètre \_ indicateurs de modification* sur la version RTM \_ \_ changer \_ nouveau pour indiquer au gestionnaire de tables de routage d’ajouter un nouvel itinéraire sur la destination, même s’il existe un autre itinéraire avec les mêmes champs propriétaire et voisin.</span><span class="sxs-lookup"><span data-stu-id="b9659-124">The client can set the *Change\_Flags* parameter to RTM\_ROUTE\_CHANGE\_NEW to instruct the routing table manager to add a new route on the destination, even if another route with the same owner and neighbor fields exists.</span></span>

    <span data-ttu-id="b9659-125">Le client peut définir le *paramètre \_ indicateurs de modification* sur RTM \_ route \_ change \_ en premier pour indiquer au gestionnaire de tables de routage de mettre à jour le premier itinéraire sur la destination appartenant au client.</span><span class="sxs-lookup"><span data-stu-id="b9659-125">The client can set the *Change\_Flags* parameter to RTM\_ROUTE\_CHANGE\_FIRST to tell the routing table manager to update the first route on the destination owned by the client.</span></span> <span data-ttu-id="b9659-126">Cette mise à jour peut être effectuée si un tel itinéraire existe, même si le champ voisin ne correspond pas.</span><span class="sxs-lookup"><span data-stu-id="b9659-126">This update can be performed if such a route exists, even if the neighbor field does not match.</span></span> <span data-ttu-id="b9659-127">Cet indicateur est utilisé par les clients qui gèrent un seul itinéraire par destination.</span><span class="sxs-lookup"><span data-stu-id="b9659-127">This flag is used by clients that maintain a single route per destination.</span></span>

<span data-ttu-id="b9659-128">**Pour mettre à jour un itinéraire, le client doit effectuer les étapes suivantes**</span><span class="sxs-lookup"><span data-stu-id="b9659-128">**To update a route, the client should take the following steps**</span></span>

1.  <span data-ttu-id="b9659-129">Appelez [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) avec le descripteur de l’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="b9659-129">Call [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) with the handle to the route.</span></span> <span data-ttu-id="b9659-130">Le handle est soit un précédemment mis en cache par le client, soit retourné par le gestionnaire de table de routage à partir d’un appel qui retourne un handle d’itinéraire tel que **RtmGetRouteInfo**.</span><span class="sxs-lookup"><span data-stu-id="b9659-130">The handle is either one previously cached by the client, or returned by the routing table manager from a call that returns a route handle such as **RtmGetRouteInfo**.</span></span>
2.  <span data-ttu-id="b9659-131">Apportez les modifications à la structure d' [**\_ \_ informations d’itinéraire RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) qui est retournée par le gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="b9659-131">Make the changes to the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure that is returned by the routing table manager.</span></span>
3.  <span data-ttu-id="b9659-132">Appelez [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) avec le handle vers l’itinéraire et la structure [**d' \_ \_ informations d’itinéraire RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) modifiée.</span><span class="sxs-lookup"><span data-stu-id="b9659-132">Call [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) with the handle to the route and the changed [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure.</span></span>

<span data-ttu-id="b9659-133">L’exemple de code suivant montre comment ajouter un itinéraire à une destination à l’aide du gestionnaire de table de routage comme intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="b9659-133">The following sample code shows how to add a route to a destination using the routing table manager as an intermediary.</span></span>


```C++
// Add a route to a destination given by (addr, masklen)
// using a next hop reachable with an interface

RTM_NEXTHOP_INFO NextHopInfo;

// First, create and add a next hop to the caller's
// next-hop tree (if it does not already exist)

ZeroMemory(&NextHopInfo, sizeof(RTM_NEXTHOP_INFO);

RTM_IPV4_MAKE_NET_ADDRESS(&NextHopInfo.NextHopAddress,
                          nexthop, // Address of the next hop
                          32);

NextHopInfo.InterfaceIndex = interface;

NextHopHandle = NULL;

Status = RtmAddNextHop(RtmRegHandle,
                       &NextHopInfo,
                       &NextHopHandle,
                       &ChangeFlags);

if (Status == NO_ERROR)
{
    // Created a new next hop or found an old one

        // Fill in the route information for the route
    
    ZeroMemory(&RouteInfo, sizeof(RTM_ROUTE_INFO);

    // Fill in the destination network's address and mask values
    RTM_IPV4_MAKE_NET_ADDRESS(&NetAddress, addr, masklen);

    // Assume 'neighbour learnt from' is the first next hop
    RouteInfo.Neighbour = NextHopHandle;

    // Set metric for route; Preference set internally
    RouteInfo.PrefInfo.Metric = metric;

    // Adding a route to both the unicast and multicast views
    RouteInfo.BelongsToViews = RTM_VIEW_MASK_UCAST|RTM_VIEW_MASK_MCAST;

    RouteInfo.NextHopsList.NumNextHops = 1;
    RouteInfo.NextHopsList.NextHops[0] = NextHopHandle;

    // If you want to add a new route, regardless of
    // whether a similar route already exists, use the following 
    //     ChangeFlags = RTM_ROUTE_CHANGE_NEW;

    ChangeFlags = 0;

    Status = RtmAddRouteToDest(RtmRegHandle,
                               &RouteHandle,     // Can be NULL if you do not need handle
                               &NetAddress,
                               &RouteInfo,
                               1000,             // Time out route after 1000 ms
                               RouteListHandle1, // Also add the route to this list
                               0,
                               NULL,
                               &ChangeFlags);

    if (Status == NO_ERROR)
    {
        if (ChangeFlags & RTM_ROUTE_CHANGE_NEW)
        {
        ; // A new route has been created
        }
        else
        {
        ; // An existing route is updated
        }

        if (ChangeFlags & RTM_ROUTE_CHANGE_BEST)
        {
        ; // Best route information has changed
        }

        // Release the route handle if you do not need it
        RtmReleaseRoutes(RtmRegHandle, 1, &RouteHandle);
    }

    // Also release the next hop since it is no longer needed 
    RtmReleaseNextHops(RtmRegHandle, 1, &NextHopHandle);
}
```



 

 




