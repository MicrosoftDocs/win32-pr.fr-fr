---
description: Indexeur ASF
ms.assetid: 3f95b0ac-d70f-4bc2-8524-c7de1df34afa
title: Indexeur ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c729b547339149ee578a90283c570ec8460b0c57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544603"
---
# <a name="asf-indexer"></a><span data-ttu-id="2c70c-103">Indexeur ASF</span><span class="sxs-lookup"><span data-stu-id="2c70c-103">ASF Indexer</span></span>

<span data-ttu-id="2c70c-104">L' *indexeur* ASF est un composant de couche WMContainer utilisé pour lire ou écrire des objets index dans un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="2c70c-104">The ASF *indexer* is a WMContainer layer component that is used to read or write Index Objects in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="2c70c-105">Pour plus d’informations sur la structure d’un fichier ASF, consultez [structure des fichiers ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="2c70c-105">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="2c70c-106">Une application peut utiliser l’indexeur pour effectuer une recherche en fonction de l’heure de la présentation ou pour générer de nouvelles entrées d’index pour un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="2c70c-106">An application can use the indexer to perform seeking based on presentation time or to generate new index entries for an ASF file.</span></span> <span data-ttu-id="2c70c-107">L’indexeur ASF implémente l’interface [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) .</span><span class="sxs-lookup"><span data-stu-id="2c70c-107">The ASF indexer implements the [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) interface.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2c70c-108">Type d’index</span><span class="sxs-lookup"><span data-stu-id="2c70c-108">Index type</span></span></th>
<th><span data-ttu-id="2c70c-109">Description</span><span class="sxs-lookup"><span data-stu-id="2c70c-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2c70c-110">Index basé sur l’heure de la présentation</span><span class="sxs-lookup"><span data-stu-id="2c70c-110">Presentation time-based Index</span></span></td>
<td><span data-ttu-id="2c70c-111">Fournit une indexation basée sur la durée de la présentation pour les flux audio et vidéo dans des blocs d’index afin de rendre l’indexation plus efficace.</span><span class="sxs-lookup"><span data-stu-id="2c70c-111">Provides presentation time-based indexing for audio and video streams in index blocks to make indexing more space efficient.</span></span> <span data-ttu-id="2c70c-112">Chaque bloc d’index fait référence à des entrées d’index qui contiennent un décalage d’octets.</span><span class="sxs-lookup"><span data-stu-id="2c70c-112">Each index block references index entries that contain a byte offset.</span></span> <br/> <span data-ttu-id="2c70c-113">Le décalage correspond à la position du paquet de données en cours de recherche, par rapport au début de l’objet de données ASF.</span><span class="sxs-lookup"><span data-stu-id="2c70c-113">The offset is the position of the data packet being seeked, relative to the start of the ASF Data Object.</span></span><br/> <span data-ttu-id="2c70c-114">GUID_NULL doit être utilisé comme type de GUID pour l’identificateur d’index.</span><span class="sxs-lookup"><span data-stu-id="2c70c-114">GUID_NULL must be used as the GUID type for the index identifier.</span></span> <span data-ttu-id="2c70c-115">Pour plus d’informations, consultez <a href="using-the-indexer-to-write-a-new-index.md">utilisation de l’indexeur pour écrire un nouvel index</a>.</span><span class="sxs-lookup"><span data-stu-id="2c70c-115">For more information; see <a href="using-the-indexer-to-write-a-new-index.md">Using the Indexer to Write a New Index</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c70c-116">Index du code temporel</span><span class="sxs-lookup"><span data-stu-id="2c70c-116">Timecode Index</span></span></td>
<td><span data-ttu-id="2c70c-117">Facilite la recherche par code temporel dans les flux qui contiennent des métadonnées de code temporel.</span><span class="sxs-lookup"><span data-stu-id="2c70c-117">Facilitates seeking by timecode in streams which contain timecode metadata.</span></span> <span data-ttu-id="2c70c-118">Les codes temporels sont conformes à un format SMPTE (<em>heures : minutes : secondes : images</em>).</span><span class="sxs-lookup"><span data-stu-id="2c70c-118">The timecodes conform to a SMPTE format (<em>Hours:Minutes:Seconds:Frames</em>).</span></span> <span data-ttu-id="2c70c-119">Chaque bloc d’index fait référence à des entrées d’index qui contiennent un décalage d’octets.</span><span class="sxs-lookup"><span data-stu-id="2c70c-119">Each index block references index entries that contain a byte offset.</span></span> <br/> <span data-ttu-id="2c70c-120">Le décalage correspond à la position du paquet de données en cours de recherche, par rapport au début de l’objet de données ASF.</span><span class="sxs-lookup"><span data-stu-id="2c70c-120">The offset is the position of the data packet being seeked, relative to the start of the ASF Data Object.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2c70c-121">Les objets d’index de code temporel ne sont pas pris en charge actuellement.</span><span class="sxs-lookup"><span data-stu-id="2c70c-121">Timecode index objects are not currently supported.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c70c-122">Index basé sur des frames</span><span class="sxs-lookup"><span data-stu-id="2c70c-122">Frame-based Index</span></span></td>
<td><span data-ttu-id="2c70c-123">Fournit l’indexation basée sur des frames pour les flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="2c70c-123">Provides frame-based indexing for video streams.</span></span> <span data-ttu-id="2c70c-124">Les index dans l’index basé sur des trames sont en termes de nombres d’images, avec le premier frame pour un flux de fichier ASF correspondant à l’entrée 0 dans l’objet d’index basé sur des trames.</span><span class="sxs-lookup"><span data-stu-id="2c70c-124">Indexes into the frame-based index are in terms of frame numbers, with the first frame for a stream in the ASF file corresponding to entry 0 in the frame-based index object.</span></span> <span data-ttu-id="2c70c-125">Chaque bloc d’index fait référence à des entrées d’index qui contiennent un décalage d’octets.</span><span class="sxs-lookup"><span data-stu-id="2c70c-125">Each index block references index entries that contain a byte offset.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2c70c-126">Les objets d’index basés sur des frames ne sont pas pris en charge actuellement.</span><span class="sxs-lookup"><span data-stu-id="2c70c-126">Frame-based index objects are not currently supported.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2c70c-127">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="2c70c-127">This section contains the following topics.</span></span>



