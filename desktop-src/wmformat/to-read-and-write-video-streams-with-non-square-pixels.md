---
title: Pour lire et écrire des flux vidéo avec des pixels non carrés
description: Pour lire et écrire des flux vidéo avec des pixels non carrés
ms.assetid: fe66d13e-61cf-4bb6-9ca2-aafeabe320ec
keywords:
- Windows Media Format SDK, lire des flux vidéo
- Windows Media Format SDK, écriture de flux vidéo
- Kit de développement logiciel (SDK) Windows Media format, flux vidéo
- Windows Media Format SDK, pixels non carrés
- Windows Media Format SDK, pixels (non carrés)
- ASF (Advanced Systems Format), lecture des flux vidéo
- ASF (format des systèmes avancés), lire les flux vidéo
- ASF (Advanced Systems Format), écriture de flux vidéo
- ASF (format avancé des systèmes), écriture de flux vidéo
- ASF (Advanced Systems Format), flux vidéo
- ASF (format de systèmes avancés), flux vidéo
- ASF (Advanced Systems Format), pixels non carrés
- ASF (format des systèmes avancés), pixels non carrés
- Format de systèmes avancés (ASF), pixels (non carrés)
- ASF (format des systèmes avancés), pixels (non carrés)
- lecture des flux vidéo
- écriture de flux vidéo
- flux vidéo, lecture
- flux vidéo, écriture
- flux vidéo, pixels non carrés
- pixels non carrés
- pixels (non carrés)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd6b3e3ba67ba42dfc144e7f95ddd042dea0f84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309926"
---
# <a name="to-read-and-write-video-streams-with-non-square-pixels"></a><span data-ttu-id="42018-125">Pour lire et écrire des flux vidéo avec des pixels non carrés</span><span class="sxs-lookup"><span data-stu-id="42018-125">To Read and Write Video Streams with Non-Square Pixels</span></span>

<span data-ttu-id="42018-126">Les moniteurs d’ordinateur présentent des pixels carrés, mais d’autres types d’écrans vidéo, y compris les téléviseurs NTSC, présentent des pixels rectangulaires ou non carrés.</span><span class="sxs-lookup"><span data-stu-id="42018-126">Computer monitors have square pixels, but other types of video screens, including NTSC televisions, have rectangular or non-square pixels.</span></span> <span data-ttu-id="42018-127">En outre, certains périphériques d’entrée, tels que les caméras vidéo numériques (DV), ont des appareils qui ont des pixels non carrés.</span><span class="sxs-lookup"><span data-stu-id="42018-127">Also, some input devices, such as Digital Video (DV) cameras, have charged couple devices with non-square pixels.</span></span> <span data-ttu-id="42018-128">Lorsque vous écrivez des fichiers qui sont basés sur des données sources de pixels non carrés ou qui sont destinés à être affichés sur des appareils avec des pixels non carrés, les informations sur les proportions de pixels doivent être incluses dans le fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="42018-128">When you are writing files that are either based on non-square pixel source data or else intended for display on devices with non-square pixels, the pixel aspect ratio information must be included in the ASF file.</span></span> <span data-ttu-id="42018-129">Les applications de lecteur doivent examiner ces informations et les utiliser pour ajuster les proportions du rectangle vidéo en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="42018-129">Reader applications must examine that information and use it to adjust the aspect ratio of the video rectangle as necessary.</span></span>

## <a name="related-topics"></a><span data-ttu-id="42018-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="42018-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42018-131">**Rubriques avancées**</span><span class="sxs-lookup"><span data-stu-id="42018-131">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="42018-132">**Lecture de flux avec des pixels non carrés**</span><span class="sxs-lookup"><span data-stu-id="42018-132">**Reading Streams with Non-Square Pixels**</span></span>](reading-streams-with-non-square-pixels.md)
</dt> <dt>

[<span data-ttu-id="42018-133">**Écriture de flux avec des pixels non carrés**</span><span class="sxs-lookup"><span data-stu-id="42018-133">**Writing Streams with Non-Square Pixels**</span></span>](writing-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




