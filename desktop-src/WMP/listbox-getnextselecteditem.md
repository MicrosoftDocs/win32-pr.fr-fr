---
title: LISTBOX. getNextSelectedItem
description: La méthode getNextSelectedItem récupère l’élément sélectionné suivant dans le contrôle de zone de liste à partir de l’élément après celui avec l’index spécifié.
ms.assetid: 060d196d-2b14-4386-ba01-34256c137db5
keywords:
- LISTBOX. getNextSelectedItem Lecteur Windows Media
topic_type:
- apiref
api_name:
- LISTBOX.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8afb3df1f1b6a6adc528e02dd6531ac4fc1a9a3e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414569"
---
# <a name="listboxgetnextselecteditem"></a>LISTBOX. getNextSelectedItem

La méthode **getNextSelectedItem** récupère l’élément sélectionné suivant dans le contrôle de zone de liste à partir de l’élément après celui avec l’index spécifié.

``` syntax
        elementID.getNextSelectedItem(startIndex)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*
</dt> <dd>

**Nombre** (**long**) contenant l’index de l’élément qui précède l’élément en cours de récupération.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode retourne un **nombre** (**long**) contenant l’index de l’élément sélectionné suivant.

## <a name="remarks"></a>Notes

Pour démarrer la recherche à partir du début, utilisez 1 pour l’index de début.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------|
| Version<br/> | Lecteur Windows Media pour Windows XP ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément LISTBOX**](listbox-element.md)
</dt> </dl>

 

 





