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
ms.openlocfilehash: f4a5d95880b1300ebfb7f1732e7c20b6975ad82cf2d15514c58e68b9f9c42cc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003399"
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

## <a name="remarks"></a>Remarques

Pour démarrer la recherche à partir du début, utilisez 1 pour l’index de début.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------|
| Version<br/> | Lecteur Windows Media pour Windows XP ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément LISTBOX**](listbox-element.md)
</dt> </dl>

 

 





