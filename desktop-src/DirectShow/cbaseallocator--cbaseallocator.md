---
description: CBaseAllocator. ~ CBaseAllocator, destructeur, méthode de destructeur.
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
ms.openlocfilehash: 9a4b754c8937b87a547f4583b3270f5782a6a415
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096417"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a><span data-ttu-id="7280b-103">CBaseAllocator. ~ CBaseAllocator, destructeur</span><span class="sxs-lookup"><span data-stu-id="7280b-103">CBaseAllocator.~CBaseAllocator destructor</span></span>

<span data-ttu-id="7280b-104">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="7280b-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7280b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7280b-105">Syntax</span></span>


```C++
~CBaseAllocator();
```



## <a name="remarks"></a><span data-ttu-id="7280b-106">Notes </span><span class="sxs-lookup"><span data-stu-id="7280b-106">Remarks</span></span>

<span data-ttu-id="7280b-107">Appelez toujours la méthode [**CBaseAllocator ::D ecommit**](cbaseallocator-decommit.md) avant de détruire l’objet.</span><span class="sxs-lookup"><span data-stu-id="7280b-107">Always call the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method before destroying the object.</span></span> <span data-ttu-id="7280b-108">Le destructeur de classe de base ne peut pas appeler **decommit**, car cette méthode appelle la méthode virtuelle pure [**CBaseAllocator :: Free**](cbaseallocator-free.md).</span><span class="sxs-lookup"><span data-stu-id="7280b-108">The base-class destructor cannot call **Decommit**, because that method calls the pure virtual method [**CBaseAllocator::Free**](cbaseallocator-free.md).</span></span> <span data-ttu-id="7280b-109">Les classes dérivées doivent substituer ce destructeur et appeler **decommit**.</span><span class="sxs-lookup"><span data-stu-id="7280b-109">Derived classes should override this destructor and call **Decommit**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7280b-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7280b-110">Requirements</span></span>



| <span data-ttu-id="7280b-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7280b-111">Requirement</span></span> | <span data-ttu-id="7280b-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="7280b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7280b-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="7280b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="7280b-114"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7280b-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7280b-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7280b-115">Library</span></span><br/> | <dl> <span data-ttu-id="7280b-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7280b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7280b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7280b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7280b-118">**CBaseAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="7280b-118">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




