---
title: Ajout de sous-titres à des médias numériques
description: Ajout de sous-titres à des médias numériques
ms.assetid: 0fdd2cdc-32d4-4fda-9596-b050107abd5f
keywords:
- Lecteur Windows Media, SAMI (Synchronized Accessible Media Interchange)
- Modèle objet du lecteur Windows Media, SAMI (Synchronized Accessible Media Interchange)
- modèle objet, SAMI (Synchronized Accessible Media Interchange)
- Windows Media Player Mobile, SAMI (Synchronized Accessible Media Interchange)
- Contrôle ActiveX du lecteur Windows Media, SAMI (Synchronized Accessible Media Interchange)
- Contrôle ActiveX Mobile Player Windows Media, SAMI (Synchronized Accessible Media Interchange)
- Contrôle ActiveX, SAMI (Synchronized Accessible Media Interchange)
- Synchronized Accessible Media Interchange (SAMI), à propos de
- SAMI (accès aux médias accessibles synchronisés), à propos de
- Lecteur Windows Media, ajout de sous-titres
- Windows Media Player Object Model, ajout de sous-titres
- modèle objet, ajouter des sous-titres
- Windows Media Player Mobile, ajout de sous-titres
- Contrôle ActiveX du lecteur Windows Media, ajout de sous-titres
- Contrôle ActiveX Windows Media Player Mobile, ajout de sous-titres
- Contrôle ActiveX, ajout de sous-titres
- SAMI (Synchronized Accessible Media Interchange), ajout de sous-titres
- SAMI (Synchronized Accessible Media Interchange), ajout de sous-titres
- Ajouter des sous-titres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc464fb879df1c7642cd0a04b319383654bae4aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028882"
---
# <a name="adding-closed-captions-to-digital-media"></a><span data-ttu-id="b1ed1-122">Ajout de sous-titres à des médias numériques</span><span class="sxs-lookup"><span data-stu-id="b1ed1-122">Adding Closed Captions to Digital Media</span></span>

<span data-ttu-id="b1ed1-123">Le format SAMI (Synchronized Accessible Media Interchange) est un format de fichier conçu pour fournir du texte synchronisé comme des sous-titres, des sous-titres ou des descriptions audio avec du contenu multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="b1ed1-123">Synchronized Accessible Media Interchange (SAMI) is a file format designed to deliver synchronized text such as captions, subtitles, or audio descriptions with digital media content.</span></span> <span data-ttu-id="b1ed1-124">Intégré dans un navigateur Web à l’aide du modèle objet du lecteur Windows Media, le same favorise l’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="b1ed1-124">Integrated in a Web browser using the Windows Media Player object model, SAMI promotes accessibility.</span></span> <span data-ttu-id="b1ed1-125">En utilisant le same, vous pouvez créer du contenu multimédia riche qui atteint un public plus large et plus diversifié.</span><span class="sxs-lookup"><span data-stu-id="b1ed1-125">By using SAMI, you can create rich media content that reaches a larger, more diverse audience.</span></span>

<span data-ttu-id="b1ed1-126">En plus des polices standard, le same peut prendre en charge d’autres styles de texte, tels que des couleurs, des tailles ou des langues différentes pour aider un grand nombre d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b1ed1-126">In addition to standard fonts, SAMI can support other text styles, such as different colors, sizes, or languages to aid a variety of users.</span></span> <span data-ttu-id="b1ed1-127">Le same peut être particulièrement utile pour les personnes malvoyantes ou sourdes ou malentendantes.</span><span class="sxs-lookup"><span data-stu-id="b1ed1-127">SAMI can be particularly useful for individuals who have low vision or those who are deaf or hard-of-hearing.</span></span> <span data-ttu-id="b1ed1-128">Le format SAMI peut également aider à des fins éducatives, telles que l’enseignement d’un autre langage pour les élèves.</span><span class="sxs-lookup"><span data-stu-id="b1ed1-128">The SAMI format can also assist in educational purposes, such as teaching students a second language.</span></span>

