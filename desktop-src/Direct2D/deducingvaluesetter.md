---
title: DeducingValueSetter (D2d1effecthelpers. h)
description: Déduire la classe et les arguments, puis appelle un rappel d’accesseur Set de propriété de fonction membre pour une propriété de type valeur.
ms.assetid: 4C3D64A8-0CC0-405A-A5B3-627C2DF25EA1
keywords:
- DeducingValueSetter Direct2D
topic_type:
- apiref
api_name:
- DeducingValueSetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e002c5a36c8ac0b196dfc5fb25e11f7f9d63806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521620"
---
# <a name="deducingvaluesetter"></a><span data-ttu-id="b5146-104">DeducingValueSetter</span><span class="sxs-lookup"><span data-stu-id="b5146-104">DeducingValueSetter</span></span>

<span data-ttu-id="b5146-105">Déduire la classe et les arguments, puis appelle un rappel d’accesseur Set de propriété de fonction membre pour une propriété de type valeur.</span><span class="sxs-lookup"><span data-stu-id="b5146-105">Deduces the class and arguments and then calls a member-function property setter callback for a value-type property.</span></span>

> [!Note]  
> <span data-ttu-id="b5146-106">DeducingValueSetter ne doit pas être appelé directement.</span><span class="sxs-lookup"><span data-stu-id="b5146-106">DeducingValueSetter should not be called directly.</span></span>

 

``` syntax
template<class C, typename P, typename I>
HRESULT DeducingValueSetter(
    _In_ HRESULT (C::*callback)(P),
    _In_ I *effect,
    _In_reads_(dataSize) const BYTE *data,
    UINT32 dataSize  
    ) 
```

## <a name="requirements"></a><span data-ttu-id="b5146-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5146-107">Requirements</span></span>



| <span data-ttu-id="b5146-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5146-108">Requirement</span></span> | <span data-ttu-id="b5146-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5146-109">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5146-110">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5146-110">Header</span></span><br/> | <dl> <span data-ttu-id="b5146-111"><dt>D2d1effecthelpers. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5146-111"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5146-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5146-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5146-113">**Direct2D ::D educingValueGetter**</span><span class="sxs-lookup"><span data-stu-id="b5146-113">**Direct2D::DeducingValueGetter**</span></span>](deducingvaluegetter.md)
</dt> </dl>

 

 





