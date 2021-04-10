---
title: Utilisation du gestionnaire de tables de routage version 2
description: Avant de commencer à développer des clients qui utilisent les API RTMv2, passez en revue les problèmes de programmation RTMv2.
ms.assetid: c0187b65-3cb2-4ab0-8d5f-ca37e8bc0ad7
keywords:
- Routage et accès à distance service RRAS, gestionnaire de table de routage version 2, tâches
- Gestionnaire de table de routage version 2 RRAS, tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29bc7acab213325a0683de215995eeb2f635b102
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940068"
---
# <a name="using-routing-table-manager-version-2"></a><span data-ttu-id="6cedd-105">Utilisation du gestionnaire de tables de routage version 2</span><span class="sxs-lookup"><span data-stu-id="6cedd-105">Using Routing Table Manager Version 2</span></span>

<span data-ttu-id="6cedd-106">Avant de commencer à développer des clients qui utilisent les API RTMv2, passez en revue les [problèmes de programmation RTMv2](rtmv2-programming-issues.md).</span><span class="sxs-lookup"><span data-stu-id="6cedd-106">Before you begin developing clients that use the RTMv2 APIs, review the [RTMv2 Programming Issues](rtmv2-programming-issues.md).</span></span>

<span data-ttu-id="6cedd-107">Cette section contient un exemple de code qui peut être utilisé lors du développement de clients tels que des protocoles de routage.</span><span class="sxs-lookup"><span data-stu-id="6cedd-107">This section contains sample code that can be used when developing clients such as routing protocols.</span></span>

-   [<span data-ttu-id="6cedd-108">Problèmes de programmation RTMv2</span><span class="sxs-lookup"><span data-stu-id="6cedd-108">RTMv2 Programming Issues</span></span>](rtmv2-programming-issues.md)
-   [<span data-ttu-id="6cedd-109">S’inscrire auprès du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="6cedd-109">Register with the Routing Table Manager</span></span>](register-with-the-routing-table-manager.md)
-   [<span data-ttu-id="6cedd-110">Énumérer les entités inscrites</span><span class="sxs-lookup"><span data-stu-id="6cedd-110">Enumerate the Registered Entities</span></span>](enumerate-the-registered-entities.md)
-   [<span data-ttu-id="6cedd-111">Obtenir et appeler les méthodes exportées pour un client</span><span class="sxs-lookup"><span data-stu-id="6cedd-111">Obtain and Call the Exported Methods for a Client</span></span>](obtain-and-call-the-exported-methods-for-a-client.md)
-   [<span data-ttu-id="6cedd-112">Inscription à la notification de modification</span><span class="sxs-lookup"><span data-stu-id="6cedd-112">Register for Change Notification</span></span>](register-for-change-notification.md)
-   [<span data-ttu-id="6cedd-113">Ajouter et mettre à jour des itinéraires à l’aide de RtmAddRouteToDest</span><span class="sxs-lookup"><span data-stu-id="6cedd-113">Add and Update Routes Using RtmAddRouteToDest</span></span>](add-and-update-routes-using-rtmaddroutetodest.md)
-   [<span data-ttu-id="6cedd-114">Mettre à jour un itinéraire sur place à l’aide de RtmUpdateAndUnlockRoute</span><span class="sxs-lookup"><span data-stu-id="6cedd-114">Update a Route In Place Using RtmUpdateAndUnlockRoute</span></span>](update-a-route-in-place-using-rtmupdateandunlockroute.md)
-   [<span data-ttu-id="6cedd-115">Utiliser l’état de Hold-Down de l’itinéraire</span><span class="sxs-lookup"><span data-stu-id="6cedd-115">Use the Route Hold-Down State</span></span>](use-the-route-hold-down-state.md)
-   [<span data-ttu-id="6cedd-116">Énumérer toutes les destinations</span><span class="sxs-lookup"><span data-stu-id="6cedd-116">Enumerate All Destinations</span></span>](enumerate-all-destinations.md)
-   [<span data-ttu-id="6cedd-117">Énumérer tous les itinéraires</span><span class="sxs-lookup"><span data-stu-id="6cedd-117">Enumerate All Routes</span></span>](enumerate-all-routes.md)
-   [<span data-ttu-id="6cedd-118">Rechercher le meilleur itinéraire</span><span class="sxs-lookup"><span data-stu-id="6cedd-118">Search for the Best Route</span></span>](search-for-the-best-route.md)
-   [<span data-ttu-id="6cedd-119">Rechercher des itinéraires à l’aide d’une arborescence de préfixe</span><span class="sxs-lookup"><span data-stu-id="6cedd-119">Search for Routes Using a Prefix Tree</span></span>](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md)
-   [<span data-ttu-id="6cedd-120">Accéder au pointeur opaque dans une destination</span><span class="sxs-lookup"><span data-stu-id="6cedd-120">Access the Opaque Pointer in a Destination</span></span>](access-the-opaque-pointer-in-a-destination.md)
-   [<span data-ttu-id="6cedd-121">Utiliser une liste d’itinéraires Client-Specific</span><span class="sxs-lookup"><span data-stu-id="6cedd-121">Use a Client-Specific Route List</span></span>](use-a-client-specific-route-list.md)
-   [<span data-ttu-id="6cedd-122">Utiliser le rappel de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="6cedd-122">Use the Event Notification Callback</span></span>](use-the-event-notification-callback.md)

 

 




