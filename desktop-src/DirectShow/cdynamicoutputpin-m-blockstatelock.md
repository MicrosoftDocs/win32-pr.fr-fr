---
description: Section critique qui protège l’état de blocage.
ms.assetid: 6d20cf4c-2c27-41e6-8d01-6cb5e3876a38
title: 'Membre CDynamicOutputPin :: m_BlockStateLock (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_BlockStateLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa5382a30dcd434965c53e893d6818ab0f08a84c19ea0ddec53846c0c01c80f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656679"
---
# <a name="cdynamicoutputpinm_blockstatelock-member"></a>CDynamicOutputPin :: m \_ BlockStateLock, membre

Section critique qui protège l’état de blocage.

## <a name="syntax"></a>Syntaxe


```C++
CCritSec m_BlockStateLock;
```



## <a name="remarks"></a>Notes

Tenez cette section critique avant d’utiliser l’une des variables de membre suivantes :

-   [**CDynamicOutputPin :: m \_ BlockState**](cdynamicoutputpin-m-blockstate.md)
-   [**CDynamicOutputPin :: m \_ dwBlockCallerThreadID**](cdynamicoutputpin-m-dwblockcallerthreadid.md)
-   [**CDynamicOutputPin :: m \_ dwNumOutstandingOutputPinUsers**](cdynamicoutputpin-m-dwnumoutstandingoutputpinusers.md)
-   [**CDynamicOutputPin :: m \_ hNotifyCallerPinBlockedEvent**](cdynamicoutputpin-m-hnotifycallerpinblockedevent.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDynamicOutputPin, classe**](cdynamicoutputpin.md)
</dt> </dl>

 

 




