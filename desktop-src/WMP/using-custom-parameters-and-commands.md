---
title: Utilisation de paramètres et de commandes personnalisés
description: Utilisation de paramètres et de commandes personnalisés
ms.assetid: 6b0bfd19-1672-41e3-9b7f-c8d541168c0e
keywords:
- Sélections de métafichiers Windows Media, paramètres personnalisés
- sélections, paramètres personnalisés
- sélections de métafichiers, paramètres personnalisés
- Sélections de métafichiers Windows Media, commandes personnalisées
- sélections, commandes personnalisées
- sélections de métafichiers, commandes personnalisées
- Sélections de métafichiers Windows Media, paramètres
- sélections, paramètres
- sélections de métafichiers, paramètres
- paramètres personnalisés
- commandes personnalisées
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59f577fa4f3af71799b163389f85987d8723e045
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840210"
---
# <a name="using-custom-parameters-and-commands"></a><span data-ttu-id="e2e49-114">Utilisation de paramètres et de commandes personnalisés</span><span class="sxs-lookup"><span data-stu-id="e2e49-114">Using Custom Parameters and Commands</span></span>

<span data-ttu-id="e2e49-115">Vous pouvez créer des paramètres personnalisés pour passer des métadonnées supplémentaires dans une sélection de métafichiers à l’aide de l’élément **param** .</span><span class="sxs-lookup"><span data-stu-id="e2e49-115">You can create custom parameters to pass additional metadata in a metafile playlist by using the **PARAM** element.</span></span> <span data-ttu-id="e2e49-116">Utilisez l’attribut **Name** de l’élément **param** pour définir le nom du paramètre personnalisé.</span><span class="sxs-lookup"><span data-stu-id="e2e49-116">Use the **NAME** attribute of the **PARAM** element to define the custom parameter name.</span></span> <span data-ttu-id="e2e49-117">Utilisez l’attribut **value** pour définir la valeur du paramètre personnalisé nommé.</span><span class="sxs-lookup"><span data-stu-id="e2e49-117">Use the **VALUE** attribute to define the value for the named custom parameter.</span></span>

<span data-ttu-id="e2e49-118">Récupérez les métadonnées **param** à l’aide des méthodes **GetItemInfo** des objets **média** et **playlist** .</span><span class="sxs-lookup"><span data-stu-id="e2e49-118">Retrieve **PARAM** metadata by using the **getItemInfo** methods of the **Media** and **Playlist** objects.</span></span> <span data-ttu-id="e2e49-119">Pour obtenir un exemple d’utilisation de ces méthodes pour récupérer des métadonnées, consultez la méthode [attributeCount](playlist-attributecount.md) de l’objet **playlist** .</span><span class="sxs-lookup"><span data-stu-id="e2e49-119">For an example using these methods to retrieve metadata, see the [attributeCount](playlist-attributecount.md) method of the **Playlist** object.</span></span>

<span data-ttu-id="e2e49-120">L’exemple de sélection de métafichier suivant illustre l’utilisation de l’élément **param** pour définir des paramètres personnalisés.</span><span class="sxs-lookup"><span data-stu-id="e2e49-120">The following example metafile playlist shows the use of the **PARAM** element to define custom parameters.</span></span>


```XML
<ASX version="3.0" BANNERBAR="auto" >
    <TITLE>Example Media Player Show</TITLE>
    <PARAM NAME="Director" VALUE="Jane D." />

    <ENTRY>
        <TITLE>Example Clip</TITLE>
        <REF HREF="https://www.proseware.com/media.wma" />
        <PARAM NAME="Title" VALUE="Example Clip" />
        <PARAM NAME="Location" VALUE="North America" />
        <PARAM NAME="Release Date" VALUE="March 1998" />
    </ENTRY>

    <ENTRY>
        <TITLE>Another Clip</TITLE>
        <REF HREF="https://www.proseware.com/more_media.wma" />
        <PARAM NAME="Title" VALUE="Another Clip" />
        <PARAM NAME="Location" VALUE="Japan" />
        <PARAM NAME="Release Date" VALUE="December 2000" />
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="e2e49-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e2e49-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2e49-122">**Utilisation des sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="e2e49-122">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> </dl>

 

 




