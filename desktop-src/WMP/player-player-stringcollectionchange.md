---
title: Événement Player. StringCollectionChange
description: L’événement StringCollectionChange se produit lorsqu’une collection de chaînes change. | Événement Player. StringCollectionChange
ms.assetid: 465ec694-afd1-4baa-b559-3ab75874388f
keywords:
- Événement StringCollectionChange lecteur Windows Media
- Événement StringCollectionChange lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement StringCollectionChange
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
ms.openlocfilehash: e6a61b8e1e09e749579f323d506371138b0d9b59
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424089"
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

## <a name="remarks"></a>Remarques

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

 

 





