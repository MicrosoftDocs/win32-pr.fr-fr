---
title: Méthode PlaylistCollection. getByName
description: La méthode getByName récupère un objet PlaylistArray contenant des sélections portant le nom spécifié, le cas échéant.
ms.assetid: 0308a98d-1149-4367-b602-33fa54c1760f
keywords:
- méthode getByName lecteur Windows Media
- méthode getByName lecteur Windows Media, classe PlaylistCollection
- Classe PlaylistCollection lecteur Windows Media, méthode getByName
topic_type:
- apiref
api_name:
- PlaylistCollection.getByName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7954df8e0ccc487df77ea31b3a26dce9eea6d2e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539974"
---
# <a name="playlistcollectiongetbyname-method"></a>Méthode PlaylistCollection. getByName

La méthode **GetByName** récupère un objet **PlaylistArray** contenant des sélections portant le nom spécifié, le cas échéant.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = PlaylistCollection.getByName(
  name
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom* \[ dans\]
</dt> <dd>

**Chaîne** contenant le nom des sélections à récupérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un objet **PlaylistArray** .

## <a name="remarks"></a>Notes

Utilisez *PlaylistArray*. **Count** pour déterminer si une sélection existe. Si **Count** est égal à zéro, aucune playlist n’existe.

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise *playlistCollection*. **GetByName** pour vérifier l’objet **playlistCollection** pour une sélection nommée « ThreeList ». Si la sélection « Threelist » existe, **GetByName** définit « Threelist » comme sélection actuelle. L’objet **Player** a été créé avec l’ID = "Player".


```JScript
//Retrieve the count of the playlists named "ThreeList".
var Checkit = Player.playlistCollection.getByName("ThreeList").count;

//Since duplicate playlist names are allowed, the count returned
//will be either zero (no playlist) or greater than zero 
//(playlist exists).
if (Checkit > 0){ 
    
   //Retrieve a playlistArray object containing "ThreeList". Assume that
   //there is only one playlist with that name, and assign it to the 
   //current playlist.
   Player.currentPlaylist = Player.playlistCollection.getByName("ThreeList").item(0);
}

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet PlaylistArray**](playlistarray-object.md)
</dt> <dt>

[**PlaylistArray. Count**](playlistarray-count.md)
</dt> <dt>

[**Objet PlaylistCollection**](playlistcollection-object.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





