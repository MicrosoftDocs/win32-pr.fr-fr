---
title: Création d’un package de téléchargement Windows Media (déconseillé)
description: Création d’un package de téléchargement Windows Media (déconseillé)
ms.assetid: 95d6a214-9da6-496d-ba40-4476814b1d5a
keywords:
- Fichiers Windows Media, packages de téléchargement Windows Media
- Windows Media Player, packages de téléchargement Windows Media
- sous-fichiers, packages de téléchargement Windows Media
- Windows Media, packages de téléchargement Windows Media
- Packages de téléchargement Windows Media, création
- création de packages de téléchargement Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a8716e1783f0e00cb561c3aba1d15a2c3e5b147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029416"
---
# <a name="creating-a-windows-media-download-package-deprecated"></a><span data-ttu-id="1eac4-109">Création d’un package de téléchargement Windows Media (déconseillé)</span><span class="sxs-lookup"><span data-stu-id="1eac4-109">Creating a Windows Media Download Package (deprecated)</span></span>

<span data-ttu-id="1eac4-110">Cette page décrit une fonctionnalité qui peut ne pas être disponible dans les versions ultérieures du lecteur Windows Media et du kit de développement logiciel (SDK) du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1eac4-110">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="1eac4-111">Pour créer un package de téléchargement Windows Media, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="1eac4-111">Follow these steps to create a Windows Media Download package.</span></span>

1.  <span data-ttu-id="1eac4-112">**Créer une bordure.**</span><span class="sxs-lookup"><span data-stu-id="1eac4-112">**Create a border.**</span></span> <span data-ttu-id="1eac4-113">Utilisez les mêmes techniques que celles que vous utiliseriez pour créer une apparence pour le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1eac4-113">Use the same techniques you would use to build a skin for Windows Media Player.</span></span> <span data-ttu-id="1eac4-114">Concevez la bordure afin que le redimensionnement du lecteur Windows Media ne supprimera pas la composition des éléments de la bordure.</span><span class="sxs-lookup"><span data-stu-id="1eac4-114">Design the border so that resizing Windows Media Player will not ruin the composition of the border elements.</span></span> <span data-ttu-id="1eac4-115">Par exemple, utilisez une couleur unie ou une visualisation comme arrière-plan, car celles-ci sont mises à l’échelle et le lecteur Windows Media est redimensionné.</span><span class="sxs-lookup"><span data-stu-id="1eac4-115">For instance, use a solid color or visualization as a background because these will scale well as Windows Media Player is resized.</span></span>
2.  <span data-ttu-id="1eac4-116">**Compresser le contenu de la bordure.**</span><span class="sxs-lookup"><span data-stu-id="1eac4-116">**Compress the border contents.**</span></span> <span data-ttu-id="1eac4-117">Créez un dossier compressé (avec l’extension de nom de fichier. zip) qui contient les fichiers de bordure : images, fichiers JScript et fichier de définition d’apparence avec une extension de nom de fichier. WMS.</span><span class="sxs-lookup"><span data-stu-id="1eac4-117">Create a compressed folder (with a .zip file name extension) that contains the border files: images, JScript files, and the skin definition file with a .wms file name extension.</span></span> <span data-ttu-id="1eac4-118">Renommez le fichier compressé afin qu’il ait une extension de nom de fichier. WMZ.</span><span class="sxs-lookup"><span data-stu-id="1eac4-118">Rename the compressed file so that it has a .wmz file name extension.</span></span>
3.  <span data-ttu-id="1eac4-119">**Écrire un métafichier Windows Media.**</span><span class="sxs-lookup"><span data-stu-id="1eac4-119">**Write a Windows Media metafile.**</span></span> <span data-ttu-id="1eac4-120">Le lecteur Windows Media ne chargera pas la bordure, sauf si vous créez un métafichier Windows Media avec une extension de nom de fichier. asx qui implémente l’élément d' **apparence** .</span><span class="sxs-lookup"><span data-stu-id="1eac4-120">Windows Media Player will not load the border unless you create a Windows Media metafile with an .asx file name extension that implements the **SKIN** element.</span></span> <span data-ttu-id="1eac4-121">Le métafichier peut également être utilisé pour créer une sélection qui décrit le contenu inclus dans le package.</span><span class="sxs-lookup"><span data-stu-id="1eac4-121">The metafile can also be used to create a playlist that describes the content included in the package.</span></span>
4.  <span data-ttu-id="1eac4-122">**Assemblez votre contenu.**</span><span class="sxs-lookup"><span data-stu-id="1eac4-122">**Assemble your content.**</span></span> <span data-ttu-id="1eac4-123">Placez tous les fichiers que vous souhaitez utiliser dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="1eac4-123">Put all the files that you want to use into a folder.</span></span> <span data-ttu-id="1eac4-124">Cela comprend les fichiers audio, les fichiers vidéo, les fichiers de données et les fichiers de définition de bordure.</span><span class="sxs-lookup"><span data-stu-id="1eac4-124">This includes audio files, video files, metafiles, and border definition files.</span></span>
5.  <span data-ttu-id="1eac4-125">**Créez le package.**</span><span class="sxs-lookup"><span data-stu-id="1eac4-125">**Create the package.**</span></span> <span data-ttu-id="1eac4-126">Créez un dossier compressé (avec l’extension de nom de fichier. zip) qui contient le fichier de bordure, les fichiers de contenu et le métafichier.</span><span class="sxs-lookup"><span data-stu-id="1eac4-126">Create a compressed folder (with a .zip file name extension) that contains the border file, content files, and the metafile.</span></span> <span data-ttu-id="1eac4-127">Remplacez l’extension de nom de fichier de ce fichier. zip par une extension de nom de fichier. WMD.</span><span class="sxs-lookup"><span data-stu-id="1eac4-127">Change the file name extension of this .zip file to a .wmd file name extension.</span></span>
6.  <span data-ttu-id="1eac4-128">**Publiez le package sur un site Web.**</span><span class="sxs-lookup"><span data-stu-id="1eac4-128">**Post the package to a website.**</span></span> <span data-ttu-id="1eac4-129">Le package terminé est prêt à être publié sur un site Web et téléchargé par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1eac4-129">The completed package is ready to be posted to a website and downloaded by users.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1eac4-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1eac4-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1eac4-131">**Packages de téléchargement Windows Media (déconseillés)**</span><span class="sxs-lookup"><span data-stu-id="1eac4-131">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




