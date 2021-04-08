---
title: Attributs d’élément multimédia
description: Attributs d’élément multimédia
ms.assetid: d43addec-e06c-4ef3-9012-3ecf589b105c
keywords:
- Lecteur Windows Media, bibliothèque
- Modèle objet du lecteur Windows Media, bibliothèque
- modèle objet, bibliothèque
- Windows Media Player Mobile, bibliothèque pour le modèle objet
- Contrôle ActiveX du lecteur Windows Media, bibliothèque pour le modèle objet
- Windows Media Player Mobile contrôle ActiveX, bibliothèque pour le modèle objet
- Contrôle ActiveX, bibliothèque pour le modèle objet
- Lecteur Windows Media, attributs des éléments multimédias
- Modèle objet du lecteur Windows Media, attributs des éléments multimédias
- modèle objet, attributs pour les éléments multimédias
- Windows Media Player Mobile, attributs pour les éléments multimédias
- Contrôle ActiveX du lecteur Windows Media, attributs des éléments multimédias
- Contrôle ActiveX Windows Media Player Mobile, attributs des éléments multimédias
- Contrôle ActiveX, attributs pour les éléments multimédias
- Bibliothèque du lecteur Windows Media, attributs pour les éléments multimédias
- bibliothèque, attributs pour les éléments multimédias
- attributs, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ac8595cc07504c9cd3e195431513a1f8565e87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029176"
---
# <a name="media-item-attributes"></a><span data-ttu-id="8bd8c-120">Attributs d’élément multimédia</span><span class="sxs-lookup"><span data-stu-id="8bd8c-120">Media Item Attributes</span></span>

<span data-ttu-id="8bd8c-121">Lorsque vous examinez la bibliothèque dans le lecteur Windows Media, vous voyez généralement une grande quantité d’informations sur un élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="8bd8c-121">When you look at the library in Windows Media Player, you typically see a great deal of information about a media item.</span></span> <span data-ttu-id="8bd8c-122">En plus du nom d’une piste audio, par exemple, vous verrez probablement le nom de l’album sur lequel se trouve la piste, les noms de l’artiste et du compositeur, le genre de la musique, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="8bd8c-122">In addition to the name of an audio track, for example, you will likely see the name of the album the track is on, the names of the artist and composer, the genre of the music, and so on.</span></span>

<span data-ttu-id="8bd8c-123">Dans le modèle objet du lecteur Windows Media, ces éléments de métadonnées sont appelés attributs.</span><span class="sxs-lookup"><span data-stu-id="8bd8c-123">In the Windows Media Player object model, these metadata items are called attributes.</span></span> <span data-ttu-id="8bd8c-124">Le modèle objet comprend des propriétés et des méthodes que vous pouvez utiliser pour interroger des éléments multimédias et des sélections pour les attributs.</span><span class="sxs-lookup"><span data-stu-id="8bd8c-124">The object model includes properties and methods you can use to query media items and playlists for attributes.</span></span> <span data-ttu-id="8bd8c-125">Vous pouvez ensuite afficher des valeurs d’attribut dans votre interface utilisateur ou votre code peut prendre des mesures en fonction de la valeur d’un attribut.</span><span class="sxs-lookup"><span data-stu-id="8bd8c-125">You can then display attribute values in your user interface, or your code can take actions based on the value of an attribute.</span></span>

<span data-ttu-id="8bd8c-126">Les rubriques suivantes décrivent l’utilisation des attributs d’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="8bd8c-126">The following topics describe working with media item attributes.</span></span>



| <span data-ttu-id="8bd8c-127">Rubrique</span><span class="sxs-lookup"><span data-stu-id="8bd8c-127">Topic</span></span>                                                                                      | <span data-ttu-id="8bd8c-128">Description</span><span class="sxs-lookup"><span data-stu-id="8bd8c-128">Description</span></span>                                                                                     |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8bd8c-129">Fonctionnement des sources d’attributs</span><span class="sxs-lookup"><span data-stu-id="8bd8c-129">Understanding Attribute Sources</span></span>](understanding-attribute-sources.md)                     | <span data-ttu-id="8bd8c-130">Décrit comment la source d’un élément multimédia affecte les attributs qui peuvent lui être associés.</span><span class="sxs-lookup"><span data-stu-id="8bd8c-130">Describes how the source of a media item affects the attributes that may be associated with it.</span></span> |
| [<span data-ttu-id="8bd8c-131">Lecture des valeurs d’attribut</span><span class="sxs-lookup"><span data-stu-id="8bd8c-131">Reading Attribute Values</span></span>](reading-attribute-values.md)                                   | <span data-ttu-id="8bd8c-132">Montre les méthodes de récupération de la valeur d’un attribut.</span><span class="sxs-lookup"><span data-stu-id="8bd8c-132">Shows the methods for retrieving the value of an attribute.</span></span>                                     |
| [<span data-ttu-id="8bd8c-133">Attributs avec plusieurs valeurs</span><span class="sxs-lookup"><span data-stu-id="8bd8c-133">Attributes with Multiple Values</span></span>](attributes-with-multiple-values.md)                     | <span data-ttu-id="8bd8c-134">Montre les méthodes de récupération de la valeur d’un attribut à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="8bd8c-134">Shows the methods for retrieving the value of a multi-valued attribute.</span></span>                         |
| [<span data-ttu-id="8bd8c-135">Lecture des valeurs d’attribut à partir d’un CD ou d’un DVD</span><span class="sxs-lookup"><span data-stu-id="8bd8c-135">Reading Attribute Values from a CD or DVD</span></span>](reading-attribute-values-from-a-cd-or-dvd.md) | <span data-ttu-id="8bd8c-136">Fournit un exemple d’application qui lit tous les attributs d’un élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="8bd8c-136">Provides a sample application that reads all of the attributes of a media item.</span></span>                 |
| [<span data-ttu-id="8bd8c-137">Modification des valeurs d’attribut</span><span class="sxs-lookup"><span data-stu-id="8bd8c-137">Changing Attribute Values</span></span>](changing-attribute-values.md)                                 | <span data-ttu-id="8bd8c-138">Affiche la méthode de modification de la valeur d’un attribut.</span><span class="sxs-lookup"><span data-stu-id="8bd8c-138">Shows the method for changing the value of an attribute.</span></span>                                        |
| [<span data-ttu-id="8bd8c-139">Valeurs d’attribut pour le contenu TV</span><span class="sxs-lookup"><span data-stu-id="8bd8c-139">Attribute Values for TV Content</span></span>](attribute-values-for-tv-content.md)                     | <span data-ttu-id="8bd8c-140">Montre comment spécifier des attributs pour le contenu vidéo numérique qui contient des émissions TV.</span><span class="sxs-lookup"><span data-stu-id="8bd8c-140">Shows how to specify attributes for digital video content that contains TV shows.</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="8bd8c-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8bd8c-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bd8c-142">**Attributs de sélection**</span><span class="sxs-lookup"><span data-stu-id="8bd8c-142">**Playlist Attributes**</span></span>](playlist-attributes.md)
</dt> <dt>

[<span data-ttu-id="8bd8c-143">**Utilisation de la bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="8bd8c-143">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




