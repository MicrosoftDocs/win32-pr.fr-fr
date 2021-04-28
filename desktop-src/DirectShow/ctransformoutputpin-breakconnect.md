---
description: 'Méthode CTransformOutputPin. BreakConnect : la méthode BreakConnect libère le code confidentiel d’une connexion.'
ms.assetid: bf68aca3-93e5-4f9d-9980-1a5eed1513f5
title: Méthode CTransformOutputPin. BreakConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 92854041e1d553945d0a1ab1755ef3557bd4a8b2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084957"
---
# <a name="ctransformoutputpinbreakconnect-method"></a>Méthode CTransformOutputPin. BreakConnect

La `BreakConnect` méthode libère le code confidentiel d’une connexion.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

Retourne S \_ OK ou une autre valeur **HRESULT** .

## <a name="remarks"></a>Notes 

Cette méthode remplace la méthode [**CBaseOutputPin :: BreakConnect**](cbaseoutputpin-breakconnect.md) . Elle appelle la méthode [**CTransformFilter :: BreakConnect**](ctransformfilter-breakconnect.md) du filtre, qui retourne la valeur \_ OK dans la classe de base. La classe dérivée peut substituer la méthode **CTransformFilter :: BreakConnect** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




