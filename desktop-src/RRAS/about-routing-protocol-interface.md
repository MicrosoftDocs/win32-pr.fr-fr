---
title: À propos de l’interface de protocole de routage
description: La documentation suivante décrit l’intégration de protocoles de routage tiers dans le service de routage et d’accès à distance (RRAS).
ms.assetid: 593e3b8a-6f26-47c6-aa93-520d36db7a6f
keywords:
- Routage et accès à distance service RRAS, interface de protocole de routage
- Routage et accès à distance service RRAS, interface de protocole de routage, décrite
- Service RRAS de l’interface de protocole de routage
- Interface de protocole de routage RRAS, décrite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bc663f249ca42ebbae509c164a828d603a9b968
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674093"
---
# <a name="about-routing-protocol-interface"></a><span data-ttu-id="33b66-107">À propos de l’interface de protocole de routage</span><span class="sxs-lookup"><span data-stu-id="33b66-107">About Routing Protocol Interface</span></span>

<span data-ttu-id="33b66-108">La documentation suivante décrit l’intégration de protocoles de routage tiers dans le service de routage et d’accès à distance (RRAS).</span><span class="sxs-lookup"><span data-stu-id="33b66-108">The following documentation describes the integration of third-party routing protocols into the Routing and Remote Access Service (RRAS).</span></span> <span data-ttu-id="33b66-109">Le service RRAS est une fonctionnalité de Windows qui joue le rôle de routeur multi-protocole.</span><span class="sxs-lookup"><span data-stu-id="33b66-109">RRAS is a feature of Windows that acts as a multi-protocol router.</span></span> <span data-ttu-id="33b66-110">Le service RRAS définit l’interface entre le gestionnaire de routeur et le protocole de routage.</span><span class="sxs-lookup"><span data-stu-id="33b66-110">RRAS defines the interface between the router manager and the routing protocol.</span></span> <span data-ttu-id="33b66-111">Le protocole de routage est implémenté dans une bibliothèque de liens dynamiques (DLL).</span><span class="sxs-lookup"><span data-stu-id="33b66-111">The routing protocol is implemented in a dynamic link library (DLL).</span></span>

<span data-ttu-id="33b66-112">Utilisez cette interface pour implémenter des protocoles de routage, tels que IGRP, NLSP et BGP, en tant que dll en mode utilisateur qui fonctionnent avec RRAS.</span><span class="sxs-lookup"><span data-stu-id="33b66-112">Use this interface to implement routing protocols, such as IGRP, NLSP, and BGP, as user-mode DLLs that work with RRAS.</span></span>

<span data-ttu-id="33b66-113">Cette documentation décrit les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="33b66-113">This documentation describes the following topics:</span></span>

-   [<span data-ttu-id="33b66-114">Adaptateurs</span><span class="sxs-lookup"><span data-stu-id="33b66-114">Adapters</span></span>](adapters.md)
-   [<span data-ttu-id="33b66-115">Interfaces</span><span class="sxs-lookup"><span data-stu-id="33b66-115">Interfaces</span></span>](interfaces.md)
-   [<span data-ttu-id="33b66-116">Itinéraires statiques et statiques</span><span class="sxs-lookup"><span data-stu-id="33b66-116">Static and Autostatic Routes</span></span>](static-and-autostatic-routes.md)

 

 




