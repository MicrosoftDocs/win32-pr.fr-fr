---
description: La méthode AddTail ajoute une autre liste à la fin de cette liste.
ms.assetid: 996523cd-d9ba-406a-afdf-494d328dc9dd
title: Méthode CBaseList. AddTail (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36d42f0b80703457032e5dde37f6d1549da089c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545496"
---
# <a name="cbaselistaddtail-method"></a>Méthode CBaseList. AddTail

La `AddTail` méthode ajoute une autre liste à la fin de cette liste.

## <a name="syntax"></a>Syntaxe


```C++
BOOL AddTail(
   CBaseList *pList
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

## <a name="remarks"></a>Notes

Si la méthode échoue, il se peut que certains éléments aient été ajoutés à la liste.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseList, classe**](cbaselist.md)
</dt> </dl>

 

 




