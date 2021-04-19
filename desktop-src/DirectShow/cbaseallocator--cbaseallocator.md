---
description: Méthode de destructeur.
ms.assetid: b1e5653f-d72f-4cde-a8c9-d25763434374
title: CBaseAllocator. ~ CBaseAllocator, destructeur (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.~CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 53587482c5d9cf8f5a772453f220c7633c17d383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541260"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a><span data-ttu-id="a4f4b-103">CBaseAllocator. ~ CBaseAllocator, destructeur</span><span class="sxs-lookup"><span data-stu-id="a4f4b-103">CBaseAllocator.~CBaseAllocator destructor</span></span>

<span data-ttu-id="a4f4b-104">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="a4f4b-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4f4b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4f4b-105">Syntax</span></span>


```C++
~CBaseAllocator();
```



## <a name="remarks"></a><span data-ttu-id="a4f4b-106">Notes</span><span class="sxs-lookup"><span data-stu-id="a4f4b-106">Remarks</span></span>

<span data-ttu-id="a4f4b-107">Appelez toujours la méthode [**CBaseAllocator ::D ecommit**](cbaseallocator-decommit.md) avant de détruire l’objet.</span><span class="sxs-lookup"><span data-stu-id="a4f4b-107">Always call the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method before destroying the object.</span></span> <span data-ttu-id="a4f4b-108">Le destructeur de classe de base ne peut pas appeler **decommit**, car cette méthode appelle la méthode virtuelle pure [**CBaseAllocator :: Free**](cbaseallocator-free.md).</span><span class="sxs-lookup"><span data-stu-id="a4f4b-108">The base-class destructor cannot call **Decommit**, because that method calls the pure virtual method [**CBaseAllocator::Free**](cbaseallocator-free.md).</span></span> <span data-ttu-id="a4f4b-109">Les classes dérivées doivent substituer ce destructeur et appeler **decommit**.</span><span class="sxs-lookup"><span data-stu-id="a4f4b-109">Derived classes should override this destructor and call **Decommit**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4f4b-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4f4b-110">Requirements</span></span>



| <span data-ttu-id="a4f4b-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4f4b-111">Requirement</span></span> | <span data-ttu-id="a4f4b-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4f4b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4f4b-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="a4f4b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="a4f4b-114"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4f4b-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a4f4b-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a4f4b-115">Library</span></span><br/> | <dl> <span data-ttu-id="a4f4b-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a4f4b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4f4b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4f4b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4f4b-118">**CBaseAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="a4f4b-118">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




