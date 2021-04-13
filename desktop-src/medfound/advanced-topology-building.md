---
description: Génération de topologie avancée
ms.assetid: 66aa07d8-6756-4d5b-9f0a-24b902da6fa2
title: Génération de topologie avancée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4cc061d4e557dda4ccbb81eabc55e8e1b3e33b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318310"
---
# <a name="advanced-topology-building"></a><span data-ttu-id="505c1-103">Génération de topologie avancée</span><span class="sxs-lookup"><span data-stu-id="505c1-103">Advanced Topology Building</span></span>

<span data-ttu-id="505c1-104">Cette section décrit quelques techniques avancées pour la création de topologies.</span><span class="sxs-lookup"><span data-stu-id="505c1-104">This section describes some advanced techniques for building topologies.</span></span> <span data-ttu-id="505c1-105">Vous pouvez utiliser ces techniques si vous souhaitez davantage de contrôle sur les topologies que vous envoyez à la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="505c1-105">You can use these techniques if you want more control over the topologies that you send to the Media Session.</span></span>

<span data-ttu-id="505c1-106">Étant donné que ces techniques sont destinées à des scénarios qui dépassent la fonctionnalité fournie par le chargeur de topologie standard, un grand nombre des détails dépendent des exigences spécifiques de votre application.</span><span class="sxs-lookup"><span data-stu-id="505c1-106">Because these techniques are intended for scenarios that go beyond the functionality provided by the standard topology loader, many of the details will depend on the particular requirements of your application.</span></span> <span data-ttu-id="505c1-107">Par conséquent, cette section est organisée de façon faible autour des tâches subordonnées plus petites, plutôt que des scénarios complets de bout en bout.</span><span class="sxs-lookup"><span data-stu-id="505c1-107">Therefore, this section is organized loosely around smaller subtasks, rather than complete, end-to-end scenarios.</span></span>

<span data-ttu-id="505c1-108">L’application de lecture classique suit les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="505c1-108">The typical playback application follows these steps:</span></span>

1.  <span data-ttu-id="505c1-109">L’application génère une topologie partielle et la met en file d’attente dans la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="505c1-109">The application builds a partial topology and queues it on the Media Session.</span></span>
2.  <span data-ttu-id="505c1-110">La session multimédia appelle le chargeur de topologie pour résoudre la topologie.</span><span class="sxs-lookup"><span data-stu-id="505c1-110">The Media Session invokes the topology loader to resolve the topology.</span></span>

<span data-ttu-id="505c1-111">Si vous souhaitez aller au-delà des fonctionnalités du chargeur de topologie, il existe trois approches générales :</span><span class="sxs-lookup"><span data-stu-id="505c1-111">If you want to go beyond the capabilities of the topology loader, there are three general approaches:</span></span>

-   <span data-ttu-id="505c1-112">Créez une topologie complète.</span><span class="sxs-lookup"><span data-stu-id="505c1-112">Build a complete topology.</span></span> <span data-ttu-id="505c1-113">Lorsque vous vous connectez à la topologie de la session multimédia, appelez [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) avec l' \_ \_ indicateur nosolution MFSESSION SetTopology.</span><span class="sxs-lookup"><span data-stu-id="505c1-113">When you queue the topology on the Media Session, call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) with the MFSESSION\_SETTOPOLOGY\_NORESOLUTION flag.</span></span> <span data-ttu-id="505c1-114">Cet indicateur empêche la session multimédia d’essayer de résoudre la topologie.</span><span class="sxs-lookup"><span data-stu-id="505c1-114">This flag prevents the Media Session from attempting to resolve the topology.</span></span>

-   <span data-ttu-id="505c1-115">Appelez directement le chargeur de topologie pour résoudre la topologie.</span><span class="sxs-lookup"><span data-stu-id="505c1-115">Directly invoke the topology loader to resolve the topology.</span></span> <span data-ttu-id="505c1-116">Vous pouvez ensuite modifier la topologie complète avant de la mettre en file d’attente dans la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="505c1-116">You can then modify the full topology before queuing it on the Media Session.</span></span>

-   <span data-ttu-id="505c1-117">Implémentez un chargeur de topologie personnalisé.</span><span class="sxs-lookup"><span data-stu-id="505c1-117">Implement a custom topology loader.</span></span> <span data-ttu-id="505c1-118">Avec cette approche, vous mettrez en file d’attente une topologie partielle, mais la session multimédia appelle votre chargeur personnalisé au lieu de l’implémentation de Media Foundation standard.</span><span class="sxs-lookup"><span data-stu-id="505c1-118">With this approach, you queue a partial topology, but the Media Session invokes your custom loader instead of the standard Media Foundation implementation.</span></span> <span data-ttu-id="505c1-119">L’un des avantages de cette approche est que vous pouvez effectuer une génération de topologie personnalisée dans l’environnement protégé.</span><span class="sxs-lookup"><span data-stu-id="505c1-119">One advantage of this approach is that you can perform custom topology building inside the protected environment.</span></span> <span data-ttu-id="505c1-120">(Dans ce cas, toutefois, le chargeur de topologie doit être un composant approuvé.</span><span class="sxs-lookup"><span data-stu-id="505c1-120">(In that case, however, the topology loader must be a trusted component.</span></span> <span data-ttu-id="505c1-121">Pour plus d’informations, consultez [chemin d’accès au média protégé](protected-media-path.md).)</span><span class="sxs-lookup"><span data-stu-id="505c1-121">For more information, see [Protected Media Path](protected-media-path.md).)</span></span>

<span data-ttu-id="505c1-122">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="505c1-122">This section contains the following topics.</span></span>



| <span data-ttu-id="505c1-123">Rubrique</span><span class="sxs-lookup"><span data-stu-id="505c1-123">Topic</span></span>                                                                          | <span data-ttu-id="505c1-124">Description</span><span class="sxs-lookup"><span data-stu-id="505c1-124">Description</span></span>                                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="505c1-125">Chargeurs de topologie personnalisés</span><span class="sxs-lookup"><span data-stu-id="505c1-125">Custom Topology Loaders</span></span>](custom-topology-loaders.md)                         | <span data-ttu-id="505c1-126">Comment fournir une implémentation personnalisée de [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) pour la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="505c1-126">How to provide a custom implementation of [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) for the Media Session.</span></span>          |
| [<span data-ttu-id="505c1-127">Liaison de nœuds de sortie à des récepteurs multimédias</span><span class="sxs-lookup"><span data-stu-id="505c1-127">Binding Output Nodes to Media Sinks</span></span>](binding-output-nodes-to-media-sinks.md) | <span data-ttu-id="505c1-128">Comment préparer les nœuds de sortie dans une topologie si vous utilisez le chargeur de topologie en dehors de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="505c1-128">How to prepare the output nodes in a topology if you are using the topology loader outside of the Media Session.</span></span> |
| [<span data-ttu-id="505c1-129">Ajout d’un décodeur à une topologie</span><span class="sxs-lookup"><span data-stu-id="505c1-129">Adding a Decoder to a Topology</span></span>](adding-a-decoder-to-a-topology.md)           | <span data-ttu-id="505c1-130">Comment sélectionner manuellement un décodeur et l’ajouter à une topologie.</span><span class="sxs-lookup"><span data-stu-id="505c1-130">How to select a decoder manually and add it to a topology.</span></span>                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="505c1-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="505c1-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="505c1-132">Topologies</span><span class="sxs-lookup"><span data-stu-id="505c1-132">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



