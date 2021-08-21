---
description: La méthode AddHead ajoute une liste au début de la liste.
ms.assetid: 9a344bed-d871-4082-9bbb-330f2ff42cca
title: Méthode CGenericList. AddHead (Wxlist. h)-paramètres plist
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c26667ce12af902f3d5cf355a6556dc95e5dd1f5e0cad77f944e663eeef8ce67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656145"
---
# <a name="cgenericlistaddhead-method-wxlisth---plist-parameter"></a>Méthode CGenericList. AddHead (Wxlist. h)-paramètres plist

La `AddHead` méthode ajoute une liste au début de la liste.

## <a name="syntax"></a>Syntaxe


```C++
BOOL AddHead(
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pList* 
</dt> <dd>

Pointeur vers la liste des éléments à ajouter.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| En-tête | Wxlist. h (inclure Flux. h) |
| Bibliothèque| Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CGenericList, classe**](cgenericlist.md)
</dt> </dl>

 

 




