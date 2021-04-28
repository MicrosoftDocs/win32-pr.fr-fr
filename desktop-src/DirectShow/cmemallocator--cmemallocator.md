---
description: CMemAllocator. ~ CMemAllocator, destructeur, méthode de destructeur.
ms.assetid: e0a04d93-fb77-4dc1-9bc8-7d3965bc6803
title: CMemAllocator. ~ CMemAllocator, destructeur (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.~CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43b0505ee34df72ab82e4204b08440ac1a2558b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095407"
---
# <a name="cmemallocatorcmemallocator-destructor"></a><span data-ttu-id="34b90-103">CMemAllocator. ~ CMemAllocator, destructeur</span><span class="sxs-lookup"><span data-stu-id="34b90-103">CMemAllocator.~CMemAllocator destructor</span></span>

<span data-ttu-id="34b90-104">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="34b90-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="34b90-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34b90-105">Syntax</span></span>


```C++
~CMemAllocator();
```



## <a name="remarks"></a><span data-ttu-id="34b90-106">Notes </span><span class="sxs-lookup"><span data-stu-id="34b90-106">Remarks</span></span>

<span data-ttu-id="34b90-107">Cette méthode remplace le destructeur de classe de base pour appeler [**CBaseAllocator ::D ecommit**](cbaseallocator-decommit.md) et [**CMemAllocator :: ReallyFree**](cmemallocator-reallyfree.md).</span><span class="sxs-lookup"><span data-stu-id="34b90-107">This method overrides the base-class destructor to call [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) and [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="34b90-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34b90-108">Requirements</span></span>



| <span data-ttu-id="34b90-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34b90-109">Requirement</span></span> | <span data-ttu-id="34b90-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="34b90-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34b90-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="34b90-111">Header</span></span><br/>  | <dl> <span data-ttu-id="34b90-112"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34b90-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="34b90-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="34b90-113">Library</span></span><br/> | <dl> <span data-ttu-id="34b90-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="34b90-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34b90-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34b90-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34b90-116">**CMemAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="34b90-116">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




