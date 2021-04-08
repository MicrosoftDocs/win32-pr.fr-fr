---
title: Index
description: Index
ms.assetid: 54c694f6-3c10-4d7c-bcd1-f2b17d652e8e
keywords:
- Windows Media Format SDK, index
- ASF (Advanced Systems Format), index
- ASF (format avancé des systèmes), index
- Windows Media Format SDK, index temporels
- ASF (Advanced Systems Format), index temporels
- ASF (format de systèmes avancés), index temporels
- Kit de développement logiciel (SDK) Windows Media format, index basés sur des frames
- ASF (Advanced Systems Format), index basés sur des trames
- ASF (format de systèmes avancés), index basés sur des trames
- Windows Media Format SDK, codes temporels SMPTE
- ASF (Advanced Systems Format), codes temporels SMPTE
- ASF (format des systèmes avancés), codes temporels SMPTE
- index, à propos de
- index temporels
- index basés sur des frames
- Codes temporels SMPTE, index
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2e5a194f9c495720cbc40ccdb192509723eee0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840581"
---
# <a name="indexes"></a><span data-ttu-id="50afe-119">Index</span><span class="sxs-lookup"><span data-stu-id="50afe-119">Indexes</span></span>

<span data-ttu-id="50afe-120">Une exigence courante pour les applications qui lisent des fichiers multimédias numériques est la possibilité de rechercher un point spécifique dans le contenu.</span><span class="sxs-lookup"><span data-stu-id="50afe-120">A common requirement for applications that read digital media files is the ability to seek to a specific point in the content.</span></span> <span data-ttu-id="50afe-121">La recherche peut être difficile, car il n’y a aucune garantie que les différents flux d’un fichier comportent des échantillons avec des heures de début simultanées.</span><span class="sxs-lookup"><span data-stu-id="50afe-121">Seeking can be difficult because there is no guarantee that the various streams in a file have samples with concurrent start times.</span></span> <span data-ttu-id="50afe-122">Ce problème est résolu avec l’utilisation d' *index*.</span><span class="sxs-lookup"><span data-stu-id="50afe-122">This problem is addressed with the use of *indexes*.</span></span> <span data-ttu-id="50afe-123">Un index est un objet dans un fichier ASF qui représente des exemples vidéo avec les durées de présentation.</span><span class="sxs-lookup"><span data-stu-id="50afe-123">An index is an object in an ASF file that equates video samples with their presentation times.</span></span> <span data-ttu-id="50afe-124">Aucun index n’est requis pour les flux audio, car les données audio sont plus étroitement liées à l’heure de présentation que les données vidéo.</span><span class="sxs-lookup"><span data-stu-id="50afe-124">No index is required for audio streams because audio data is more closely connected with presentation time than video data is.</span></span>

<span data-ttu-id="50afe-125">L’objet indexeur du kit de développement logiciel (SDK) du format Windows Media peut créer trois types d’index différents : les index temporels, les index basés sur des trames et les index de code temporel SMPTE.</span><span class="sxs-lookup"><span data-stu-id="50afe-125">The indexer object of the Windows Media Format SDK can create three different types of indexes: temporal indexes, frame-based indexes, and SMPTE time code indexes.</span></span>

<span data-ttu-id="50afe-126">Les index temporels sont le type le plus courant.</span><span class="sxs-lookup"><span data-stu-id="50afe-126">Temporal indexes are the most common type.</span></span> <span data-ttu-id="50afe-127">Ils associent simplement les exemples de vidéos aux temps de présentation correspondants.</span><span class="sxs-lookup"><span data-stu-id="50afe-127">They simply equate video samples with the corresponding presentation times.</span></span>

<span data-ttu-id="50afe-128">Un index basé sur des frames correspond à des exemples vidéo avec des nombres d’images vidéo et des durées de présentation.</span><span class="sxs-lookup"><span data-stu-id="50afe-128">A frame-based index equates video samples with video frame numbers and presentation times.</span></span> <span data-ttu-id="50afe-129">Les numéros de frame sont particulièrement utiles dans les applications qui modifient la vidéo.</span><span class="sxs-lookup"><span data-stu-id="50afe-129">Frame numbers are particularly useful in applications that edit video.</span></span>

<span data-ttu-id="50afe-130">Un index de code de temps SMTP est le type d’index le plus rare.</span><span class="sxs-lookup"><span data-stu-id="50afe-130">A SMTPE time code index is the rarest type of index.</span></span> <span data-ttu-id="50afe-131">Il utilise le code de temps SMPTE comme base de l’index et peut être utilisé uniquement sur les flux qui ont des horodatages SMPTE inclus avec leurs échantillons.</span><span class="sxs-lookup"><span data-stu-id="50afe-131">It uses SMPTE time code as the basis of the index and can be used only on streams that have SMPTE time stamps included with their samples.</span></span> <span data-ttu-id="50afe-132">Pour plus d’informations sur le code temporel SMPTE, consultez [prise en charge du code temporel SMPTE](smpte-time-code-support.md).</span><span class="sxs-lookup"><span data-stu-id="50afe-132">For more information about SMPTE time code, see [SMPTE Time Code Support](smpte-time-code-support.md).</span></span>

<span data-ttu-id="50afe-133">Un fichier ASF peut contenir un index de chaque type pour chaque flux vidéo qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="50afe-133">An ASF file can contain an index of each type for each video stream it contains.</span></span> <span data-ttu-id="50afe-134">Par défaut, un index temporel est inclus pour chaque flux vidéo dans des fichiers créés par l’objet Writer.</span><span class="sxs-lookup"><span data-stu-id="50afe-134">As a default, a temporal index is included for each video stream in files created by the writer object.</span></span> <span data-ttu-id="50afe-135">Vous pouvez modifier les paramètres d’indexation automatique de vos fichiers en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="50afe-135">You can change the automatic indexing settings for your files to suit your needs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50afe-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="50afe-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50afe-137">**Fonctionnalités des fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="50afe-137">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="50afe-138">**Utilisation des index**</span><span class="sxs-lookup"><span data-stu-id="50afe-138">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> <dt>

[<span data-ttu-id="50afe-139">**Lecture des fichiers avec le lecteur asynchrone**</span><span class="sxs-lookup"><span data-stu-id="50afe-139">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="50afe-140">**Lecture des fichiers avec le lecteur synchrone**</span><span class="sxs-lookup"><span data-stu-id="50afe-140">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




