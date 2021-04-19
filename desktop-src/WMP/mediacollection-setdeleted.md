---
title: Méthode MediaCollection. setDeleted
description: La méthode setDeleted déplace l’élément multimédia spécifié vers le dossier éléments supprimés. | Méthode MediaCollection. setDeleted
ms.assetid: 3e3c9a16-37e1-41b4-8593-58aaf4541eb9
keywords:
- méthode setDeleted lecteur Windows Media
- méthode setDeleted lecteur Windows Media, classe MediaCollection
- Classe MediaCollection lecteur Windows Media, méthode setDeleted
topic_type:
- apiref
api_name:
- MediaCollection.setDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f545953899883933286f3c38def62d9f254dfdc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520885"
---
# <a name="mediacollectionsetdeleted-method"></a>Méthode MediaCollection. setDeleted

La méthode **setDeleted** déplace l’élément multimédia spécifié vers le dossier éléments supprimés.

## <a name="syntax"></a>Syntaxe


```JScript
MediaCollection.setDeleted(
  item,
  true
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*élément* \[ dans\]
</dt> <dd>

Objet **multimédia** déplacé.

</dd> <dt>

*true* \[ dans\]
</dt> <dd>

Spécifiez toujours cette valeur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode ne supprime pas les fichiers de l’ordinateur de l’utilisateur.

Pour utiliser cette méthode, l’accès complet à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise *MediaCollection*. **setDeleted** pour déplacer un élément multimédia particulier, stocké dans la variable nommée mediaObject, vers le dossier éléments supprimés. *MediaCollection*. méthode **IsDeleted** teste d’abord si l’élément a déjà été supprimé. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The item is available to be deleted; move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Item moved to deleted items folder.");}

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

[**MediaCollection. isDeleted**](mediacollection-isdeleted.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





