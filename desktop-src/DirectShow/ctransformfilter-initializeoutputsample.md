---
description: La méthode InitializeOutputSample récupère un nouvel exemple de sortie et l’initialise.
ms.assetid: a4f8f514-cf1a-4f8f-ac17-17378705c2ea
title: CTransformFilter.Iniméthode tializeOutputSample (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.InitializeOutputSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 083867f2ef6b2e40462112036dbbb000c25bc3ad2bb443f011235e36bf245ab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953618"
---
# <a name="ctransformfilterinitializeoutputsample-method"></a>CTransformFilter.Iniméthode tializeOutputSample

La `InitializeOutputSample` méthode récupère un nouvel exemple de sortie et l’initialise.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT InitializeOutputSample(
   IMediaSample *pSample,
   IMediaSample **ppOutSample
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSample* 
</dt> <dd>

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple d’entrée.

</dd> <dt>

*ppOutSample* 
</dt> <dd>

Reçoit un pointeur vers l’interface **IMediaSample** de l’exemple de sortie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK ou une autre valeur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette méthode est appelée par la méthode [**CTransformFilter :: Receive**](ctransformfilter-receive.md) pour préparer l’exemple de sortie. En général, il n’est pas nécessaire d’appeler cette méthode dans votre classe dérivée, sauf si vous substituez la méthode **Receive** .

Cette méthode récupère un nouvel exemple à partir de l’allocateur de la broche de sortie. Il copie ensuite les exemples de propriétés de l’exemple d’entrée dans l’exemple de sortie. Les exemples de propriétés sont définis dans la structure de [**\_ \_ Propriétés am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




