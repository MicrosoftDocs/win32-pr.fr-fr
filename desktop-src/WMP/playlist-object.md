---
title: Objet playlist
description: L’objet playlist offre un moyen d’organiser les éléments multimédias dans une liste pour faciliter leur manipulation à l’aide des propriétés et méthodes suivantes.
ms.assetid: c2d2f265-b207-4b82-bb76-aee467f00659
keywords:
- objet Playlist Lecteur Windows Media
topic_type:
- apiref
api_name:
- Playlist Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d517e13f8da103b1f9cee9498cce58a62eaf6462
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292987"
---
# <a name="playlist-object"></a>Objet playlist

L’objet **playlist** offre un moyen d’organiser les éléments multimédias dans une liste pour faciliter leur manipulation à l’aide des propriétés et méthodes suivantes.

L’objet **playlist** prend en charge les propriétés suivantes.



| Propriété                                      | Description                                                      |
|-----------------------------------------------|------------------------------------------------------------------|
| [attributeCount](playlist-attributecount.md) | Récupère le nombre d’attributs associés à la sélection. |
| [attributeName](playlist-attributename.md)   | Récupère le nom d’un attribut spécifié par un index.        |
| [count](playlist-count.md)                   | Récupère le nombre d’éléments dans la sélection.                   |
| [name](playlist-name.md)                     | Spécifie ou récupère le nom de la sélection.                 |



 

L’objet **playlist** prend en charge les méthodes suivantes.



| Méthode                                  | Description                                                                                            |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------|
| [appendItem](playlist-appenditem.md)   | Ajoute un élément multimédia à la fin de la sélection.                                                          |
| **clear**                               | Réservé pour un usage futur.                                                                               |
| [getItemInfo](playlist-getiteminfo.md) | Récupère la valeur d’un attribut playlist.                                                           |
| [insertItem](playlist-insertitem.md)   | Insère un élément multimédia dans la sélection à l’emplacement spécifié.                                      |
| [isIdentical](playlist-isidentical.md) | Récupère une valeur indiquant si l’objet de **sélection** fourni est identique à l’objet actuel. |
| [item](playlist-item.md)               | Récupère l’élément multimédia à l’index spécifié.                                                       |
| [moveItem](playlist-moveitem.md)       | Modifie l’emplacement d’un élément dans la sélection.                                                       |
| [removeItem](playlist-removeitem.md)   | Supprime l’élément spécifié de la sélection.                                                          |
| [setItemInfo](playlist-setiteminfo.md) | Spécifie la valeur d’un attribut playlist.                                                           |



 

L’objet **playlist** est accessible par le biais des propriétés et méthodes suivantes.



| Object                                              | Propriété ou méthode                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [-](cdrom-object.md)                           | [playlist](cdrom-playlist.md)                                                                                                                                                                                                                                                     |
| [MediaCollection](mediacollection-object.md)       | [GetAll](mediacollection-getall.md), [getByAlbum](mediacollection-getbyalbum.md), [getByAttribute](mediacollection-getbyattribute.md), [getByAuthor](mediacollection-getbyauthor.md), [getByGenre](mediacollection-getbygenre.md), [GetByName](mediacollection-getbyname.md) |
| [Lecteur](player-object.md)                         | [currentPlaylist](player-currentplaylist.md), [newPlaylist](player-newplaylist.md)                                                                                                                                                                                               |
| [PlaylistArray](playlistarray-object.md)           | [item](playlistarray-item.md)                                                                                                                                                                                                                                                     |
| [PlaylistCollection](playlistcollection-object.md) | [newPlaylist](playlistcollection-newplaylist.md)                                                                                                                                                                                                                                  |



 

Parce qu’il s’agit de la méthode d’accès la plus courante, *Player*. **currentPlaylist** est utilisé à des fins d’illustration dans les sections de syntaxe de référence.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence du modèle objet pour l’écriture de scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




