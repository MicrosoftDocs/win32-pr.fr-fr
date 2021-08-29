---
description: 'Méthode CSourceSeeking. ses : la méthode seplaces définit la vitesse de lecture. Cette méthode implémente la méthode IMediaSeeking :: se.'
ms.assetid: 954e2381-207a-47d9-a0a5-87dc325f52b4
title: Méthode CSourceSeeking. se, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f51b0425837cc48176490ea5d5d35cd2eae1851e7e56fa35b3578e37898afdd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053879"
---
# <a name="csourceseekingsetrate-method"></a>CSourceSeeking. se, méthode

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

Vitesse de lecture.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette méthode met à jour la valeur de la variable membre [**CSourceSeeking :: m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) , puis appelle la méthode virtuelle pure [**CSourceSeeking :: ChangeRate**](csourceseeking-changerate.md). La méthode ne valide pas le paramètre *dRate* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceSeeking, classe**](csourceseeking.md)
</dt> </dl>

 

 




