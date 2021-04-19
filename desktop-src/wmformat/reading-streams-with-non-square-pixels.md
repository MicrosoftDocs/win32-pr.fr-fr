---
title: Lecture de flux avec des pixels non carrés
description: Lecture de flux avec des pixels non carrés
ms.assetid: 32114c81-cb78-43de-9ea7-f210056f5aab
keywords:
- Windows Media Format SDK, lire des flux vidéo
- Kit de développement logiciel (SDK) Windows Media format, flux vidéo
- Windows Media Format SDK, pixels non carrés
- Windows Media Format SDK, pixels (non carrés)
- ASF (Advanced Systems Format), lecture des flux vidéo
- ASF (format des systèmes avancés), lire les flux vidéo
- ASF (Advanced Systems Format), flux vidéo
- ASF (format de systèmes avancés), flux vidéo
- ASF (Advanced Systems Format), pixels non carrés
- ASF (format des systèmes avancés), pixels non carrés
- Format de systèmes avancés (ASF), pixels (non carrés)
- ASF (format des systèmes avancés), pixels (non carrés)
- lecture des flux vidéo
- flux vidéo, lecture
- flux vidéo, pixels non carrés
- pixels non carrés
- pixels (non carrés)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfc14019e9822aefedb7600adc4209317293b2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510229"
---
# <a name="reading-streams-with-non-square-pixels"></a><span data-ttu-id="d3a9e-120">Lecture de flux avec des pixels non carrés</span><span class="sxs-lookup"><span data-stu-id="d3a9e-120">Reading Streams with Non-Square Pixels</span></span>

<span data-ttu-id="d3a9e-121">Les applications de lecteur qui doivent gérer correctement les pixels non carrés doivent examiner à la fois les attributs au niveau du flux dans l’en-tête ASF et les extensions d’unité de données sur chaque exemple.</span><span class="sxs-lookup"><span data-stu-id="d3a9e-121">Reader applications that need to correctly handle non-square pixels should examine both the stream-level attributes in the ASF header and the data unit extensions on each sample.</span></span> <span data-ttu-id="d3a9e-122">Il existe deux cas où le rectangle de sortie doit être ajusté pour compenser les pixels non carrés.</span><span class="sxs-lookup"><span data-stu-id="d3a9e-122">There are two cases when the output rectangle must be adjusted to compensate for non-square pixels.</span></span>

<span data-ttu-id="d3a9e-123">Lorsque le contenu source a été capturé à partir d’un appareil tel qu’une caméra DV (vidéo numérique) avec des pixels non carrés dans son CCD, une application de lecteur doit ajuster son rectangle de sortie vidéo afin que l’image s’affiche correctement sur un moniteur d’ordinateur avec des pixels carrés.</span><span class="sxs-lookup"><span data-stu-id="d3a9e-123">When the source content has been captured from a device such as a DV (digital video) camera with non-square pixels in its CCD, a reader application must adjust its video output rectangle so that the image displays correctly on a computer monitor with square pixels.</span></span>

<span data-ttu-id="d3a9e-124">Lorsque votre application de lecteur produit une vidéo qui est lue sur une télévision NTSC, par exemple par le biais d’une connexion out S-Video sur la carte vidéo, vous devez ajuster le rectangle vidéo afin que l’image s’affiche correctement sur les pixels non carrés de la télévision.</span><span class="sxs-lookup"><span data-stu-id="d3a9e-124">When your reader application outputs video that will be played back on an NTSC television, for example through an S-Video out connection on the video card, you must adjust the video rectangle so that the image displays correctly on the television's non-square pixels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3a9e-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d3a9e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3a9e-126">**Pour lire et écrire des flux vidéo avec des pixels non carrés**</span><span class="sxs-lookup"><span data-stu-id="d3a9e-126">**To Read and Write Video Streams with Non-Square Pixels**</span></span>](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




