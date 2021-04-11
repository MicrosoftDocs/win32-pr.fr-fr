---
title: Bordures du lecteur Windows Media (déconseillée)
description: Bordures du lecteur Windows Media (déconseillée)
ms.assetid: defa461b-ffa5-4fee-bed4-aba3e733b8c4
keywords:
- Windows Media Player, bordures
- Apparences du lecteur Windows Media, bordures
- apparences, bordures
- bordures, comparaison avec les habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a48ff3ec17230002e9c6b4a1eb17e3024375a58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309982"
---
# <a name="borders-for-windows-media-player-deprecated"></a><span data-ttu-id="3a808-107">Bordures du lecteur Windows Media (déconseillée)</span><span class="sxs-lookup"><span data-stu-id="3a808-107">Borders for Windows Media Player (deprecated)</span></span>

<span data-ttu-id="3a808-108">Cette page décrit une fonctionnalité qui peut ne pas être disponible dans les versions ultérieures du lecteur Windows Media et du kit de développement logiciel (SDK) du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3a808-108">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="3a808-109">Une bordure est similaire à une apparence, mais au lieu de remplacer l’interface utilisateur pour le mode compact du lecteur Windows Media, une bordure est incorporée dans le volet de lecture en cours du lecteur Windows Media en mode plein.</span><span class="sxs-lookup"><span data-stu-id="3a808-109">A border is similar to a skin, but instead of replacing the user interface for the compact mode of Windows Media Player, a border is embedded in the Now Playing pane of the full mode Windows Media Player.</span></span>

<span data-ttu-id="3a808-110">À l’aide d’un package de téléchargement Windows Media, vous pouvez inclure du contenu avec une bordure, ce qui vous permet de reformer les applications multimédias.</span><span class="sxs-lookup"><span data-stu-id="3a808-110">By using a Windows Media Download package, you can include content with a border, paving the way to multimedia applications.</span></span>

<span data-ttu-id="3a808-111">Un exemple de package de téléchargement Windows Media incluant une bordure et du contenu incorporé est inclus dans le répertoire d’exemples de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="3a808-111">A sample Windows Media Download package that includes a border and embedded content is included in the samples directory of this SDK.</span></span>

## <a name="creating-a-border"></a><span data-ttu-id="3a808-112">Création d’une bordure</span><span class="sxs-lookup"><span data-stu-id="3a808-112">Creating a Border</span></span>

<span data-ttu-id="3a808-113">Une bordure est créée de la même façon qu’une apparence.</span><span class="sxs-lookup"><span data-stu-id="3a808-113">A border is created the same way as a skin.</span></span> <span data-ttu-id="3a808-114">La seule différence est que l’apparence est incorporée dans le volet **Playing Now** .</span><span class="sxs-lookup"><span data-stu-id="3a808-114">The only difference is that the skin is embedded inside the **Now Playing** pane.</span></span> <span data-ttu-id="3a808-115">Cela signifie que la taille de l’apparence ne peut pas être calculée et que tous les éléments d’apparence doivent être relatifs.</span><span class="sxs-lookup"><span data-stu-id="3a808-115">This means that the skin size cannot be calculated and that all skin elements must be relative.</span></span> <span data-ttu-id="3a808-116">Si l’utilisateur redimensionne le lecteur Windows Media, certaines parties de la bordure peuvent être découpées et invisibles.</span><span class="sxs-lookup"><span data-stu-id="3a808-116">If the user resizes Windows Media Player, portions of the border may be clipped off and not seen.</span></span>

## <a name="loading-a-border"></a><span data-ttu-id="3a808-117">Chargement d’une bordure</span><span class="sxs-lookup"><span data-stu-id="3a808-117">Loading a Border</span></span>

<span data-ttu-id="3a808-118">Une bordure est chargée lorsqu’un métafichier Windows Media qui utilise l’élément d' **apparence** est chargé.</span><span class="sxs-lookup"><span data-stu-id="3a808-118">A border is loaded when a Windows Media metafile that uses the **SKIN** element is loaded.</span></span> <span data-ttu-id="3a808-119">L’attribut **href** de l’élément **Skin** doit faire référence à une apparence.</span><span class="sxs-lookup"><span data-stu-id="3a808-119">The **HREF** attribute of the **SKIN** element must reference a skin.</span></span> <span data-ttu-id="3a808-120">Un élément d' **apparence** typique ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="3a808-120">A typical **SKIN** element would look like this:</span></span>


```C++
<SKIN HREF="myborder.wmz">

```



<span data-ttu-id="3a808-121">Pour plus d’informations, consultez [élément Skin (déconseillé)](skin-element--deprecated.md).</span><span class="sxs-lookup"><span data-stu-id="3a808-121">For more information, see [SKIN Element (deprecated)](skin-element--deprecated.md).</span></span>

