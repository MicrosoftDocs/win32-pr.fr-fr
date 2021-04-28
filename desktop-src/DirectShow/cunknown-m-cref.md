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
ms.openlocfilehash: a3f6be7d09149f651bce8d1042b7f3e3a5dc9307
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084577"
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
| En-tête<br/>  | <dl> <dt>ComBase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




