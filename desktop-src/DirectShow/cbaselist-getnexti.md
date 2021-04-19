---
description: La méthode GetNextI récupère l’élément à la position spécifiée et avance la position.
ms.assetid: 3ec217ec-b0f9-4ff4-bdb7-ac204df99010
title: Méthode CBaseList. GetNextI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetNextI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f96be8d8cdf286a4017e56af7050970d45e8a56e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530535"
---
# <a name="cbaselistgetnexti-method"></a>Méthode CBaseList. GetNextI

La `GetNextI` méthode récupère l’élément à la position spécifiée et avance la position.

## <a name="syntax"></a>Syntaxe


```C++
void* GetNextI(
  [ref] POSITION &rp
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RP* \[ Réf\]
</dt> <dd>

Référence à une valeur de POSITION.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers l’élément. Si *RP* a la **valeur null**, la méthode retourne la **valeur null**.

## <a name="remarks"></a>Notes

Cette méthode avance l’indicateur de position à la position suivante. Si l’indicateur de position se déplace au-delà de la fin de la liste, la méthode lui affecte la **valeur null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseList, classe**](cbaselist.md)
</dt> </dl>

 

 




