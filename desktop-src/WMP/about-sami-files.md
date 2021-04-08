---
title: À propos des fichiers SAMI
description: À propos des fichiers SAMI
ms.assetid: 39b1e8a8-bbeb-4376-89d9-03a147f4c4fd
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
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d310ab3eb3016937f148ebb26e810dd9e6e6b6b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840150"
---
# <a name="about-sami-files"></a><span data-ttu-id="02506-112">À propos des fichiers SAMI</span><span class="sxs-lookup"><span data-stu-id="02506-112">About SAMI Files</span></span>

<span data-ttu-id="02506-113">Les fichiers SAMI sont des fichiers texte qui ont une extension de nom de fichier. SMI ou. sami.</span><span class="sxs-lookup"><span data-stu-id="02506-113">SAMI files are text files that have an .smi or .sami file name extension.</span></span> <span data-ttu-id="02506-114">Ils contiennent les chaînes de texte utilisées pour les légendes fermées, les sous-titres et les descriptions audio synchronisées.</span><span class="sxs-lookup"><span data-stu-id="02506-114">They contain the text strings used for synchronized closed captions, subtitles, and audio descriptions.</span></span> <span data-ttu-id="02506-115">Ils spécifient également les paramètres de minutage utilisés par le contrôle du lecteur Windows Media pour synchroniser le texte des sous-titres avec du contenu audio ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="02506-115">They also specify the timing parameters used by the Windows Media Player control to synchronize closed caption text with audio or video content.</span></span> <span data-ttu-id="02506-116">Lorsqu’un fichier multimédia numérique atteint une heure désignée dans le fichier SAMI, le texte change en conséquence dans la zone d’affichage de la légende fermée de la page Web.</span><span class="sxs-lookup"><span data-stu-id="02506-116">When a digital media file reaches a time designated in the SAMI file, the text changes accordingly in the closed caption display area of the webpage.</span></span>

<span data-ttu-id="02506-117">En dehors d’un simple éditeur de texte (tel que le bloc-notes Microsoft), aucun logiciel spécial n’est requis pour créer un fichier SAMI.</span><span class="sxs-lookup"><span data-stu-id="02506-117">Other than a simple text editor (such as Microsoft Notepad), special software is not required to create a SAMI file.</span></span> <span data-ttu-id="02506-118">SAMI et HTML partagent des éléments communs, tels que <HEAD> les <BODY> balises et.</span><span class="sxs-lookup"><span data-stu-id="02506-118">SAMI and HTML share common elements, such as the <HEAD> and <BODY> tags.</span></span> <span data-ttu-id="02506-119">Comme en HTML, les balises utilisées dans les fichiers SAMI doivent toujours être utilisées par paires.</span><span class="sxs-lookup"><span data-stu-id="02506-119">As in HTML, tags used in SAMI files must always be used in pairs.</span></span> <span data-ttu-id="02506-120">Par exemple, un élément BODY commence par une <BODY> balise et doit toujours se terminer par une </BODY> balise.</span><span class="sxs-lookup"><span data-stu-id="02506-120">For example, a BODY element begins with a <BODY> tag and must always end with a </BODY> tag.</span></span>

<span data-ttu-id="02506-121">Un fichier SAMI de base requiert trois balises fondamentales : <SAMI> , <HEAD> et <BODY> .</span><span class="sxs-lookup"><span data-stu-id="02506-121">A basic SAMI file requires three fundamental tags: <SAMI>, <HEAD>, and <BODY>.</span></span>

<span data-ttu-id="02506-122">La <SAMI> balise identifie le document sous la forme d’un document sami afin que d’autres applications puissent reconnaître son format de fichier.</span><span class="sxs-lookup"><span data-stu-id="02506-122">The <SAMI> tag identifies the document as a SAMI document so other applications can recognize its file format.</span></span>

<span data-ttu-id="02506-123">Entre les balises <HEAD> et </HEAD> , vous définissez des indications de base et d’autres informations de mise en forme pour le document sami, telles que le titre du document, des informations générales et des propriétés de style pour les sous-titres.</span><span class="sxs-lookup"><span data-stu-id="02506-123">Between the <HEAD> and </HEAD> tags, you define basic guidelines and other format information for the SAMI document, such as the document title, general information, and style properties for closed captions.</span></span> <span data-ttu-id="02506-124">Comme HTML, le contenu déclaré dans l’élément HEAD ne s’affiche pas comme OUTPUT.</span><span class="sxs-lookup"><span data-stu-id="02506-124">Like HTML, content declared within the HEAD element does not display as output.</span></span>

<span data-ttu-id="02506-125">Les éléments et les attributs définis entre les balises <BODY> et </BODY> affichent le contenu affiché par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="02506-125">Elements and attributes defined between the <BODY> and </BODY> tags display content seen by the user.</span></span> <span data-ttu-id="02506-126">En same, l’élément BODY contient les paramètres de synchronisation et les chaînes de texte utilisées pour les sous-titres.</span><span class="sxs-lookup"><span data-stu-id="02506-126">In SAMI, the BODY element contains the parameters for synchronization and the text strings used for closed captions.</span></span>

<span data-ttu-id="02506-127">Défini dans l’élément HEAD, l’élément STYLE fournit des fonctionnalités ajoutées en SAMI.</span><span class="sxs-lookup"><span data-stu-id="02506-127">Defined within the HEAD element, the STYLE element provides for added functionality in SAMI.</span></span> <span data-ttu-id="02506-128">Entre les balises <STYLE> et </STYLE> , vous pouvez définir plusieurs sélecteurs de feuille de style en cascade (CSS) pour le style et la mise en page.</span><span class="sxs-lookup"><span data-stu-id="02506-128">Between the <STYLE> and </STYLE> tags, you can define several Cascading Style Sheet (CSS) selectors for style and layout.</span></span> <span data-ttu-id="02506-129">Des propriétés de style telles que des polices, des tailles et des alignements peuvent être personnalisées pour offrir une expérience utilisateur riche tout en promouvant également l’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="02506-129">Style properties such as fonts, sizes, and alignments can be customized to provide a rich user experience while also promoting accessibility.</span></span> <span data-ttu-id="02506-130">Par exemple, la définition d’une classe de style de police de texte volumineux peut améliorer la lisibilité pour les utilisateurs qui éprouvent des difficultés à lire un texte de petite taille.</span><span class="sxs-lookup"><span data-stu-id="02506-130">For example, defining a large text font style class can improve the readability for users who have difficulty reading small text.</span></span> <span data-ttu-id="02506-131">En outre, en définissant plusieurs classes de langage différentes, vous pouvez aider les utilisateurs internationaux à mieux comprendre le contenu multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="02506-131">In addition, by defining several different language classes, you can help international users better understand the digital media content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02506-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="02506-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02506-133">**Ajout de sous-titres à des médias numériques**</span><span class="sxs-lookup"><span data-stu-id="02506-133">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




