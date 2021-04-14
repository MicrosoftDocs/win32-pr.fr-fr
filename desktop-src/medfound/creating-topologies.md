---
description: Création de topologies
ms.assetid: afd1e646-9bb6-4265-a225-6aaaf1a7bb2a
title: Création de topologies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a9ec738c82ea2b85bcae7d4c05627b81ad939db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393295"
---
# <a name="creating-topologies"></a><span data-ttu-id="c31cf-103">Création de topologies</span><span class="sxs-lookup"><span data-stu-id="c31cf-103">Creating Topologies</span></span>

<span data-ttu-id="c31cf-104">Cette section décrit quelques-unes des procédures générales pour la création d’une topologie.</span><span class="sxs-lookup"><span data-stu-id="c31cf-104">This section describes some of the general procedures for creating a topology.</span></span>

<span data-ttu-id="c31cf-105">Les étapes générales de la création d’une topologie sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="c31cf-105">The general steps for creating a topology are as follows:</span></span>

1.  <span data-ttu-id="c31cf-106">Créez un nouvel objet topologique en appelant [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span><span class="sxs-lookup"><span data-stu-id="c31cf-106">Create a new topology object by calling [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span></span> <span data-ttu-id="c31cf-107">Cette fonction retourne un pointeur vers l’interface [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) de la topologie.</span><span class="sxs-lookup"><span data-stu-id="c31cf-107">This function returns a pointer to the topology's [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface.</span></span>

2.  <span data-ttu-id="c31cf-108">Au départ, la topologie ne contient aucun nœud.</span><span class="sxs-lookup"><span data-stu-id="c31cf-108">Initially, the topology does not contain any nodes.</span></span> <span data-ttu-id="c31cf-109">Pour créer des nœuds pour la topologie, appelez [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode).</span><span class="sxs-lookup"><span data-stu-id="c31cf-109">To create nodes for the topology, call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode).</span></span> <span data-ttu-id="c31cf-110">Cette fonction retourne un pointeur vers l’interface [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) du nœud.</span><span class="sxs-lookup"><span data-stu-id="c31cf-110">This function returns a pointer to the node's [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) interface.</span></span> <span data-ttu-id="c31cf-111">Vous devez spécifier le type de nœud lorsque vous créez le nœud :</span><span class="sxs-lookup"><span data-stu-id="c31cf-111">You must specify the node type when you create the node:</span></span>

    -   <span data-ttu-id="c31cf-112">Nœud source.</span><span class="sxs-lookup"><span data-stu-id="c31cf-112">Source node.</span></span>

    -   <span data-ttu-id="c31cf-113">Nœud transformer.</span><span class="sxs-lookup"><span data-stu-id="c31cf-113">Transform node.</span></span>

    -   <span data-ttu-id="c31cf-114">Nœud de sortie.</span><span class="sxs-lookup"><span data-stu-id="c31cf-114">Output node.</span></span>

    -   <span data-ttu-id="c31cf-115">Nœud tee.</span><span class="sxs-lookup"><span data-stu-id="c31cf-115">Tee node.</span></span>

3.  <span data-ttu-id="c31cf-116">Initialisez chaque nœud.</span><span class="sxs-lookup"><span data-stu-id="c31cf-116">Initialize each node.</span></span> <span data-ttu-id="c31cf-117">Le processus d’initialisation dépend du type de nœud, comme décrit dans les rubriques qui suivent.</span><span class="sxs-lookup"><span data-stu-id="c31cf-117">The initialization process depends on the node type, as described in the topics that follow.</span></span>

4.  <span data-ttu-id="c31cf-118">Ajoutez chaque nœud à la topologie en appelant [**IMFTopology :: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode).</span><span class="sxs-lookup"><span data-stu-id="c31cf-118">Add each node to the topology by calling [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode).</span></span>

5.  <span data-ttu-id="c31cf-119">Connectez les nœuds.</span><span class="sxs-lookup"><span data-stu-id="c31cf-119">Connect the nodes.</span></span> <span data-ttu-id="c31cf-120">Pour connecter un nœud, appelez [**IMFTopologyNode :: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) sur le nœud amont, puis transmettez un pointeur vers le nœud en aval.</span><span class="sxs-lookup"><span data-stu-id="c31cf-120">To connect a node, call [**IMFTopologyNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) on the upstream node, and pass in a pointer to the downstream node.</span></span>

<span data-ttu-id="c31cf-121">Les rubriques suivantes fournissent les étapes spécifiques pour chaque type de nœud.</span><span class="sxs-lookup"><span data-stu-id="c31cf-121">The following topics give the specific steps for each node type.</span></span>



| <span data-ttu-id="c31cf-122">Rubrique</span><span class="sxs-lookup"><span data-stu-id="c31cf-122">Topic</span></span>                                                    | <span data-ttu-id="c31cf-123">Description</span><span class="sxs-lookup"><span data-stu-id="c31cf-123">Description</span></span>                     |
|----------------------------------------------------------|---------------------------------|
| [<span data-ttu-id="c31cf-124">Création de nœuds sources</span><span class="sxs-lookup"><span data-stu-id="c31cf-124">Creating Source Nodes</span></span>](creating-source-nodes.md)       | <span data-ttu-id="c31cf-125">Comment créer un nœud source.</span><span class="sxs-lookup"><span data-stu-id="c31cf-125">How to create a source node.</span></span>    |
| [<span data-ttu-id="c31cf-126">Création de nœuds de transformation</span><span class="sxs-lookup"><span data-stu-id="c31cf-126">Creating Transform Nodes</span></span>](creating-transform-nodes.md) | <span data-ttu-id="c31cf-127">Comment créer un nœud de transformation.</span><span class="sxs-lookup"><span data-stu-id="c31cf-127">How to create a transform node.</span></span> |
| [<span data-ttu-id="c31cf-128">Création de nœuds de sortie</span><span class="sxs-lookup"><span data-stu-id="c31cf-128">Creating Output Nodes</span></span>](creating-output-nodes.md)       | <span data-ttu-id="c31cf-129">Comment créer un nœud de sortie.</span><span class="sxs-lookup"><span data-stu-id="c31cf-129">How to create an output node.</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="c31cf-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c31cf-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c31cf-131">Topologies</span><span class="sxs-lookup"><span data-stu-id="c31cf-131">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



