---
title: Objet PlaylistCollection
description: L’objet PlaylistCollection offre un moyen d’organiser vos sélections.
ms.assetid: 9ea61954-d185-4a77-9016-4d58340a96fc
keywords:
- Objet PlaylistCollection lecteur Windows Media
topic_type:
- apiref
api_name:
- PlaylistCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2266537e0df9fc0ba5527784c254b27313d636d3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106540758"
---
# <a name="playlistcollection-object"></a>Objet PlaylistCollection

L’objet **PlaylistCollection** offre un moyen d’organiser vos sélections.

L’objet **PlaylistCollection** prend en charge les méthodes suivantes.



| Méthode                                                  | Description                                                                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [getAll](playlistcollection-getall.md)                 | Récupère un objet [PlaylistArray](playlistarray-object.md) contenant toutes les sélections de la bibliothèque.                |
| [getByName](playlistcollection-getbyname.md)           | Récupère un objet [PlaylistArray](playlistarray-object.md) contenant les playlists portant le nom spécifié, le cas échéant. |
| [importPlaylist](playlistcollection-importplaylist.md) | Ajoute une sélection statique à la bibliothèque.                                                                                   |
| [isDeleted](playlistcollection-isdeleted.md)           | Récupère une valeur indiquant si la sélection spécifiée se trouve dans le dossier éléments supprimés.                              |
| [newPlaylist](playlistcollection-newplaylist.md)       | Crée une nouvelle sélection dans la bibliothèque.                                                                                   |
| [remove](playlistcollection-remove.md)                 | Supprime une sélection de la bibliothèque.                                                                                     |
| [setDeleted](playlistcollection-setdeleted.md)         | Déplace une sélection vers le dossier éléments supprimés.                                                                            |



 

L’objet **PlaylistCollection** est accessible par le biais de la propriété suivante.



| Object                      | Propriété                                            |
|-----------------------------|-----------------------------------------------------|
| [Lecteur](player-object.md) | [playlistCollection](player-playlistcollection.md) |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence du modèle objet pour l’écriture de scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




