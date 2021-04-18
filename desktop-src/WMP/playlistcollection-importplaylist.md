---
title: Méthode PlaylistCollection. importPlaylist
description: La méthode importPlaylist ajoute une sélection statique à la bibliothèque. | Méthode PlaylistCollection. importPlaylist
ms.assetid: 0611ba42-fd8f-4fb9-9fbb-809a82775c2a
keywords:
- méthode importPlaylist lecteur Windows Media
- méthode importPlaylist lecteur Windows Media, classe PlaylistCollection
- Classe PlaylistCollection lecteur Windows Media, méthode importPlaylist
topic_type:
- apiref
api_name:
- PlaylistCollection.importPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736e9afa17f571428fada48660726b606268796a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526326"
---
# <a name="playlistcollectionimportplaylist-method"></a>Méthode PlaylistCollection. importPlaylist

La méthode **importPlaylist** ajoute une sélection statique à la bibliothèque.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = PlaylistCollection.importPlaylist(
  playlist
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sélection* \[ dans\]
</dt> <dd>

Objet **playlist** à ajouter.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’objet **playlist** qui a été ajouté.

## <a name="remarks"></a>Notes

Les sélections qui ne contiennent pas d’éléments multimédias ne peuvent pas être ajoutées à la bibliothèque à l’aide de cette méthode. Pour créer une playlist vide dans la bibliothèque, utilisez la méthode **newPlaylist** . Vous pouvez ensuite remplir la playlist obtenue avec des éléments multimédias à l’aide d’une *sélection*. **appendItem** ou *playlist*. **InsertItem**.

Si vous transmettez cette méthode à une sélection automatique, la requête est exécutée une fois et le résultat est ajouté à la bibliothèque en tant que sélection statique. Pour ajouter une sélection automatique à la bibliothèque et conserver son comportement automatique, utilisez *MediaCollection*. **Ajoutez**. Pour plus d’informations, consultez [sélections statiques et automatiques](static-and-auto-playlists.md).

Pour utiliser cette méthode, l’accès complet à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Gestion des sélections**](managing-playlists.md)
</dt> <dt>

[**Objet MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection. Add**](mediacollection-add.md)
</dt> <dt>

[**Playlist. appendItem**](playlist-appenditem.md)
</dt> <dt>

[**Playlist. insertItem**](playlist-insertitem.md)
</dt> <dt>

[**Objet PlaylistCollection**](playlistcollection-object.md)
</dt> <dt>

[**PlaylistCollection. newPlaylist**](playlistcollection-newplaylist.md)
</dt> <dt>

[**PlaylistCollection. Remove**](playlistcollection-remove.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





