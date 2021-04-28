---
description: 'CDynamicOutputPin. active, méthode : la méthode active indique au code confidentiel que le filtre est maintenant actif.'
ms.assetid: c2b8eb54-1bae-4f52-8324-dc70e3cac577
title: CDynamicOutputPin. active, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d9544c0fd125146b10f008565fcfbe330d18de1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099327"
---
# <a name="cdynamicoutputpinactive-method"></a>CDynamicOutputPin. active, méthode

La `Active` méthode notifie le code confidentiel que le filtre est maintenant actif.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Active();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                            | Description                                                                                                     |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Réussite.<br/>                                                                                             |
| <dl> <dt>**E \_ échec**</dt> </dl> | Échec. [**CDynamicOutputPin :: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) n’a pas été appelé.<br/> |



 

## <a name="remarks"></a>Notes 

Cette méthode remplace la méthode [**CBaseOutputPin :: active**](cbaseoutputpin-active.md) . Il réinitialise l’événement [**CDynamicOutputPin :: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) . Si le filtre propriétaire n’a pas appelé **SetConfigInfo**, cette méthode retourne E \_ Fail.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDynamicOutputPin, classe**](cdynamicoutputpin.md)
</dt> </dl>

 

 




