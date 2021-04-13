---
title: Utilisation des bordures dans les packages de téléchargement Windows Media (déconseillés)
description: Utilisation des bordures dans les packages de téléchargement Windows Media (déconseillés)
ms.assetid: d3961c5f-8cce-439d-9a13-41be2f45d92c
keywords:
- Fichiers Windows Media, packages de téléchargement Windows Media
- Windows Media Player, packages de téléchargement Windows Media
- sous-fichiers, packages de téléchargement Windows Media
- Windows Media, packages de téléchargement Windows Media
- bordures, à propos de
- Packages de téléchargement Windows Media, bordures
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 87f7d0fec341bb79bfe9b8dd739b63a9ba3a66ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380031"
---
# <a name="using-borders-in-windows-media-download-packages-deprecated"></a><span data-ttu-id="01fa6-109">Utilisation des bordures dans les packages de téléchargement Windows Media (déconseillés)</span><span class="sxs-lookup"><span data-stu-id="01fa6-109">Using Borders in Windows Media Download Packages (deprecated)</span></span>

<span data-ttu-id="01fa6-110">Cette page décrit une fonctionnalité qui peut ne pas être disponible dans les versions ultérieures du lecteur Windows Media et du kit de développement logiciel (SDK) du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="01fa6-110">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="01fa6-111">Les bordures vous permettent de créer une interface utilisateur graphique personnalisée pour votre contenu empaqueté.</span><span class="sxs-lookup"><span data-stu-id="01fa6-111">Borders enable you to create a customized graphical user interface for your packaged content.</span></span> <span data-ttu-id="01fa6-112">La bordure peut inclure des éléments tels que des images, des contrôles interactifs et des liens vers des sites Web.</span><span class="sxs-lookup"><span data-stu-id="01fa6-112">The border can include elements such as images, interactive controls, and links to websites.</span></span> <span data-ttu-id="01fa6-113">Vous pouvez utiliser des bordures dans les cas où vous souhaitez ajouter de la valeur supplémentaire à votre contenu empaqueté, par exemple pour la personnalisation ou la publicité.</span><span class="sxs-lookup"><span data-stu-id="01fa6-113">You can use borders in cases where you want to add additional value to your packaged content, such as for branding or advertising.</span></span> <span data-ttu-id="01fa6-114">Une fois que les utilisateurs ont téléchargé et ouvert votre package de téléchargement Windows Media, le lecteur Windows Media affiche automatiquement votre bordure personnalisée quand il lit le contenu empaqueté.</span><span class="sxs-lookup"><span data-stu-id="01fa6-114">After users download and open your Windows Media Download package, Windows Media Player automatically displays your custom border when it plays the packaged content.</span></span>

<span data-ttu-id="01fa6-115">Contrairement à une apparence, qui permet aux utilisateurs de remplacer complètement l’interface utilisateur du lecteur Windows Media, une bordure s’affiche uniquement dans le volet de **lecture** en cours du lecteur en mode complet.</span><span class="sxs-lookup"><span data-stu-id="01fa6-115">Unlike a skin, which enables users to completely replace the Windows Media Player user interface, a border is displayed only in the **Now Playing** pane of the full mode Player.</span></span> <span data-ttu-id="01fa6-116">Toutefois, les outils et les technologies que vous utilisez pour créer des apparences sont également utilisés pour créer des bordures.</span><span class="sxs-lookup"><span data-stu-id="01fa6-116">However, the same tools and technologies that you use to create skins are also used to create borders.</span></span> <span data-ttu-id="01fa6-117">L’illustration suivante montre une bordure.</span><span class="sxs-lookup"><span data-stu-id="01fa6-117">The following illustration shows a border.</span></span>

![une bordure affiche le lecteur Windows Media 10](images/border-v10.png)

<span data-ttu-id="01fa6-119">Il est important de comprendre les techniques de base pour créer une apparence avant de tenter de créer une bordure.</span><span class="sxs-lookup"><span data-stu-id="01fa6-119">It is important to understand the basic techniques for creating a skin before attempting to create a border.</span></span> <span data-ttu-id="01fa6-120">La programmation des bordures s’effectue à l’aide de deux langages de programmation : Extensible Markup Language (XML) et Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="01fa6-120">Border programming is accomplished using two programming languages: Extensible Markup Language (XML) and Microsoft JScript.</span></span> <span data-ttu-id="01fa6-121">XML est utilisé pour définir des éléments d’interface tels que des boutons, des curseurs et des zones de texte.</span><span class="sxs-lookup"><span data-stu-id="01fa6-121">XML is used to define interface elements such as buttons, sliders, and text boxes.</span></span> <span data-ttu-id="01fa6-122">Vous n’avez pas besoin de comprendre tous les détails du XML, car vous n’avez pas à écrire de nouveaux éléments de code XML. vous pouvez simplement utiliser ceux fournis par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="01fa6-122">You don't need to understand all the details of XML since you don't have to write new XML code elements; you can simply use the ones provided by Windows Media Player.</span></span> <span data-ttu-id="01fa6-123">Même si JScript n’est pas requis pour la création de bordures, il peut être utilisé pour fournir des fonctionnalités supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="01fa6-123">Although JScript is not required for creating borders, it can be used to provide additional functionality.</span></span>

<span data-ttu-id="01fa6-124">Un fichier de bordure compressé avec une extension de nom de fichier. WMZ comprend un fichier de définition de bordure avec une extension de nom de fichier. WMS et tous les fichiers image utilisés dans la bordure.</span><span class="sxs-lookup"><span data-stu-id="01fa6-124">A compressed border file with a .wmz file name extension includes a border definition file with a .wms file name extension and all the image files used within the border.</span></span>

<span data-ttu-id="01fa6-125">Pour inclure une bordure dans un package de téléchargement Windows Media, il vous suffit de créer une bordure et de faire référence à cette bordure dans une sélection de métafichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="01fa6-125">To include a border in a Windows Media Download package, simply create a border and reference that border in a Windows Media metafile playlist.</span></span> <span data-ttu-id="01fa6-126">Le fichier de bordure est chargé dans le lecteur Windows Media une fois que le lecteur a analysé le métafichier et interprète l’élément d' **apparence** qui fait référence à la bordure.</span><span class="sxs-lookup"><span data-stu-id="01fa6-126">The border file is loaded into Windows Media Player after the Player parses the metafile and interprets the **SKIN** element that references the border.</span></span> <span data-ttu-id="01fa6-127">L’élément **Skin** est utilisé uniquement pour les bordures, et l’attribut href de l’élément **Skin** ne peut faire référence qu’à une seule apparence pour chaque package.</span><span class="sxs-lookup"><span data-stu-id="01fa6-127">The **SKIN** element is used only for borders, and the HREF attribute of the **SKIN** element can reference only one skin for each package.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01fa6-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="01fa6-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01fa6-129">**Bordures du lecteur Windows Media (déconseillée)**</span><span class="sxs-lookup"><span data-stu-id="01fa6-129">**Borders for Windows Media Player (deprecated)**</span></span>](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[<span data-ttu-id="01fa6-130">**Packages de téléchargement Windows Media (déconseillés)**</span><span class="sxs-lookup"><span data-stu-id="01fa6-130">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> <dt>

[<span data-ttu-id="01fa6-131">**Apparences du lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="01fa6-131">**Windows Media Player Skins**</span></span>](windows-media-player-skins.md)
</dt> </dl>

 

 




