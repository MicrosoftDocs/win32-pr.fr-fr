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
ms.openlocfilehash: a4cf47469800a4d1ecd8abe373d6f3c1fd53ece5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121965"
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

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

L’interface peut être appelée uniquement lorsque le filtre a été connecté avec succès. L’objet est passé par cette méthode au code confidentiel avec lequel il est synchronisé ; dans la plupart des cas, il détermine si le code confidentiel est connecté lorsqu’il a une méthode d’interface appelée et retourne VFW \_ E \_ non \_ connecté en cas d’échec.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




