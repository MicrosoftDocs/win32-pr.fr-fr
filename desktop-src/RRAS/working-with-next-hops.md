---
title: Utilisation des tronçons suivants
description: L’API RTMv2 permet aux clients de travailler avec la liste des tronçons suivants associés aux itinéraires et aux destinations.
ms.assetid: ef474091-48fe-48e5-b476-73d77dbcbec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d20a812fd272afafd2cd8eb1d6fb93d97530a2a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380312"
---
# <a name="working-with-next-hops"></a><span data-ttu-id="acdce-103">Utilisation des tronçons suivants</span><span class="sxs-lookup"><span data-stu-id="acdce-103">Working with Next Hops</span></span>

<span data-ttu-id="acdce-104">L’API RTMv2 permet aux clients de travailler avec la liste des tronçons suivants associés aux itinéraires et aux destinations.</span><span class="sxs-lookup"><span data-stu-id="acdce-104">The RTMv2 API allows clients to work with the list of next hops that are associated with routes and destinations.</span></span> <span data-ttu-id="acdce-105">Les clients peuvent ajouter ou mettre à jour un tronçon suivant en appelant [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop).</span><span class="sxs-lookup"><span data-stu-id="acdce-105">Clients can add or update a next hop by calling [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop).</span></span> <span data-ttu-id="acdce-106">Les clients peuvent supprimer un tronçon suivant à l’aide de [**RtmDeleteNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop).</span><span class="sxs-lookup"><span data-stu-id="acdce-106">Clients can delete a next hop using [**RtmDeleteNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop).</span></span> <span data-ttu-id="acdce-107">Les clients peuvent rechercher les tronçons suivants en appelant [**RtmFindNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop).</span><span class="sxs-lookup"><span data-stu-id="acdce-107">Clients can search for next hops by calling [**RtmFindNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop).</span></span>

<span data-ttu-id="acdce-108">Les clients peuvent également mettre à jour le tronçon suivant directement.</span><span class="sxs-lookup"><span data-stu-id="acdce-108">Clients can also update the next hop directly.</span></span> <span data-ttu-id="acdce-109">Pour ce faire, le client doit d’abord verrouiller le tronçon suivant avec la fonction [**RtmLockNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop) .</span><span class="sxs-lookup"><span data-stu-id="acdce-109">To do so, the client must first lock the next hop with the [**RtmLockNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop) function.</span></span> <span data-ttu-id="acdce-110">Le client peut ensuite utiliser le pointeur direct vers la structure d' [**\_ \_ informations du tronçon RTM RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) du gestionnaire de tables de routage pour effectuer les modifications nécessaires.</span><span class="sxs-lookup"><span data-stu-id="acdce-110">Then the client can use the direct pointer to the routing table manager's [**RTM\_NEXTHOP\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) structure to make necessary modifications.</span></span> <span data-ttu-id="acdce-111">Enfin, le client peut déverrouiller le tronçon suivant.</span><span class="sxs-lookup"><span data-stu-id="acdce-111">Finally, the client can unlock the next hop.</span></span>

> [!Note]  
> <span data-ttu-id="acdce-112">L’adresse de saut suivant et les champs d’index d’interface dans le tronçon suivant identifient de façon unique le tronçon suivant et ne doivent pas être modifiés.</span><span class="sxs-lookup"><span data-stu-id="acdce-112">The next-hop address and interface index fields in the next hop uniquely identify the next hop and should not be modified.</span></span>

 

 

 




