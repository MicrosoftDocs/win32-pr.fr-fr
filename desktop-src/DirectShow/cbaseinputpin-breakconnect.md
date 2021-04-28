---
description: 'Méthode CBaseInputPin. BreakConnect : la méthode BreakConnect libère le code confidentiel d’une connexion.'
ms.assetid: 73b228a9-0a59-4647-b400-c33fa06c7e34
title: Méthode CBaseInputPin. BreakConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5398f675e056da2c60747c0b4eb17c475771bdc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099737"
---
# <a name="cbaseinputpinbreakconnect-method"></a>Méthode CBaseInputPin. BreakConnect

La `BreakConnect` méthode libère le code confidentiel d’une connexion.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.

## <a name="remarks"></a>Notes 

Cette méthode remplace la méthode [**CBasePin :: BreakConnect**](cbasepin-breakconnect.md) . Il annule l’allocation et libère l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .

Si vous substituez cette méthode, appelez la méthode de la classe de base à partir de votre méthode de substitution. Dans le cas contraire, vous risquez de provoquer des fuites de mémoire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseInputPin, classe**](cbaseinputpin.md)
</dt> </dl>

 

 




