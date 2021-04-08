---
title: Utilisation des sélections de métafichiers
description: Utilisation des sélections de métafichiers
ms.assetid: f5711a7f-7674-4b92-8262-cee8bac4aa77
keywords:
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
ms.openlocfilehash: 71f245d1fc1610174f842347a15dfcfaa13286e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839558"
---
# <a name="using-metafile-playlists"></a><span data-ttu-id="43fd3-106">Utilisation des sélections de métafichiers</span><span class="sxs-lookup"><span data-stu-id="43fd3-106">Using Metafile Playlists</span></span>

<span data-ttu-id="43fd3-107">Les sélections spécifient la façon dont les fichiers multimédias ou multimédia de diffusion en continu sont lus et les métadonnées affichées par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="43fd3-107">Playlists specify how the streaming media or media files will be played and what metadata Windows Media Player will display.</span></span>

<span data-ttu-id="43fd3-108">Cette section décrit plusieurs façons d’utiliser des sélections.</span><span class="sxs-lookup"><span data-stu-id="43fd3-108">This section explains several ways you can use playlists.</span></span> <span data-ttu-id="43fd3-109">La section est composée des rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="43fd3-109">The section is divided into the following topics.</span></span>



| <span data-ttu-id="43fd3-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="43fd3-110">Topic</span></span>                                                                                              | <span data-ttu-id="43fd3-111">Description</span><span class="sxs-lookup"><span data-stu-id="43fd3-111">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43fd3-112">Modification de l’affichage</span><span class="sxs-lookup"><span data-stu-id="43fd3-112">Modifying the Display</span></span>](modifying-the-display.md)                                                 | <span data-ttu-id="43fd3-113">Ajouter du texte, des liens et des images.</span><span class="sxs-lookup"><span data-stu-id="43fd3-113">Adding text, links, and images.</span></span>                                                                                                                                |
| [<span data-ttu-id="43fd3-114">Redirection</span><span class="sxs-lookup"><span data-stu-id="43fd3-114">Redirection</span></span>](redirection.md)                                                                     | <span data-ttu-id="43fd3-115">Utilisation des sélections pour rediriger le navigateur vers le lecteur Windows Media et spécifier l’URL d’un flux ou d’un fichier multimédia à lire.</span><span class="sxs-lookup"><span data-stu-id="43fd3-115">Using playlists to redirect the browser to Windows Media Player and specifying the URL of a stream or media file to play.</span></span>                                      |
| [<span data-ttu-id="43fd3-116">Accès au média</span><span class="sxs-lookup"><span data-stu-id="43fd3-116">Accessing Media</span></span>](accessing-media.md)                                                             | <span data-ttu-id="43fd3-117">Utilisation d’éléments de métafichier et de leurs éléments enfants pour spécifier le contenu auquel accéder, ainsi que l’ordre et la durée de leur lecture.</span><span class="sxs-lookup"><span data-stu-id="43fd3-117">Using metafile elements and their child elements to specify the content to access, and the order and duration of their playback.</span></span>                               |
| [<span data-ttu-id="43fd3-118">Utilisation du basculement de flux d’événements en temps réel</span><span class="sxs-lookup"><span data-stu-id="43fd3-118">Using Live Event Stream Switching</span></span>](using-live-event-stream-switching.md)                         | <span data-ttu-id="43fd3-119">Utilisation de l’élément **Event** pour spécifier un flux multimédia auquel accéder, puis reprendre la diffusion du flux d’origine.</span><span class="sxs-lookup"><span data-stu-id="43fd3-119">Using the **EVENT** element to specify a media stream to access and then resume playing the original stream.</span></span> <span data-ttu-id="43fd3-120">Utilisé pour l’insertion d’AD.</span><span class="sxs-lookup"><span data-stu-id="43fd3-120">Used for ad insertion.</span></span>                            |
| [<span data-ttu-id="43fd3-121">Utilisation de safiles pour basculer en continu</span><span class="sxs-lookup"><span data-stu-id="43fd3-121">Using Metafiles for Seamless Stream Switching</span></span>](using-metafiles-for-seamless-stream-switching.md) | <span data-ttu-id="43fd3-122">Utilisation de l’élément **Event** pour précharger le flux multimédia suivant afin d’éviter les écarts dans la présentation.</span><span class="sxs-lookup"><span data-stu-id="43fd3-122">Using the **EVENT** element to preload the next media stream to access to avoid gaps in the presentation.</span></span>                                                      |
| [<span data-ttu-id="43fd3-123">Utilisation d’annonces</span><span class="sxs-lookup"><span data-stu-id="43fd3-123">Using Announcements</span></span>](using-announcements.md)                                                     | <span data-ttu-id="43fd3-124">Utilisation d’un métafichier pour fournir des informations sur l’URL d’un flux multimédia, y compris l’adresse IP de multidiffusion, le port, le format de flux et d’autres paramètres de station.</span><span class="sxs-lookup"><span data-stu-id="43fd3-124">Using a metafile to provide information about the URL for a media stream, including the multicast IP address, port, stream format, and other station settings.</span></span> |
| [<span data-ttu-id="43fd3-125">Utilisation de la substitution d’URL et de serveur</span><span class="sxs-lookup"><span data-stu-id="43fd3-125">Using URL and Server Rollover</span></span>](using-url-and-server-rollover.md)                                 | <span data-ttu-id="43fd3-126">Utilisation de sélections de métafichiers pour fournir un moyen de basculer automatiquement vers d’autres sources de contenu lorsqu’un flux n’est pas accessible ou lu.</span><span class="sxs-lookup"><span data-stu-id="43fd3-126">Using metafile playlists to provide a means of automatically rolling over to alternate content sources when a stream cannot be accessed or played.</span></span>             |
| [<span data-ttu-id="43fd3-127">Utilisation de paramètres et de commandes personnalisés</span><span class="sxs-lookup"><span data-stu-id="43fd3-127">Using Custom Parameters and Commands</span></span>](using-custom-parameters-and-commands.md)                   | <span data-ttu-id="43fd3-128">Utilisation de l’élément **param** pour définir des éléments personnalisés afin de fournir des métadonnées supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="43fd3-128">Using the **PARAM** element to define custom elements to provide additional metadata.</span></span>                                                                          |
| [<span data-ttu-id="43fd3-129">Personnalisation de la distribution des médias</span><span class="sxs-lookup"><span data-stu-id="43fd3-129">Personalizing Media Delivery</span></span>](personalizing-media-delivery.md)                                   | <span data-ttu-id="43fd3-130">Utilisation des préférences utilisateur pour déterminer le contenu de la diffusion.</span><span class="sxs-lookup"><span data-stu-id="43fd3-130">Using user preferences to determine broadcast content.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="43fd3-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="43fd3-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43fd3-132">**Sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="43fd3-132">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="43fd3-133">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="43fd3-133">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="43fd3-134">**Guide des métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="43fd3-134">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




