---
title: Méthode playlist. appendItem
description: La méthode appendItem ajoute un élément multimédia à la fin de la sélection.
ms.assetid: cc956491-7936-49e7-90ca-1f71e03448cd
keywords:
- méthode appendItem lecteur Windows Media
- méthode appendItem lecteur Windows Media, classe de sélection
- Classe de sélection lecteur Windows Media, méthode appendItem
topic_type:
- apiref
api_name:
- Playlist.appendItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 828799d5b6e71e7ff0e7be4c1e55714f6343be51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540418"
---
# <a name="playlistappenditem-method"></a>Méthode playlist. appendItem

La méthode **appendItem** ajoute un élément multimédia à la fin de la sélection.

## <a name="syntax"></a>Syntaxe


```JScript
Playlist.appendItem(
  item
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*élément* \[ dans\]
</dt> <dd>

Objet **multimédia** à ajouter.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Pour utiliser cette méthode, l’accès complet à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise la *sélection*. **appendItem** pour ajouter l’élément multimédia actuel à la sélection nommée « ThreeList ». L’objet **Player** a été créé avec ID = "Player".


```JScript
// Get the current media item.
var currMedia = Player.currentMedia;

// Get the playlist object by name.
var plThreeList = Player.playlistCollection.getByName("ThreeList").item(0);

// Append the media item to the playlist.
plThreeList.appendItem(currMedia);

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet playlist**](playlist-object.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





