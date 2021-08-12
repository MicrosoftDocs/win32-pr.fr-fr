---
description: Événement signalé lorsque le code confidentiel se bloque correctement ou lorsque l’utilisateur annule un bloc en attente.
ms.assetid: 699bb7f7-e4f7-47c3-bbb1-0bc6556651ae
title: 'Membre CDynamicOutputPin :: m_hNotifyCallerPinBlockedEvent (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hNotifyCallerPinBlockedEvent
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cfea481a3f24aee808fffba9be91b1fecf63fce8a875dc056420a8f075b677d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656404"
---
# <a name="cdynamicoutputpinm_hnotifycallerpinblockedevent-member"></a>CDynamicOutputPin :: m \_ hNotifyCallerPinBlockedEvent, membre

Événement signalé lorsque le code confidentiel se bloque correctement ou lorsque l’utilisateur annule un bloc en attente.

## <a name="syntax"></a>Syntaxe


```C++
HANDLE m_hNotifyCallerPinBlockedEvent;
```



## <a name="remarks"></a>Notes

Avant d’accéder à cette variable, maintenez la section critique [**CDynamicOutputPin :: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDynamicOutputPin, classe**](cdynamicoutputpin.md)
</dt> </dl>

 

 




