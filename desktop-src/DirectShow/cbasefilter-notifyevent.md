---
description: La méthode NotifyEvent envoie une notification d’événement au gestionnaire de graphique de filtre.
ms.assetid: 79587b72-4152-4443-9fde-c2746bf06191
title: Méthode CBaseFilter. NotifyEvent (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.NotifyEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e21ab1275aba05331055b7a38631f8c98ae65476aacf8f17073ed1dc45c90bf4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640309"
---
# <a name="cbasefilternotifyevent-method"></a>Méthode CBaseFilter. NotifyEvent

La `NotifyEvent` méthode envoie une notification d’événement au gestionnaire de graphique de filtre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT NotifyEvent(
   long     EventCode,
   LONG_PTR EventParam1,
   LONG_PTR EventParam2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*EventCode* 
</dt> <dd>

Code de notification d’événement.

</dd> <dt>

*EventParam1* 
</dt> <dd>

Premier paramètre de l’événement.

</dd> <dt>

*EventParam2* 
</dt> <dd>

Deuxième paramètre de l’événement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                               | Description                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | Le gestionnaire de graphique de filtre n’accepte pas les notifications d’événements.<br/>                              |
| <dl> <dt>**\_OK**</dt> </dl>      | Réussite.<br/>                                                                                    |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl> | Le filtre n’a pas de pointeur vers l’interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) .<br/> |



 

## <a name="remarks"></a>Remarques

Pour obtenir la liste des codes de notification et des valeurs de paramètres, consultez [codes de notification d’événement](event-notification-codes.md).

Dans la classe de base, si le code d’événement est EC \_ Complete, la méthode définit le paramètre *EventParam2* sur un pointeur vers l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) du filtre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseFilter, classe**](cbasefilter.md)
</dt> </dl>

 

 




