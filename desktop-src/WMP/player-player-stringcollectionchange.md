---
title: Événement Player. StringCollectionChange
description: L’événement StringCollectionChange se produit lorsqu’une collection de chaînes change. | Événement Player. StringCollectionChange
ms.assetid: 465ec694-afd1-4baa-b559-3ab75874388f
keywords:
- Lecteur Windows Media d’événements StringCollectionChange
- Lecteur Windows Media d’événements StringCollectionChange, classe Player
- Lecteur Windows Media de classe Player, événement StringCollectionChange
topic_type:
- apiref
api_name:
- Player.StringCollectionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5012cd94c14532eb94eb452c9c7aa20d50ffb8a447c2d14f56e8c6df02456849
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572417"
---
# <a name="playerstringcollectionchange-event"></a>Événement Player. StringCollectionChange

L’événement StringCollectionChange se produit lorsqu’une collection de chaînes change.

## <a name="syntax"></a>Syntaxe


```JScript
Player.StringCollectionChange(
  pdispStringCollection,
  change,
  lCollectionIndex
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pdispStringCollection* 
</dt> <dd>

Objet **StringCollection** modifié.

</dd> <dt>

*change* 
</dt> <dd>

Nombre (long) indiquant le type de modification qui s’est produite dans la collection de chaînes. Contient l’une des valeurs suivantes.



| Number | Description                        |
|--------|------------------------------------|
| 0      | Inconnu. (Valeur non valide)       |
| 1      | Un élément a été inséré.              |
| 2      | La collection de chaînes a changé.     |
| 3      | Un élément a été supprimé.               |
| 4      | La collection de chaînes a été effacée. |
| 5      | Les mises à jour en bloc commencent.        |
| 6      | Les mises à jour en bloc se sont terminées.           |



 

</dd> <dt>

*lCollectionIndex* 
</dt> <dd>

Nombre (long) contenant l’index de l’élément de collection de chaînes qui a changé.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> <dt>

[**StringCollection, objet**](stringcollection-object.md)
</dt> </dl>

 

 





