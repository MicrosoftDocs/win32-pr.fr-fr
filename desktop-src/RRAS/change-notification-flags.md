---
title: Indicateurs de notification de modification
description: Indicateurs de notification de modification
ms.assetid: 1f1aef71-a2b7-49ad-a0bc-f61f10b701c9
keywords:
- Modifier
- Indicateurs de notification de modification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e6d3015be29c84b6b93b47b373d05f96f4388b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310186"
---
# <a name="change-notification-flags"></a><span data-ttu-id="627b1-105">Indicateurs de notification de modification</span><span class="sxs-lookup"><span data-stu-id="627b1-105">Change Notification Flags</span></span>



| <span data-ttu-id="627b1-106">Constante</span><span class="sxs-lookup"><span data-stu-id="627b1-106">Constant</span></span>                         | <span data-ttu-id="627b1-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="627b1-107">Value</span></span>      | <span data-ttu-id="627b1-108">Description</span><span class="sxs-lookup"><span data-stu-id="627b1-108">Description</span></span>                                                                                                                                                           |
|----------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="627b1-109">\_types de \_ changement de nombre RTM \_</span><span class="sxs-lookup"><span data-stu-id="627b1-109">RTM\_NUM\_CHANGE\_TYPES</span></span>          | <span data-ttu-id="627b1-110">3</span><span class="sxs-lookup"><span data-stu-id="627b1-110">3</span></span>          | <span data-ttu-id="627b1-111">Spécifie le nombre de types de modification actuellement utilisés par le gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="627b1-111">Specifies the number of change types that are currently used by the routing table manager.</span></span>                                                                            |
| <span data-ttu-id="627b1-112">\_type de modification RTM \_ \_ tout</span><span class="sxs-lookup"><span data-stu-id="627b1-112">RTM\_CHANGE\_TYPE\_ALL</span></span>           | <span data-ttu-id="627b1-113">0x0001</span><span class="sxs-lookup"><span data-stu-id="627b1-113">0x0001</span></span>     | <span data-ttu-id="627b1-114">Notifie le client de toute modification apportée à une destination.</span><span class="sxs-lookup"><span data-stu-id="627b1-114">Notifies the client of any change to a destination.</span></span>                                                                                                                   |
| <span data-ttu-id="627b1-115">\_type de modification RTM \_ \_ optimal</span><span class="sxs-lookup"><span data-stu-id="627b1-115">RTM\_CHANGE\_TYPE\_BEST</span></span>          | <span data-ttu-id="627b1-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="627b1-116">0x0002</span></span>     | <span data-ttu-id="627b1-117">Notifie le client des modifications apportées au meilleur itinéraire ou lorsque le meilleur itinéraire change.</span><span class="sxs-lookup"><span data-stu-id="627b1-117">Notifies the client of changes to the best route, or when the best route changes.</span></span>                                                                                     |
| <span data-ttu-id="627b1-118">\_transfert de \_ type de modification RTM \_</span><span class="sxs-lookup"><span data-stu-id="627b1-118">RTM\_CHANGE\_TYPE\_FORWARDING</span></span>    | <span data-ttu-id="627b1-119">0x0004</span><span class="sxs-lookup"><span data-stu-id="627b1-119">0x0004</span></span>     | <span data-ttu-id="627b1-120">Notifie le client des modifications de routage les plus adaptées qui affectent le transfert (par exemple, les changements de tronçons suivants).</span><span class="sxs-lookup"><span data-stu-id="627b1-120">Notifies the client of any best route changes that affect forwarding (such as next hop changes).</span></span>                                                                      |
| <span data-ttu-id="627b1-121">les \_ notifications RTM signalent \_ uniquement les \_ \_ dest.</span><span class="sxs-lookup"><span data-stu-id="627b1-121">RTM\_NOTIFY\_ONLY\_MARKED\_DESTS</span></span> | <span data-ttu-id="627b1-122">0x00010000</span><span class="sxs-lookup"><span data-stu-id="627b1-122">0x00010000</span></span> | <span data-ttu-id="627b1-123">Notifie le client des modifications apportées aux destinations marquées par le client.</span><span class="sxs-lookup"><span data-stu-id="627b1-123">Notifies the client of changes to destinations that the client has marked.</span></span> <span data-ttu-id="627b1-124">Si cet indicateur n’est pas spécifié, les messages de notification de modification pour toutes les destinations sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="627b1-124">If this flag is not specified, change notification messages for all destinations are sent.</span></span> |



 

 

 




