---
description: La méthode Free libère toute la mémoire tampon. Cette méthode est appelée lorsque le filtre propriétaire annule la validation de l’allocateur, après la libération du dernier échantillon multimédia.
ms.assetid: dd1e6c4d-762a-4caf-902b-015c6c9fdb4d
title: CBaseAllocator. free, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3534eac01a6769e090c8c808f16cc6ad5c6b84c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526093"
---
# <a name="cbaseallocatorfree-method"></a><span data-ttu-id="75ae5-104">CBaseAllocator. free, méthode</span><span class="sxs-lookup"><span data-stu-id="75ae5-104">CBaseAllocator.Free method</span></span>

<span data-ttu-id="75ae5-105">La `Free` méthode libère toute la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="75ae5-105">The `Free` method releases all of the buffer memory.</span></span> <span data-ttu-id="75ae5-106">Cette méthode est appelée lorsque le filtre propriétaire annule la validation de l’allocateur, après la libération du dernier échantillon multimédia.</span><span class="sxs-lookup"><span data-stu-id="75ae5-106">This method is called when the owning filter decommits the allocator, after the last media sample is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="75ae5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75ae5-107">Syntax</span></span>


```C++
virtual void Free() = 0;
```



## <a name="parameters"></a><span data-ttu-id="75ae5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75ae5-108">Parameters</span></span>

<span data-ttu-id="75ae5-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="75ae5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="75ae5-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="75ae5-110">Return value</span></span>

<span data-ttu-id="75ae5-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="75ae5-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="75ae5-112">Notes</span><span class="sxs-lookup"><span data-stu-id="75ae5-112">Remarks</span></span>

<span data-ttu-id="75ae5-113">Après l’appel de la méthode de [**dévalidation**](cbaseallocator-decommit.md) , l’allocateur appelle cette méthode lorsqu’il libère le dernier exemple multimédia.</span><span class="sxs-lookup"><span data-stu-id="75ae5-113">After the [**Decommit**](cbaseallocator-decommit.md) method is called, the allocator calls this method when it releases the last media sample.</span></span> <span data-ttu-id="75ae5-114">La classe dérivée doit implémenter cette méthode.</span><span class="sxs-lookup"><span data-stu-id="75ae5-114">The derived class must implement this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="75ae5-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75ae5-115">Requirements</span></span>



| <span data-ttu-id="75ae5-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75ae5-116">Requirement</span></span> | <span data-ttu-id="75ae5-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="75ae5-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75ae5-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="75ae5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="75ae5-119"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75ae5-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="75ae5-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="75ae5-120">Library</span></span><br/> | <dl> <span data-ttu-id="75ae5-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="75ae5-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75ae5-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75ae5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75ae5-123">**CBaseAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="75ae5-123">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




