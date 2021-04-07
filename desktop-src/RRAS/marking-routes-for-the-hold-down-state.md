---
title: Marquage des itinéraires pour l’État Hold-Down
description: Certains clients, tels que les protocoles de vecteur de distance tels que RIP et DVMRP, requièrent que les destinations soient publiées comme inaccessibles pendant un certain temps après la suppression du dernier itinéraire vers la destination.
ms.assetid: 2a86c092-d8a6-4fd4-8b2e-451c160f743f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af10832452a3a0b9ca851c209d240c97998ef519
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940057"
---
# <a name="marking-routes-for-the-hold-down-state"></a><span data-ttu-id="6495c-103">Marquage des itinéraires pour l’État Hold-Down</span><span class="sxs-lookup"><span data-stu-id="6495c-103">Marking Routes for the Hold-Down State</span></span>

<span data-ttu-id="6495c-104">Certains clients, tels que les protocoles de vecteur de distance tels que RIP et DVMRP, requièrent que les destinations soient publiées comme inaccessibles pendant un certain temps après la suppression du dernier itinéraire vers la destination.</span><span class="sxs-lookup"><span data-stu-id="6495c-104">Some clients, such as distance vector protocols like RIP and DVMRP, require that destinations be advertised as unreachable for a certain time after the last route to the destination is deleted.</span></span> <span data-ttu-id="6495c-105">Le dernier itinéraire qui est supprimé doit être publié comme étant inaccessible, même si des itinéraires plus récents arrivent en attendant.</span><span class="sxs-lookup"><span data-stu-id="6495c-105">The last route that is deleted must be advertised as unreachable even if newer routes arrive in the meantime.</span></span> <span data-ttu-id="6495c-106">Le dernier itinéraire supprimé est marqué comme étant dans un *État de blocage*.</span><span class="sxs-lookup"><span data-stu-id="6495c-106">The last route deleted is marked as being in a *hold-down state*.</span></span> <span data-ttu-id="6495c-107">Le processus de blocage empêche la formation de boucles de routage.</span><span class="sxs-lookup"><span data-stu-id="6495c-107">The hold-down process prevents the formation of routing loops.</span></span> <span data-ttu-id="6495c-108">Les boucles de routage sont générées lorsqu’un protocole de routage publie des informations de routage obsolètes.</span><span class="sxs-lookup"><span data-stu-id="6495c-108">Routing loops are caused when a routing protocol advertises obsolete routing information.</span></span> <span data-ttu-id="6495c-109">Lorsque le délai d’attente expire, ces protocoles reprennent leur publication avec le nouvel itinéraire le plus approprié.</span><span class="sxs-lookup"><span data-stu-id="6495c-109">When the hold-down expires, these protocols resume their advertisement with the new best route.</span></span>

<span data-ttu-id="6495c-110">Un protocole qui implémente des États de blocage indique qu’une destination est dans un état de blocage à l’aide de la fonction [**RtmHoldDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination) .</span><span class="sxs-lookup"><span data-stu-id="6495c-110">A protocol that implements hold-down states indicates that a destination is in a hold-down state by using the [**RtmHoldDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination) function.</span></span> <span data-ttu-id="6495c-111">Le client appelle cette fonction lorsqu’il publie le meilleur itinéraire vers cette destination.</span><span class="sxs-lookup"><span data-stu-id="6495c-111">The client calls this function when it advertises the best route to this destination.</span></span> <span data-ttu-id="6495c-112">Si tous les itinéraires vers cette destination sont supprimés par la suite, le dernier itinéraire supprimé est conservé dans un état de blocage pendant la période spécifiée dans l’appel précédent à **RtmHoldDestination**.</span><span class="sxs-lookup"><span data-stu-id="6495c-112">If all routes to this destination are later deleted, the last route that is deleted is kept in a hold-down state for the period of time specified in the earlier call to **RtmHoldDestination**.</span></span>

<span data-ttu-id="6495c-113">Lorsqu’un protocole publie une destination, les informations d’itinéraire qui sont utilisées varient selon que le protocole utilise des États de blocage et si un itinéraire dans l’état de blocage existe pour la destination.</span><span class="sxs-lookup"><span data-stu-id="6495c-113">When a protocol advertises a destination, the route information that is used depends on whether the protocol uses hold-down states and if a route in the hold-down state exists for the destination.</span></span>

<span data-ttu-id="6495c-114">Les protocoles qui n’utilisent pas d’États de blocage peuvent ignorer les informations de routage relatives aux États de maintien d’une destination et publier toujours le meilleur itinéraire.</span><span class="sxs-lookup"><span data-stu-id="6495c-114">Protocols that do not use hold-down states can ignore route information that relates to hold-down states for a destination, and always advertise the best route.</span></span>

<span data-ttu-id="6495c-115">Pour obtenir un exemple de code qui montre comment utiliser ces fonctions, consultez [utiliser l’état de Hold-Down d’itinéraire](use-the-route-hold-down-state.md).</span><span class="sxs-lookup"><span data-stu-id="6495c-115">For sample code that shows how to use these functions, see [Use the Route Hold-Down State](use-the-route-hold-down-state.md).</span></span>

 

 




