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
# <a name="retrieving-metadata"></a>Récupération de métadonnées

Pendant la lecture d’un affichage ou d’un clip, votre script peut récupérer des métadonnées, telles que le titre et l’auteur, à l’aide des méthodes **getItemInfo** des objets **multimédia** et **playlist** du lecteur Windows Media. Vous pouvez récupérer des métadonnées à partir de l’étendue ASX à l’aide des méthodes d’objet **playlist** et de l’étendue d’entrée à l’aide des méthodes d’objet **Media** .

Par exemple, pour récupérer les valeurs de AUTHOR, ABSTRACT et PARAM dans le fichier suivant, utilisez la méthode **getItemInfo** de l’objet **playlist** . Le nom d’attribut est requis pour cette méthode. Les noms d’attributs peuvent être obtenus en fournissant le numéro d’index à la propriété **AttributeName** . Les index disponibles pour un objet **playlist** peuvent être obtenus à l’aide de la propriété **attributeCount** .

## <a name="example-code"></a>Exemple de code


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



Pour récupérer les valeurs de l’objet **média** actuel dans l’étendue d’entrée pour REF, title, Copyright et Param ("trois"), utilisez la propriété **currentMedia** de l’objet **Player** . Utilisez la propriété **attributeCount** de l’objet **Media** pour déterminer le nombre d’attributs disponibles pour l’objet **multimédia** spécifié. Utilisez des numéros d’index avec la méthode **getItemInfoByAtom** pour récupérer des valeurs d’attribut. Utilisez des numéros d’index avec la méthode **getAttributeName** de l’objet **Media** pour déterminer les noms des attributs disponibles, puis utilisez les résultats avec la méthode **getItemInfo** .

Pour obtenir un exemple d’utilisation de méthodes d’objet lecteur Windows Media pour récupérer des métadonnées, consultez [playlist. attributeCount](playlist-attributecount.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création de sélections de métafichiers**](creating-metafile-playlists.md)
</dt> <dt>

[**Sélections de métafichiers**](metafile-playlists.md)
</dt> <dt>

[**Guide des métafichiers Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




