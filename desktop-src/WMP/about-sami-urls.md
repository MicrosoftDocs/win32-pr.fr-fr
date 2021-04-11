---
title: À propos des URL SAMI
description: À propos des URL SAMI
ms.assetid: 6898a0d5-cfd0-4ba5-8cd1-907cf110667c
keywords:
- Lecteur Windows Media, SAMI (Synchronized Accessible Media Interchange)
- Modèle objet du lecteur Windows Media, SAMI (Synchronized Accessible Media Interchange)
- modèle objet, SAMI (Synchronized Accessible Media Interchange)
- Windows Media Player Mobile, SAMI (Synchronized Accessible Media Interchange)
- Contrôle ActiveX du lecteur Windows Media, SAMI (Synchronized Accessible Media Interchange)
- Contrôle ActiveX Mobile Player Windows Media, SAMI (Synchronized Accessible Media Interchange)
- Contrôle ActiveX, SAMI (Synchronized Accessible Media Interchange)
- Fichiers de Media Interchange (SAMI) synchronisés, fichiers
- SAMI (Synchronized Accessible Media Interchange), fichiers
- SAMI (Synchronized Accessible Media Interchange), URL
- SAMI (Synchronized Accessible Media Interchange), URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a7a41e70d0239b9bdac7d12f9a2dd2f75be15b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196590"
---
# <a name="about-sami-urls"></a><span data-ttu-id="3d0bf-114">À propos des URL SAMI</span><span class="sxs-lookup"><span data-stu-id="3d0bf-114">About SAMI URLs</span></span>

<span data-ttu-id="3d0bf-115">Les fichiers SAMI peuvent être associés à des fichiers multimédias numériques à l’aide d’une URL unique.</span><span class="sxs-lookup"><span data-stu-id="3d0bf-115">SAMI files can be associated with digital media files by using a single URL.</span></span> <span data-ttu-id="3d0bf-116">Pour ce faire, utilisez *le* paramètre d’URL sami.</span><span class="sxs-lookup"><span data-stu-id="3d0bf-116">This is accomplished by using *the sami* URL parameter.</span></span> <span data-ttu-id="3d0bf-117">Le paramètre d’URL est précédé de l’URL de base et d’un ?</span><span class="sxs-lookup"><span data-stu-id="3d0bf-117">The URL parameter is preceded by the base URL and a ?</span></span> <span data-ttu-id="3d0bf-118">.</span><span class="sxs-lookup"><span data-stu-id="3d0bf-118">character.</span></span> <span data-ttu-id="3d0bf-119">Une URL avec un paramètre *sami* respecte la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="3d0bf-119">A URL with a *sami* parameter follows this syntax:</span></span>

<span data-ttu-id="3d0bf-120">*URL*? *same* = *captionsURL*.</span><span class="sxs-lookup"><span data-stu-id="3d0bf-120">*URL*?*sami*=*captionsURL*.</span></span>

<span data-ttu-id="3d0bf-121">La valeur du paramètre URL suit le nom du paramètre et le signe égal, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="3d0bf-121">The value of the URL parameter follows the parameter name and an equals sign, as in the following example:</span></span>


```C++
https://proseware.com/samitest.wma?sami=https://acc.proseware.com/test.smi

```



<span data-ttu-id="3d0bf-122">Cette syntaxe d’URL est couramment utilisée dans un lien hypertexte ou un métafichier Windows Media pour établir une liaison directe avec les emplacements du fichier multimédia numérique et du fichier SAMI.</span><span class="sxs-lookup"><span data-stu-id="3d0bf-122">This URL syntax is commonly used in a hyperlink or a Windows Media metafile to link directly to the locations of both the digital media file and the SAMI file.</span></span> <span data-ttu-id="3d0bf-123">Lorsque l’utilisateur clique sur le lien hypertexte, le lecteur Windows Media démarre en mode complet et lit le contenu multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="3d0bf-123">When the user clicks on the hyperlink, Windows Media Player launches in full mode and plays the digital media content.</span></span>

<span data-ttu-id="3d0bf-124">Si le paramètre d’URL *sami* n’est pas spécifié, le lecteur Windows Media recherche un fichier sami qui se trouve dans le même emplacement que le fichier multimédia numérique et qui porte le même nom de fichier, à l’exception de l’extension de nom de fichier, qui doit être. SMI.</span><span class="sxs-lookup"><span data-stu-id="3d0bf-124">If the *sami* URL parameter is not specified, Windows Media Player will look for a SAMI file that is in the same location as the digital media file and that has the same file name except for the file name extension, which must be .smi.</span></span> <span data-ttu-id="3d0bf-125">Si un tel fichier est présent, il est automatiquement ouvert si l’affichage des sous-titres a été activé dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="3d0bf-125">If such a file is present, it will be opened automatically if caption display has been enabled in the Player.</span></span>

<span data-ttu-id="3d0bf-126">Les sous-titres sont activés dans le lecteur Windows Media en cliquant sur le menu **lire** , puis en cliquant sur **légendes et** sous-titres, puis en cliquant **sur activé**.</span><span class="sxs-lookup"><span data-stu-id="3d0bf-126">Closed captions are enabled in Windows Media Player by clicking the **Play** menu, then clicking **Captions and Subtitles**, and then clicking **On**.</span></span> <span data-ttu-id="3d0bf-127">Si les sous-titres sont activés, les légendes contenues dans le fichier SAMI s’affichent pendant la lecture de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="3d0bf-127">If closed captions are enabled, the captions contained in the SAMI file will display while the media item plays.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d0bf-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3d0bf-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d0bf-129">**Ajout de sous-titres à des médias numériques**</span><span class="sxs-lookup"><span data-stu-id="3d0bf-129">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




