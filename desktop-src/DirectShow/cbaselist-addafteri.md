---
description: La méthode AddAfterI insère un élément après la position spécifiée.
ms.assetid: 6da6c1ed-5f22-4364-b636-64b5a0ce1560
title: Méthode CBaseList. AddAfterI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfterI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b72be7342e6085b773ef2493f5ad138f73349dffcdafc1a60a380692df3f16ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016987"
---
# <a name="cbaselistaddafteri-method"></a>Méthode CBaseList. AddAfterI

La `AddAfterI` méthode insère un élément après la position spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
POSITION AddAfterI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pos* 
</dt> <dd>

Position après laquelle l’élément doit être ajouté.

</dd> <dt>

*pObj* 
</dt> <dd>

Pointeur vers l’élément à ajouter.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’indicateur de position de l’élément inséré.

## <a name="remarks"></a>Remarques

Si *pos* a la **valeur null**, cette méthode ajoute l’élément au début de la liste (équivalent à l’appel de la méthode [**CBaseList :: AddHeadI**](cbaselist-addheadi.md) ).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseList, classe**](cbaselist.md)
</dt> </dl>

 

 




