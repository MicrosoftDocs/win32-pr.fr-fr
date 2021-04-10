---
title: Redirection
description: Redirection
ms.assetid: c8e3b43f-c11a-4ca7-b85c-038f0bfc3eb3
keywords:
- Sélections de métafichiers Windows Media, redirection
- listes de sélection, redirection
- sélections de métafichiers, redirection
- Lecteur Windows Media, redirection
- redirection
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf1bb4d690c8aa6808e009a45a7bff1d6efada72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309326"
---
# <a name="redirection"></a><span data-ttu-id="3bf0e-108">Redirection</span><span class="sxs-lookup"><span data-stu-id="3bf0e-108">Redirection</span></span>

<span data-ttu-id="3bf0e-109">La sélection permet de rediriger le navigateur vers le lecteur Windows Media pour lire le fichier multimédia ou le flux de média désigné.</span><span class="sxs-lookup"><span data-stu-id="3bf0e-109">The playlist will redirect the browser to Windows Media Player to play the designated media stream or media file.</span></span> <span data-ttu-id="3bf0e-110">La sélection de métafichier la plus basique contient uniquement l’Uniform Resource Locator (URL) d’un fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="3bf0e-110">The most basic metafile playlist contains only the Uniform Resource Locator (URL) of a media file.</span></span>

<span data-ttu-id="3bf0e-111">Pour créer une sélection de métafichier de base, ouvrez votre éditeur de texte favori, tel que le bloc-notes Microsoft, puis tapez l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="3bf0e-111">To create a basic metafile playlist, open your favorite text editor, such as Microsoft Notepad, and type the following example code.</span></span>


```XML
<ASX version="3.0">
   <ENTRY>
      <REF HREF="PathToYourFile"/>
   </ENTRY>
</ASX>

```



<span data-ttu-id="3bf0e-112">Remplacez un chemin d’accès valide à votre fichier Windows Media à l’aide de la syntaxe du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3bf0e-112">Substitute a valid path to your Windows Media file using the syntax in the following table.</span></span>



| <span data-ttu-id="3bf0e-113">Source de contenu</span><span class="sxs-lookup"><span data-stu-id="3bf0e-113">Source of content</span></span>                                                                                 | <span data-ttu-id="3bf0e-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3bf0e-114">Syntax</span></span>                                    |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="3bf0e-115">Le contenu est un fichier sur un serveur Windows Media</span><span class="sxs-lookup"><span data-stu-id="3bf0e-115">Content is a file on a Windows Media server</span></span>                                                       | <span data-ttu-id="3bf0e-116">mms://ServerName/Path/FileName.wma</span><span class="sxs-lookup"><span data-stu-id="3bf0e-116">mms://ServerName/Path/FileName.wma</span></span>        |
| <span data-ttu-id="3bf0e-117">Le contenu est une multidiffusion de diffusion accessible à partir d’une station Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3bf0e-117">Content is a broadcast multicast that is accessed from a Windows Media station</span></span>                    | https://WebServerName/Stations/kxyz.nsc    |
| <span data-ttu-id="3bf0e-118">Le contenu est une monodiffusion de diffusion accessible à partir d’un point de publication sur un serveur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3bf0e-118">Content is a broadcast unicast that is accessed from a publishing point on a Windows Media server</span></span> | <span data-ttu-id="3bf0e-119">mms://ServerName/PublishingPointAlias</span><span class="sxs-lookup"><span data-stu-id="3bf0e-119">mms://ServerName/PublishingPointAlias</span></span>     |
| <span data-ttu-id="3bf0e-120">Le contenu est un fichier sur un serveur Web</span><span class="sxs-lookup"><span data-stu-id="3bf0e-120">Content is a file on a web server</span></span>                                                                 | https://WebServerName/Path/Filename.wma    |
| <span data-ttu-id="3bf0e-121">Le contenu est un fichier sur un disque dur local</span><span class="sxs-lookup"><span data-stu-id="3bf0e-121">Content is a file on a local hard disk</span></span>                                                            | <span data-ttu-id="3bf0e-122">file://c : \\ chemin \\ nom_de_fichier. WMA</span><span class="sxs-lookup"><span data-stu-id="3bf0e-122">file://c:\\Path\\Filename.wma</span></span>             |
| <span data-ttu-id="3bf0e-123">Le contenu est un fichier sur un partage réseau</span><span class="sxs-lookup"><span data-stu-id="3bf0e-123">Content is a file on a network share</span></span>                                                              | <span data-ttu-id="3bf0e-124">file:// \\ \\ nom_serveur \\ chemin \\ nom_de_fichier. WMA</span><span class="sxs-lookup"><span data-stu-id="3bf0e-124">file://\\\\ServerName\\Path\\Filename.wma</span></span> |
| <span data-ttu-id="3bf0e-125">Le contenu est un fichier sur un serveur Windows Media</span><span class="sxs-lookup"><span data-stu-id="3bf0e-125">Content is a file on a Windows Media server</span></span>                                                       | <span data-ttu-id="3bf0e-126">mms://ServerName/Path/FileName.wmv</span><span class="sxs-lookup"><span data-stu-id="3bf0e-126">mms://ServerName/Path/FileName.wmv</span></span>        |



 

<span data-ttu-id="3bf0e-127">Enregistrez le fichier que vous avez créé avec un nom de fichier et une extension, comme décrit dans [extensions de noms de fichiers](file-name-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="3bf0e-127">Save the file you have created with a file name and extension as described in [File Name Extensions](file-name-extensions.md).</span></span> <span data-ttu-id="3bf0e-128">Double-cliquez dessus dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="3bf0e-128">Double-click it in Windows Explorer.</span></span> <span data-ttu-id="3bf0e-129">Le lecteur Windows Media doit ouvrir et démarrer la diffusion en continu du contenu.</span><span class="sxs-lookup"><span data-stu-id="3bf0e-129">Windows Media Player should open and start streaming the content.</span></span> <span data-ttu-id="3bf0e-130">Vous pouvez enregistrer le fichier sur votre serveur Web, avec vos pages Web, et le lier à un élément **href** , ou l’incorporer dans une page Web à l’aide de la balise d' **objet** du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3bf0e-130">You can save the file to your web server, along with your webpages, and link to it with an **HREF** element, or embed it in a webpage using the Windows Media Player **OBJECT** tag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3bf0e-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3bf0e-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bf0e-132">**Sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="3bf0e-132">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="3bf0e-133">**Utilisation des sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="3bf0e-133">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="3bf0e-134">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="3bf0e-134">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="3bf0e-135">**Guide des métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="3bf0e-135">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




