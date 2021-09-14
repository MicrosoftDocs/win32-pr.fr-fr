---
description: La \_ variable membre m pAlloc est un pointeur vers l’interface IMemAllocator de l’allocateur de mémoire.
ms.assetid: a3be5982-83f0-4552-9bcd-85da4a4918ff
title: 'Membre CPullPin :: m_pAlloc (Pullpin. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAlloc
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e9945bd7b5f3c5b54f0ef578c2b012d0e56935d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007599"
---
# <a name="cpullpinm_palloc-member"></a>CPullPin :: m \_ pAlloc, membre

La `m_pAlloc` variable membre est un pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur de mémoire.

## <a name="syntax"></a>Syntaxe


```C++
IMemAllocator *m_pAlloc;
```



## <a name="remarks"></a>Notes

La méthode [**CPullPin ::D ecideallocator**](cpullpin-decideallocator.md) définit cette variable membre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPullPin, classe**](cpullpin.md)
</dt> </dl>

 

 




