---
description: L’infrastructure homologue est un ensemble de plusieurs API qui sont puissantes et flexibles.
ms.assetid: aed7585a-88e5-4ca3-a8c3-e2ccfe13d35d
title: Qu’est-ce que l’infrastructure homologue ?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873717b3f90497fe9ab9f50bb9c18e6f0692a4e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527477"
---
# <a name="what-is-the-peer-infrastructure"></a><span data-ttu-id="b141d-103">Qu’est-ce que l’infrastructure homologue ?</span><span class="sxs-lookup"><span data-stu-id="b141d-103">What is the Peer Infrastructure?</span></span>

<span data-ttu-id="b141d-104">L’infrastructure homologue est un ensemble de plusieurs API qui sont puissantes et flexibles.</span><span class="sxs-lookup"><span data-stu-id="b141d-104">The Peer Infrastructure is a set of several APIs that are powerful and flexible.</span></span> <span data-ttu-id="b141d-105">Les principaux composants sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="b141d-105">The major components include the following:</span></span>

-   [<span data-ttu-id="b141d-106">API graphique d’homologues</span><span class="sxs-lookup"><span data-stu-id="b141d-106">Peer Graphing API</span></span>](#peer-graphing-api)
-   [<span data-ttu-id="b141d-107">API de regroupement d’homologues</span><span class="sxs-lookup"><span data-stu-id="b141d-107">Peer Grouping API</span></span>](#peer-grouping-api)
-   [<span data-ttu-id="b141d-108">API du gestionnaire d’identités homologues</span><span class="sxs-lookup"><span data-stu-id="b141d-108">Peer Identity Manager API</span></span>](#peer-identity-manager-api)
-   [<span data-ttu-id="b141d-109">API du fournisseur d’espace de noms PNRP</span><span class="sxs-lookup"><span data-stu-id="b141d-109">PNRP Namespace Provider API</span></span>](#pnrp-namespace-provider-api)

## <a name="peer-graphing-api"></a><span data-ttu-id="b141d-110">API graphique d’homologues</span><span class="sxs-lookup"><span data-stu-id="b141d-110">Peer Graphing API</span></span>

<span data-ttu-id="b141d-111">L’infrastructure de pairs fournit une technologie graphique qui permet de transmettre des informations de manière efficace et fiable entre les pairs d’un graphique homologue.</span><span class="sxs-lookup"><span data-stu-id="b141d-111">The Peer Infrastructure provides a graphing technology that can pass information efficiently and reliably between peers in a peer graph.</span></span> <span data-ttu-id="b141d-112">L' [API graphique d’homologue](graphing-api.md) garantit que chaque nœud dispose d’une vue cohérente des données dans un graphique.</span><span class="sxs-lookup"><span data-stu-id="b141d-112">The [Peer Graphing API](graphing-api.md) ensures that each node has a consistent view of the data in a graph.</span></span>

<span data-ttu-id="b141d-113">Vous pouvez utiliser l' [API graphique d’homologues](graphing-api.md) pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b141d-113">You can use the [Peer Graphing API](graphing-api.md) to do the following:</span></span>

-   <span data-ttu-id="b141d-114">Créer et gérer des graphiques homologues</span><span class="sxs-lookup"><span data-stu-id="b141d-114">Create and manage peer graphs</span></span>
-   <span data-ttu-id="b141d-115">Énumérer et interagir avec d’autres pairs dans un graphique homologue</span><span class="sxs-lookup"><span data-stu-id="b141d-115">Enumerate and interact with other peers in a peer graph</span></span>
-   <span data-ttu-id="b141d-116">Envoyer des données sous la forme d’un [enregistrement](records.md) à chaque nœud dans un graphique homologue</span><span class="sxs-lookup"><span data-stu-id="b141d-116">Send data in the form of a [record](records.md) to each node in a peer graph</span></span>

## <a name="peer-grouping-api"></a><span data-ttu-id="b141d-117">API de regroupement d’homologues</span><span class="sxs-lookup"><span data-stu-id="b141d-117">Peer Grouping API</span></span>

<span data-ttu-id="b141d-118">L' [API de regroupement d’homologues](grouping-api.md) combine et améliore les API [PNRP](#pnrp-namespace-provider-api) et [graphique](#peer-graphing-api) de l’homologue, et ajoute les deux composants suivants :</span><span class="sxs-lookup"><span data-stu-id="b141d-118">The [Peer Grouping API](grouping-api.md) combines and enhances the Peer [PNRP](#pnrp-namespace-provider-api) and [Graphing](#peer-graphing-api) APIs, and adds the following two components:</span></span>

-   <span data-ttu-id="b141d-119">Couche de multiplexage qui permet à plusieurs applications s’exécutant sur une entité homologue de se connecter à un groupe</span><span class="sxs-lookup"><span data-stu-id="b141d-119">A multiplexing layer that allows multiple applications running on one peer entity to connect to a group</span></span>
-   <span data-ttu-id="b141d-120">Un modèle de sécurité spécifique qui garantit que seuls les homologues invités à un groupe peuvent se connecter au groupe tout au long de la durée de vie du groupe.</span><span class="sxs-lookup"><span data-stu-id="b141d-120">A specific security model that ensures only peers invited to a group can connect to the group through the lifetime of the group</span></span>

<span data-ttu-id="b141d-121">Vous pouvez utiliser l’API de regroupement d’homologues pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b141d-121">You can use the Peer Grouping API to do the following:</span></span>

-   <span data-ttu-id="b141d-122">Créer et gérer des groupes homologues sécurisés</span><span class="sxs-lookup"><span data-stu-id="b141d-122">Create and manage secure peer groups</span></span>
-   <span data-ttu-id="b141d-123">Énumérer et interagir avec d’autres pairs dans un groupe</span><span class="sxs-lookup"><span data-stu-id="b141d-123">Enumerate and interact with other peers in a group</span></span>
-   <span data-ttu-id="b141d-124">Envoyer des données sous la forme d’un [enregistrement](records.md) à chaque nœud dans un groupe homologue</span><span class="sxs-lookup"><span data-stu-id="b141d-124">Send data in the form of a [record](records.md) to each node in a peer group</span></span>

## <a name="peer-identity-manager-api"></a><span data-ttu-id="b141d-125">API du gestionnaire d’identités homologues</span><span class="sxs-lookup"><span data-stu-id="b141d-125">Peer Identity Manager API</span></span>

<span data-ttu-id="b141d-126">À l’aide de l' [API du gestionnaire d’identités homologues](identity-manager-api.md) , vous pouvez créer des [noms d’homologues](peer-names.md) sécurisés que PNRP peut utiliser pour s’assurer qu’une personne publiant un nom possède officiellement le nom.</span><span class="sxs-lookup"><span data-stu-id="b141d-126">By using the [Peer Identity Manager API](identity-manager-api.md) you can create secure [peer names](peer-names.md) that PNRP can use to ensure that a person publishing a name officially owns the name.</span></span> <span data-ttu-id="b141d-127">Les noms d’homologues sont également appelés identités, et ils sont utilisés dans l’API de regroupement d’homologues pour identifier les individus d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="b141d-127">Peer names are also called identities, and they are used in the Peer Grouping API to identify the individuals in a group.</span></span>

<span data-ttu-id="b141d-128">Vous pouvez utiliser l' [API du gestionnaire d’identités homologues](identity-manager-api.md) pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b141d-128">You can use the [Peer Identity Manager API](identity-manager-api.md) to do the following:</span></span>

-   <span data-ttu-id="b141d-129">Créer, énumérer et gérer des identités d’homologue.</span><span class="sxs-lookup"><span data-stu-id="b141d-129">Create, enumerate, and manage peer identities.</span></span>

## <a name="pnrp-namespace-provider-api"></a><span data-ttu-id="b141d-130">API du fournisseur d’espace de noms PNRP</span><span class="sxs-lookup"><span data-stu-id="b141d-130">PNRP Namespace Provider API</span></span>

<span data-ttu-id="b141d-131">L’infrastructure homologue fournit une technologie de résolution de noms sans serveur appelée [API du fournisseur d’espace de noms PNRP](pnrp-namespace-provider-api.md).</span><span class="sxs-lookup"><span data-stu-id="b141d-131">The Peer Infrastructure provides a serverless name resolution technology called the [PNRP Namespace Provider API](pnrp-namespace-provider-api.md).</span></span> <span data-ttu-id="b141d-132">À l’aide de l’API du fournisseur d’espace de noms PNRP de Winsock 2, un homologue, un service, un appareil informatique et un point de terminaison de groupe pair peuvent gérer, inscrire, désinscrire et résoudre un autre point de terminaison dans un [Cloud](clouds.md)PNRP.</span><span class="sxs-lookup"><span data-stu-id="b141d-132">By using the Winsock 2 PNRP Namespace Provider API, a peer, service, computing device, and peer group endpoint can manage, register, unregister, and resolve another endpoint in a PNRP [cloud](clouds.md).</span></span>

> [!Note]  
> <span data-ttu-id="b141d-133">PNRP est un acronyme pour le protocole PNRP ( **Peer Name Resolution Protocol**).</span><span class="sxs-lookup"><span data-stu-id="b141d-133">PNRP is an acronym for **peer name resolution protocol**.</span></span>

 

 

 



