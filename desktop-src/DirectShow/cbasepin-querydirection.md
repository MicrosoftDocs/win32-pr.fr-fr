---
description: 'La méthode QueryDirection récupère la direction du code confidentiel (entrée ou sortie). Cette méthode implémente la méthode IPin :: QueryDirection.'
ms.assetid: c28332dc-5ac4-4c89-98b4-281424f36ba9
title: Méthode CBasePin. QueryDirection (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryDirection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7e2ebfaa3d12b5f582b4b67014280fa0a0d5299d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543801"
---
# <a name="cbasepinquerydirection-method"></a>Méthode CBasePin. QueryDirection

La `QueryDirection` méthode récupère la direction du code confidentiel (entrée ou sortie). Cette méthode implémente la méthode [**IPIN :: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT QueryDirection(
   PIN_DIRECTION *pPinDir
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPinDir* 
</dt> <dd>

Pointeur vers une variable qui reçoit un membre du type énuméré de [**\_ direction de l’épinglage**](/windows/win32/api/strmif/ne-strmif-pin_direction) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le \_ pointeur S ou OK \_ .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