<span data-ttu-id="b1ed1-129">Cette rubrique se concentre sur l’incorporation de SAMI avec le modèle objet de contrôle ActiveX du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b1ed1-129">This topic focuses on the incorporation of SAMI with the Windows Media Player ActiveX control object model.</span></span> <span data-ttu-id="b1ed1-130">Les fichiers SAMI existent indépendamment des fichiers multimédias numériques et ne s’appuient pas sur un format vidéo ou audio spécifique pour fonctionner.</span><span class="sxs-lookup"><span data-stu-id="b1ed1-130">SAMI files exist independently from digital media files and do not rely on a specific video or audio format to function.</span></span> <span data-ttu-id="b1ed1-131">Étant donné que les fichiers sont distincts, le contrôle du lecteur Windows Media localise, analyse, synchronise et restitue chaque fichier sur l’ordinateur du client.</span><span class="sxs-lookup"><span data-stu-id="b1ed1-131">Since the files are separate, the Windows Media Player control will locate, parse, synchronize, and render each file on the client's computer.</span></span> <span data-ttu-id="b1ed1-132">Cela offre une flexibilité et une fonctionnalité accrues, car elle permet la modification de fichiers SAMI individuels, l’incorporation du fichier SAMI avec différents formats multimédias numériques et le stockage de fichiers SAMI sur différents emplacements de serveurs.</span><span class="sxs-lookup"><span data-stu-id="b1ed1-132">This provides for added flexibility and functionality because it allows for the editing of individual SAMI files, the incorporation of the SAMI file with different digital media formats, and the storage of SAMI files on different server locations.</span></span>

<span data-ttu-id="b1ed1-133">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="b1ed1-133">This topic contains the following sections.</span></span>



| <span data-ttu-id="b1ed1-134">Section</span><span class="sxs-lookup"><span data-stu-id="b1ed1-134">Section</span></span>                                                                                                                            | <span data-ttu-id="b1ed1-135">Description</span><span class="sxs-lookup"><span data-stu-id="b1ed1-135">Description</span></span>                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1ed1-136">À propos des fichiers SAMI</span><span class="sxs-lookup"><span data-stu-id="b1ed1-136">About SAMI Files</span></span>](about-sami-files.md)                                                                                           | <span data-ttu-id="b1ed1-137">Décrit la structure de base des fichiers SAMI.</span><span class="sxs-lookup"><span data-stu-id="b1ed1-137">Describes the basic structure of SAMI files.</span></span>                                               |
| [<span data-ttu-id="b1ed1-138">Exemple de fichier SAMI</span><span class="sxs-lookup"><span data-stu-id="b1ed1-138">SAMI File Example</span></span>](sami-file-example.md)                                                                                         | <span data-ttu-id="b1ed1-139">Décrit la structure d’un exemple de fichier SAMI.</span><span class="sxs-lookup"><span data-stu-id="b1ed1-139">Describes the structure of an example SAMI file.</span></span>                                           |
| [<span data-ttu-id="b1ed1-140">Utilisation de SAMI avec le contrôle du lecteur Windows Media dans un navigateur</span><span class="sxs-lookup"><span data-stu-id="b1ed1-140">Using SAMI with the Windows Media Player Control in a Browser</span></span>](using-sami-with-the-windows-media-player-control-in-a-browser.md) | <span data-ttu-id="b1ed1-141">Décrit comment utiliser le same dans une page Web avec le contrôle du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b1ed1-141">Describes how to use SAMI in a webpage with the Windows Media Player control.</span></span>              |
| [<span data-ttu-id="b1ed1-142">À propos des URL SAMI</span><span class="sxs-lookup"><span data-stu-id="b1ed1-142">About SAMI URLs</span></span>](about-sami-urls.md)                                                                                             | <span data-ttu-id="b1ed1-143">Décrit comment les fichiers multimédias numériques peuvent être associés à des fichiers SAMI à l’aide d’une URL unique.</span><span class="sxs-lookup"><span data-stu-id="b1ed1-143">Describes how digital media files can be associated with SAMI files by using a single URL.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b1ed1-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b1ed1-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1ed1-145">**Guide de contrôle du lecteur**</span><span class="sxs-lookup"><span data-stu-id="b1ed1-145">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




