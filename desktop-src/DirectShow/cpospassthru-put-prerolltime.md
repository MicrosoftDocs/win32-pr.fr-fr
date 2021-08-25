---
description: La \_ méthode put PrerollTime définit la quantité de données qui seront placées en file d’attente avant la position de début. Cette méthode implémente la méthode IMediaPosition ::p ut \_ PrerollTime.
ms.assetid: 5c35fb1d-2296-493f-8104-601127d7dd9f
title: Méthode CPosPassThru.put_PrerollTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 825c3c584fc6db7eb9f94b4e8d01e003f5cf6c36ff8adac4041fd48f792ca858
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909199"
---
# <a name="cpospassthruput_prerolltime-method"></a>CPosPassThru. put \_ PrerollTime, méthode

La `put_PrerollTime` méthode définit la quantité de données qui seront placées en file d’attente avant la position de début. Cette méthode implémente la méthode [**IMediaPosition ::p ut \_ PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_prerolltime) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_PrerollTime(
   REFTIME llTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*llTime* 
</dt> <dd>

Durée du préroll, en secondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur **HRESULT** de la broche connectée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPosPassThru, classe**](cpospassthru.md)
</dt> </dl>

 

 




