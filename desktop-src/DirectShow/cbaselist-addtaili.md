---
description: La méthode AddTailI ajoute un élément à la fin de la liste.
ms.assetid: 699408d1-fee2-43d7-b2c3-51637d063b2c
title: Méthode CBaseList. AddTailI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTailI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3317877bfa67d2d39d469882e0b12b9fd79a923873022a51ee48712fc772743
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659125"
---
# <a name="cbaselistaddtaili-method"></a>Méthode CBaseList. AddTailI

La `AddTailI` méthode ajoute un élément à la fin de la liste.

## <a name="syntax"></a>Syntaxe


```C++
POSITION AddTailI(
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

Retourne une valeur de POSITION pour la nouvelle position de fin.

## <a name="remarks"></a>Remarques

Si la méthode échoue, elle retourne la **valeur null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseList, classe**](cbaselist.md)
</dt> </dl>

 

 




