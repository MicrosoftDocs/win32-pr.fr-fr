---
title: DeducingStringGetter (D2d1effecthelpers. h)
description: Déduire la classe et les arguments, puis appelle un rappel d’accesseur Get de propriété de fonction membre pour une propriété de type chaîne.
ms.assetid: 434E3360-D6C3-46CB-818E-15A185F4BB84
keywords:
- DeducingStringGetter Direct2D
topic_type:
- apiref
api_name:
- DeducingStringGetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac65b9e5d7e37e2db83f06f80172e90f9f27f80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532891"
---
# <a name="deducingstringgetter"></a><span data-ttu-id="c380c-104">DeducingStringGetter</span><span class="sxs-lookup"><span data-stu-id="c380c-104">DeducingStringGetter</span></span>

<span data-ttu-id="c380c-105">Déduire la classe et les arguments, puis appelle un rappel d’accesseur Get de propriété de fonction membre pour une propriété de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="c380c-105">Deduces the class and arguments and then calls a member-function property getter callback for a string-type property.</span></span>

> [!Note]  
> <span data-ttu-id="c380c-106">DeducingStringGetter ne doit pas être appelé directement.</span><span class="sxs-lookup"><span data-stu-id="c380c-106">DeducingStringGetter should not be called directly.</span></span>

 

``` syntax
template<class C, typename I>  
HRESULT DeducingStringGetter(
    _In_ HRESULT (C::*callback)(PWSTR, UINT32, UINT32*) const,
    _In_ const I *effect,
    _Out_writes_opt_(dataSize) BYTE *data,
    UINT32 dataSize,
    _Out_opt_ UINT32 *actualSize 
    ) 
```

## <a name="requirements"></a><span data-ttu-id="c380c-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c380c-107">Requirements</span></span>



| <span data-ttu-id="c380c-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c380c-108">Requirement</span></span> | <span data-ttu-id="c380c-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="c380c-109">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c380c-110">En-tête</span><span class="sxs-lookup"><span data-stu-id="c380c-110">Header</span></span><br/> | <dl> <span data-ttu-id="c380c-111"><dt>D2d1effecthelpers. h</dt></span><span class="sxs-lookup"><span data-stu-id="c380c-111"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c380c-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c380c-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c380c-113">**Direct2D ::D educingStringSetter**</span><span class="sxs-lookup"><span data-stu-id="c380c-113">**Direct2D::DeducingStringSetter**</span></span>](deducingstringsetter.md)
</dt> </dl>

 

 





