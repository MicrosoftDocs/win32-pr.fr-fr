---
description: La méthode AsynchronousBlockOutputPin bloque le code confidentiel. La méthode peut retourner avant que le code confidentiel soit bloqué.
ms.assetid: 14cdc973-f0d3-4d1b-8491-67c1421f630b
title: Méthode CDynamicOutputPin. AsynchronousBlockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.AsynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67232bf1081f9c9ea088968cb6c5d02667b00eeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542784"
---
# <a name="cdynamicoutputpinasynchronousblockoutputpin-method"></a>Méthode CDynamicOutputPin. AsynchronousBlockOutputPin

La `AsynchronousBlockOutputPin` méthode bloque le code confidentiel. La méthode peut retourner avant que le code confidentiel soit bloqué.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AsynchronousBlockOutputPin(
   HANDLE hNotifyCallerPinBlockedEvent
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hNotifyCallerPinBlockedEvent* 
</dt> <dd>

Handle vers un événement. L’événement est signalé lorsque la broche de sortie est bloquée, ou si l’appelant annule l’opération de blocage.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                                                    | Description                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                           | Opération réussie.<br/>                                      |
| <dl> <dt>**\_code PIN de VFW E \_ \_ déjà \_ bloqué**</dt> </dl>                   | Le code PIN est déjà bloqué sur un autre thread.<br/>     |
| <dl> <dt>**\_ \_ code PIN de VFW E \_ déjà \_ bloqué \_ sur \_ ce \_ thread**</dt> </dl> | Le code PIN est déjà bloqué sur le thread appelant.<br/> |



 

## <a name="remarks"></a>Notes

N’appelez pas cette méthode à partir du thread de streaming.

Si aucun thread de streaming n’utilise le code confidentiel, cette méthode bloque immédiatement le code confidentiel. Dans le cas contraire, elle définit l’état du pin sur « Pending » et retourne. Lorsque l’opération de diffusion en continu est terminée, le thread de streaming appelle la méthode [**CDynamicOutputPin :: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) , qui bloque le code confidentiel et signale l’événement **hNotifyCallerPinBlockedEvent** . Pour annuler un bloc en attente, appelez la méthode [**CDynamicOutputPin :: UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDynamicOutputPin, classe**](cdynamicoutputpin.md)
</dt> </dl>

 

 




