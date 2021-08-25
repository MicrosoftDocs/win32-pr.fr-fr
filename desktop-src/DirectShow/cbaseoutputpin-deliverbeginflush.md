---
description: 'Méthode CBaseOutputPin. DeliverBeginFlush : la méthode DeliverBeginFlush demande à la broche d’entrée connectée de commencer une opération de vidage.'
ms.assetid: 0d7c7bd7-2a7a-42a4-a0de-60205b62e49c
title: Méthode CBaseOutputPin. DeliverBeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverBeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f154835a78ba2dab40f6cd505f6dc25e00ef60b6d070a2b4b19e1123c370478f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814199"
---
# <a name="cbaseoutputpindeliverbeginflush-method"></a>Méthode CBaseOutputPin. DeliverBeginFlush

La `DeliverBeginFlush` méthode demande à la broche d’entrée connectée de commencer une opération de vidage.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                           | Description                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Réussite.<br/>              |
| <dl> <dt>**VFW \_ E \_ non \_ connecté**</dt> </dl> | Le pin n’est pas connecté.<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode appelle la méthode [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sur la broche d’entrée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseOutputPin, classe**](cbaseoutputpin.md)
</dt> </dl>

 

 




