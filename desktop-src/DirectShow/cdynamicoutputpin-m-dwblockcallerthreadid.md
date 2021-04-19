---
description: 'Identificateur du thread qui a appelé la méthode IPinFlowControl :: Block sur ce code confidentiel. Cette variable membre est valide uniquement lorsque le code confidentiel est bloqué.'
ms.assetid: 7f8429c5-7e58-49a1-9f36-01088379a193
title: 'Membre CDynamicOutputPin :: m_dwBlockCallerThreadID (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwBlockCallerThreadID
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9aa2de66f1afe690715ab658483c01cdfeb3f451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542782"
---
# <a name="cdynamicoutputpinm_dwblockcallerthreadid-member"></a>CDynamicOutputPin :: m \_ dwBlockCallerThreadID, membre

Identificateur du thread qui a appelé la méthode [**IPinFlowControl :: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) sur ce code confidentiel. Cette variable membre est valide uniquement lorsque le code confidentiel est bloqué.

## <a name="syntax"></a>Syntaxe


```C++
DWORD m_dwBlockCallerThreadID;
```



## <a name="remarks"></a>Notes

Avant d’accéder à cette variable, maintenez la section critique [**CDynamicOutputPin :: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDynamicOutputPin, classe**](cdynamicoutputpin.md)
</dt> </dl>

 

 




