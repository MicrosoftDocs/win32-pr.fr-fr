---
description: 'Méthode CBaseOutputPin. BreakConnect : la méthode BreakConnect libère le code confidentiel d’une connexion.'
ms.assetid: 0dec3c9d-1adf-4fa3-ab5a-c351053f8054
title: Méthode CBaseOutputPin. BreakConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ae03edb843a2b9c6f1cbc98a46c2464de0e76e2eecf5d77bc309efa2dd60fd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793218"
---
# <a name="cbaseoutputpinbreakconnect-method"></a>Méthode CBaseOutputPin. BreakConnect

La `BreakConnect` méthode libère le code confidentiel d’une connexion.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.

## <a name="remarks"></a>Remarques

Cette méthode remplace la méthode [**CBasePin :: BreakConnect**](cbasepin-breakconnect.md) . Il annule l’allocation et libère les interfaces [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) et [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) .

Si vous substituez cette méthode, appelez la méthode de la classe de base à partir de votre méthode de substitution. Dans le cas contraire, vous risquez de provoquer des fuites de mémoire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseOutputPin, classe**](cbaseoutputpin.md)
</dt> </dl>

 

 




