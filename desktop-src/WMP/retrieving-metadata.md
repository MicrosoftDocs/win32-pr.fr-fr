---
title: Récupération de métadonnées
description: Récupération de métadonnées
ms.assetid: f634118a-0a62-4407-8be1-a907347de55b
keywords:
- Windows Sélections de métafichiers multimédia, récupération de métadonnées
- sélections, récupération de métadonnées
- sélections de métafichiers, récupération des métadonnées
- Windows Sélections de métafichiers multimédia, récupération de métadonnées
- sélections, récupération des métadonnées
- sélections de métafichiers, récupération de métadonnées
- métadonnées, récupération
- récupération de métadonnées
- Lecteur Windows Media, récupérer des métadonnées
- Lecteur Windows Media, récupération des métadonnées
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c9855ec1dc95a52429561e91aa82abdac088523
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010897"
---
# <a name="retrieving-metadata"></a>Récupération de métadonnées

pendant la lecture d’un affichage ou d’un clip, votre script peut récupérer des métadonnées, telles que le titre et l’auteur, en utilisant les méthodes **getItemInfo** des objets **multimédia** et de **sélection** de Lecteur Windows Media. Vous pouvez récupérer des métadonnées à partir de l’étendue ASX à l’aide des méthodes d’objet **playlist** et de l’étendue d’entrée à l’aide des méthodes d’objet **Media** .

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

pour obtenir un exemple d’utilisation de Lecteur Windows Media méthodes d’objet pour récupérer des métadonnées, consultez [Playlist. attributeCount](playlist-attributecount.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création de sélections de métafichiers**](creating-metafile-playlists.md)
</dt> <dt>

[**Sélections de métafichiers**](metafile-playlists.md)
</dt> <dt>

[**Windows Guide du métafichier multimédia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




