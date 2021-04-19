---
description: La méthode MoveToHead fractionne la liste et insère la partie de la fin à l’en-tête d’une autre liste.
ms.assetid: 46e4f8fe-6707-44c6-9d49-0168b35d2364
title: Méthode CBaseList. MoveToHead (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 80adec6c8e2f6d42b5cf2cabd3a83a4c3aededa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539688"
---
# <a name="cbaselistmovetohead-method"></a>Méthode CBaseList. MoveToHead

La `MoveToHead` méthode fractionne la liste et insère la partie de la fin à l’en-tête d’une autre liste.

## <a name="syntax"></a>Syntaxe


```C++
BOOL MoveToHead(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pos* 
</dt> <dd>

Indicateur de position qui marque le fractionnement dans la liste.

</dd> <dt>

*pList* 
</dt> <dd>

Pointeur vers une autre liste.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Cette méthode fractionne la liste avant la position spécifiée par le paramètre *pos* . La partie Head reste dans la liste. La partie fin est insérée au début de l’autre liste.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseList, classe**](cbaselist.md)
</dt> </dl>

 

 




