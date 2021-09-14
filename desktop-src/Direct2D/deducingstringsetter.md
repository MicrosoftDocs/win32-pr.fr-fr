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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113377"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D2d1effecthelpers. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Direct2D ::D educingStringGetter**](deducingstringgetter.md)
</dt> </dl>

 

 