| <span data-ttu-id="2c70c-128">Rubrique</span><span class="sxs-lookup"><span data-stu-id="2c70c-128">Topic</span></span>                                                                                | <span data-ttu-id="2c70c-129">Description</span><span class="sxs-lookup"><span data-stu-id="2c70c-129">Description</span></span>                                                                                                                      |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c70c-130">Création et configuration de l’indexeur</span><span class="sxs-lookup"><span data-stu-id="2c70c-130">Indexer Creation and Configuration</span></span>](indexer-creation-and-configuration.md)         | <span data-ttu-id="2c70c-131">Comment créer un objet indexeur et le configurer pour la lecture d’un index existant ou pour l’écriture d’un nouvel objet d’index ASF pour un fichier.</span><span class="sxs-lookup"><span data-stu-id="2c70c-131">How to create an indexer object and configure it for reading an existing index or for writing a new ASF Index Object for a file.</span></span> |
| [<span data-ttu-id="2c70c-132">Utilisation de l’indexeur pour rechercher dans un fichier</span><span class="sxs-lookup"><span data-stu-id="2c70c-132">Using the Indexer to Seek in a File</span></span>](using-the-indexer-to-seek.md)                 | <span data-ttu-id="2c70c-133">Comment utiliser l’indexeur pour rechercher dans un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="2c70c-133">How to use the indexer to seek within an ASF file.</span></span>                                                                               |
| [<span data-ttu-id="2c70c-134">Utilisation de l’indexeur pour écrire un nouvel index</span><span class="sxs-lookup"><span data-stu-id="2c70c-134">Using the Indexer to Write a New Index</span></span>](using-the-indexer-to-write-a-new-index.md) | <span data-ttu-id="2c70c-135">Comment utiliser l’indexeur pour générer des entrées d’index et écrire un nouvel objet d’index pour un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="2c70c-135">How to use the indexer to generate index entries and write a new Index Object for an ASF file.</span></span>                                   |



 

## <a name="related-topics"></a><span data-ttu-id="2c70c-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2c70c-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c70c-137">Composants WMContainer ASF</span><span class="sxs-lookup"><span data-stu-id="2c70c-137">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="2c70c-138">Prise en charge ASF dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2c70c-138">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




