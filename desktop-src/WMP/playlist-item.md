---
title: Méthode playlist. Item
description: La méthode Item récupère l’élément multimédia au niveau de l’index spécifié.
ms.assetid: a564f6db-ede4-4c85-87ca-0e2539d914c2
keywords:
- méthode Item lecteur Windows Media
- méthode Item lecteur Windows Media, classe playlist
- Classe de sélection lecteur Windows Media, méthode d’élément
topic_type:
- apiref
api_name:
- Playlist.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c69386871aeec33dbc36a066ce3f75e80d7514
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534872"
---
# <a name="playlistitem-method"></a>Méthode playlist. Item

La méthode **Item** récupère l’élément multimédia au niveau de l’index spécifié.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = Playlist.item(
  index
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* \[ dans\]
</dt> <dd>

**Nombre** (**long**) contenant l’index de l’élément à récupérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un objet **multimédia** .

## <a name="remarks"></a>Notes

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise la *sélection*. **élément** permettant de récupérer un élément multimédia à partir de la sélection actuelle en fonction d’une sélection de l’utilisateur. Un élément SELECT HTML a été créé avec le nom « weblist » et rempli avec les titres de la sélection actuelle. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Store the value of the selected item in the list box
// using the selectedIndex property.
var index = weblist.selectedIndex;

// Store the corresponding digital media object from the current playlist.
var listItem = Player.currentPlaylist.item(index);

// Set the URL using the listItem variable.
Player.URL = listItem.sourceURL;

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Media**](media-object.md)
</dt> <dt>

[**Objet playlist**](playlist-object.md)
</dt> <dt>

[**Playlist. insertItem**](playlist-insertitem.md)
</dt> <dt>

[**Playlist. removeItem**](playlist-removeitem.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





