---
description: La méthode SendQuality envoie un message de qualité pour indiquer ce que le fournisseur doit faire sur la qualité.
ms.assetid: 9ce11c35-958c-4eda-9130-1139c4074bf7
title: Méthode CBaseVideoRenderer. SendQuality (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SendQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acda4bd9b00434e33c24ac44625b3c1d45350d45b4ec0b242d2638333ad11ed9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074763"
---
# <a name="cbasevideorenderersendquality-method"></a>Méthode CBaseVideoRenderer. SendQuality

La `SendQuality` méthode envoie un message de qualité pour indiquer ce que le fournisseur doit faire sur la qualité.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT SendQuality(
   REFERENCE_TIME trLate,
   REFERENCE_TIME trRealStream
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*trLate* 
</dt> <dd>

Durée pendant laquelle le cadre est en retard.

</dd> <dt>

*trRealStream* 
</dt> <dd>

Currentstream.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette fonction membre envoie un message de contrôle qualité en amont pour contrôler la gestion de la qualité. La nature du message de qualité (c’est-à-dire si vous souhaitez réduire ou augmenter le nombre d’échantillons) est déterminée dans l’implémentation de la gestion de la qualité dans cette classe dérivée (voir [**CBaseVideoRenderer :: ShouldDrawSampleNow**](cbasevideorenderer-shoulddrawsamplenow.md)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




