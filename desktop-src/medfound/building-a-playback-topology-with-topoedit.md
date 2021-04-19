---
description: Génération d’une topologie de lecture avec TopoEdit
ms.assetid: 4d4c4ff9-dad1-4c79-a44a-2ad20f1bbca0
title: Génération d’une topologie de lecture avec TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f942984b3ba56ef1288566cee80e7d30026de155
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "106539781"
---
# <a name="building-a-playback-topology-with-topoedit"></a><span data-ttu-id="45d57-103">Génération d’une topologie de lecture avec TopoEdit</span><span class="sxs-lookup"><span data-stu-id="45d57-103">Building a Playback Topology with TopoEdit</span></span>

<span data-ttu-id="45d57-104">TopoEdit peut créer une topologie de lecture pour un fichier de média local en ajoutant et en connectant automatiquement les nœuds source, de transformation et de sortie.</span><span class="sxs-lookup"><span data-stu-id="45d57-104">TopoEdit can build a playback topology for a local media file by automatically adding and connecting the source, transform, and output nodes.</span></span> <span data-ttu-id="45d57-105">TopoEdit ne résout pas automatiquement la topologie.</span><span class="sxs-lookup"><span data-stu-id="45d57-105">TopoEdit does not automatically resolve the topology.</span></span> <span data-ttu-id="45d57-106">Pour lire la topologie, résolvez-la, puis utilisez les contrôles de transport.</span><span class="sxs-lookup"><span data-stu-id="45d57-106">To play the topology, resolve it and then use the transport controls.</span></span>

## <a name="to-build-and-play-a-topology-for-a-media-file"></a><span data-ttu-id="45d57-107">Pour générer et lire une topologie pour un fichier multimédia</span><span class="sxs-lookup"><span data-stu-id="45d57-107">To build and play a topology for a media file</span></span>

1.  <span data-ttu-id="45d57-108">Dans le menu **fichier** , cliquez sur **fichier de rendu**.</span><span class="sxs-lookup"><span data-stu-id="45d57-108">On the **File** menu, click **Render File**.</span></span>

    <span data-ttu-id="45d57-109">La boîte de dialogue **Sélectionner la source du média** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="45d57-109">This opens the **Select Media Source** dialog box.</span></span>

2.  <span data-ttu-id="45d57-110">Accédez au dossier où se trouve le fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="45d57-110">Navigate to the folder where the media file is located.</span></span>
3.  <span data-ttu-id="45d57-111">Dans le champ **nom du fichier :** , entrez le nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="45d57-111">In the **File name:** field, enter the name of the file.</span></span>
4.  <span data-ttu-id="45d57-112">Cliquez sur **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="45d57-112">Click **Open**.</span></span>

    <span data-ttu-id="45d57-113">Le **volet topologie** affiche la topologie connectée.</span><span class="sxs-lookup"><span data-stu-id="45d57-113">The **Topology Pane** shows the connected topology.</span></span> <span data-ttu-id="45d57-114">En interne, TopoEdit effectue les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="45d57-114">Internally, TopoEdit performs the following tasks:</span></span>

    -   <span data-ttu-id="45d57-115">Énumère les flux dans le fichier multimédia et crée les nœuds sources.</span><span class="sxs-lookup"><span data-stu-id="45d57-115">Enumerates the streams in the media file and creates the source nodes.</span></span>
    -   <span data-ttu-id="45d57-116">En fonction du type de média des nœuds sources, ajoute des nœuds de transformation, tels que des décodeurs.</span><span class="sxs-lookup"><span data-stu-id="45d57-116">Depending on the media type of the source nodes, adds transform nodes, such as decoders.</span></span>
    -   <span data-ttu-id="45d57-117">Ajoute le récepteur de diffusion audio en continu (SAR) pour le flux audio et le récepteur Video Enhancer (EVR) pour le flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="45d57-117">Adds the Streaming Audio Renderer (SAR) sink for audio stream and the enhanced video renderer (EVR) sink for the video stream.</span></span>
    -   <span data-ttu-id="45d57-118">Connecte les entrées de nœud et les sorties de nœud.</span><span class="sxs-lookup"><span data-stu-id="45d57-118">Connects the node inputs and the node outputs.</span></span>

5.  <span data-ttu-id="45d57-119">Dans le menu **Topology (topologie** ), cliquez sur **Resolve Topology**.</span><span class="sxs-lookup"><span data-stu-id="45d57-119">On the **Topology** menu, click **Resolve Topology**.</span></span>
6.  <span data-ttu-id="45d57-120">Cliquez sur le bouton **lecture** dans la barre d’outils pour lire la topologie.</span><span class="sxs-lookup"><span data-stu-id="45d57-120">Click the **Play** button on the toolbar to play the topology.</span></span> L’illustration suivante montre le  bouton lecture :::image type="icon" source="images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg"::: .

## <a name="related-topics"></a><span data-ttu-id="45d57-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="45d57-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45d57-123">Contrôles de lecture dans TopoEdit</span><span class="sxs-lookup"><span data-stu-id="45d57-123">Playback Controls in TopoEdit</span></span>](playback-controls-in-topoedit.md)
</dt> <dt>

[<span data-ttu-id="45d57-124">Résolution d’une topologie avec TopoEdit</span><span class="sxs-lookup"><span data-stu-id="45d57-124">Resolving a Topology with TopoEdit</span></span>](resolving-a-topology-with-topoedit.md)
</dt> <dt>

[<span data-ttu-id="45d57-125">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="45d57-125">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



