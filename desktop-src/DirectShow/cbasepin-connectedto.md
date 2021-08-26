---
description: 'La méthode ConnectedTo récupère un pointeur désignant le code confidentiel connecté, le cas échéant. Cette méthode implémente la méthode IPin :: ConnectedTo.'
ms.assetid: d8978c9a-e498-4411-a052-f3c2fca570ef
title: Méthode CBasePin. ConnectedTo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectedTo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a37eafe9abf226be20cf5d573abc91bc52ee070e7667dbab3a8799f74022c92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916759"
---
# <a name="cbasepinconnectedto-method"></a>Méthode CBasePin. ConnectedTo

La `ConnectedTo` méthode récupère un pointeur vers le code confidentiel connecté, le cas échéant. Cette méthode implémente la méthode [**IPIN :: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ConnectedTo(
   IPin **ppPin
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppPin* 
</dt> <dd>

Adresse d’une variable qui reçoit un pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de l’autre code PIN.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                           | Description                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Réussite.<br/>                   |
| <dl> <dt>**\_pointeur E**</dt> </dl>             | Argument de pointeur **null** .<br/> |
| <dl> <dt>**VFW \_ E \_ non \_ connecté**</dt> </dl> | Le pin n’est pas connecté.<br/>      |



 

## <a name="remarks"></a>Remarques

Si la méthode est réussie, l’interface **IPIN** qu’elle retourne a un nombre de références en suspens. Veillez à le libérer lorsque vous avez terminé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




