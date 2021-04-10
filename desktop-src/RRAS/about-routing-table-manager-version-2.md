---
title: À propos du gestionnaire de table de routage version 2
description: La documentation suivante décrit la technologie du gestionnaire de tables de routage version 2 (RTMv2).
ms.assetid: 9f84863e-45ed-49d1-8df4-3b59b1b5f3c9
keywords:
- Routage et accès à distance service RRAS, gestionnaire de tables de routage version 2
- Routage et accès à distance service RRAS, gestionnaire de table de routage version 2, Description
- Gestionnaire de routage de la version 2 RRAS
- Gestionnaire de routage de la version 2 RRAS, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5014dc894c4a517bfdfac8478e520658a4987d4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029332"
---
# <a name="about-routing-table-manager-version-2"></a><span data-ttu-id="4c7ac-107">À propos du gestionnaire de table de routage version 2</span><span class="sxs-lookup"><span data-stu-id="4c7ac-107">About Routing Table Manager Version 2</span></span>

<span data-ttu-id="4c7ac-108">La documentation suivante décrit la technologie du gestionnaire de tables de routage version 2 (RTMv2).</span><span class="sxs-lookup"><span data-stu-id="4c7ac-108">The following documentation describes the Routing Table Manager Version 2 (RTMv2) technology.</span></span> <span data-ttu-id="4c7ac-109">L’API RTMv2 est une fonctionnalité de Windows 2000 et des systèmes d’exploitation ultérieurs que vous pouvez utiliser pour écrire des protocoles de routage qui interagissent avec le gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="4c7ac-109">The RTMv2 API is a feature of Windows 2000 and later operating systems that you can use to write routing protocols that interact with the routing table manager.</span></span>

<span data-ttu-id="4c7ac-110">Le gestionnaire de tables de routage est le référentiel central des informations de routage pour tous les protocoles de routage qui fonctionnent sous le service de routage et d’accès à distance (RRAS).</span><span class="sxs-lookup"><span data-stu-id="4c7ac-110">The routing table manager is the central repository of routing information for all routing protocols that operate under the Routing and Remote Access Service (RRAS).</span></span>

<span data-ttu-id="4c7ac-111">RTMv2 n’est pas disponible pour Windows NT version 4,0.</span><span class="sxs-lookup"><span data-stu-id="4c7ac-111">RTMv2 is not available for Windows NT version 4.0.</span></span> <span data-ttu-id="4c7ac-112">En outre, RTMv2 ne peut pas être utilisé pour les protocoles de routage IPX qui s’exécutent sur Windows NT 4,0 ou Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="4c7ac-112">Additionally, RTMv2 cannot be used for IPX routing protocols that run on Windows NT 4.0 or Windows 2000.</span></span> <span data-ttu-id="4c7ac-113">Si vous utilisez IPX ou écrivez des protocoles de routage pour Windows NT 4,0, reportez-vous à la rubrique [à propos de la version 1 du gestionnaire de tables de routage](about-routing-table-manager-version-1.md).</span><span class="sxs-lookup"><span data-stu-id="4c7ac-113">If you are using IPX or writing routing protocols for Windows NT 4.0, please refer to [About Routing Table Manager Version 1](about-routing-table-manager-version-1.md).</span></span>

<span data-ttu-id="4c7ac-114">Cette vue d’ensemble décrit les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="4c7ac-114">This overview describes the following topics:</span></span>

-   [<span data-ttu-id="4c7ac-115">Composants de l’architecture du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="4c7ac-115">Components of the Routing Table Manager Architecture</span></span>](components-of-the-routing-table-manager-architecture.md)
-   [<span data-ttu-id="4c7ac-116">Inscription auprès du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="4c7ac-116">Registering with the Routing Table Manager</span></span>](registering-with-the-routing-table-manager.md)
-   [<span data-ttu-id="4c7ac-117">Énumération des entités inscrites</span><span class="sxs-lookup"><span data-stu-id="4c7ac-117">Enumerating Registered Entities</span></span>](enumerating-registered-entities.md)
-   [<span data-ttu-id="4c7ac-118">Utilisation de méthodes</span><span class="sxs-lookup"><span data-stu-id="4c7ac-118">Using Methods</span></span>](using-methods.md)
-   [<span data-ttu-id="4c7ac-119">Utilisation de pointeurs opaques</span><span class="sxs-lookup"><span data-stu-id="4c7ac-119">Using Opaque Pointers</span></span>](using-opaque-pointers.md)
-   [<span data-ttu-id="4c7ac-120">Marquage des itinéraires pour l’État Hold-Down</span><span class="sxs-lookup"><span data-stu-id="4c7ac-120">Marking Routes for the Hold-Down State</span></span>](marking-routes-for-the-hold-down-state.md)
-   [<span data-ttu-id="4c7ac-121">Ajout d’itinéraires</span><span class="sxs-lookup"><span data-stu-id="4c7ac-121">Adding Routes</span></span>](adding-routes.md)
-   [<span data-ttu-id="4c7ac-122">Récupération des informations d’itinéraire</span><span class="sxs-lookup"><span data-stu-id="4c7ac-122">Retrieving Route Information</span></span>](retrieving-route-information.md)
-   [<span data-ttu-id="4c7ac-123">Mise à jour des itinéraires</span><span class="sxs-lookup"><span data-stu-id="4c7ac-123">Updating Routes</span></span>](updating-routes.md)
-   [<span data-ttu-id="4c7ac-124">Réception des notifications de modifications</span><span class="sxs-lookup"><span data-stu-id="4c7ac-124">Receiving Notification of Changes</span></span>](receiving-notification-of-changes.md)
-   [<span data-ttu-id="4c7ac-125">Utilisation des tronçons suivants</span><span class="sxs-lookup"><span data-stu-id="4c7ac-125">Working with Next Hops</span></span>](working-with-next-hops.md)
-   [<span data-ttu-id="4c7ac-126">Énumération des entrées de table de routage</span><span class="sxs-lookup"><span data-stu-id="4c7ac-126">Enumerating Routing Table Entries</span></span>](enumerating-routing-table-entries.md)
-   [<span data-ttu-id="4c7ac-127">Recherche d’informations spécifiques dans la table de routage</span><span class="sxs-lookup"><span data-stu-id="4c7ac-127">Finding Specific Information in the Routing Table</span></span>](finding-specific-information-in-the-routing-table.md)
-   [<span data-ttu-id="4c7ac-128">Maintenance des listes de Client-Specific</span><span class="sxs-lookup"><span data-stu-id="4c7ac-128">Maintaining Client-Specific Lists</span></span>](maintaining-client-specific-lists.md)
-   [<span data-ttu-id="4c7ac-129">Gestion des handles</span><span class="sxs-lookup"><span data-stu-id="4c7ac-129">Managing Handles</span></span>](managing-handles.md)

 

 




