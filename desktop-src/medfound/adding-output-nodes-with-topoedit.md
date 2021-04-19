---
description: Ajout de nœuds de sortie avec TopoEdit
ms.assetid: 23d60fc7-547b-4ef5-b334-5f1b38e58e92
title: Ajout de nœuds de sortie avec TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84dc30631332e8138b35e4bbc0ccde75ec9b0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515230"
---
# <a name="adding-output-nodes-with-topoedit"></a><span data-ttu-id="b2c84-103">Ajout de nœuds de sortie avec TopoEdit</span><span class="sxs-lookup"><span data-stu-id="b2c84-103">Adding Output Nodes with TopoEdit</span></span>

<span data-ttu-id="b2c84-104">Dans une topologie, un nœud de sortie représente un récepteur multimédia qui reçoit des données multimédia à partir d’un nœud de transformation et le présente pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="b2c84-104">In a topology, an output node represents a media sink that receives media data from a transform node and presents it for playback.</span></span> <span data-ttu-id="b2c84-105">Le type de nœud de sortie dépend du type de média du nœud source.</span><span class="sxs-lookup"><span data-stu-id="b2c84-105">The type of output node depends on the media type of the source node.</span></span>

<span data-ttu-id="b2c84-106">Le tableau suivant présente la commande de menu/barre d’outils permettant d’ajouter un nœud de sortie à la topologie.</span><span class="sxs-lookup"><span data-stu-id="b2c84-106">The following table shows the menu/toolbar command for adding an output node to the topology.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b2c84-107">Type de média source</span><span class="sxs-lookup"><span data-stu-id="b2c84-107">Source media type</span></span></th>
<th><span data-ttu-id="b2c84-108">Menu/commande de barre d’outils</span><span class="sxs-lookup"><span data-stu-id="b2c84-108">Menu/Toolbar Command</span></span></th>
<th><span data-ttu-id="b2c84-109">Description</span><span class="sxs-lookup"><span data-stu-id="b2c84-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b2c84-110">Flux audio</span><span class="sxs-lookup"><span data-stu-id="b2c84-110">Audio stream</span></span></td>
<td><span data-ttu-id="b2c84-111">Dans le menu <strong>Topology (topologie</strong> ), cliquez sur <strong>Add SAR</strong>.</span><span class="sxs-lookup"><span data-stu-id="b2c84-111">On the <strong>Topology</strong> menu, click <strong>Add SAR</strong>.</span></span></td>
<td><span data-ttu-id="b2c84-112">Crée un nœud de sortie pour le convertisseur audio en continu qui lit un flux audio via un périphérique audio tel qu’une carte son.</span><span class="sxs-lookup"><span data-stu-id="b2c84-112">Creates an output node for the Streaming Audio Renderer (SAR) that plays an audio stream through an audio device such as a sound card.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2c84-113">Flux vidéo</span><span class="sxs-lookup"><span data-stu-id="b2c84-113">Video stream</span></span></td>
<td><span data-ttu-id="b2c84-114">Dans le menu <strong>Topology (topologie</strong> ), cliquez sur <strong>Add EVR</strong>.</span><span class="sxs-lookup"><span data-stu-id="b2c84-114">On the <strong>Topology</strong> menu, click <strong>Add EVR</strong>.</span></span></td>
<td><span data-ttu-id="b2c84-115">Crée un nœud de sortie pour le convertisseur vidéo amélioré (EVR) qui affiche des frames pour un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="b2c84-115">Creates an output node for the enhanced video renderer (EVR) that displays frames for a video stream.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b2c84-116">Récepteur multimédia personnalisé</span><span class="sxs-lookup"><span data-stu-id="b2c84-116">Custom media sink</span></span></td>
<td><ol>
<li><span data-ttu-id="b2c84-117">Dans le menu <strong>Topology (topologie</strong> ), cliquez sur <strong>Add Custom Sink</strong>.</span><span class="sxs-lookup"><span data-stu-id="b2c84-117">On the <strong>Topology</strong> menu, click <strong>Add Custom Sink</strong>.</span></span><br/> <span data-ttu-id="b2c84-118">La boîte de dialogue <strong>GUID personnalisé d’entrée</strong> s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="b2c84-118">The <strong>Input Custom GUID</strong> dialog box opens.</span></span><br/></li>
<li><p><span data-ttu-id="b2c84-119">Dans le champ <strong>GUID :</strong> , entrez le GUID de votre récepteur personnalisé que vous souhaitez ajouter à la topologie.</span><span class="sxs-lookup"><span data-stu-id="b2c84-119">In the <strong>GUID:</strong> field, enter the GUID of your custom sink that you want to add to the topology.</span></span><br/></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="b2c84-120">TopoEdit attend le GUID au format &quot; {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} &quot; .</span><span class="sxs-lookup"><span data-stu-id="b2c84-120">TopoEdit expects the GUID in the format &quot;{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}&quot;.</span></span> <span data-ttu-id="b2c84-121">Dans le cas contraire, il ne parvient pas à ajouter le nœud et affiche un &quot; message d’erreur GUID non valide &quot; .</span><span class="sxs-lookup"><span data-stu-id="b2c84-121">Otherwise, it fails to add the node and displays an &quot;Invalid GUID&quot; error message.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="b2c84-122">Cliquez sur <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="b2c84-122">Click <strong>OK</strong>.</span></span><br/></li>
</ol></td>
<td><span data-ttu-id="b2c84-123">Crée un nœud de sortie pour le récepteur de flux pour une source de média personnalisée.</span><span class="sxs-lookup"><span data-stu-id="b2c84-123">Creates an output node for the stream sink for a custom media source.</span></span><br/> <span data-ttu-id="b2c84-124">Le récepteur personnalisé doit prendre en charge <strong>CoCreateInstance</strong> afin que le récepteur puisse être spécifié avec un CLSID.</span><span class="sxs-lookup"><span data-stu-id="b2c84-124">The custom sink must support <strong>CoCreateInstance</strong> so that the sink can be specified with a CLSID.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b2c84-125">TopoEdit crée le nœud de sortie spécifié.</span><span class="sxs-lookup"><span data-stu-id="b2c84-125">TopoEdit creates the specified output node.</span></span> <span data-ttu-id="b2c84-126">Le **volet topologie** affiche le nœud sortie sous la forme d’une zone verte qui indique le nom du récepteur de flux.</span><span class="sxs-lookup"><span data-stu-id="b2c84-126">The **Topology Pane** shows the output node as a green box that shows the name of the stream sink.</span></span>

<span data-ttu-id="b2c84-127">Pour plus d’informations sur l’ajout par programme de nœuds de sortie à l’aide d’API Media Foundation, consultez [création de nœuds de sortie](creating-output-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="b2c84-127">For information about adding output nodes programmatically by using Media Foundation APIs, see [Creating Output Nodes](creating-output-nodes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2c84-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b2c84-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2c84-129">Création de topologies à l’aide de TopoEdit</span><span class="sxs-lookup"><span data-stu-id="b2c84-129">Building Topologies by Using TopoEdit</span></span>](building-topologies-by-using-topoedit.md)
</dt> <dt>

[<span data-ttu-id="b2c84-130">Convertisseur audio de streaming</span><span class="sxs-lookup"><span data-stu-id="b2c84-130">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> <dt>

[<span data-ttu-id="b2c84-131">Convertisseur vidéo amélioré</span><span class="sxs-lookup"><span data-stu-id="b2c84-131">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="b2c84-132">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="b2c84-132">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 




