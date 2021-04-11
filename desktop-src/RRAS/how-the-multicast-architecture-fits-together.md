---
title: Combinaison de l’architecture de multidiffusion
description: Cette section décrit un exemple de configuration et la façon dont les principaux composants s’imbriquent.
ms.assetid: 1fa0b343-0276-402b-8c3d-5ca114ad43cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc82178568bac01e89eb0a4d6ea9222d45e7f5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197018"
---
# <a name="how-the-multicast-architecture-fits-together"></a><span data-ttu-id="e3a04-103">Combinaison de l’architecture de multidiffusion</span><span class="sxs-lookup"><span data-stu-id="e3a04-103">How the Multicast Architecture Fits Together</span></span>

<span data-ttu-id="e3a04-104">Cette section décrit un exemple de configuration et la façon dont les principaux composants s’imbriquent.</span><span class="sxs-lookup"><span data-stu-id="e3a04-104">This section describes a sample configuration and how the major components fit together.</span></span>

<span data-ttu-id="e3a04-105">L’illustration suivante montre la relation entre les différents composants d’un routeur.</span><span class="sxs-lookup"><span data-stu-id="e3a04-105">The following illustration shows the relationship between the various components of a router.</span></span>

![relation entre les composants du routeur Windows 2000](images/mrarch1.png)

<span data-ttu-id="e3a04-107">Le gestionnaire de groupe de multidiffusion fait partie du service RRAS qui s’exécute sur un serveur qui fonctionne en tant que routeur.</span><span class="sxs-lookup"><span data-stu-id="e3a04-107">The multicast group manager is a part of the RRAS service that runs on a server that is operating as a router.</span></span>

<span data-ttu-id="e3a04-108">Trois protocoles de routage de multidiffusion (protocole 1, protocole 2, protocole 3) sont exécutés sur le routeur.</span><span class="sxs-lookup"><span data-stu-id="e3a04-108">The router shown has three multicast routing protocols (Protocol 1, Protocol 2, Protocol 3) running on it.</span></span> <span data-ttu-id="e3a04-109">Chaque protocole peut posséder une ou plusieurs interfaces (dans cette illustration, le protocole 1 possède l’interface 1, le protocole 2 possède l’interface 2 et le protocole 3 est propriétaire de l’interface 3).</span><span class="sxs-lookup"><span data-stu-id="e3a04-109">Each protocol can own one or more interfaces (in this illustration, Protocol 1 owns Interface 1, Protocol 2 owns Interface 2, and Protocol 3 owns Interface 3).</span></span> <span data-ttu-id="e3a04-110">Chaque interface ne peut appartenir qu’à un seul protocole de routage (en plus de IGMP, ce qui est un cas spécial).</span><span class="sxs-lookup"><span data-stu-id="e3a04-110">Each interface can be owned by only one routing protocol (in addition to IGMP, which is a special case).</span></span>

<span data-ttu-id="e3a04-111">Le gestionnaire de groupe de multidiffusion s’exécute sur le routeur et coordonne la distribution des informations de groupe entre les protocoles de routage.</span><span class="sxs-lookup"><span data-stu-id="e3a04-111">The multicast group manager runs on the router and coordinates the distribution of group information between the routing protocols.</span></span>

<span data-ttu-id="e3a04-112">L’illustration suivante montre la relation entre deux routeurs dans une architecture de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="e3a04-112">The following illustration shows the relationship between two routers in a multicast architecture.</span></span>

![relation entre deux routeurs dans une architecture de multidiffusion](images/mrarch2.png)

<span data-ttu-id="e3a04-114">Dans l’illustration précédente, le routeur 2 envoie un message de multidiffusion au réseau 2 sur l’interface 3.</span><span class="sxs-lookup"><span data-stu-id="e3a04-114">In the previous illustration, Router 2 sends a multicast message to Network 2 on Interface 3.</span></span> <span data-ttu-id="e3a04-115">Le routeur 1 reçoit le message de multidiffusion du réseau 2 sur l’interface 3.</span><span class="sxs-lookup"><span data-stu-id="e3a04-115">Router 1 receives the multicast message from Network 2 on Interface 3.</span></span> <span data-ttu-id="e3a04-116">Sur les deux routeurs, le protocole 3 est propriétaire de l’interface respective 3.</span><span class="sxs-lookup"><span data-stu-id="e3a04-116">On both routers, Protocol 3 owns the respective Interface 3.</span></span>

<span data-ttu-id="e3a04-117">L’illustration suivante montre le chemin d’accès d’un message provenant d’une source de multidiffusion (à un groupe multicast) pour atteindre l’hôte qui a rejoint le groupe de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="e3a04-117">The following illustration shows the path a message from a multicast source (to a multicast group) takes to reach the host that has joined the multicast group.</span></span> <span data-ttu-id="e3a04-118">Les routeurs de l’illustration utilisent la même configuration que les illustrations précédentes. Toutefois, les détails de l’interface et du protocole ne sont pas affichés afin de conserver la figure en simple.</span><span class="sxs-lookup"><span data-stu-id="e3a04-118">The routers in the illustration use the same configuration as previous illustrations; however, the interface and protocol details are not shown in order to keep the figure simple.</span></span>

![chemin d’accès du message de la source de multidiffusion à l’hôte de destination](images/mrarch3.png)

