---
description: La méthode SetControlVideoPin définit le code confidentiel utilisé par le filtre.
ms.assetid: 4346f828-4380-4150-9ecb-74eb690bdcdf
title: Méthode CBaseControlVideo. SetControlVideoPin (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetControlVideoPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6169b5d2ec71148cd868e340c5a2f4e206355044ce55e0905c20787ddb3a263e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660784"
---
# <a name="cbasecontrolvideosetcontrolvideopin-method"></a>Méthode CBaseControlVideo. SetControlVideoPin

La `SetControlVideoPin` méthode définit le code confidentiel utilisé par le filtre.

## <a name="syntax"></a>Syntaxe


```C++
void SetControlVideoPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPin* 
</dt> <dd>

Pointeur vers le code confidentiel avec lequel l’interface est synchronisée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

L’interface peut être appelée uniquement lorsque le filtre a été connecté avec succès. L’objet est passé par cette méthode au code confidentiel avec lequel il est synchronisé ; dans la plupart des cas, il détermine si le code confidentiel est connecté lorsqu’il a une méthode d’interface appelée et retourne VFW \_ E \_ non \_ connecté en cas d’échec.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




