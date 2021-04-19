---
title: Obtenir les meilleures performances de recherche de vidéos
description: Obtenir les meilleures performances de recherche de vidéos
ms.assetid: 21269f0c-fc3a-46fc-88b4-f71828b5d5a7
keywords:
- Windows Media Format SDK, meilleures performances de recherche de vidéos
- ASF (Advanced Systems Format), meilleures performances de recherche de vidéos
- ASF (format de systèmes avancés), meilleures performances de recherche de vidéos
- ASF (Advanced Systems Format), performances de recherche de vidéos
- ASF (format de systèmes avancés), performances de recherche de vidéos
- ASF (Advanced Systems Format), performances
- ASF (format des systèmes avancés), performances
- recherche de vidéos
- performances, recherche de vidéos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c95feb9158bbab09ce28024100f3ebbffb56ad9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513475"
---
# <a name="getting-the-best-video-seeking-performance"></a><span data-ttu-id="b410d-112">Obtenir les meilleures performances de recherche de vidéos</span><span class="sxs-lookup"><span data-stu-id="b410d-112">Getting the Best Video Seeking Performance</span></span>

<span data-ttu-id="b410d-113">La recherche de contenu dans un fichier est une opération très courante qui est potentiellement un problème de performances.</span><span class="sxs-lookup"><span data-stu-id="b410d-113">Seeking to content in a file is a very common operation that is potentially a performance issue.</span></span> <span data-ttu-id="b410d-114">La vidéo encodée avec le codec Windows Media Video 9 est constituée principalement d’images Delta, qui enregistrent uniquement les modifications par rapport au frame précédent.</span><span class="sxs-lookup"><span data-stu-id="b410d-114">Video encoded with the Windows Media Video 9 codec is made up primarily of delta frames, which only record the changes in relation to the previous frame.</span></span> <span data-ttu-id="b410d-115">La reconstruction des frames Delta prend du temps, en particulier si les images clés sont éloignées.</span><span class="sxs-lookup"><span data-stu-id="b410d-115">Reconstructing delta frames takes time, particularly if the key frames are far apart.</span></span> <span data-ttu-id="b410d-116">Pour plus d’informations sur la configuration d’images clés pour une recherche efficace, consultez [Configuration des flux vidéo pour la recherche de performances](configuring-video-streams-for-seeking-performance.md).</span><span class="sxs-lookup"><span data-stu-id="b410d-116">For more information about configuring key frames for efficient seeking, see [Configuring Video Streams for Seeking Performance](configuring-video-streams-for-seeking-performance.md).</span></span>

<span data-ttu-id="b410d-117">En plus de la configuration appropriée, vous pouvez améliorer les performances de recherche à l’aide de l’indexation des frames pour le flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="b410d-117">In addition to proper configuration, you can improve seeking performance by using frame indexing for the video stream.</span></span> <span data-ttu-id="b410d-118">La recherche d’un numéro de trame est généralement plus rapide que la recherche d’une heure de présentation.</span><span class="sxs-lookup"><span data-stu-id="b410d-118">Seeking to a frame number is typically faster than seeking to a presentation time.</span></span>

<span data-ttu-id="b410d-119">En cas de recherche dans un fichier contenant plusieurs flux, vous ne devez sélectionner que les flux nécessaires.</span><span class="sxs-lookup"><span data-stu-id="b410d-119">If seeking in a file with multiple streams, you should select only the streams that are needed.</span></span> <span data-ttu-id="b410d-120">Chaque flux de donnée configuré pour la lecture aura une incidence sur les performances de la recherche, car tous les flux sélectionnés sont synchronisés lorsque vous recherchez un point dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="b410d-120">Each stream configured for reading will affect the performance of seeking, because all selected streams are synchronized when you seek to a point in a file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b410d-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b410d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b410d-122">**Lecture des fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="b410d-122">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="b410d-123">**Pour rechercher par numéro de frame à l’aide du lecteur asynchrone**</span><span class="sxs-lookup"><span data-stu-id="b410d-123">**To Seek By Frame Number Using the Asynchronous Reader**</span></span>](to-seek-by-frame-number-using-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="b410d-124">**Pour rechercher par numéro de frame à l’aide du lecteur synchrone**</span><span class="sxs-lookup"><span data-stu-id="b410d-124">**To Seek By Frame Number Using the Synchronous Reader**</span></span>](to-seek-by-frame-number-using-the-synchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="b410d-125">**Pour effectuer une recherche par heure à l’aide du lecteur asynchrone**</span><span class="sxs-lookup"><span data-stu-id="b410d-125">**To Seek By Time Using the Asynchronous Reader**</span></span>](to-seek-by-time-using-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="b410d-126">**Pour effectuer une recherche par heure à l’aide du lecteur synchrone**</span><span class="sxs-lookup"><span data-stu-id="b410d-126">**To Seek By Time Using the Synchronous Reader**</span></span>](to-seek-by-time-using-the-synchronous-reader.md)
</dt> </dl>

 

 




