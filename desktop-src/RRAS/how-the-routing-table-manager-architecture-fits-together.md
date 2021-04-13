---
title: Combinaison de l’architecture du gestionnaire de tables de routage
description: L’illustration suivante montre la relation entre les différents composants d’un routeur.
ms.assetid: 862566ce-47c4-424a-84c2-99f4c92efcc0
keywords:
- RTM, architecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc36c339ac89f01d5ba14c00857b3ced9c29414c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311593"
---
# <a name="how-the-routing-table-manager-architecture-fits-together"></a><span data-ttu-id="52e47-104">Combinaison de l’architecture du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="52e47-104">How the Routing Table Manager Architecture Fits Together</span></span>

<span data-ttu-id="52e47-105">L’illustration suivante montre la relation entre les différents composants d’un routeur.</span><span class="sxs-lookup"><span data-stu-id="52e47-105">The following illustration shows the relationship between the different components of a router.</span></span>

![relation entre les composants de routeur](images/rtsrvarch.png)

<span data-ttu-id="52e47-107">Lorsque le routeur est amorcé, le Service Router Manager est démarré, ainsi qu’un ou plusieurs protocoles de routage.</span><span class="sxs-lookup"><span data-stu-id="52e47-107">When the router is bootstrapped, the router manager service is started, as well as one or more routing protocols.</span></span> <span data-ttu-id="52e47-108">Les protocoles de routage sont associés aux différentes interfaces sur le routeur.</span><span class="sxs-lookup"><span data-stu-id="52e47-108">Routing protocols are associated with the various interfaces on the router.</span></span> <span data-ttu-id="52e47-109">Le gestionnaire de routeur démarre également le gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="52e47-109">The router manager also starts the routing table manager.</span></span>

<span data-ttu-id="52e47-110">L’illustration suivante montre la relation entre les clients et les différents composants du gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="52e47-110">The following illustration shows the relationship between clients and the different components of the routing table manager.</span></span>

![relation entre les clients et les composants du gestionnaire de tables de routage](images/rtmentrel.png)

<span data-ttu-id="52e47-112">Le gestionnaire de routeur démarre une ou plusieurs instances du gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="52e47-112">The router manager starts one or more instances of the routing table manager.</span></span> <span data-ttu-id="52e47-113">Lorsque plusieurs instances du gestionnaire de tables de routage sont démarrées, le routeur a été configuré pour agir comme un ou plusieurs routeurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="52e47-113">When multiple instances of the routing table manager are started, the router has been configured to act as one or more virtual routers.</span></span> <span data-ttu-id="52e47-114">Chaque instance du gestionnaire de tables de routage possède une ou plusieurs interfaces ; chaque interface ne peut appartenir qu’à une seule instance du gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="52e47-114">Each instance of the routing table manager owns one or more interfaces; each interface can only be owned by one instance of the routing table manager.</span></span>

<span data-ttu-id="52e47-115">Chaque instance du gestionnaire de tables de routage est indépendante des autres. aucune information n’est échangée entre les instances.</span><span class="sxs-lookup"><span data-stu-id="52e47-115">Each instance of the routing table manager is independent from the others; no information is exchanged between the instances.</span></span>

<span data-ttu-id="52e47-116">Chaque instance du gestionnaire de tables de routage contient une ou plusieurs tables de routage.</span><span class="sxs-lookup"><span data-stu-id="52e47-116">Each instance of the routing table manager contains one or more routing tables.</span></span> <span data-ttu-id="52e47-117">Chaque table de routage est associée à une famille d’adresses.</span><span class="sxs-lookup"><span data-stu-id="52e47-117">Each routing table is associated with an address family.</span></span>

<span data-ttu-id="52e47-118">Chaque table de routage contient une ou plusieurs vues.</span><span class="sxs-lookup"><span data-stu-id="52e47-118">Each routing table contains one or more views.</span></span> <span data-ttu-id="52e47-119">Dans cet exemple, la table de routage est affichée avec une vue monodiffusion et multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="52e47-119">In this example, the routing table is shown with a unicast and multicast view.</span></span> <span data-ttu-id="52e47-120">Chaque vue est un sous-ensemble de la table de routage.</span><span class="sxs-lookup"><span data-stu-id="52e47-120">Each view is a subset of the routing table.</span></span>

<span data-ttu-id="52e47-121">L’illustration suivante montre la relation entre les clients et plusieurs instances du gestionnaire de tables de routage, les tables de routage et les vues.</span><span class="sxs-lookup"><span data-stu-id="52e47-121">The following illustration shows the relationship between clients and multiple instances of the routing table manager, routing tables, and views.</span></span>

![clients de relation, gestionnaire de tables de routage, tables de routage, vues](images/multrtabrel.png)

<span data-ttu-id="52e47-123">Une instance du client peut s’inscrire plusieurs fois auprès d’une instance du gestionnaire de table de routage, une fois par famille d’adresses.</span><span class="sxs-lookup"><span data-stu-id="52e47-123">An instance of the client can register multiple times with an instance of the routing table manager — once per address family.</span></span> <span data-ttu-id="52e47-124">Un client peut s’inscrire auprès de chaque instance du gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="52e47-124">A client can register with each instance of the routing table manager.</span></span>

<span data-ttu-id="52e47-125">L’illustration suivante montre la relation entre les entrées de la table de routage.</span><span class="sxs-lookup"><span data-stu-id="52e47-125">The following illustration shows how the routing table entries are related.</span></span> <span data-ttu-id="52e47-126">Pour plus d’informations sur les entrées de table de routage, consultez [entrées de table de routage](routing-table-entries.md).</span><span class="sxs-lookup"><span data-stu-id="52e47-126">For more information on routing table entries, see [Routing Table Entries](routing-table-entries.md).</span></span>

![relation entre les entrées de la table de routage](images/nexthop.png)

<span data-ttu-id="52e47-128">La table de routage contient des destinations.</span><span class="sxs-lookup"><span data-stu-id="52e47-128">The routing table contains destinations.</span></span> <span data-ttu-id="52e47-129">Chaque destination est associée à un ou plusieurs itinéraires.</span><span class="sxs-lookup"><span data-stu-id="52e47-129">Each destination is related to one or more routes.</span></span> <span data-ttu-id="52e47-130">Chaque itinéraire a zéro, un ou plusieurs pointeurs vers les tronçons suivants associés à l’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="52e47-130">Each route has zero, one, or more pointers to next hops that are associated with the route.</span></span> <span data-ttu-id="52e47-131">Chaque pointeur fait référence au tronçon suivant réel dans la liste des tronçons suivants.</span><span class="sxs-lookup"><span data-stu-id="52e47-131">Each pointer refers to the actual next hop in the list of next hops.</span></span> <span data-ttu-id="52e47-132">Chaque client qui s’inscrit auprès du gestionnaire de tables de routage crée une liste de sauts suivants détenus par le client.</span><span class="sxs-lookup"><span data-stu-id="52e47-132">Each client that registers with the routing table manager creates a list of next hops that the client owns.</span></span>

<span data-ttu-id="52e47-133">Les itinéraires ne peuvent contenir que des pointeurs vers la liste de tronçons suivants associée au client qui possède l’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="52e47-133">Routes can only contain pointers to the next-hop list associated with the client that owns the route.</span></span>

 

 




