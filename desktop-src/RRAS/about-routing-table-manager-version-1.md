---
title: À propos du gestionnaire de tables de routage version 1
description: Le gestionnaire de tables de routage est un référentiel central d’informations de routage pour tous les protocoles de routage qui fonctionnent sous le service Routage et accès distant (RRAS).
ms.assetid: 6d0e7697-5c52-4a69-b2a1-9c893600191b
keywords:
- Routage et accès à distance service RRAS, gestionnaire de tables de routage version 1
- Routage et accès à distance service RRAS, gestionnaire de table de routage version 1, décrit
- Gestionnaire de routage de la version 1 RRAS
- Gestionnaire de table de routage version 1 RRAS, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b99f913230db6e6882a36b414914c3924181a221
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029333"
---
# <a name="about-routing-table-manager-version-1"></a><span data-ttu-id="3d1cb-107">À propos du gestionnaire de tables de routage version 1</span><span class="sxs-lookup"><span data-stu-id="3d1cb-107">About Routing Table Manager Version 1</span></span>

<span data-ttu-id="3d1cb-108">**Windows Server 2003 :** Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3d1cb-108">**Windows Server 2003:** This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="3d1cb-109">Les nouvelles applications doivent utiliser l’API du gestionnaire de table de routage version 2.</span><span class="sxs-lookup"><span data-stu-id="3d1cb-109">New applications should use the Routing Table Manager Version 2 API.</span></span>

<span data-ttu-id="3d1cb-110">Le gestionnaire de tables de routage est un référentiel central d’informations de routage pour tous les protocoles de routage qui fonctionnent sous le service Routage et accès distant (RRAS).</span><span class="sxs-lookup"><span data-stu-id="3d1cb-110">The routing table manager is a central repository of routing information for all routing protocols that operate under Routing and Remote Access Service (RRAS).</span></span> <span data-ttu-id="3d1cb-111">Le gestionnaire de tables de routage fournit des informations de routage à tous les composants concernés, tels que les protocoles de routage, les agents de gestion et les agents de surveillance.</span><span class="sxs-lookup"><span data-stu-id="3d1cb-111">The routing table manager provides routing information to all interested components, such as routing protocols, management agents, and monitoring agents.</span></span> <span data-ttu-id="3d1cb-112">Le gestionnaire de tables de routage détermine également le meilleur itinéraire vers chaque réseau de destination connu des protocoles de routage.</span><span class="sxs-lookup"><span data-stu-id="3d1cb-112">The routing table manager also determines the best route to each destination network known to the routing protocols.</span></span> <span data-ttu-id="3d1cb-113">Il détermine cet itinéraire en fonction des priorités de protocole de routage et des métriques associées aux itinéraires.</span><span class="sxs-lookup"><span data-stu-id="3d1cb-113">It determines this route based on routing protocol priorities and on metrics associated with the routes.</span></span> <span data-ttu-id="3d1cb-114">Notez que l’administrateur peut configurer des priorités de protocole de routage.</span><span class="sxs-lookup"><span data-stu-id="3d1cb-114">Note that the administrator is able to configure routing protocol priorities.</span></span> <span data-ttu-id="3d1cb-115">Le gestionnaire de tables de routage transmet ensuite les informations les plus adaptées aux redirecteurs et les achemine vers les protocoles de routage.</span><span class="sxs-lookup"><span data-stu-id="3d1cb-115">The routing table manager then passes the best-route information on to the forwarders and back to the routing protocols.</span></span>

<span data-ttu-id="3d1cb-116">Chaque protocole de routage appelle [**RtmRegisterClient**](rtmregisterclient.md) pour s’inscrire auprès du gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="3d1cb-116">Each routing protocol calls [**RtmRegisterClient**](rtmregisterclient.md) to register with the routing table manager.</span></span> <span data-ttu-id="3d1cb-117">**RtmRegisterClient** retourne un handle qui est utilisé par le protocole de routage pour ajouter ou supprimer des entrées d’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="3d1cb-117">**RtmRegisterClient** returns a handle that is used by the routing protocol to add or delete route entries.</span></span> <span data-ttu-id="3d1cb-118">**RtmRegisterClient** permet également au protocole de routage d’inscrire un objet d’événement auprès du gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="3d1cb-118">**RtmRegisterClient** also allows the routing protocol to register an event object with the routing table manager.</span></span> <span data-ttu-id="3d1cb-119">Le gestionnaire de table de routage signale cet objet d’événement pour notifier le protocole de routage des modifications apportées aux meilleures informations de routage.</span><span class="sxs-lookup"><span data-stu-id="3d1cb-119">The routing table manager signals this event object to notify the routing protocol of changes in best-route information.</span></span> <span data-ttu-id="3d1cb-120">Tous les autres composants peuvent obtenir des informations stockées dans le gestionnaire de tables de routage par le biais de l’énumération d’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="3d1cb-120">All other components can obtain information stored in the routing table manager through route enumeration.</span></span>

 

 




