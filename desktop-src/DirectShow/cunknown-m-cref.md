---
description: 'CUnknown :: m_cRef nombre de références de membre.'
ms.assetid: be619a85-ca73-4cee-9df7-20e7be21853b
title: 'CUnknown :: m_cRef, membre (ComBase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_cRef
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0b7830b63e92bea8fa077f6764c080e312c3b820a399129e34887ffe1f9c5c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076019"
---
# <a name="cunknownm_cref-member"></a>CUnknown :: m, \_ membre CREF

Nombre de références.

## <a name="syntax"></a>Syntaxe


```C++
LONG m_cRef;
```



## <a name="remarks"></a>Notes

Utilisez cette variable membre si vous substituez la méthode [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md) ou [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>combase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