## <a name="including-content-with-a-border"></a><span data-ttu-id="3a808-122">Inclusion de contenu avec une bordure</span><span class="sxs-lookup"><span data-stu-id="3a808-122">Including Content with a Border</span></span>

<span data-ttu-id="3a808-123">Vous pouvez inclure du contenu avec une bordure à l’aide d’un fichier de téléchargement Windows Media (avec l’extension de nom de fichier. WMD).</span><span class="sxs-lookup"><span data-stu-id="3a808-123">You can include content with a border by using a Windows Media Download file (with a .wmd file name extension).</span></span> <span data-ttu-id="3a808-124">Suivez ces étapes :</span><span class="sxs-lookup"><span data-stu-id="3a808-124">Follow these steps:</span></span>

1.  <span data-ttu-id="3a808-125">Créez la bordure.</span><span class="sxs-lookup"><span data-stu-id="3a808-125">Create the border.</span></span> <span data-ttu-id="3a808-126">Veillez à la créer de telle sorte que le redimensionnement ne supprimera pas la composition de la bordure.</span><span class="sxs-lookup"><span data-stu-id="3a808-126">Take care to create it in such a way that resizing will not ruin the composition of the border.</span></span> <span data-ttu-id="3a808-127">Par exemple, n’incluez pas de fichier d’arrière-plan ; rendre l’arrière-plan transparent pour qu’une visualisation puisse s’exécuter derrière.</span><span class="sxs-lookup"><span data-stu-id="3a808-127">For example, do not include a background file; make the background transparent so that a visualization could run behind it.</span></span>
2.  <span data-ttu-id="3a808-128">Compressez le contenu de l’apparence (art, fichiers JScript et fichier de définition d’apparence) dans un fichier portant l’extension de nom de fichier. WMZ.</span><span class="sxs-lookup"><span data-stu-id="3a808-128">Compress the skin contents (art, JScript files, and skin definition file) into a file with a .wmz file name extension.</span></span>
3.  <span data-ttu-id="3a808-129">Créez un métafichier Windows Media (avec une extension de nom de fichier. asx) qui fait référence au fichier de bordure compressé (avec l’extension de nom de fichier. WMZ).</span><span class="sxs-lookup"><span data-stu-id="3a808-129">Create a Windows Media metafile (with an .asx file name extension) that references the compressed border file (with a .wmz file name extension).</span></span> <span data-ttu-id="3a808-130">Le métafichier peut inclure des informations de sélection avec les métadonnées de l’art et des URL pour du contenu spécifique.</span><span class="sxs-lookup"><span data-stu-id="3a808-130">The metafile can include playlist information with metadata for art and URLs for specific content.</span></span>
4.  <span data-ttu-id="3a808-131">Assemblez le contenu multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="3a808-131">Assemble the digital media content.</span></span>
5.  <span data-ttu-id="3a808-132">Compressez la bordure, le métafichier et le contenu dans un seul fichier et attribuez-lui une extension de nom de fichier. WMD.</span><span class="sxs-lookup"><span data-stu-id="3a808-132">Compress the border, metafile, and content into one file and give it a .wmd file name extension.</span></span>

## <a name="using-a-border"></a><span data-ttu-id="3a808-133">Utilisation d’une bordure</span><span class="sxs-lookup"><span data-stu-id="3a808-133">Using a Border</span></span>

<span data-ttu-id="3a808-134">Une fois que vous avez créé le fichier de téléchargement Windows Media, il suffit de double-cliquer dessus pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3a808-134">After you have created the Windows Media Download file, all that the user has to do is double-click on it.</span></span> <span data-ttu-id="3a808-135">Le fichier sera téléchargé sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3a808-135">The file will be downloaded to the user's computer.</span></span> <span data-ttu-id="3a808-136">Les fichiers à l’intérieur du package seront décompressés, la sélection sera ajoutée aux playlists, la bordure apparaîtra dans le volet de **lecture** en cours du lecteur Windows Media en mode plein et le premier élément de la nouvelle sélection commencera à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="3a808-136">The files inside the package will be unpacked, the playlist will be added to the playlists, the border will appear in the **Now Playing** pane of the full mode Windows Media Player, and the first item on the new playlist will begin playing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a808-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3a808-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a808-138">**À propos des apparences**</span><span class="sxs-lookup"><span data-stu-id="3a808-138">**About Skins**</span></span>](about-skins.md)
</dt> <dt>

[<span data-ttu-id="3a808-139">**Exemples**</span><span class="sxs-lookup"><span data-stu-id="3a808-139">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="3a808-140">**Packages de téléchargement Windows Media (déconseillés)**</span><span class="sxs-lookup"><span data-stu-id="3a808-140">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




