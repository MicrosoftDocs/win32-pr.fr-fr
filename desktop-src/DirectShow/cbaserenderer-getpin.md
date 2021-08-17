---
description: 'Méthode CBaseRenderer. GetPin : la méthode GetPin récupère un code confidentiel.'
ms.assetid: 665e1aaf-4491-4241-94c6-6ea356d7a665
title: Méthode CBaseRenderer. GetPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c85b1a33abec4dfd10cf093e8673e270e7df02533846791a5d5d37702b51313
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822700"
---
# <a name="cbaserenderergetpin-method"></a>Méthode CBaseRenderer. GetPin

La `GetPin` méthode récupère un code confidentiel.

## <a name="syntax"></a>Syntaxe


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*n* 
</dt> <dd>

Numéro du code confidentiel spécifié. Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le pointeur [**CBaseRenderer :: m \_ pInputPin**](cbaserenderer-m-pinputpin.md) .

## <a name="remarks"></a>Remarques

Cette méthode implémente la méthode [**CBaseFilter :: GetPin**](cbasefilter-getpin.md) , qui est virtuelle pure dans la classe **CBaseFilter** . Le filtre prend en charge exactement un pin (la broche d’entrée). La première fois que cette méthode est appelée, elle crée le code confidentiel en tant que nouvel objet [**CRendererInputPin**](crendererinputpin.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




