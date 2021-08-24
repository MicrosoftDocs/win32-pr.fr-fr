---
description: 'La méthode SetPreroll spécifie si cet exemple est un exemple de préroll. Un exemple de préroll ne doit pas être affiché. Cette méthode implémente la méthode IMediaSample :: SetPreroll.'
ms.assetid: 2887e627-5999-407a-88d3-811c803c9a43
title: Méthode CMediaSample. SetPreroll (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 410031ccf60e830c51615d267d3324167169c5de7960f79dc05b8c9e267463bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832099"
---
# <a name="cmediasamplesetpreroll-method"></a>Méthode CMediaSample. SetPreroll

La `SetPreroll` méthode spécifie si cet exemple est un exemple de préroll. Un exemple de préroll ne doit pas être affiché. Cette méthode implémente la méthode [**IMediaSample :: SetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setpreroll) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetPreroll(
   BOOL bIsPreroll
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bIsPreroll* 
</dt> <dd>

Valeur booléenne qui spécifie s’il s’agit d’un exemple de préroll. Si la **valeur est true**, il s’agit d’un exemple de préroll.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

Cette méthode met à jour la variable de membre [**CMediaSample :: m \_ dwFlags**](cmediasample-m-dwflags.md) , qui spécifie la propriété preroll.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

 




