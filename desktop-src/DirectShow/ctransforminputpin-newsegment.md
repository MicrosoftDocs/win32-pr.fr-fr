---
description: 'La méthode NewSegment avertit le code confidentiel que les exemples de supports reçus après cet appel sont regroupés en tant que segment. Cette méthode implémente la méthode IPin :: NewSegment.'
ms.assetid: 8925b8b5-13dd-4127-82d8-96525bd4d6fc
title: Méthode CTransformInputPin. NewSegment (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c522755fe898717f0c06af9698be07ab2ebca491666982d6ff62756ef48ae08f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907419"
---
# <a name="ctransforminputpinnewsegment-method"></a>Méthode CTransformInputPin. NewSegment

La `NewSegment` méthode notifie le code confidentiel que les exemples de supports reçus après cet appel sont regroupés en tant que segment. Cette méthode implémente la méthode [**IPIN :: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*tStart* 
</dt> <dd>

Heure de début du segment.

</dd> <dt>

*tStop* 
</dt> <dd>

Heure d’arrêt du segment.

</dd> <dt>

*dRate* 
</dt> <dd>

Taux du segment.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK ou une autre valeur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette méthode remplace la méthode [**CBasePin :: NewSegment**](cbasepin-newsegment.md) . Elle appelle la méthode [**CTransformFilter :: NewSegment**](ctransformfilter-newsegment.md) du filtre pour remettre l’appel en aval.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




