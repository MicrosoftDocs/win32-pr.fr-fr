---
title: Méthode PlaylistCollection. newPlaylist
description: La méthode newPlaylist crée une nouvelle sélection dans la bibliothèque.
ms.assetid: 428b5779-4dc0-466b-9834-6b2c43324013
keywords:
- Lecteur Windows Media de la méthode newPlaylist
- méthode newPlaylist Lecteur Windows Media, classe PlaylistCollection
- Lecteur Windows Media de la classe PlaylistCollection, méthode newPlaylist
topic_type:
- apiref
api_name:
- PlaylistCollection.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af40d4de424997cb943711d84bf62805f2036afeb551c5d397ce82ae0975e812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334593"
---
# <a name="playlistcollectionnewplaylist-method"></a>Méthode PlaylistCollection. newPlaylist

La méthode **newPlaylist** crée une nouvelle sélection dans la bibliothèque.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = PlaylistCollection.newPlaylist(
  name
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom* \[ dans\]
</dt> <dd>

**Chaîne** contenant le nom de la sélection à créer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un objet **playlist** .

## <a name="remarks"></a>Remarques

Cette méthode crée une sélection vide dans la bibliothèque. Pour remplir la sélection avec des éléments multimédias, utilisez la *sélection*. **appendItem** ou *playlist*. **InsertItem**.

Plusieurs playlists portant le même nom sont autorisées dans la bibliothèque. Pour éviter de créer un nom de playlist dupliqué avec cette méthode, utilisez **GetByName** et *PlaylistArray*. **Count** pour déterminer si une sélection portant un nom particulier existe déjà.

Les espaces de début et de fin ne sont pas autorisés dans les noms de playlist et sont automatiquement supprimés de la valeur spécifiée pour le paramètre *Name* .

Pour utiliser cette méthode, l’accès complet à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

l’exemple de JScript suivant crée une nouvelle sélection vide appelée « ThreeList ». L’objet **Player** a été créé avec ID = "Player".


```JScript
//Add a new empty playlist, named ThreeList, to the playlist collection.
var NewList = Player.playlistCollection.newPlaylist("ThreeList");

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MediaCollection. Add**](mediacollection-add.md)
</dt> <dt>

[**Playlist. appendItem**](playlist-appenditem.md)
</dt> <dt>

[**Playlist. insertItem**](playlist-insertitem.md)
</dt> <dt>

[**PlaylistArray. Count**](playlistarray-count.md)
</dt> <dt>

[**Objet PlaylistCollection**](playlistcollection-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> <dt>

[**PlaylistCollection.importPlaylist**](playlistcollection-importplaylist.md)
</dt> <dt>

[**PlaylistCollection. Remove**](playlistcollection-remove.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





