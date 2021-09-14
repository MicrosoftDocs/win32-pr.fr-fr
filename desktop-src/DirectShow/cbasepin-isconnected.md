---
description: La méthode IsConnected détermine si le pin est connecté à un autre code confidentiel.
ms.assetid: d8b9b43b-6f8d-4d75-9688-f0cee3794a78
title: CBasePin. IsConnected, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IsConnected
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b857e1ceff4844d66c55cf729a3d2b9771d48846
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923851"
---
# <a name="cbasepinisconnected-method"></a>CBasePin. IsConnected, méthode

La `IsConnected` méthode détermine si le pin est connecté à un autre code confidentiel.

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsConnected();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** si le code PIN est connecté. Sinon, retourne **false**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




