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
ms.openlocfilehash: efe7e62936c6feb1984a339a67783cdbc1e4f124
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543284"
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

## <a name="remarks"></a>Notes

Cette méthode est appelée par la méthode [**CTransformFilter :: Receive**](ctransformfilter-receive.md) pour préparer l’exemple de sortie. En général, il n’est pas nécessaire d’appeler cette méthode dans votre classe dérivée, sauf si vous substituez la méthode **Receive** .

Cette méthode récupère un nouvel exemple à partir de l’allocateur de la broche de sortie. Il copie ensuite les exemples de propriétés de l’exemple d’entrée dans l’exemple de sortie. Les exemples de propriétés sont définis dans la structure de [**\_ \_ Propriétés am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




