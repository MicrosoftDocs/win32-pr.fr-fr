---
description: La méthode AddHeadI ajoute un élément au début de la liste.
ms.assetid: d83b3c5e-2c6d-4369-a74d-18bf19cfd34d
title: Méthode CBaseList. AddHeadI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6104b6acae0f22c028f3bad050567f4da34ff0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542388"
---
# <a name="cbaselistaddheadi-method"></a>Méthode CBaseList. AddHeadI

La `AddHeadI` méthode ajoute un élément au début de la liste.

## <a name="syntax"></a>Syntaxe


```C++
POSITION AddHeadI(
   void *pObj
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pObj* 
</dt> <dd>

Pointeur désignant l’élément.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur de POSITION indiquant la nouvelle position de la tête.

## <a name="remarks"></a>Notes

Si la méthode échoue, la valeur de retour est **null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseList, classe**](cbaselist.md)
</dt> </dl>

 

 




