---
description: La méthode AddBeforeI insère un élément avant la position spécifiée.
ms.assetid: d310e303-889a-43a6-bda5-2e7b805b25d1
title: Méthode CBaseList. AddBeforeI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBeforeI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6996d2fd3ed0cad07a442530e3ae77470aaf6890
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536016"
---
# <a name="cbaselistaddbeforei-method"></a>Méthode CBaseList. AddBeforeI

La `AddBeforeI` méthode insère un élément avant la position spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
POSITION AddBeforeI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pos* 
</dt> <dd>

Position avant laquelle l’élément doit être ajouté.

</dd> <dt>

*pObj* 
</dt> <dd>

Pointeur désignant l’élément.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’indicateur de position pour l’élément inséré.

## <a name="remarks"></a>Notes

Si *pos* a la **valeur null**, cette méthode ajoute l’élément à la fin de la liste (équivalent à l’appel de la méthode [**CBaseList :: AddTailI**](cbaselist-addtaili.md) ).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseList, classe**](cbaselist.md)
</dt> </dl>

 

 




