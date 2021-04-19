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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541669"
---
# <a name="cpullpinm_palloc-member"></a><span data-ttu-id="1c229-103">CPullPin :: m \_ pAlloc, membre</span><span class="sxs-lookup"><span data-stu-id="1c229-103">CPullPin::m\_pAlloc member</span></span>

<span data-ttu-id="1c229-104">La `m_pAlloc` variable membre est un pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="1c229-104">The `m_pAlloc` member variable is a pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface of the memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c229-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c229-105">Syntax</span></span>


```C++
IMemAllocator *m_pAlloc;
```



## <a name="remarks"></a><span data-ttu-id="1c229-106">Notes</span><span class="sxs-lookup"><span data-stu-id="1c229-106">Remarks</span></span>

<span data-ttu-id="1c229-107">La méthode [**CPullPin ::D ecideallocator**](cpullpin-decideallocator.md) définit cette variable membre.</span><span class="sxs-lookup"><span data-stu-id="1c229-107">The [**CPullPin::DecideAllocator**](cpullpin-decideallocator.md) method sets this member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c229-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c229-108">Requirements</span></span>



| <span data-ttu-id="1c229-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c229-109">Requirement</span></span> | <span data-ttu-id="1c229-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c229-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c229-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="1c229-111">Header</span></span><br/>  | <dl> <span data-ttu-id="1c229-112"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c229-112"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="1c229-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1c229-113">Library</span></span><br/> | <dl> <span data-ttu-id="1c229-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1c229-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c229-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c229-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c229-116">**CPullPin, classe**</span><span class="sxs-lookup"><span data-stu-id="1c229-116">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




