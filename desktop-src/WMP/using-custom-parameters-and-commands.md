---
title: Utilisation de paramètres et de commandes personnalisés
description: Utilisation de paramètres et de commandes personnalisés
ms.assetid: 6b0bfd19-1672-41e3-9b7f-c8d541168c0e
keywords:
- Windows Sélections de métafichiers multimédias, paramètres personnalisés
- sélections, paramètres personnalisés
- sélections de métafichiers, paramètres personnalisés
- Windows Sélections de métafichiers multimédias, commandes personnalisées
- sélections, commandes personnalisées
- sélections de métafichiers, commandes personnalisées
- Windows Sélections de métafichiers multimédia, paramètres
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010844"
---
# <a name="using-custom-parameters-and-commands"></a>Utilisation de paramètres et de commandes personnalisés

Vous pouvez créer des paramètres personnalisés pour passer des métadonnées supplémentaires dans une sélection de métafichiers à l’aide de l’élément **param** . Utilisez l’attribut **Name** de l’élément **param** pour définir le nom du paramètre personnalisé. Utilisez l’attribut **value** pour définir la valeur du paramètre personnalisé nommé.

Récupérez les métadonnées **param** à l’aide des méthodes **GetItemInfo** des objets **média** et **playlist** . Pour obtenir un exemple d’utilisation de ces méthodes pour récupérer des métadonnées, consultez la méthode [attributeCount](playlist-attributecount.md) de l’objet **playlist** .

L’exemple de sélection de métafichier suivant illustre l’utilisation de l’élément **param** pour définir des paramètres personnalisés.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation des sélections de métafichiers**](using-metafile-playlists.md)
</dt> </dl>

 

 




