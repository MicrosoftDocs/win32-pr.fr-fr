---
title: MediaCollection. Remove, méthode
description: La méthode Remove supprime un élément de la collection de supports.
ms.assetid: 7d4c03ed-01c8-4112-90b6-5de52eacb199
keywords:
- supprimer la méthode Lecteur Windows Media
- remove, méthode Lecteur Windows Media, MediaCollection, classe
- Lecteur Windows Media de la classe MediaCollection, remove, méthode
topic_type:
- apiref
api_name:
- MediaCollection.remove
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8dd0643741a15bf114acfef63459e67c332b06b33e6284b032979d4ad15c1d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574606"
---
# <a name="mediacollectionremove-method"></a>MediaCollection. Remove, méthode

La méthode **Remove** supprime un élément de la collection de supports.

## <a name="syntax"></a>Syntaxe


```JScript
MediaCollection.remove(
  item,
  delete
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*élément* \[ dans\]
</dt> <dd>

Objet **multimédia** à supprimer.

</dd> <dt>

*supprimer* \[ dans\]
</dt> <dd>

**Valeur booléenne** indiquant si l’élément doit être supprimé.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode supprime un élément de la bibliothèque. Cette méthode ne supprime pas les fichiers de l’ordinateur de l’utilisateur.

Pour utiliser cette méthode, l’accès complet à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

l’exemple de JScript suivant, après l’invite de l’utilisateur, supprime définitivement le premier élément multimédia de la collection de supports à l’aide de *MediaCollection*. **supprimez**. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Retrieve the first item from the media collection.
var mediaObject = Player.mediaCollection.getAll().item(0);

// Store the name of the retrieved object.
var mediaName = mediaObject.name;

// Prompt the user for permission to delete the object.
var answer = confirm("OK to permanently delete " + mediaName + "?");

// Check the user response.
if (answer){

    // Permanently delete the item.
    Player.mediaCollection.remove(mediaObject, true);

    // Report that the item was deleted.
    alert("Deleted item " + mediaName);
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

[**Objet MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection. Add**](mediacollection-add.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





