---
title: Création de graphiques de filtre pour écrire des fichiers ASF (QASF)
description: Création de graphiques de filtre pour écrire des fichiers ASF (QASF)
ms.assetid: 45583c97-4e59-4a6a-987b-5486e6f33990
keywords:
- Kit de développement logiciel (SDK) de format Windows Media, création de graphiques de filtres (QASF)
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, écriture de fichiers ASF (QASF)
- ASF (Advanced Systems Format), création de graphiques de filtre (QASF)
- ASF (format de systèmes avancés), création de graphiques de filtre (QASF)
- ASF (Advanced Systems Format), écriture (QASF)
- ASF (Advanced Systems Format), écriture (QASF)
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- DirectShow, génération de graphiques de filtre (QASF)
- DirectShow, écriture de fichiers ASF (QASF)
- Windows Media Format SDK, QASF
- ASF (Advanced Systems Format), QASF
- ASF (format avancé des systèmes), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbf0a261d1502f76cebc0eb2141cd230c509029
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106517942"
---
# <a name="building-filter-graphs-to-write-asf-files-qasf"></a><span data-ttu-id="3fbea-118">Création de graphiques de filtre pour écrire des fichiers ASF (QASF)</span><span class="sxs-lookup"><span data-stu-id="3fbea-118">Building Filter Graphs to Write ASF Files (QASF)</span></span>

<span data-ttu-id="3fbea-119">Les applications basées sur DirectShow utilisent généralement l’un des trois types de graphiques de filtre de base lors de la création de contenu Windows Media :</span><span class="sxs-lookup"><span data-stu-id="3fbea-119">Applications based on DirectShow typically use one of three basic types of filter graphs when creating Windows Media–based content:</span></span>

-   <span data-ttu-id="3fbea-120">Les graphiques de filtre pour la conversion ou le transcodage de contenu à partir d’un autre format au format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3fbea-120">Filter graphs for converting or transcoding content from some other format into Windows Media Format.</span></span>
-   <span data-ttu-id="3fbea-121">Graphiques de filtre pour l’insertion de contenu qui n’est pas basé sur Windows Media (formats de flux natifs) dans des fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="3fbea-121">Filter graphs for inserting content that is not Windows Media-based (native stream formats) into ASF files.</span></span>
-   <span data-ttu-id="3fbea-122">Les graphiques de filtre permettant de capturer des données actives et de les encoder immédiatement dans le format Windows Media avant de les enregistrer sur le disque.</span><span class="sxs-lookup"><span data-stu-id="3fbea-122">Filter graphs for capturing live data and encoding it immediately into Windows Media Format before saving it to disk.</span></span>

<span data-ttu-id="3fbea-123">Chaque type de graphique de filtre est décrit plus en détail dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="3fbea-123">Each type of filter graph is described in more detail in the following sections.</span></span>



| <span data-ttu-id="3fbea-124">Section</span><span class="sxs-lookup"><span data-stu-id="3fbea-124">Section</span></span>                                                                                                             | <span data-ttu-id="3fbea-125">Description</span><span class="sxs-lookup"><span data-stu-id="3fbea-125">Description</span></span>                                                                                           |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3fbea-126">Transcodage de fichiers (QASF)</span><span class="sxs-lookup"><span data-stu-id="3fbea-126">Transcoding Files (QASF)</span></span>](transcoding-files--qasf.md)                                                             | <span data-ttu-id="3fbea-127">Décrit comment créer des graphiques de filtre de transcodage de fichier.</span><span class="sxs-lookup"><span data-stu-id="3fbea-127">Describes how to create file-transcoding filter graphs.</span></span>                                               |
| [<span data-ttu-id="3fbea-128">Insertion de formats de flux natifs dans des fichiers ASF (QASF)</span><span class="sxs-lookup"><span data-stu-id="3fbea-128">Inserting Native Stream Formats Into ASF Files (QASF)</span></span>](inserting-native-stream-formats-into-asf-files--qasf.md)   | <span data-ttu-id="3fbea-129">Décrit comment placer tout type de données audio ou vidéo compressées ou non compressées dans un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="3fbea-129">Describes how to place any type of compressed or non-compressed audio or video data into an ASF file.</span></span> |
| [<span data-ttu-id="3fbea-130">Capture directe à partir d’un appareil dans un fichier ASF (QASF)</span><span class="sxs-lookup"><span data-stu-id="3fbea-130">Capturing Directly from a Device to an ASF File (QASF)</span></span>](capturing-directly-from-a-device-to-an-asf-file--qasf.md) | <span data-ttu-id="3fbea-131">Décrit comment créer des graphiques de filtre de capture qui sont générés dans un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="3fbea-131">Describes how to create capture filter graphs that output to an ASF file.</span></span>                             |



 

 

 




