---
description: La méthode ReallyFree libère la mémoire pour les mémoires tampons.
ms.assetid: c5c5d09f-b4f2-4a06-9309-3b2a8b8f8f1f
title: Méthode CMemAllocator. ReallyFree (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.ReallyFree
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 187807658c8e15ddf530ca6687d860fe826f4208
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537987"
---
# <a name="cmemallocatorreallyfree-method"></a><span data-ttu-id="f9b43-103">Méthode CMemAllocator. ReallyFree</span><span class="sxs-lookup"><span data-stu-id="f9b43-103">CMemAllocator.ReallyFree method</span></span>

<span data-ttu-id="f9b43-104">La `ReallyFree` méthode libère la mémoire pour les mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="f9b43-104">The `ReallyFree` method releases the memory for the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9b43-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9b43-105">Syntax</span></span>


```C++
void ReallyFree();
```



## <a name="parameters"></a><span data-ttu-id="f9b43-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9b43-106">Parameters</span></span>

<span data-ttu-id="f9b43-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f9b43-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f9b43-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f9b43-108">Return value</span></span>

<span data-ttu-id="f9b43-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f9b43-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9b43-110">Notes</span><span class="sxs-lookup"><span data-stu-id="f9b43-110">Remarks</span></span>

<span data-ttu-id="f9b43-111">La classe [**CMemAllocator**](cmemallocator.md) conserve la mémoire jusqu’à ce que l’objet soit supprimé.</span><span class="sxs-lookup"><span data-stu-id="f9b43-111">The [**CMemAllocator**](cmemallocator.md) class holds memory until the object is deleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9b43-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9b43-112">Requirements</span></span>



| <span data-ttu-id="f9b43-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9b43-113">Requirement</span></span> | <span data-ttu-id="f9b43-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9b43-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9b43-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9b43-115">Header</span></span><br/>  | <dl> <span data-ttu-id="f9b43-116"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9b43-116"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f9b43-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f9b43-117">Library</span></span><br/> | <dl> <span data-ttu-id="f9b43-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f9b43-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9b43-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9b43-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9b43-120">**CMemAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="f9b43-120">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




