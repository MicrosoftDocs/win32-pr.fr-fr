---
description: La méthode GetI récupère l’élément à la position spécifiée.
ms.assetid: fc775230-491a-49b6-b631-e7d5b8c82d8c
title: Méthode CBaseList. GetI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f543a38c3394943e3ccb1eeb8bb97d29297a4ca230966940245a2f8a8c121b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087439"
---
# <a name="cbaselistgeti-method"></a>Méthode CBaseList. GetI

La `GetI` méthode récupère l’élément à la position spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
void* GetI(
   POSITION pos
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pos* 
</dt> <dd>

Indicateur de position de l’élément à récupérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers l’élément.

## <a name="remarks"></a>Remarques

Si *pos* a la **valeur null**, la méthode retourne la **valeur null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseList, classe**](cbaselist.md)
</dt> </dl>

 

 




