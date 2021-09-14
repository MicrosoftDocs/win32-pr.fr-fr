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
ms.openlocfilehash: e188a29689a6dd1a54ef401f8bd2677e30989972
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012261"
---
# <a name="csourceseekingm_rtduration-member"></a>CSourceSeeking :: m \_ rtDuration, membre

Durée du flux. Par défaut, la valeur est définie sur la valeur de la variable membre [**CSourceSeeking :: m \_ rtStop**](csourceseeking-m-rtstop.md) .

## <a name="syntax"></a>Syntaxe


```C++
CRefTime m_rtDuration;
```



## <a name="remarks"></a>Notes

Conservez la section critique **m \_ pLock** avant d’accéder à cette variable.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceSeeking, classe**](csourceseeking.md)
</dt> </dl>

 

 




