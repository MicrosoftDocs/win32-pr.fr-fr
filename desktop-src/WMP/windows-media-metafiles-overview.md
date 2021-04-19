---
title: Présentation des fichiers Windows Media
description: Présentation des fichiers Windows Media
ms.assetid: 5b7742c0-f416-4bf4-ae03-9554b51fe620
keywords:
- Fichiers Windows Media, à propos de
- Lecteur Windows Media, fichiers
- Windows Media Player, Windows Media
- refichiers, à propos de
- Windows Media, sous-fichiers
- Sélections de métafichiers Windows Media, à propos de
- sélections, à propos de
- Fichiers Windows Media, syntaxe
- refichiers, syntaxe
- sélections de métafichiers, à propos de
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e7ed86cca023103c044f28141e0212542d83d200
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106517954"
---
# <a name="windows-media-metafiles-overview"></a><span data-ttu-id="508bb-113">Présentation des fichiers Windows Media</span><span class="sxs-lookup"><span data-stu-id="508bb-113">Windows Media Metafiles Overview</span></span>

<span data-ttu-id="508bb-114">La partie la plus importante de l’utilisation correcte des métafichiers Windows Media est l’utilisation de la syntaxe correcte pour les éléments de métafichier.</span><span class="sxs-lookup"><span data-stu-id="508bb-114">The most important part of successfully using Windows Media metafiles is using the correct syntax for the metafile elements.</span></span> <span data-ttu-id="508bb-115">Les erreurs de syntaxe dans un métafichier Windows Media peuvent entraîner la non-reconnaissance d’un attribut unique dans le métafichier qui n’est pas reconnu comme étant valide et qui ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="508bb-115">Syntax errors in a Windows Media metafile can cause anything from a single attribute being overlooked, to the metafile not being recognized as valid and failing to work.</span></span>

<span data-ttu-id="508bb-116">Presque aussi important est l’ordre dans lequel les éléments apparaissent dans un métafichier Windows Media.</span><span class="sxs-lookup"><span data-stu-id="508bb-116">Almost as important is the order in which the elements appear in a Windows Media metafile.</span></span> <span data-ttu-id="508bb-117">Les attributs de certains éléments substituent temporairement les attributs des éléments similaires dans différentes sections du métafichier.</span><span class="sxs-lookup"><span data-stu-id="508bb-117">The attributes of some elements temporarily override the attributes of similar elements in different sections of the metafile.</span></span> <span data-ttu-id="508bb-118">Il existe un [ordre de priorité](order-of-precedence.md)défini.</span><span class="sxs-lookup"><span data-stu-id="508bb-118">There is a defined [Order of Precedence](order-of-precedence.md).</span></span>

<span data-ttu-id="508bb-119">Les sélections de métafichiers Windows Media sont des métafichiers Windows Media qui fournissent des informations que le lecteur Windows Media utilise pour recevoir des flux de monodiffusion, des flux de multidiffusion et d’autres supports pris en charge à partir d’un intranet ou d’Internet.</span><span class="sxs-lookup"><span data-stu-id="508bb-119">Windows Media metafile playlists are Windows Media metafiles that provide information that Windows Media Player uses to receive unicast streams, multicast streams, and other supported media from an intranet or the Internet.</span></span> <span data-ttu-id="508bb-120">Une sélection de métafichiers est fondamentalement un raccourci vers du contenu multimédia.</span><span class="sxs-lookup"><span data-stu-id="508bb-120">A metafile playlist is basically a shortcut to media content.</span></span> <span data-ttu-id="508bb-121">Une sélection de métafichier peut être envoyée sous forme de courrier électronique, utilisée en tant que référence de lien sur une page Web, créée dynamiquement à l’aide de pages Active Server (ASP) ou en tant que fichier autonome sur un lecteur de disque local.</span><span class="sxs-lookup"><span data-stu-id="508bb-121">A metafile playlist can be sent as email, used as a link reference on a webpage, created dynamically using Active Server Pages (ASP), or exist as a stand-alone file on a local disk drive.</span></span> <span data-ttu-id="508bb-122">Une sélection de métafichiers peut faire référence à une autre sélection de métafichiers, à une page ASP ou à un fichier de station Windows Media (avec une extension de nom de fichier. NSC).</span><span class="sxs-lookup"><span data-stu-id="508bb-122">A metafile playlist can reference another metafile playlist, an ASP page, or a Windows Media station file (with an .nsc file name extension).</span></span> <span data-ttu-id="508bb-123">Un fichier. NSC est utilisé pour définir une station Windows Media sur le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="508bb-123">An .nsc file is used to define a Windows Media station to Windows Media Player.</span></span> <span data-ttu-id="508bb-124">Le processus de gestion de base est le même pour chaque cas.</span><span class="sxs-lookup"><span data-stu-id="508bb-124">The basic handling process is the same for each case.</span></span>

## <a name="related-topics"></a><span data-ttu-id="508bb-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="508bb-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="508bb-126">**À propos des fichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="508bb-126">**About Windows Media Metafiles**</span></span>](about-windows-media-metafiles.md)
</dt> </dl>

 

 




