---
description: 'Méthode CPosPassThru. GetAvailable : la méthode GetAvailable récupère la plage de temps pendant laquelle la recherche est efficace. Cette méthode implémente la méthode IMediaSeeking :: GetAvailable.'
ms.assetid: 5f4af41a-eb7b-4caa-97e0-aaed78467723
title: Méthode CPosPassThru. GetAvailable (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e1db45b20264f192b2ade7d8863f9da86d5fc02159567611eff86e9cdfff1b10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084249"
---
# <a name="cpospassthrugetavailable-method"></a>Méthode CPosPassThru. GetAvailable

La `GetAvailable` méthode récupère la plage de temps pendant laquelle la recherche est efficace. Cette méthode implémente la méthode [**IMediaSeeking :: GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pEarliest* 
</dt> <dd>

Pointeur vers une variable qui reçoit l’heure la plus précoce pour une recherche efficace.

</dd> <dt>

*Plaque* 
</dt> <dd>

Pointeur vers une variable qui reçoit l’heure la plus récente pour une recherche efficace.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur **HRESULT** de la broche connectée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPosPassThru, classe**](cpospassthru.md)
</dt> </dl>

 

 




