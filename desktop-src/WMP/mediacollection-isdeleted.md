---
title: MediaCollection. isDeleted, méthode
description: La méthode isDeleted récupère une valeur indiquant si l’élément multimédia spécifié se trouve dans le dossier éléments supprimés.
ms.assetid: bb3ce9c9-9e43-45a5-8802-dc6783cf2ad7
keywords:
- isDeleted, méthode Windows Media Player
- isDeleted, méthode lecteur Windows Media, classe MediaCollection
- Classe MediaCollection lecteur Windows Media, méthode isDeleted
topic_type:
- apiref
api_name:
- MediaCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3cdc27c84c88eb65df5b7635f34c79c1b4fe82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522794"
---
# <a name="mediacollectionisdeleted-method"></a>MediaCollection. isDeleted, méthode

La méthode **IsDeleted** récupère une valeur indiquant si l’élément multimédia spécifié se trouve dans le dossier éléments supprimés.

## <a name="syntax"></a>Syntaxe


```JScript
bRetVal = MediaCollection.isDeleted(
  item
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*élément* \[ dans\]
</dt> <dd>

Objet **multimédia** qui peut être supprimé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne une **valeur booléenne**.

## <a name="remarks"></a>Notes

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

**Lecteur Windows Media 10 Mobile :** Cette méthode retourne toujours **false**.

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise *MediaCollection*. **IsDeleted** pour tester si un élément multimédia particulier, stocké dans la variable nommée mediaObject, se trouve dans le dossier éléments supprimés. Si l’élément multimédia n’a pas déjà été supprimé, il est déplacé vers le dossier éléments supprimés. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The media item is available to be deleted, move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Media item moved to deleted items folder.");}

else
    // Tell the user the operation is unnecessary.
    alert("Item is already deleted!");
}

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0, lecteur Windows Media version 7,1 ou lecteur Windows Media pour Windows XP. Cette méthode n’est pas prise en charge pour le lecteur Windows Media série 9 ou version ultérieure.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                                                              |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Media**](media-object.md)
</dt> <dt>

[**Objet MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection.setDeleted**](mediacollection-setdeleted.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





