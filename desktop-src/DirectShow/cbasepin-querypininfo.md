---
description: 'La méthode QueryPinInfo récupère des informations sur le code confidentiel. Cette méthode implémente la méthode IPin :: QueryPinInfo.'
ms.assetid: 9de41f61-9f03-4594-a320-2f7f0ed734fd
title: Méthode CBasePin. QueryPinInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 544039b1076848cb796f290ea98aa8aac359b26ebfb64f90a27d316a9d0cc34f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823229"
---
# <a name="cbasepinquerypininfo-method"></a>Méthode CBasePin. QueryPinInfo

La `QueryPinInfo` méthode récupère des informations sur le code confidentiel. Cette méthode implémente la méthode [**IPIN :: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT QueryPinInfo(
   PIN_INFO *pInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pInfo* 
</dt> <dd>

Pointeur vers une structure d' [**\_ informations de code confidentiel**](/windows/win32/api/strmif/ns-strmif-pin_info) qui reçoit les informations de code confidentiel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le \_ pointeur S ou OK \_ .

## <a name="remarks"></a>Remarques

Cette méthode utilise la variable membre [**CBasePin :: m \_ pname**](cbasepin-m-pname.md) pour le membre **achName** de la structure d’informations sur le code confidentiel \_ .

Lorsque la méthode est retournée, si le membre **pFilter** de la structure info de code confidentiel \_ est non **null**, il a un nombre de références en suspens. Veillez à libérer l’interface lorsque vous avez terminé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




