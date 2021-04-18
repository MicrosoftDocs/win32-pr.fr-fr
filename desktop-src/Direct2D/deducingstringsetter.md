---
title: DeducingStringSetter (D2d1effecthelpers. h)
description: Déduire la classe et les arguments, puis appelle un rappel d’accesseur Set de propriété de fonction membre pour une propriété de type chaîne.
ms.assetid: D3075B7B-D253-4F85-9FD2-3487C4207122
keywords:
- DeducingStringSetter Direct2D
topic_type:
- apiref
api_name:
- DeducingStringSetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7860978fd271b2ff395caae068cd651d3057020
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540498"
---
# <a name="deducingstringsetter"></a>DeducingStringSetter

Déduire la classe et les arguments, puis appelle un rappel d’accesseur Set de propriété de fonction membre pour une propriété de type chaîne.

> [!Note]  
> DeducingStringSetter ne doit pas être appelé directement.

 

``` syntax
template<class C, typename I>  
HRESULT DeducingStringSetter(  
    _In_ HRESULT (C::*callback)(PCWSTR string),
    _In_ I *effect,
    _In_reads_(dataSize) const BYTE *data,
    UINT32 dataSize  
    ) 
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D2d1effecthelpers. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Direct2D ::D educingStringGetter**](deducingstringgetter.md)
</dt> </dl>

 

 





