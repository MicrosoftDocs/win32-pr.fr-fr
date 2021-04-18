---
title: Utilisation d’annonces
description: Utilisation d’annonces
ms.assetid: c372a4f8-2355-4c69-bba2-72b224879c4d
keywords:
- Sélections de métafichiers Windows Media, annonces
- sélections, annonces
- sélections de métafichiers, annonces
- Windows Media Player, annonces
- annonces
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c16fafee1984d08992b96c39d7c3893ea54f682
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512242"
---
# <a name="using-announcements"></a><span data-ttu-id="951c9-108">Utilisation d’annonces</span><span class="sxs-lookup"><span data-stu-id="951c9-108">Using Announcements</span></span>

<span data-ttu-id="951c9-109">Une annonce est un fichier qui contient des informations sur l’URL d’un flux multimédia, y compris l’adresse IP de multidiffusion, le port, le format de flux et d’autres paramètres de station.</span><span class="sxs-lookup"><span data-stu-id="951c9-109">An announcement is a file that contains information about the URL for a media stream, including the multicast IP address, port, stream format, and other station settings.</span></span> <span data-ttu-id="951c9-110">Les annonces sont créées par l’administrateur Windows Media lors de la création d’un flux de publication de monodiffusion ou de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="951c9-110">Announcements are created by Windows Media Administrator when a unicast or multicast publishing stream is created.</span></span> <span data-ttu-id="951c9-111">Le client peut charger rapidement le fichier d’annonce, puis continuer à accéder au fichier multimédia de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="951c9-111">The client can quickly load the announcement file, then proceed to access the streaming media file.</span></span>

<span data-ttu-id="951c9-112">Pour un point de publication monodiffusion, le flux de média du point de publication est ouvert.</span><span class="sxs-lookup"><span data-stu-id="951c9-112">For a unicast publishing point, the publishing point media stream is opened.</span></span> <span data-ttu-id="951c9-113">Pour un point de publication de multidiffusion, l’URL est extraite d’un fichier de station de diffusion avec une extension. NSC et le média de streaming est accessible.</span><span class="sxs-lookup"><span data-stu-id="951c9-113">For a multicast publishing point, the URL is extracted from a broadcast station file with an .nsc extension, and the streaming media is accessed.</span></span> <span data-ttu-id="951c9-114">Contrairement à un flux de données en monodiffusion, aucune information d’en-tête n’est contenue dans un flux de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="951c9-114">Unlike a unicast stream, no header information is contained in a multicast stream.</span></span> <span data-ttu-id="951c9-115">Ces informations proviennent du fichier de station de diffusion avec une extension. NSC.</span><span class="sxs-lookup"><span data-stu-id="951c9-115">That information comes from the broadcast station file with an .nsc extension.</span></span> <span data-ttu-id="951c9-116">Le lecteur Windows Media ouvre généralement d’abord un fichier d’annonce, qui est une utilisation pour les sélections de métafichiers, qui pointe vers l’emplacement du fichier de station de diffusion.</span><span class="sxs-lookup"><span data-stu-id="951c9-116">Windows Media Player usually first opens an announcement file, which is one use for metafile playlists, that points to the location of the broadcast station file.</span></span>

<span data-ttu-id="951c9-117">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="951c9-117">Example Code</span></span>


```XML
<ASX VERSION="3.0">
    <TITLE>title</TITLE>
    <ENTRY>
        <REF HREF="mms://proseware.com/pubpoint"/>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="951c9-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="951c9-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="951c9-119">**Création de sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="951c9-119">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="951c9-120">**Utilisation des sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="951c9-120">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> </dl>

 

 




