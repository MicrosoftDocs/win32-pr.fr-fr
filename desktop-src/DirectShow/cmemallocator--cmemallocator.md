---
description: Méthode de destructeur.
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
ms.openlocfilehash: d49046eccd8d7ef71c4eeb4c75acffbf90f7d826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534978"
---
# <a name="cmemallocatorcmemallocator-destructor"></a><span data-ttu-id="f0ed9-103">CMemAllocator. ~ CMemAllocator, destructeur</span><span class="sxs-lookup"><span data-stu-id="f0ed9-103">CMemAllocator.~CMemAllocator destructor</span></span>

<span data-ttu-id="f0ed9-104">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="f0ed9-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0ed9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0ed9-105">Syntax</span></span>


```C++
~CMemAllocator();
```



## <a name="remarks"></a><span data-ttu-id="f0ed9-106">Notes</span><span class="sxs-lookup"><span data-stu-id="f0ed9-106">Remarks</span></span>

<span data-ttu-id="f0ed9-107">Cette méthode remplace le destructeur de classe de base pour appeler [**CBaseAllocator ::D ecommit**](cbaseallocator-decommit.md) et [**CMemAllocator :: ReallyFree**](cmemallocator-reallyfree.md).</span><span class="sxs-lookup"><span data-stu-id="f0ed9-107">This method overrides the base-class destructor to call [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) and [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0ed9-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0ed9-108">Requirements</span></span>



| <span data-ttu-id="f0ed9-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0ed9-109">Requirement</span></span> | <span data-ttu-id="f0ed9-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0ed9-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0ed9-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0ed9-111">Header</span></span><br/>  | <dl> <span data-ttu-id="f0ed9-112"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0ed9-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f0ed9-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f0ed9-113">Library</span></span><br/> | <dl> <span data-ttu-id="f0ed9-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f0ed9-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0ed9-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0ed9-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0ed9-116">**CMemAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="f0ed9-116">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




