---
description: Nombre de mémoires tampons à fournir.
ms.assetid: 73f87b14-4346-4909-bd1e-c4981cde403d
title: 'Membre CBaseAllocator :: m_lCount (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16ab469db1d50007bd3aa55ab692c51aa7600452
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525521"
---
# <a name="cbaseallocatorm_lcount-member"></a><span data-ttu-id="f1c2d-103">CBaseAllocator :: m \_ lCount, membre</span><span class="sxs-lookup"><span data-stu-id="f1c2d-103">CBaseAllocator::m\_lCount member</span></span>

<span data-ttu-id="f1c2d-104">Nombre de mémoires tampons à fournir.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-104">Number of buffers to provide.</span></span> <span data-ttu-id="f1c2d-105">La méthode [**CBaseAllocator :: SetProperties**](cbaseallocator-setproperties.md) définit cette valeur.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-105">The [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method sets this value.</span></span> <span data-ttu-id="f1c2d-106">Les mémoires tampons ne sont pas allouées tant que la méthode [**CBaseAllocator :: Commit**](cbaseallocator-commit.md) n’est pas appelée.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-106">The buffers are not allocated until the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method is called.</span></span> <span data-ttu-id="f1c2d-107">Le nombre actuel de mémoires tampons allouées est spécifié par la variable de membre [**CBaseAllocator :: m \_ lAllocated**](cbaseallocator-m-lallocated.md) .</span><span class="sxs-lookup"><span data-stu-id="f1c2d-107">The current number of allocated buffers is specified by the [**CBaseAllocator::m\_lAllocated**](cbaseallocator-m-lallocated.md) member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1c2d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1c2d-108">Syntax</span></span>


```C++
long m_lCount;
```



## <a name="requirements"></a><span data-ttu-id="f1c2d-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1c2d-109">Requirements</span></span>



| <span data-ttu-id="f1c2d-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1c2d-110">Requirement</span></span> | <span data-ttu-id="f1c2d-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1c2d-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1c2d-112">En-tête</span><span class="sxs-lookup"><span data-stu-id="f1c2d-112">Header</span></span><br/>  | <dl> <span data-ttu-id="f1c2d-113"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1c2d-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f1c2d-114">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f1c2d-114">Library</span></span><br/> | <dl> <span data-ttu-id="f1c2d-115"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f1c2d-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1c2d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1c2d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1c2d-117">**CBaseAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="f1c2d-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




