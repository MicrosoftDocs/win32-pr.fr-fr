---
description: Création de topologies à l’aide de TopoEdit
ms.assetid: 04173f3d-3722-48ee-a6fb-9cdb2a897a33
title: Création de topologies à l’aide de TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92758911113c7500cb13fa814d07321435fafeb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111883"
---
# <a name="building-topologies-by-using-topoedit"></a><span data-ttu-id="bc2c6-103">Création de topologies à l’aide de TopoEdit</span><span class="sxs-lookup"><span data-stu-id="bc2c6-103">Building Topologies by Using TopoEdit</span></span>

<span data-ttu-id="bc2c6-104">Une topologie doit avoir les trois nœuds suivants :</span><span class="sxs-lookup"><span data-stu-id="bc2c6-104">A topology must have the following three nodes:</span></span>

-   <span data-ttu-id="bc2c6-105">Nœud source : flux d’un fichier multimédia, qui sont utilisés comme source pour la topologie.</span><span class="sxs-lookup"><span data-stu-id="bc2c6-105">Source node: The streams from a media file, which are used as a source for the topology.</span></span>
-   <span data-ttu-id="bc2c6-106">Nœud de transformation : une transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="bc2c6-106">Transform node: A Media Foundation transform (MFT).</span></span> <span data-ttu-id="bc2c6-107">Ces nœuds sont généralement des encodeurs, des décodeurs et des effets pour la topologie.</span><span class="sxs-lookup"><span data-stu-id="bc2c6-107">These nodes are usually encoders, decoders, and effects for the topology.</span></span>
-   <span data-ttu-id="bc2c6-108">Nœud de sortie : récepteur de flux qui transmet les données multimédia, les images vidéo ou les flux audio à la session multimédia pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="bc2c6-108">Output node: The stream sink that passes the media data, video frames, or audio streams to the Media Session for playback.</span></span>

