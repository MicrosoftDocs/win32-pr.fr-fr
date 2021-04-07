---
title: Utilisation d’une sélection de métafichiers
description: Utilisation d’une sélection de métafichiers
ms.assetid: e6cbdb76-4405-409e-93c3-38a3baa7c231
keywords:
- Sélections de métafichiers Windows Media, utilisation
- sélections de métafichiers, utilisation
- sélections, utilisation
- Sélections de métafichiers Windows Media, à propos de
- sélections de métafichiers, à propos de
- sélections, à propos de
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a5f1832c0c739874fbbd4db219f2c622fc2debfa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672766"
---
# <a name="using-a-metafile-playlist"></a><span data-ttu-id="7efeb-109">Utilisation d’une sélection de métafichiers</span><span class="sxs-lookup"><span data-stu-id="7efeb-109">Using a Metafile Playlist</span></span>

<span data-ttu-id="7efeb-110">Étant donné que vous ne pouvez pas lier directement d’une page Web à un serveur multimédia de diffusion en continu, vous utilisez des sélections de métafichiers.</span><span class="sxs-lookup"><span data-stu-id="7efeb-110">Because you cannot link directly from a webpage to a streaming media server, you use metafile playlists.</span></span> <span data-ttu-id="7efeb-111">Les sélections de métafichiers contiennent les informations requises par le lecteur Windows Media et sont stockées sur un serveur Web.</span><span class="sxs-lookup"><span data-stu-id="7efeb-111">The metafile playlists contain the information needed by Windows Media Player and are stored on a web server.</span></span> <span data-ttu-id="7efeb-112">Vous pouvez ensuite créer un lien à partir du document Web vers une sélection de métafichiers.</span><span class="sxs-lookup"><span data-stu-id="7efeb-112">You can then link from the Web document to a metafile playlist.</span></span> <span data-ttu-id="7efeb-113">Lorsqu’une sélection de métafichier est ouverte, le contrôle est transféré vers le lecteur Windows Media, qui traite le fichier, se connecte au serveur de diffusion multimédia en continu et lit le contenu spécifié.</span><span class="sxs-lookup"><span data-stu-id="7efeb-113">When a metafile playlist is opened, control transfers to Windows Media Player, which processes the file, connects to the streaming media server, and plays the specified content.</span></span>

<span data-ttu-id="7efeb-114">Le navigateur télécharge d’abord la sélection de métafichiers dans le répertoire de cache de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7efeb-114">The browser first downloads the metafile playlist to the user's cache directory.</span></span> <span data-ttu-id="7efeb-115">Étant donné que la sélection de métafichiers est petite, il s’agit d’une étape très rapide.</span><span class="sxs-lookup"><span data-stu-id="7efeb-115">Because the metafile playlist is small, this is a very quick step.</span></span> <span data-ttu-id="7efeb-116">L’ordinateur de l’utilisateur trouve ensuite dans son tableau associations de fichiers l’Association de la sélection de métafichiers avec le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7efeb-116">The user's computer then finds in its file associations table the association of the metafile playlist with Windows Media Player.</span></span> <span data-ttu-id="7efeb-117">Le lecteur Windows Media ouvre et interprète les scripts dans la sélection de métafichiers, qui contient, entre autres choses, l’URL du contenu de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="7efeb-117">Windows Media Player opens and interprets the scripting in the metafile playlist, which contains, among other things, the URL of the streaming content.</span></span> <span data-ttu-id="7efeb-118">Le lecteur Windows Media utilise l’URL pour localiser le contenu et initier le flux.</span><span class="sxs-lookup"><span data-stu-id="7efeb-118">Windows Media Player uses the URL to locate the content and initiate the stream.</span></span> <span data-ttu-id="7efeb-119">Le script de sélection de métafichiers contrôle ensuite l’expérience de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="7efeb-119">The metafile playlist scripting then controls the streaming experience.</span></span>

<span data-ttu-id="7efeb-120">Étant donné que les playlists de métafichiers fonctionnent par le biais d’une application auxiliaire associée au type ASXMIME (application/Mplayer2 ou Video/x-ms-asf), elles sont compatibles avec n’importe quel navigateur prenant en charge les applications auxiliaires.</span><span class="sxs-lookup"><span data-stu-id="7efeb-120">Because metafile playlists work through a helper application associated with the ASXMIME type (application/mplayer2 or video/x-ms-asf), they are compatible with any browser that supports helper applications.</span></span> <span data-ttu-id="7efeb-121">Les exemples présentés dans ce document fonctionnent avec Microsoft Internet Explorer 4,0 et versions ultérieures, et avec Netscape Navigator 4,0 et versions ultérieures sur les plateformes Microsoft Win32® et Apple Macintosh.</span><span class="sxs-lookup"><span data-stu-id="7efeb-121">The examples shown in this document will work with Microsoft Internet Explorer 4.0 and later, and with Netscape Navigator 4.0 and later on Microsoft Win32® and Apple Macintosh platforms.</span></span> <span data-ttu-id="7efeb-122">Dans tous les exemples, vous devez vous assurer que tous les fichiers multimédias numériques référencés ont des chemins d’accès et des noms de fichiers valides pour votre environnement.</span><span class="sxs-lookup"><span data-stu-id="7efeb-122">In all examples, you will have to be sure that any digital media files referenced have valid paths and file names for your environment.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7efeb-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7efeb-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7efeb-124">**Guide des métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="7efeb-124">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> <dt>

[<span data-ttu-id="7efeb-125">**Informations de référence sur les métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="7efeb-125">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> <dt>

[<span data-ttu-id="7efeb-126">**Présentation des fichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="7efeb-126">**Windows Media Metafiles Overview**</span></span>](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




