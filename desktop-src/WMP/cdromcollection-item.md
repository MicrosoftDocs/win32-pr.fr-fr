---
title: CdromCollection. Item, méthode
description: La méthode Item récupère l’objet cdrom à l’index donné.
ms.assetid: c1efa972-736d-4fa0-9835-14ee594ae719
keywords:
- méthode Item lecteur Windows Media
- méthode Item lecteur Windows Media, classe CdromCollection
- Classe CdromCollection lecteur Windows Media, méthode Item
topic_type:
- apiref
api_name:
- CdromCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a67dc58ae75819fa42940346b4f588b23a2f645a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521758"
---
# <a name="cdromcollectionitem-method"></a>CdromCollection. Item, méthode

La méthode **Item** récupère l’objet **cdrom** à l’index donné.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = CdromCollection.item(
  index
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* \[ dans\]
</dt> <dd>

**Nombre** (**long**) contenant l’index.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un objet **cdrom** .

## <a name="remarks"></a>Notes

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise *CdromCollection*. **élément** pour imprimer le nom de la sélection à partir de chaque CD disponible sur l’ordinateur. Si le lecteur contient réellement du contenu DVD, Windows XP ou version ultérieure est requis. Un élément TextArea HTML a été créé avec ID = "Playlists". L’objet **Player** a été créé avec ID = "Player".


```JScript
// Create an array to store the CD playlists.
var cdPlaylists = new Array();

// Loop through the available CD drives.
for (var i = 0; i < Player.cdromCollection.count; i++){

     // Fill the cdPlaylists array with playlist objects.
     cdPlaylists[i] = Player.cdromCollection.item(i).Playlist;

     // Print each drive specifier.
     playlists.value+=Player.cdromCollection.item(i).driveSpecifier + " ";

     // Print the name of each CD playlist to the text area.
     playlists.value += cdPlaylists[i].name + "\n";
}

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Cdrom. driveSpecifier**](cdrom-drivespecifier.md)
</dt> <dt>

[**Objet CdromCollection**](cdromcollection-object.md)
</dt> <dt>

[**CdromCollection. Count**](cdromcollection-count.md)
</dt> <dt>

[**Playlist.name**](playlist-name.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





