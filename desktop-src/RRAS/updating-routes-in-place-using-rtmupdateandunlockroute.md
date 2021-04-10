---
title: Mise à jour des itinéraires sur place à l’aide de RtmUpdateAndUnlockRoute
description: La mise à jour sur place est généralement plus efficace que la mise à jour de la table de routage avec une méthode indirecte telle que celle utilisée par la fonction RtmAddRouteToDest.
ms.assetid: d4b0b14e-957a-43d5-bacc-8eee4512e2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d76d2af5d60172b890eefa1041a08d47a5221b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029369"
---
# <a name="updating-routes-in-place-using-rtmupdateandunlockroute"></a><span data-ttu-id="7d1b4-103">Mise à jour des itinéraires sur place à l’aide de RtmUpdateAndUnlockRoute</span><span class="sxs-lookup"><span data-stu-id="7d1b4-103">Updating Routes In Place Using RtmUpdateAndUnlockRoute</span></span>

<span data-ttu-id="7d1b4-104">La mise à jour sur place est généralement plus efficace que la mise à jour de la table de routage avec une méthode indirecte telle que celle utilisée par la fonction [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) .</span><span class="sxs-lookup"><span data-stu-id="7d1b4-104">Updating in place is generally more efficient than updating the routing table with an indirect method such as that used by the [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) function.</span></span> <span data-ttu-id="7d1b4-105">Cette méthode est plus efficace, car le client n’est pas obligé d’obtenir un descripteur, ni de passer la structure d' [**\_ \_ informations d’itinéraire RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) à et à partir du gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="7d1b4-105">This method is more efficient because the client is not required to obtain a handle, nor to pass the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure to and from the routing table manager.</span></span> <span data-ttu-id="7d1b4-106">Cette méthode prend également moins de temps.</span><span class="sxs-lookup"><span data-stu-id="7d1b4-106">This method also takes less time.</span></span> <span data-ttu-id="7d1b4-107">Toutefois, la mise à jour directe de la table de routage peut être risquée, étant donné que le gestionnaire de tables de routage ne fonctionne pas comme intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="7d1b4-107">However, directly updating the routing table can be risky, since the routing table manager is not functioning as an intermediary.</span></span>

<span data-ttu-id="7d1b4-108">Pour obtenir un exemple de code qui montre comment utiliser ces fonctions, consultez [mettre à jour un itinéraire sur place à l’aide de RtmUpdateAndUnlockRoute](update-a-route-in-place-using-rtmupdateandunlockroute.md).</span><span class="sxs-lookup"><span data-stu-id="7d1b4-108">For sample code that shows how to use these functions, see [Update a Route In Place Using RtmUpdateAndUnlockRoute](update-a-route-in-place-using-rtmupdateandunlockroute.md).</span></span>

 

 