<span data-ttu-id="bc2c6-109">Pour plus d’informations sur la structure de la topologie, consultez [à propos des topologies](about-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="bc2c6-109">For information about topology structure, see [About Topologies](about-topologies.md).</span></span>

<span data-ttu-id="bc2c6-110">Pour créer une topologie, vous devez ajouter les nœuds, connecter les nœuds et résoudre la topologie de manière à ce qu’elle puisse être lue.</span><span class="sxs-lookup"><span data-stu-id="bc2c6-110">To build a topology, you must add the nodes, connect the nodes, and resolve the topology so that it can be played.</span></span>

<span data-ttu-id="bc2c6-111">Les nœuds de topologie sont affichés sous forme de zones, avec un texte affichant le nom du nœud.</span><span class="sxs-lookup"><span data-stu-id="bc2c6-111">Topology nodes are displayed as boxes, with text showing the name of the node.</span></span> <span data-ttu-id="bc2c6-112">Les zones vertes représentent les nœuds ajoutés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bc2c6-112">Green boxes represent the nodes that are added by the user.</span></span> <span data-ttu-id="bc2c6-113">Quand une topologie est résolue, TopoEdit peut ajouter automatiquement des nœuds de transformation à la topologie.</span><span class="sxs-lookup"><span data-stu-id="bc2c6-113">When a topology is resolved, TopoEdit can add transform nodes to the topology automatically.</span></span> <span data-ttu-id="bc2c6-114">Celles-ci apparaissent sous forme de zones bleues dans le **volet Topology**.</span><span class="sxs-lookup"><span data-stu-id="bc2c6-114">These appear as blue boxes on the **Topology Pane**.</span></span>

<span data-ttu-id="bc2c6-115">Les entrées et sorties de topologie sont représentées par des carrés noirs le long du bord du nœud.</span><span class="sxs-lookup"><span data-stu-id="bc2c6-115">Topology inputs and outputs are represented by as black squares along the edge of the node.</span></span> <span data-ttu-id="bc2c6-116">L' *entrée de nœud* s’affiche sur le côté gauche du nœud, et la *sortie du nœud* se trouve à droite du nœud.</span><span class="sxs-lookup"><span data-stu-id="bc2c6-116">The *node input* is shown on the left side of the node, and the *node output* is on the right side of the node.</span></span>

<span data-ttu-id="bc2c6-117">Les nœuds de topologie sont connectés via une *connexion de nœud* qui s’affiche sous la forme d’une ligne noire connectant l’entrée de nœud d’un nœud à la sortie de nœud d’un autre nœud.</span><span class="sxs-lookup"><span data-stu-id="bc2c6-117">The topology nodes are connected through a *node connection* that appears as a black line connecting the node input of one node to the node output of another node.</span></span>

<span data-ttu-id="bc2c6-118">L’illustration suivante montre une topologie connectée pour une source audio.</span><span class="sxs-lookup"><span data-stu-id="bc2c6-118">The following illustration shows a connected topology for an audio source.</span></span>

![Illustration montrant les connexions du nœud source, à deux nœuds de transformation, puis au nœud de sortie](images/e94b4cce-aa8a-497f-94c2-cc9dace17291.gif)

<span data-ttu-id="bc2c6-120">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="bc2c6-120">This section contains the following topics:</span></span>



| <span data-ttu-id="bc2c6-121">Rubrique</span><span class="sxs-lookup"><span data-stu-id="bc2c6-121">Topic</span></span>                                                                                          | <span data-ttu-id="bc2c6-122">Description</span><span class="sxs-lookup"><span data-stu-id="bc2c6-122">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="bc2c6-123">Ajout de nœuds sources avec TopoEdit</span><span class="sxs-lookup"><span data-stu-id="bc2c6-123">Adding Source Nodes with TopoEdit</span></span>](adding-source-nodes-with-topoedit.md)                     | <span data-ttu-id="bc2c6-124">Décrit le processus d’ajout de nœuds sources à une topologie.</span><span class="sxs-lookup"><span data-stu-id="bc2c6-124">Describes the process of adding source nodes to a topology.</span></span>    |
| [<span data-ttu-id="bc2c6-125">Ajout de nœuds de transformation avec TopoEdit</span><span class="sxs-lookup"><span data-stu-id="bc2c6-125">Adding Transform Nodes with TopoEdit</span></span>](adding-transform-nodes-with-topoedit.md)               | <span data-ttu-id="bc2c6-126">Décrit le processus d’ajout de nœuds de transformation à une topologie.</span><span class="sxs-lookup"><span data-stu-id="bc2c6-126">Describes the process of adding transform nodes to a topology.</span></span> |
| [<span data-ttu-id="bc2c6-127">Ajout de nœuds de sortie avec TopoEdit</span><span class="sxs-lookup"><span data-stu-id="bc2c6-127">Adding Output Nodes with TopoEdit</span></span>](adding-output-nodes-with-topoedit.md)                     | <span data-ttu-id="bc2c6-128">Décrit le processus d’ajout de nœuds de sortie à une topologie.</span><span class="sxs-lookup"><span data-stu-id="bc2c6-128">Describes the process of adding output nodes to a topology.</span></span>    |
| [<span data-ttu-id="bc2c6-129">Connexion et déconnexion des nœuds de topologie</span><span class="sxs-lookup"><span data-stu-id="bc2c6-129">Connecting and Disconnecting Topology Nodes</span></span>](connecting-and-disconnecting-topology-nodes.md) | <span data-ttu-id="bc2c6-130">Décrit le processus de connexion de deux nœuds.</span><span class="sxs-lookup"><span data-stu-id="bc2c6-130">Describes the process of connecting two nodes.</span></span>                 |
| [<span data-ttu-id="bc2c6-131">Résolution d’une topologie avec TopoEdit</span><span class="sxs-lookup"><span data-stu-id="bc2c6-131">Resolving a Topology with TopoEdit</span></span>](resolving-a-topology-with-topoedit.md)                   | <span data-ttu-id="bc2c6-132">Décrit le processus de résolution de la topologie.</span><span class="sxs-lookup"><span data-stu-id="bc2c6-132">Describes the process of topology resolution.</span></span>                  |



 

## <a name="related-topics"></a><span data-ttu-id="bc2c6-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc2c6-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc2c6-134">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="bc2c6-134">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



