---
description: Résolution d’une topologie avec TopoEdit
ms.assetid: da3e2bbc-7c9f-4a15-8842-c1bb00662cd2
title: Résolution d’une topologie avec TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8397e380b19a6f45736c06e859d2a80456aad079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201851"
---
# <a name="resolving-a-topology-with-topoedit"></a><span data-ttu-id="2dd4d-103">Résolution d’une topologie avec TopoEdit</span><span class="sxs-lookup"><span data-stu-id="2dd4d-103">Resolving a Topology with TopoEdit</span></span>

<span data-ttu-id="2dd4d-104">Il existe deux types de topologies :</span><span class="sxs-lookup"><span data-stu-id="2dd4d-104">There are two types of topologies:</span></span>

-   <span data-ttu-id="2dd4d-105">Topologie partielle.</span><span class="sxs-lookup"><span data-stu-id="2dd4d-105">Partial Topology.</span></span> <span data-ttu-id="2dd4d-106">Le nœud source est directement connecté au nœud de sortie.</span><span class="sxs-lookup"><span data-stu-id="2dd4d-106">The source node is connected directly to the output node.</span></span> <span data-ttu-id="2dd4d-107">Dans certains cas, une topologie partielle peut avoir des nœuds de transformation intermédiaires, tels que des effets, mais pas tous.</span><span class="sxs-lookup"><span data-stu-id="2dd4d-107">In some cases, a partial topology can have some intermediate transform nodes, such as effects, but not all.</span></span> <span data-ttu-id="2dd4d-108">Les nœuds de transformation qui sont omis sont généralement des décodeurs ou des MFTs de conversion de format, tels que des convertisseurs de couleurs et des échantillonnages audio.</span><span class="sxs-lookup"><span data-stu-id="2dd4d-108">The transform nodes that are omitted are typically decoders or format conversion MFTs, such as color converters and audio resamplers.</span></span>

-   <span data-ttu-id="2dd4d-109">Topologie complète.</span><span class="sxs-lookup"><span data-stu-id="2dd4d-109">Full Topology.</span></span> <span data-ttu-id="2dd4d-110">Le nœud source est connecté au nœud de sortie via un nœud de transformation.</span><span class="sxs-lookup"><span data-stu-id="2dd4d-110">The source node is connected to the output node through a transform node.</span></span> <span data-ttu-id="2dd4d-111">Ce type de topologie doit avoir chaque nœud pour traiter les données.</span><span class="sxs-lookup"><span data-stu-id="2dd4d-111">This type of topology must have every node to process data.</span></span>

<span data-ttu-id="2dd4d-112">TopoEdit peut uniquement lire des topologies complètes.</span><span class="sxs-lookup"><span data-stu-id="2dd4d-112">TopoEdit can only play full topologies.</span></span> <span data-ttu-id="2dd4d-113">TopoEdit utilise l’objet de chargeur de topologie, fourni par Media Foundation, pour convertir une topologie partielle en une topologie complète en insérant les transformations requises.</span><span class="sxs-lookup"><span data-stu-id="2dd4d-113">TopoEdit uses the topology loader object, provided by Media Foundation, to convert a partial topology into a full topology by inserting the required transforms.</span></span> <span data-ttu-id="2dd4d-114">Le processus de création d’une topologie complète est appelé résolution d’une topologie.</span><span class="sxs-lookup"><span data-stu-id="2dd4d-114">The process of creating a full topology is called resolving a topology.</span></span>

<span data-ttu-id="2dd4d-115">Pour plus d’informations sur les types de topologies, consultez la section topologies partielles dans [à propos des topologies](about-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="2dd4d-115">For information about topology types, see the Partial Topologies section in [About Topologies](about-topologies.md).</span></span>

<span data-ttu-id="2dd4d-116">Avant de résoudre une topologie, assurez-vous que :</span><span class="sxs-lookup"><span data-stu-id="2dd4d-116">Before you resolve a topology ensure that:</span></span>

-   <span data-ttu-id="2dd4d-117">La topologie contient un nœud source et un nœud de sortie.</span><span class="sxs-lookup"><span data-stu-id="2dd4d-117">The topology contains a source node and an output node.</span></span>

-   <span data-ttu-id="2dd4d-118">Les nœuds source et de sortie sont connectés par une connexion de nœud valide.</span><span class="sxs-lookup"><span data-stu-id="2dd4d-118">The source and the output nodes are connected by a valid node connection.</span></span> <span data-ttu-id="2dd4d-119">Pendant la résolution de la topologie, le chargeur de topologie vérifie la compatibilité du type de média des nœuds.</span><span class="sxs-lookup"><span data-stu-id="2dd4d-119">During topology resolution, the topology loader checks the media type of the nodes for compatibility.</span></span> <span data-ttu-id="2dd4d-120">S’il existe une connexion de nœud non valide, le processus échoue et un message d’erreur s’affiche.</span><span class="sxs-lookup"><span data-stu-id="2dd4d-120">If an invalid node connection exists, then the process fails and an error message is displayed.</span></span>

<span data-ttu-id="2dd4d-121">Pour résoudre une topologie, dans le menu **topologie** , cliquez sur **résoudre** la topologie.</span><span class="sxs-lookup"><span data-stu-id="2dd4d-121">To resolve a topology, from the **Topology** menu, click **Resolve Topology**.</span></span>

<span data-ttu-id="2dd4d-122">La barre d’outils indique l’état de la topologie : **\[ résolu \]** ou **\[ non résolu \]**.</span><span class="sxs-lookup"><span data-stu-id="2dd4d-122">The toolbar indicates the topology status: **\[Resolved\]** or **\[Not Resolved\]**.</span></span>

<span data-ttu-id="2dd4d-123">Si TopoEdit résout correctement une topologie, l’état de la **topologie** est défini sur **\[ résolu \]** et les contrôles de lecture sont activés.</span><span class="sxs-lookup"><span data-stu-id="2dd4d-123">If TopoEdit resolves a topology successfully, **Topology Status** is set to **\[Resolved\]** and the playback controls are enabled.</span></span>

<span data-ttu-id="2dd4d-124">Chaque fois que vous apportez des modifications à la topologie, l’état de la **topologie** est défini sur **\[ non résolu \]** , ce qui indique qu’il doit être résolu à nouveau.</span><span class="sxs-lookup"><span data-stu-id="2dd4d-124">Each time you make changes to the topology, **Topology Status** is set to **\[Not Resolved\]** which indicates that it must be resolved again.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2dd4d-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2dd4d-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2dd4d-126">Création de topologies à l’aide de TopoEdit</span><span class="sxs-lookup"><span data-stu-id="2dd4d-126">Building Topologies by Using TopoEdit</span></span>](building-topologies-by-using-topoedit.md)
</dt> <dt>

[<span data-ttu-id="2dd4d-127">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="2dd4d-127">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



