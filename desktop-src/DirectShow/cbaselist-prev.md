---
description: La méthode PREV récupère la position précédente dans la liste.
ms.assetid: 537c3019-373a-4974-a42e-72150da72767
title: CBaseList. prev, méthode (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Prev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03c35a89754b27aa67a5bba33ee694433d74c0fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526104"
---
# <a name="cbaselistprev-method"></a>CBaseList. prev, méthode

La `Prev` méthode récupère la position précédente dans la liste.

## <a name="syntax"></a>Syntaxe


```C++
POSITION Prev(
   POSITION pos
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pos* 
</dt> <dd>

Valeur de POSITION.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’indicateur de position qui est le précédent à la position spécifiée dans *pos*.

## <a name="remarks"></a>Notes

Si *pos* est la première position dans la liste, la méthode retourne **null**. Si *pos* a la **valeur null**, la méthode retourne la dernière position dans la liste.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseList, classe**](cbaselist.md)
</dt> </dl>

 

 




