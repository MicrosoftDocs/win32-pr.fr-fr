---
title: Création d’une présentation HTMLView
description: Création d’une présentation HTMLView
ms.assetid: 70203160-2dd9-4096-be6a-c704db757f7f
keywords:
- Sélections de métafichiers Windows Media, présentations HTMLView
- sélections, présentations HTMLView
- sélections de métafichiers, présentations HTMLView
- Sélections de métafichiers Windows Media, création de présentations HTMLView
- sélections, création de présentations HTMLView
- sélections de métafichiers, création de présentations HTMLView
- création de présentations HTMLView
- Windows Media Player, création de présentations HTMLView
- Windows Media Player, présentations HTMLView
- HTMLView, création de présentations
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1094ce787e55fbeb98e628389b5fd51ab94ab415
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380097"
---
# <a name="creating-an-htmlview-presentation"></a><span data-ttu-id="d106c-113">Création d’une présentation HTMLView</span><span class="sxs-lookup"><span data-stu-id="d106c-113">Creating an HTMLView Presentation</span></span>

<span data-ttu-id="d106c-114">Pour créer une présentation HTMLView de base, vous avez besoin d’au moins trois éléments :</span><span class="sxs-lookup"><span data-stu-id="d106c-114">To create a basic HTMLView presentation, you need at least three elements:</span></span>

-   <span data-ttu-id="d106c-115">**Contenu multimédia numérique.**</span><span class="sxs-lookup"><span data-stu-id="d106c-115">**Digital media content.**</span></span> <span data-ttu-id="d106c-116">Il s’agit d’un ou plusieurs fichiers audio ou vidéo que le lecteur Windows Media lit.</span><span class="sxs-lookup"><span data-stu-id="d106c-116">This is one or more audio or video files that Windows Media Player plays.</span></span>
-   <span data-ttu-id="d106c-117">**Une page Web.**</span><span class="sxs-lookup"><span data-stu-id="d106c-117">**A webpage.**</span></span> <span data-ttu-id="d106c-118">Il s’agit du contenu Web qui s’affiche dans la fonctionnalité de **lecture** en cours de l’interface utilisateur du lecteur.</span><span class="sxs-lookup"><span data-stu-id="d106c-118">This is the Web-based content that displays in the **Now Playing** feature of the Player UI.</span></span>
-   <span data-ttu-id="d106c-119">**Métafichier Windows Media.**</span><span class="sxs-lookup"><span data-stu-id="d106c-119">**A Windows Media metafile.**</span></span> <span data-ttu-id="d106c-120">Il s’agit de la sélection de métafichiers qui indique au lecteur Windows Media de combiner le contenu multimédia numérique avec la page Web.</span><span class="sxs-lookup"><span data-stu-id="d106c-120">This is the metafile playlist that directs Windows Media Player to combine the digital media content with the webpage.</span></span>

<span data-ttu-id="d106c-121">Un fichier. asx est un fichier texte qui fournit des informations sur un flux de fichier et sa présentation.</span><span class="sxs-lookup"><span data-stu-id="d106c-121">An .asx file is a text file that provides information about a file stream and its presentation.</span></span> <span data-ttu-id="d106c-122">En fonction de la syntaxe Extensible Markup Language (XML), les fichiers. asx peuvent contenir divers éléments, chacun identifié par une balise avec des attributs associés.</span><span class="sxs-lookup"><span data-stu-id="d106c-122">Based on Extensible Markup Language (XML) syntax, .asx files can contain a variety of elements, each identified by a tag with associated attributes.</span></span> <span data-ttu-id="d106c-123">L’élément **param** permet d’associer un paramètre personnalisé à une entrée particulière dans une sélection de métafichier ou dans le métafichier entier.</span><span class="sxs-lookup"><span data-stu-id="d106c-123">The **PARAM** element provides a way to associate a custom parameter with either a particular entry in a metafile playlist or the entire metafile.</span></span> <span data-ttu-id="d106c-124">L’un des noms de paramètres prédéfinis disponibles pour votre utilisation est « HTMLView ».</span><span class="sxs-lookup"><span data-stu-id="d106c-124">One of the predefined parameter names available for your use is "HTMLView".</span></span> <span data-ttu-id="d106c-125">Il s’agit du paramètre qui permet d’afficher la page Web spécifiée par la valeur de l’URL dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d106c-125">This is the parameter that causes the webpage specified by the URL value to be displayed in Windows Media Player.</span></span>

<span data-ttu-id="d106c-126">L’exemple de code suivant montre un fichier. asx qui combine un fichier multimédia numérique unique à une seule page Web :</span><span class="sxs-lookup"><span data-stu-id="d106c-126">The following example code shows an .asx file that combines a single digital media file with a single webpage:</span></span>


```XML
<ASX version="3.0">
<PARAM name="HTMLView" value="https://www.proseware.com/htmlview.htm"/>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



<span data-ttu-id="d106c-127">Lorsque le lecteur Windows Media ouvre le fichier. asx dans l’exemple précédent, il lit le fichier audio à partir du fichier nommé Content1. WMA et ouvre la page Web nommée htmlview.htm dans la fonctionnalité de **lecture** en cours du lecteur en mode plein.</span><span class="sxs-lookup"><span data-stu-id="d106c-127">When Windows Media Player opens the .asx file in the preceding example, it plays the audio from the file named content1.wma and opens the webpage named htmlview.htm in the **Now Playing** feature of the full-mode Player.</span></span> <span data-ttu-id="d106c-128">L’utilisateur peut suspendre, Rechercher et arrêter le contenu audio à l’aide des commandes du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d106c-128">The user can pause, seek, and stop the audio content using the Windows Media Player controls.</span></span>

<span data-ttu-id="d106c-129">Vous pouvez facilement modifier la page Web affichée pour chaque élément de contenu en associant un élément **param** à chaque entrée, comme le montre l’exemple de code suivant :</span><span class="sxs-lookup"><span data-stu-id="d106c-129">You can easily change the webpage that is displayed for each piece of content by associating a **PARAM** element with each entry, as the following code example shows:</span></span>


```XML
<ASX version="3.0">

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview2.htm"/>
   <REF href="rtsp://www.proseware.com/content2.wma"/>
</ENTRY>

</ASX>

```



<span data-ttu-id="d106c-130">Dans l’exemple précédent, le lecteur Windows Media affiche d’abord la page Web htmlview1.htm lors de la lecture du fichier audio numérique Content1. WMA.</span><span class="sxs-lookup"><span data-stu-id="d106c-130">In the preceding example, Windows Media Player first displays the webpage htmlview1.htm while playing the digital audio file content1.wma.</span></span> <span data-ttu-id="d106c-131">Lorsque le joueur ouvre l’entrée suivante dans la playlist, Content2. WMA, la page Web affichée dans **lecture** passe à htmlview2.htm.</span><span class="sxs-lookup"><span data-stu-id="d106c-131">When the Player opens the next entry in the playlist, content2.wma, the webpage displayed in **Now Playing** changes to htmlview2.htm.</span></span> <span data-ttu-id="d106c-132">De cette façon, vous pouvez spécifier la page Web que l’utilisateur voit pour chaque morceau de contenu multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="d106c-132">In this way, you can specify which webpage the user sees for each piece of digital media content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d106c-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d106c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d106c-134">**Affichage des pages Web dans le lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d106c-134">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="d106c-135">**Élément PARAM**</span><span class="sxs-lookup"><span data-stu-id="d106c-135">**PARAM Element**</span></span>](param-element.md)
</dt> </dl>

 

 




