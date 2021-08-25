---
description: La méthode DeliverEndOfStream fournit une notification de fin de flux à la broche d’entrée connectée.
ms.assetid: 5b564675-a1e0-4010-b35d-28315c262bcc
title: Méthode CBaseOutputPin. DeliverEndOfStream (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c13463ae4effb9fee31ad7c9201ad5af6fd406099c5259c2e6fdff9dcbb62798
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814189"
---
# <a name="cbaseoutputpindeliverendofstream-method"></a>Méthode CBaseOutputPin. DeliverEndOfStream

La `DeliverEndOfStream` méthode fournit une notification de fin de flux à la broche d’entrée connectée.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT DeliverEndOfStream();
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

Cette méthode appelle la méthode [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sur la broche d’entrée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseOutputPin, classe**](cbaseoutputpin.md)
</dt> </dl>

 

 




