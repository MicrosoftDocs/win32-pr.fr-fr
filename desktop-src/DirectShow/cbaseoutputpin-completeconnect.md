---
description: 'Méthode CBaseOutputPin. CompleteConnect : la méthode CompleteConnect effectue une connexion à une broche d’entrée.'
ms.assetid: 44c28c71-2c69-40ca-9bc4-c10394475a0f
title: Méthode CBaseOutputPin. CompleteConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9832ddc0a68936461f9fe9ee8a70a7da3227f93e9b0bc9f7328d4cc2f95c2f28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823669"
---
# <a name="cbaseoutputpincompleteconnect-method"></a>Méthode CBaseOutputPin. CompleteConnect

La `CompleteConnect` méthode termine une connexion à une broche d’entrée.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Pointeur vers la broche d’entrée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.

## <a name="remarks"></a>Remarques

Cette méthode remplace la méthode [**CBasePin :: CompleteConnect**](cbasepin-completeconnect.md) . Elle appelle la méthode [**DecideAllocator**](cbaseoutputpin-decideallocator.md) , qui sélectionne l’allocateur de mémoire à utiliser pour cette connexion.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseOutputPin, classe**](cbaseoutputpin.md)
</dt> </dl>

 

 




