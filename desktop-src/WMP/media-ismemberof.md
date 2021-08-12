---
title: Méthode Media. isMemberOf
description: La méthode isMemberOf retourne une valeur indiquant si l’élément multimédia est membre de la sélection spécifiée.
ms.assetid: e620741f-6807-4a61-ba9b-f45426d6e33e
keywords:
- Lecteur Windows Media de la méthode isMemberOf
- méthode isMemberOf Lecteur Windows Media, classe multimédia
- Lecteur Windows Media de classe de média, méthode isMemberOf
topic_type:
- apiref
api_name:
- Media.isMemberOf
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef9fc5eb55a306dad8b9d5de6d6501b615a9156c026c8e0fc12664795a23ab21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574801"
---
# <a name="mediaismemberof-method"></a>Méthode Media. isMemberOf

La méthode **isMemberOf** retourne une valeur indiquant si l’élément multimédia est membre de la sélection spécifiée.

## <a name="syntax"></a>Syntaxe


```JScript
bRetVal = Media.isMemberOf(
  playlist
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sélection* \[ dans\]
</dt> <dd>

Objet **playlist** qui peut contenir l’élément multimédia.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode retourne une **valeur booléenne**.

## <a name="remarks"></a>Notes

Cette méthode ne peut pas vérifier les sélections récupérées par le biais de l’objet **MediaCollection** . Pour déterminer si un élément multimédia est membre d’une sélection nommée particulière, récupérez la sélection avec le *lecteur*. *playlistCollection*. **GetByName**(*nom*). **Item**(0). Cette méthode peut également être utilisée avec les sélections de CD et les sélections de métafichiers.

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise un *média*. **isMemberOf** pour vérifier si l’élément multimédia actuel est membre de la sélection nommée Sample playlist. Si ce n’est pas le cas, l’élément multimédia actuel est ajouté à l’exemple de sélection. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Store the playlist object named Sample Playlist.
var sPlaylist = Player.playlistcollection.getbyname("Sample Playlist").item(0);

// Test whether the current media item is a member of Sample Playlist.
 var answer = ((Player.currentMedia.isMemberOf(sPlaylist))?"Yes":"No");

// If the current media item is not a member of Sample Playlist,
// append the current media item to the playlist.
if (answer == "No"){
   sPlaylist.appendItem(Player.currentMedia);
}

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

[**Objet PlaylistCollection**](playlistcollection-object.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





