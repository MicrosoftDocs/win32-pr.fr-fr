---
title: Mise à jour d’itinéraires à l’aide de RtmAddRouteToDest
description: Si le client n’a pas besoin d’efficacité lors de l’ajout d’un itinéraire, il doit utiliser la méthode de mise à jour des itinéraires suivante.
ms.assetid: bfa914ea-5d54-4ce9-a97c-903c497d135b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c7972b2d5ec0996cafc1dd32a8a4056a6aeb0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940243"
---
# <a name="updating-routes-using-rtmaddroutetodest"></a><span data-ttu-id="6d6f5-103">Mise à jour d’itinéraires à l’aide de RtmAddRouteToDest</span><span class="sxs-lookup"><span data-stu-id="6d6f5-103">Updating Routes Using RtmAddRouteToDest</span></span>

<span data-ttu-id="6d6f5-104">Si le client n’a pas besoin d’efficacité lors de l’ajout d’un itinéraire, il doit utiliser la méthode de mise à jour des itinéraires suivante.</span><span class="sxs-lookup"><span data-stu-id="6d6f5-104">If the client does not require efficiency when adding a route, it should use the following method of updating routes.</span></span> <span data-ttu-id="6d6f5-105">Cette méthode est moins efficace car elle nécessite l’obtention d’un handle vers l’itinéraire et la transmission de la structure d' [**\_ \_ informations d’itinéraire RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) vers et à partir du gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="6d6f5-105">This method is less efficient since it requires obtaining a handle to the route and passing the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure to and from the routing table manager.</span></span> <span data-ttu-id="6d6f5-106">Cette méthode prend également plus de temps.</span><span class="sxs-lookup"><span data-stu-id="6d6f5-106">This method also takes more time.</span></span> <span data-ttu-id="6d6f5-107">Étant donné que [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) ne manipule pas directement la table de routage, cette méthode vous aide à améliorer la simplicité.</span><span class="sxs-lookup"><span data-stu-id="6d6f5-107">Since [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) does not manipulate the routing table directly, using this method trades efficiency for simplicity.</span></span>

<span data-ttu-id="6d6f5-108">Pour obtenir un exemple de code qui montre comment utiliser ces fonctions, consultez [Ajouter et mettre à jour des itinéraires à l’aide de RtmAddRouteToDest](add-and-update-routes-using-rtmaddroutetodest.md).</span><span class="sxs-lookup"><span data-stu-id="6d6f5-108">For sample code that shows how to use these functions, see [Add and Update Routes Using RtmAddRouteToDest](add-and-update-routes-using-rtmaddroutetodest.md).</span></span>

 

 




