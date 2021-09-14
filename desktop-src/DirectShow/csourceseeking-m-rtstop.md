---
description: Heure d’arrêt. Par défaut, la valeur est définie sur un très grand nombre. La classe dérivée peut réinitialiser la valeur dans son constructeur, ou lorsque le filtre est initialisé.
ms.assetid: 1fddcf84-fd9a-4dad-892c-1b0abbb0ca55
title: 'Membre CSourceSeeking :: m_rtStop (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtStop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 28031f245ef877eca38129df2a86210f90093db4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012258"
---
# <a name="csourceseekingm_rtstop-member"></a>CSourceSeeking :: m \_ rtStop, membre

Heure d’arrêt. Par défaut, la valeur est définie sur un très grand nombre. La classe dérivée peut réinitialiser la valeur dans son constructeur, ou lorsque le filtre est initialisé.

## <a name="syntax"></a>Syntaxe


```C++
CRefTime m_rtStop;
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

 

 




