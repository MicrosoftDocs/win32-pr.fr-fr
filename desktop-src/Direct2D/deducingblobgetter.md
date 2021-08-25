---
title: DeducingBlobGetter (D2d1effecthelpers. h)
description: Déduire la classe et les arguments, puis appelle un rappel d’accesseur Get de propriété de fonction membre pour une propriété de type BLOB.
ms.assetid: 1B8800CB-2AD0-4684-99D7-986F6C53A6F1
keywords:
- DeducingBlobGetter Direct2D
topic_type:
- apiref
api_name:
- DeducingBlobGetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f045f781ae22aa4550a298ba7becfe2bc4a939528657f663ec021870bf3afa78
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918279"
---
# <a name="deducingblobgetter"></a>DeducingBlobGetter

Déduire la classe et les arguments, puis appelle un rappel d’accesseur Get de propriété de fonction membre pour une propriété de type BLOB.

> [!Note]  
> DeducingBlobGetter ne doit pas être appelé directement.

 

``` syntax
template<class C, typename I>  
HRESULT DeducingBlobGetter(  
    _In_ HRESULT (C::*callback)(BYTE *, UINT32, UINT32*) const,  
    _In_ const I *effect,  
    _Out_writes_opt_(dataSize) BYTE *data,  
    UINT32 dataSize,  
    _Out_opt_ UINT32 *actualSize  
    ) 
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D2d1effecthelpers. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Direct2D ::D educingBlobSetter**](deducingblobsetter.md)
</dt> </dl>

 

 





