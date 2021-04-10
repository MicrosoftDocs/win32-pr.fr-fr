---
title: Guide des métafichiers Windows Media
description: Guide des métafichiers Windows Media
ms.assetid: d2360a63-f073-44b0-8637-1f22b577f51a
keywords:
- Fichiers Windows Media, à propos de
- Lecteur Windows Media, fichiers
- Windows Media Player, Windows Media
- refichiers, à propos de
- Windows Media, sous-fichiers
- Sélections de métafichiers Windows Media, à propos de
- sélections, à propos de
- sélections de métafichiers, à propos de
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fcf0a4c98ae49d1cdf3b7e36e8a278f184cd4632
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940274"
---
# <a name="windows-media-metafile-guide"></a><span data-ttu-id="afd13-111">Guide des métafichiers Windows Media</span><span class="sxs-lookup"><span data-stu-id="afd13-111">Windows Media Metafile Guide</span></span>

<span data-ttu-id="afd13-112">Un métafichier Windows Media peut être aussi simple ou complexe que vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="afd13-112">A Windows Media metafile can be as simple or complex as you need it to be.</span></span> <span data-ttu-id="afd13-113">Le métafichier Windows Media le plus basique contient uniquement l’Uniform Resource Locator (URL) de certains contenus multimédias sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="afd13-113">The most basic Windows Media metafile contains only the Uniform Resource Locator (URL) of some multimedia content on a server.</span></span> <span data-ttu-id="afd13-114">Le client, le lecteur Windows Media, analyse ces informations, puis ouvre le fichier multimédia ou le flux défini dans le métafichier Windows Media.</span><span class="sxs-lookup"><span data-stu-id="afd13-114">The client, Windows Media Player, parses this information and then opens the media file or stream defined in the Windows Media metafile.</span></span> <span data-ttu-id="afd13-115">Un métafichier complexe peut contenir plusieurs fichiers ou flux organisés dans une sélection, des instructions sur la façon de lire les fichiers, les flux, le texte et les éléments graphiques tels que le titre, l’auteur et le texte de copyright, l’insertion de publicité personnalisée dans un flux en direct, des liens hypertexte associés à des éléments de l’interface du lecteur Windows Media, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="afd13-115">A complex metafile can contain multiple files or streams arranged in a playlist, instructions on how to play the files or streams, text and graphic elements such as title, author, and copyright text, personalized ad insertion into a live stream, hyperlinks associated with elements on the Windows Media Player interface, and more.</span></span>

<span data-ttu-id="afd13-116">Les sections suivantes fournissent des informations détaillées sur la création et l’utilisation des sélections de métafichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="afd13-116">The following sections provide detailed information on how to create and use Windows Media metafile playlists.</span></span>



| <span data-ttu-id="afd13-117">Section</span><span class="sxs-lookup"><span data-stu-id="afd13-117">Section</span></span>                                                            | <span data-ttu-id="afd13-118">Description</span><span class="sxs-lookup"><span data-stu-id="afd13-118">Description</span></span>                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="afd13-119">Types de sélections</span><span class="sxs-lookup"><span data-stu-id="afd13-119">Types of Playlists</span></span>](types-of-playlists.md)                       | <span data-ttu-id="afd13-120">Répertorie les extensions de nom de fichier disponibles.</span><span class="sxs-lookup"><span data-stu-id="afd13-120">Lists available file name extensions.</span></span>                                               |
| [<span data-ttu-id="afd13-121">Création de sélections de métafichiers</span><span class="sxs-lookup"><span data-stu-id="afd13-121">Creating Metafile Playlists</span></span>](creating-metafile-playlists.md)     | <span data-ttu-id="afd13-122">Décrit comment créer des sélections de métafichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="afd13-122">Describes how to create Windows Media metafile playlists.</span></span>                           |
| [<span data-ttu-id="afd13-123">Sélections de métafichiers</span><span class="sxs-lookup"><span data-stu-id="afd13-123">Metafile Playlists</span></span>](metafile-playlists.md)                       | <span data-ttu-id="afd13-124">Décrit l’utilisation des sélections de métafichiers, les scripts, les métadonnées et le traitement.</span><span class="sxs-lookup"><span data-stu-id="afd13-124">Describes metafile playlist usage, scripting, metadata, and processing.</span></span>             |
| [<span data-ttu-id="afd13-125">Instructions relatives aux extensions de métafichiers</span><span class="sxs-lookup"><span data-stu-id="afd13-125">Metafile Extension Guidelines</span></span>](metafile-extension-guidelines.md) | <span data-ttu-id="afd13-126">Décrit l’utilisation par défaut des extensions de nom de fichier pour la diffusion de fichiers multimédias.</span><span class="sxs-lookup"><span data-stu-id="afd13-126">Describes the preferred use of file name extensions for streaming media files.</span></span>      |
| [<span data-ttu-id="afd13-127">Ordre de priorité</span><span class="sxs-lookup"><span data-stu-id="afd13-127">Order of Precedence</span></span>](order-of-precedence.md)                     | <span data-ttu-id="afd13-128">Décrit comment les éléments de la sélection de métafichiers remplacent les autres éléments de sélection de métafichier.</span><span class="sxs-lookup"><span data-stu-id="afd13-128">Describes how metafile playlist elements override other metafile playlist elements.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="afd13-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="afd13-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afd13-130">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="afd13-130">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="afd13-131">**Fichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="afd13-131">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 




