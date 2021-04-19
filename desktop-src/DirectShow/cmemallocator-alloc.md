---
description: La méthode Alloc alloue de la mémoire pour les mémoires tampons.
ms.assetid: 81886163-2f7d-4d4f-be90-4491f76b8514
title: CMemAllocator. Alloc, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a142f6c0cea6cdb9b18507becabb909ce67b0fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528720"
---
# <a name="cmemallocatoralloc-method"></a><span data-ttu-id="19fa9-103">CMemAllocator. Alloc, méthode</span><span class="sxs-lookup"><span data-stu-id="19fa9-103">CMemAllocator.Alloc method</span></span>

<span data-ttu-id="19fa9-104">La `Alloc` méthode alloue de la mémoire pour les mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="19fa9-104">The `Alloc` method allocates memory for the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="19fa9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19fa9-105">Syntax</span></span>


```C++
HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="19fa9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19fa9-106">Parameters</span></span>

<span data-ttu-id="19fa9-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="19fa9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="19fa9-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="19fa9-108">Return value</span></span>

<span data-ttu-id="19fa9-109">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="19fa9-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="19fa9-110">Code de retour</span><span class="sxs-lookup"><span data-stu-id="19fa9-110">Return code</span></span>                                                                                       | <span data-ttu-id="19fa9-111">Description</span><span class="sxs-lookup"><span data-stu-id="19fa9-111">Description</span></span>                                  |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="19fa9-112"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="19fa9-112"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="19fa9-113">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="19fa9-113">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="19fa9-114"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="19fa9-114"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>     | <span data-ttu-id="19fa9-115">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="19fa9-115">Insufficient memory.</span></span><br/>              |
| <dl> <span data-ttu-id="19fa9-116"><dt>**VFW \_ E \_ SIZENOTSET**</dt></span><span class="sxs-lookup"><span data-stu-id="19fa9-116"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="19fa9-117">Les exigences de mémoire tampon n’ont pas été définies.</span><span class="sxs-lookup"><span data-stu-id="19fa9-117">Buffer requirements were not set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="19fa9-118">Notes</span><span class="sxs-lookup"><span data-stu-id="19fa9-118">Remarks</span></span>

<span data-ttu-id="19fa9-119">Cette méthode est appelée par la méthode [**CBaseAllocator :: Commit**](cbaseallocator-commit.md) .</span><span class="sxs-lookup"><span data-stu-id="19fa9-119">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method.</span></span> <span data-ttu-id="19fa9-120">Elle alloue un bloc de mémoire contigu suffisant pour les exigences de mémoire tampon fournies dans la méthode [**CMemAllocator :: SetProperties**](cmemallocator-setproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="19fa9-120">It allocates a contiguous block of memory sufficient for the buffer requirements given in the [**CMemAllocator::SetProperties**](cmemallocator-setproperties.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="19fa9-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19fa9-121">Requirements</span></span>



| <span data-ttu-id="19fa9-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19fa9-122">Requirement</span></span> | <span data-ttu-id="19fa9-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="19fa9-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19fa9-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="19fa9-124">Header</span></span><br/>  | <dl> <span data-ttu-id="19fa9-125"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="19fa9-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="19fa9-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="19fa9-126">Library</span></span><br/> | <dl> <span data-ttu-id="19fa9-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="19fa9-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19fa9-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19fa9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19fa9-129">**CMemAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="19fa9-129">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




