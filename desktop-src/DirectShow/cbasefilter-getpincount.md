---
description: La méthode GetPinCount récupère le nombre de broches.
ms.assetid: 6cbeb123-d899-4f13-8b40-5666adec610f
title: Méthode CBaseFilter. GetPinCount (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8da1cbc22a49b149bdccc36c3b854b44101b9bbc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526820"
---
# <a name="cbasefiltergetpincount-method"></a>Méthode CBaseFilter. GetPinCount

La `GetPinCount` méthode récupère le nombre de broches.

## <a name="syntax"></a>Syntaxe


```C++
virtual int GetPinCount() = 0;
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne le nombre de broches.

## <a name="remarks"></a>Notes

La classe dérivée doit implémenter cette méthode virtuelle pure. Retourne le nombre de codes confidentiels actuellement disponibles sur ce filtre. Les filtres peuvent créer ou détruire dynamiquement des broches.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseFilter, classe**](cbasefilter.md)
</dt> </dl>

 

 




