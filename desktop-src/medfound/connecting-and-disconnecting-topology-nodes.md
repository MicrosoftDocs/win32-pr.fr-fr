---
description: Connexion et déconnexion des nœuds de topologie
ms.assetid: b2f70989-f0a8-4a11-baeb-18f026afaeab
title: Connexion et déconnexion des nœuds de topologie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08057eba74314ae6b87da418b743a089506a3b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536953"
---
# <a name="connecting-and-disconnecting-topology-nodes"></a><span data-ttu-id="36f76-103">Connexion et déconnexion des nœuds de topologie</span><span class="sxs-lookup"><span data-stu-id="36f76-103">Connecting and Disconnecting Topology Nodes</span></span>

<span data-ttu-id="36f76-104">Pour qu’une topologie soit fonctionnelle, le nœud source et le nœud de sortie doivent être connectés.</span><span class="sxs-lookup"><span data-stu-id="36f76-104">For a topology to be functional, the source node and the output node must be connected.</span></span> <span data-ttu-id="36f76-105">Pour connecter deux nœuds de topologie, faites glisser la sortie de nœud d’un nœud vers l’entrée de nœud de l’autre nœud.</span><span class="sxs-lookup"><span data-stu-id="36f76-105">To connect two topology nodes, drag the node output of one node to the node input of the other node.</span></span> <span data-ttu-id="36f76-106">TopoEdit affiche la connexion de nœud sous la forme d’une ligne noire.</span><span class="sxs-lookup"><span data-stu-id="36f76-106">TopoEdit displays the node connection as a black line.</span></span> <span data-ttu-id="36f76-107">Cela équivaut à connecter des nœuds de topologie en appelant la méthode [**IMFTopologyNode :: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) .</span><span class="sxs-lookup"><span data-stu-id="36f76-107">This is equivalent to connecting topology nodes by calling the [**IMFTopologyNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) method.</span></span>

<span data-ttu-id="36f76-108">La topologie peut être résolue uniquement si la connexion au nœud est valide ; autrement dit, si les types de média des deux nœuds sont compatibles.</span><span class="sxs-lookup"><span data-stu-id="36f76-108">The topology can be resolved only if the node connection is valid; that is, if the media types of the two nodes are compatible.</span></span> <span data-ttu-id="36f76-109">Pour plus d’informations sur la résolution des topologies, consultez [résolution d’une topologie à l’aide de TopoEdit](resolving-a-topology-with-topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="36f76-109">For information about resolving topologies, see [Resolving a Topology with TopoEdit](resolving-a-topology-with-topoedit.md).</span></span>

<span data-ttu-id="36f76-110">Si vous tentez d’établir une connexion à partir d’un nœud qui est déjà connecté, la nouvelle connexion de nœud remplace l’ancienne connexion de nœud.</span><span class="sxs-lookup"><span data-stu-id="36f76-110">If you attempt to make a connection from a node that is already connected, the new node connection replaces the old node connection.</span></span>

<span data-ttu-id="36f76-111">Pour supprimer une connexion, sélectionnez la connexion de nœud et appuyez sur la touche SUPPR ou sélectionnez **supprimer** dans le menu **Topology (topologie** ).</span><span class="sxs-lookup"><span data-stu-id="36f76-111">To delete a connection, select the node connection and press the DELETE key or select **Delete** from the **Topology** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36f76-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="36f76-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36f76-113">Création de topologies à l’aide de TopoEdit</span><span class="sxs-lookup"><span data-stu-id="36f76-113">Building Topologies by Using TopoEdit</span></span>](building-topologies-by-using-topoedit.md)
</dt> <dt>

[<span data-ttu-id="36f76-114">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="36f76-114">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



