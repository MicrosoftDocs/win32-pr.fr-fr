---
description: La méthode DeliverNewSegment fournit une notification de nouveau segment à la broche d’entrée connectée.
ms.assetid: 304f0267-88e0-4642-98a2-68ce973bdeab
title: Méthode CBaseOutputPin. DeliverNewSegment (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverNewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f4c89bb14377cf46e5395fc106807133d53cd090c0ba9e0eae8e103b438d69fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910600"
---
# <a name="cbaseoutputpindelivernewsegment-method"></a>Méthode CBaseOutputPin. DeliverNewSegment

La `DeliverNewSegment` méthode fournit une notification de nouveau segment à la broche d’entrée connectée.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT DeliverNewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*tStart* 
</dt> <dd>

Position du média de départ du segment, en unités de 100 nanosecondes.

</dd> <dt>

*tStop* 
</dt> <dd>

Position du média de fin du segment, en unités de 100 nanosecondes.

</dd> <dt>

*dRate* 
</dt> <dd>

Taux auquel ce segment doit être traité, sous la forme d’un pourcentage du taux d’origine.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                           | Description                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Réussite.<br/>              |
| <dl> <dt>**VFW \_ E \_ non \_ connecté**</dt> </dl> | Le pin n’est pas connecté.<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode appelle la méthode [**IPIN :: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) sur la broche d’entrée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseOutputPin, classe**](cbaseoutputpin.md)
</dt> </dl>

 

 




