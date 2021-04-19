---
description: La méthode GetPinCount récupère le nombre de broches.
ms.assetid: 518de15d-2ecf-425e-b4cd-14aaaf938417
title: Méthode CBaseRenderer. GetPinCount (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71b3703389019e2217a595884ac983e90835cdac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532770"
---
# <a name="cbaserenderergetpincount-method"></a>Méthode CBaseRenderer. GetPinCount

La `GetPinCount` méthode récupère le nombre de broches.

## <a name="syntax"></a>Syntaxe


```C++
virtual int GetPinCount();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Renvoie 1.

## <a name="remarks"></a>Notes

Cette méthode implémente la méthode [**CBaseFilter :: GetPinCount**](cbasefilter-getpincount.md) , qui est virtuelle pure dans la classe **CBaseFilter** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




