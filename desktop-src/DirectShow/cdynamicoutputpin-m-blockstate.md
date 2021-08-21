---
description: État de blocage.
ms.assetid: 55afd314-efd3-47bf-80e3-e17c1332a4cf
title: 'Membre CDynamicOutputPin :: m_BlockState (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_BlockState
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f539f200e6424aeccf4e507c25f5debbcc295cfdd9469e05dd1c9db71d6d121
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119292179"
---
# <a name="cdynamicoutputpinm_blockstate-member"></a>CDynamicOutputPin :: m \_ BlockState, membre

État de blocage.

## <a name="syntax"></a>Syntaxe


```C++
BLOCK_STATE m_BlockState;
```



## <a name="remarks"></a>Notes

Les États suivants sont définis :

-   NON \_ bloqué
-   PENDING
-   OBSTRUÉ

Avant d’accéder à cette variable, maintenez la section critique [**CDynamicOutputPin :: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) .

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDynamicOutputPin, classe**](cdynamicoutputpin.md)
</dt> </dl>

 

 




