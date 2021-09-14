---
description: La méthode SynchronousBlockOutputPin bloque le code confidentiel. n’est pas retourné tant que le code confidentiel n’est pas bloqué.
ms.assetid: 10fdb788-bc72-4eda-b60b-af83f954d689
title: Méthode CDynamicOutputPin. SynchronousBlockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7fff1a0a1f093b97d07c74d7916ef2a7511d0e16
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006792"
---
# <a name="cdynamicoutputpinsynchronousblockoutputpin-method"></a>Méthode CDynamicOutputPin. SynchronousBlockOutputPin

La `SynchronousBlockOutputPin` méthode bloque le code confidentiel ; ne retourne pas tant que le code confidentiel n’est pas bloqué.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SynchronousBlockOutputPin();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                                                    | Description                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                           | Réussite.<br/>                                      |
| <dl> <dt>**\_code PIN de VFW E \_ \_ déjà \_ bloqué**</dt> </dl>                   | Le code PIN est déjà bloqué sur un autre thread.<br/>     |
| <dl> <dt>**\_ \_ code PIN de VFW E \_ déjà \_ bloqué \_ sur \_ ce \_ thread**</dt> </dl> | Le code PIN est déjà bloqué sur le thread appelant.<br/> |



 

## <a name="remarks"></a>Notes

N’appelez pas cette méthode à partir du thread de streaming.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDynamicOutputPin, classe**](cdynamicoutputpin.md)
</dt> </dl>

 

 




