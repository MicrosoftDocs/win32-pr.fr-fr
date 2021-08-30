---
description: La méthode AddTail ajoute une liste à la fin de la liste.
ms.assetid: 006cccc5-4fb2-4e3f-9481-5d10c090d24e
title: Méthode CGenericList. AddTail (Wxlist. h)-paramètres plist
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1cf647fb70b6d2896991bda2e8558ad34407f3427a2eef2d2ce8cd4295c95486
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813999"
---
# <a name="cgenericlistaddtail-method-wxlisth---plist-parameter"></a>Méthode CGenericList. AddTail (Wxlist. h)-paramètres plist

La `AddTail` méthode ajoute une liste à la fin de la liste.

## <a name="syntax"></a>Syntaxe


```C++
BOOL AddTail(
   CGenericList<OBJECT> pList
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pList* 
</dt> <dd>

Pointeur vers la liste à ajouter.

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

 

 




