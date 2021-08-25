---
description: 'Méthode CPosPassThru. ses : la méthode seplaces définit la vitesse de lecture. Cette méthode implémente la méthode IMediaSeeking :: se.'
ms.assetid: 1b38eb5d-38fd-408b-9f20-4f8d18158f92
title: Méthode CPosPassThru. se, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c411f2c342bd54f89ac85ad4275a05e9d7854908c1d8ba88b1181f34e56f57d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909069"
---
# <a name="cpospassthrusetrate-method"></a>CPosPassThru. se, méthode

La `SetRate` méthode définit la vitesse de lecture. Cette méthode implémente la méthode [**IMediaSeeking ::**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) se.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dRate* 
</dt> <dd>

Vitesse de lecture. Ne doit pas être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne E \_ INVALIDARG si *dRate* est égal à zéro. Sinon, retourne la valeur **HRESULT** de la broche connectée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPosPassThru, classe**](cpospassthru.md)
</dt> </dl>

 

 




