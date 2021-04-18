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
# <a name="deducingstringsetter"></a><span data-ttu-id="57516-104">DeducingStringSetter</span><span class="sxs-lookup"><span data-stu-id="57516-104">DeducingStringSetter</span></span>

<span data-ttu-id="57516-105">Déduire la classe et les arguments, puis appelle un rappel d’accesseur Set de propriété de fonction membre pour une propriété de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="57516-105">Deduces the class and arguments and then calls a member-function property setter callback for a string-type property.</span></span>

> [!Note]  
> <span data-ttu-id="57516-106">DeducingStringSetter ne doit pas être appelé directement.</span><span class="sxs-lookup"><span data-stu-id="57516-106">DeducingStringSetter should not be called directly.</span></span>

 

``` syntax
template<class C, typename I>  
HRESULT DeducingStringSetter(  
    _In_ HRESULT (C::*callback)(PCWSTR string),
    _In_ I *effect,
    _In_reads_(dataSize) const BYTE *data,
    UINT32 dataSize  
    ) 
```

## <a name="requirements"></a><span data-ttu-id="57516-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57516-107">Requirements</span></span>



| <span data-ttu-id="57516-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57516-108">Requirement</span></span> | <span data-ttu-id="57516-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="57516-109">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57516-110">En-tête</span><span class="sxs-lookup"><span data-stu-id="57516-110">Header</span></span><br/> | <dl> <span data-ttu-id="57516-111"><dt>D2d1effecthelpers. h</dt></span><span class="sxs-lookup"><span data-stu-id="57516-111"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57516-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57516-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57516-113">**Direct2D ::D educingStringGetter**</span><span class="sxs-lookup"><span data-stu-id="57516-113">**Direct2D::DeducingStringGetter**</span></span>](deducingstringgetter.md)
</dt> </dl>

 

 