<span data-ttu-id="e3a04-120">Le scénario suivant décrit les événements qui se produisent lorsqu’un hôte rejoint un groupe de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="e3a04-120">The following scenario describes the events that take place when a host joins a multicast group.</span></span> <span data-ttu-id="e3a04-121">Reportez-vous à l’illustration précédente pour les relations entre les différentes entités.</span><span class="sxs-lookup"><span data-stu-id="e3a04-121">Refer to the previous illustration for relationships between the various entities.</span></span>

1.  <span data-ttu-id="e3a04-122">L’hôte 1 rejoint le groupe de multidiffusion G sur le réseau 3.</span><span class="sxs-lookup"><span data-stu-id="e3a04-122">Host 1 joins the multicast group G on Network 3.</span></span>
2.  <span data-ttu-id="e3a04-123">Le routeur 3 apprend G via IGMP.</span><span class="sxs-lookup"><span data-stu-id="e3a04-123">Router 3 learns about G via IGMP.</span></span>
3.  <span data-ttu-id="e3a04-124">Le gestionnaire de groupe de multidiffusion sur le routeur 3 notifie le protocole 3 sur le routeur 3 qu’il existe de nouveaux récepteurs pour G.</span><span class="sxs-lookup"><span data-stu-id="e3a04-124">The multicast group manager on Router 3 notifies Protocol 3 on Router 3 that there are new receivers for G.</span></span>
4.  <span data-ttu-id="e3a04-125">Le protocole 3 sur le routeur 3 notifie ensuite le protocole 3 sur le routeur 1 à propos de G.</span><span class="sxs-lookup"><span data-stu-id="e3a04-125">Protocol 3 on Router 3 then notifies Protocol 3 on Router 1 about G.</span></span>
5.  <span data-ttu-id="e3a04-126">À son tour, le protocole 3 sur le routeur 1 notifie le gestionnaire de groupe de multidiffusion sur le routeur 1 à propos de G.</span><span class="sxs-lookup"><span data-stu-id="e3a04-126">In turn, Protocol 3 on Router 1 notifies the multicast group manager on Router 1 about G.</span></span>
6.  <span data-ttu-id="e3a04-127">Le gestionnaire de groupe de multidiffusion sur le routeur 1 notifie ensuite le protocole 1 et le protocole 2 sur G.</span><span class="sxs-lookup"><span data-stu-id="e3a04-127">The multicast group manager on Router 1 then notifies Protocol 1 and Protocol 2 about G.</span></span>
7.  <span data-ttu-id="e3a04-128">Le protocole 2 peut informer le routeur 2 de G, si le protocole est conçu à cette fin.</span><span class="sxs-lookup"><span data-stu-id="e3a04-128">Protocol 2 may inform Router 2 about G, if the protocol is designed to do so.</span></span>

<span data-ttu-id="e3a04-129">Le scénario suivant décrit les événements qui se produisent lorsqu’un message est envoyé à un groupe de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="e3a04-129">The following scenario describes the events that take place when a message is sent to a multicast group.</span></span> <span data-ttu-id="e3a04-130">Reportez-vous à l’illustration précédente pour les relations entre les différentes entités.</span><span class="sxs-lookup"><span data-stu-id="e3a04-130">Refer to the previous illustration for the relationships between the various entities.</span></span>

1.  <span data-ttu-id="e3a04-131">Une source sur le réseau 1 envoie un message au groupe G.</span><span class="sxs-lookup"><span data-stu-id="e3a04-131">A source on Network 1 sends a message to Group G.</span></span>
2.  <span data-ttu-id="e3a04-132">Le message envoyé à partir de la source est d’abord dirigé vers le routeur 2, qui le transfère ensuite au routeur 1 à l’aide de l’interface 2 (puisque le routeur 2 a été informé par le protocole 2 que les récepteurs sont présents en aval).</span><span class="sxs-lookup"><span data-stu-id="e3a04-132">The message sent from Source S goes first to Router 2, which then forwards it to Router 1 using Interface 2 (since Router 2 has been informed by Protocol 2 that receivers are present downstream).</span></span>
3.  <span data-ttu-id="e3a04-133">Le routeur 1 transfère le message au routeur 3 (puisque le routeur 1 a été informé par le protocole 2 que les récepteurs sont présents en aval).</span><span class="sxs-lookup"><span data-stu-id="e3a04-133">Router 1 forwards the message to Router 3 (since Router 1 has been informed by Protocol 2 that receivers are present downstream).</span></span>
4.  <span data-ttu-id="e3a04-134">Le routeur 3 envoie le message au réseau 3, et il arrive donc à l’hôte 1.</span><span class="sxs-lookup"><span data-stu-id="e3a04-134">Router 3 forwards the message to Network 3, and therefore it arrives at Host 1.</span></span>

<span data-ttu-id="e3a04-135">Pour plus d’informations sur l’interaction du protocole de routage multidiffusion, consultez [RFC 2715](routing-protocols-request-for-comments.md), règles d’interopérabilité pour les protocoles de routage de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="e3a04-135">For further information on multicast routing protocol interaction, see [RFC 2715](routing-protocols-request-for-comments.md), Interoperability Rules for Multicast Routing Protocols.</span></span>

 

 




