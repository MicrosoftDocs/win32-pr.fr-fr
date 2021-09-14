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
ms.openlocfilehash: 3eb6d31a50095affdf38d44b69040304674ec6fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999357"
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

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                           | Description                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Réussite.<br/>              |
| <dl> <dt>**VFW \_ E \_ non \_ connecté**</dt> </dl> | Le pin n’est pas connecté.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode appelle la méthode [**IPIN :: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) sur la broche d’entrée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseOutputPin, classe**](cbaseoutputpin.md)
</dt> </dl>

 

 




