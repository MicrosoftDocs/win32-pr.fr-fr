---
description: La \_ méthode put StopTime définit l’heure à laquelle la lecture s’arrête, par rapport à la durée du flux. Cette méthode implémente la méthode IMediaPosition ::p ut \_ StopTime.
ms.assetid: 0a344cad-df93-47f1-8c7f-5d5ef775b850
title: Méthode CPosPassThru.put_StopTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f5763700947596a0fb437ba3840df058d4d3239
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010060"
---
# <a name="cpospassthruput_stoptime-method"></a>CPosPassThru. put \_ StopTime, méthode

La `put_StopTime` méthode définit l’heure à laquelle la lecture s’arrêtera, par rapport à la durée du flux. Cette méthode implémente la méthode [**IMediaPosition ::p ut \_ StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_stoptime) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_StopTime(
   REFTIME llTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*llTime* 
</dt> <dd>

Heure d’arrêt en tant que valeur **double** , en secondes.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la valeur **HRESULT** de la broche connectée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPosPassThru, classe**](cpospassthru.md)
</dt> </dl>

 

 




