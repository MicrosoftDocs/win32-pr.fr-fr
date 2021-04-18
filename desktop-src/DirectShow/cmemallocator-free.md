---
description: La méthode Free est appelée pendant une opération de dévalidation.
ms.assetid: 71a84730-ca71-4418-bf76-52fd42fc7a5a
title: CMemAllocator. free, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b707bb5b2a35466c47d05690a0f57f278d784542
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540686"
---
# <a name="cmemallocatorfree-method"></a><span data-ttu-id="869b1-103">CMemAllocator. free, méthode</span><span class="sxs-lookup"><span data-stu-id="869b1-103">CMemAllocator.Free method</span></span>

<span data-ttu-id="869b1-104">La `Free` méthode est appelée pendant une opération de dévalidation.</span><span class="sxs-lookup"><span data-stu-id="869b1-104">The `Free` method is called during a decommit operation.</span></span> <span data-ttu-id="869b1-105">Cette méthode implémente la méthode [**CBaseAllocator :: Free**](cbaseallocator-free.md) virtuelle pure, mais ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="869b1-105">This method implements the pure virtual [**CBaseAllocator::Free**](cbaseallocator-free.md) method, but does nothing.</span></span> <span data-ttu-id="869b1-106">La mémoire tampon n’est pas libérée tant que l’objet **CMemAllocator** n’est pas détruit.</span><span class="sxs-lookup"><span data-stu-id="869b1-106">The buffer memory is not actually released until the **CMemAllocator** object is destroyed.</span></span> <span data-ttu-id="869b1-107">La méthode de destructeur appelle [**CMemAllocator :: ReallyFree**](cmemallocator-reallyfree.md) pour libérer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="869b1-107">The destructor method calls [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md) to release the memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="869b1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="869b1-108">Syntax</span></span>


```C++
void Free();
```



## <a name="parameters"></a><span data-ttu-id="869b1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="869b1-109">Parameters</span></span>

<span data-ttu-id="869b1-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="869b1-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="869b1-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="869b1-111">Return value</span></span>

<span data-ttu-id="869b1-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="869b1-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="869b1-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="869b1-113">Requirements</span></span>



| <span data-ttu-id="869b1-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="869b1-114">Requirement</span></span> | <span data-ttu-id="869b1-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="869b1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="869b1-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="869b1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="869b1-117"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="869b1-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="869b1-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="869b1-118">Library</span></span><br/> | <dl> <span data-ttu-id="869b1-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="869b1-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="869b1-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="869b1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="869b1-121">**CMemAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="869b1-121">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




