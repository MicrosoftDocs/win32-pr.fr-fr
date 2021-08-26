---
description: 'Durée du flux. Par défaut, la valeur est définie sur la valeur de la variable membre CSourceSeeking :: m \_ rtStop.'
ms.assetid: a87b321e-3179-4485-969b-bf12cb634b43
title: 'Membre CSourceSeeking :: m_rtDuration (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtDuration
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6aa62a3cdf906a4e9666b7786c08e49fca250ef042d187902132410cc2f0abaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053969"
---
# <a name="csourceseekingm_rtduration-member"></a>CSourceSeeking :: m \_ rtDuration, membre

Durée du flux. Par défaut, la valeur est définie sur la valeur de la variable membre [**CSourceSeeking :: m \_ rtStop**](csourceseeking-m-rtstop.md) .

## <a name="syntax"></a>Syntaxe


```C++
CRefTime m_rtDuration;
```



## <a name="remarks"></a>Notes

Conservez la section critique **m \_ pLock** avant d’accéder à cette variable.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceSeeking, classe**](csourceseeking.md)
</dt> </dl>

 

 




