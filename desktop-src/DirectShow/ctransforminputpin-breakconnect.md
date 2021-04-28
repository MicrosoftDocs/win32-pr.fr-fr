---
description: 'Méthode CTransformInputPin. BreakConnect : la méthode BreakConnect libère le code confidentiel d’une connexion.'
ms.assetid: 9874717d-f4d8-426d-a717-9f5d83b4683c
title: Méthode CTransformInputPin. BreakConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe425ba617909dcfb1d66dbb4777b579139d436b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085017"
---
# <a name="ctransforminputpinbreakconnect-method"></a>Méthode CTransformInputPin. BreakConnect

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

Cette méthode remplace la méthode [**CBaseInputPin :: BreakConnect**](cbaseinputpin-breakconnect.md) . Elle appelle la méthode [**CTransformFilter :: BreakConnect**](ctransformfilter-breakconnect.md) du filtre, qui retourne la valeur \_ OK dans la classe de base. La classe dérivée peut substituer la méthode **CTransformFilter :: BreakConnect** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




