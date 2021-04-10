---
title: Récupération de métadonnées
description: Récupération de métadonnées
ms.assetid: f634118a-0a62-4407-8be1-a907347de55b
keywords:
- Sélections de métafichiers Windows Media, récupération des métadonnées
- sélections, récupération de métadonnées
- sélections de métafichiers, récupération des métadonnées
- Sélections de métafichiers Windows Media, récupération des métadonnées
- sélections, récupération des métadonnées
- sélections de métafichiers, récupération de métadonnées
- métadonnées, récupération
- récupération de métadonnées
- Lecteur Windows Media, récupération des métadonnées
- Lecteur Windows Media, récupération des métadonnées
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c9855ec1dc95a52429561e91aa82abdac088523
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940104"
---
# <a name="retrieving-metadata"></a><span data-ttu-id="5064d-113">Récupération de métadonnées</span><span class="sxs-lookup"><span data-stu-id="5064d-113">Retrieving Metadata</span></span>

<span data-ttu-id="5064d-114">Pendant la lecture d’un affichage ou d’un clip, votre script peut récupérer des métadonnées, telles que le titre et l’auteur, à l’aide des méthodes **getItemInfo** des objets **multimédia** et **playlist** du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5064d-114">While a show or clip is playing, your script can retrieve metadata, such as title and author, by using the **getItemInfo** methods of the Windows Media Player **Media** and **Playlist** objects.</span></span> <span data-ttu-id="5064d-115">Vous pouvez récupérer des métadonnées à partir de l’étendue ASX à l’aide des méthodes d’objet **playlist** et de l’étendue d’entrée à l’aide des méthodes d’objet **Media** .</span><span class="sxs-lookup"><span data-stu-id="5064d-115">You can retrieve metadata from the ASX scope using **Playlist** object methods and from the ENTRY scope using **Media** object methods.</span></span>

<span data-ttu-id="5064d-116">Par exemple, pour récupérer les valeurs de AUTHOR, ABSTRACT et PARAM dans le fichier suivant, utilisez la méthode **getItemInfo** de l’objet **playlist** .</span><span class="sxs-lookup"><span data-stu-id="5064d-116">For example, to retrieve the values for AUTHOR, ABSTRACT and PARAM in the following file, use the **getItemInfo** method of the **Playlist** object.</span></span> <span data-ttu-id="5064d-117">Le nom d’attribut est requis pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="5064d-117">The attribute name is required for this method.</span></span> <span data-ttu-id="5064d-118">Les noms d’attributs peuvent être obtenus en fournissant le numéro d’index à la propriété **AttributeName** .</span><span class="sxs-lookup"><span data-stu-id="5064d-118">Attribute names can be obtained by providing the index number to the **attributeName** property.</span></span> <span data-ttu-id="5064d-119">Les index disponibles pour un objet **playlist** peuvent être obtenus à l’aide de la propriété **attributeCount** .</span><span class="sxs-lookup"><span data-stu-id="5064d-119">The available indexes for a **Playlist** object can be obtained using the **attributeCount** property.</span></span>

## <a name="example-code"></a><span data-ttu-id="5064d-120">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="5064d-120">Example Code</span></span>


```XML

    <ASX version="3.0">
        <AUTHOR>My Talking File</AUTHOR>
        <ABSTRACT>Talking File Album</ABSTRACT>
        <PARAM name="one" value="111"/>
        <ENTRY>
            <REF href="Artists_Only.wma"/>
            <TITLE>Artists Only</TITLE>
            <COPYRIGHT>2000</COPYRIGHT>
            <PARAM name="three" value="333"/>
        </ENTRY>
        <PARAM name="two" value="222"/>
    </ASX>
    

```



<span data-ttu-id="5064d-121">Pour récupérer les valeurs de l’objet **média** actuel dans l’étendue d’entrée pour REF, title, Copyright et Param ("trois"), utilisez la propriété **currentMedia** de l’objet **Player** .</span><span class="sxs-lookup"><span data-stu-id="5064d-121">To retrieve the values of the current **Media** object in the ENTRY scope for REF,TITLE,COPYRIGHT, and PARAM ("three"), use the **currentMedia** property of the **Player** object.</span></span> <span data-ttu-id="5064d-122">Utilisez la propriété **attributeCount** de l’objet **Media** pour déterminer le nombre d’attributs disponibles pour l’objet **multimédia** spécifié.</span><span class="sxs-lookup"><span data-stu-id="5064d-122">Use the **attributeCount** property of the **Media** object to determine the number of attributes available for the specified **Media** object.</span></span> <span data-ttu-id="5064d-123">Utilisez des numéros d’index avec la méthode **getItemInfoByAtom** pour récupérer des valeurs d’attribut.</span><span class="sxs-lookup"><span data-stu-id="5064d-123">Use index numbers with the **getItemInfoByAtom** method to retrieve attribute values.</span></span> <span data-ttu-id="5064d-124">Utilisez des numéros d’index avec la méthode **getAttributeName** de l’objet **Media** pour déterminer les noms des attributs disponibles, puis utilisez les résultats avec la méthode **getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="5064d-124">Use index numbers with the **getAttributeName** method of the **Media** object to determine the names of the available attributes, and then use the results with the **getItemInfo** method.</span></span>

<span data-ttu-id="5064d-125">Pour obtenir un exemple d’utilisation de méthodes d’objet lecteur Windows Media pour récupérer des métadonnées, consultez [playlist. attributeCount](playlist-attributecount.md).</span><span class="sxs-lookup"><span data-stu-id="5064d-125">For an example of using Windows Media Player object methods to retrieve metadata, see [Playlist.attributeCount](playlist-attributecount.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5064d-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5064d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5064d-127">**Création de sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="5064d-127">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="5064d-128">**Sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="5064d-128">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="5064d-129">**Guide des métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="5064d-129">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




