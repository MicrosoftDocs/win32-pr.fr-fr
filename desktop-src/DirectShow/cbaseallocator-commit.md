---
description: 'La méthode Commit alloue la mémoire pour les mémoires tampons. Cette méthode implémente la méthode IMemAllocator :: Commit.'
ms.assetid: e8c36276-0229-428f-b030-978651ab7534
title: CBaseAllocator. Commit, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Commit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b49fae72e5588105b1235c1f0c461d5cc45cfa2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538108"
---
# <a name="cbaseallocatorcommit-method"></a><span data-ttu-id="433a1-104">CBaseAllocator. Commit, méthode</span><span class="sxs-lookup"><span data-stu-id="433a1-104">CBaseAllocator.Commit method</span></span>

<span data-ttu-id="433a1-105">La `Commit` méthode alloue la mémoire pour les mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="433a1-105">The `Commit` method allocates the memory for the buffers.</span></span> <span data-ttu-id="433a1-106">Cette méthode implémente la méthode [**IMemAllocator :: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) .</span><span class="sxs-lookup"><span data-stu-id="433a1-106">This method implements the [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="433a1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="433a1-107">Syntax</span></span>


```C++
HRESULT Commit();
```



## <a name="parameters"></a><span data-ttu-id="433a1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="433a1-108">Parameters</span></span>

<span data-ttu-id="433a1-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="433a1-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="433a1-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="433a1-110">Return value</span></span>

<span data-ttu-id="433a1-111">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="433a1-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="433a1-112">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="433a1-112">Possible values include those in the following list.</span></span>



| <span data-ttu-id="433a1-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="433a1-113">Return code</span></span>                                                                                       | <span data-ttu-id="433a1-114">Description</span><span class="sxs-lookup"><span data-stu-id="433a1-114">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="433a1-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="433a1-115"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="433a1-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="433a1-116">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="433a1-117"><dt>**VFW \_ E \_ SIZENOTSET**</dt></span><span class="sxs-lookup"><span data-stu-id="433a1-117"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="433a1-118">Les exigences de mémoire tampon n’ont pas été spécifiées.</span><span class="sxs-lookup"><span data-stu-id="433a1-118">Buffer requirements were not specified.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="433a1-119">Notes</span><span class="sxs-lookup"><span data-stu-id="433a1-119">Remarks</span></span>

<span data-ttu-id="433a1-120">Avant d’appeler cette méthode, appelez la méthode [**CBaseAllocator :: SetProperties**](cbaseallocator-setproperties.md) pour spécifier les exigences en matière de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="433a1-120">Before calling this method, call the [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method to specify the buffer requirements.</span></span>

<span data-ttu-id="433a1-121">Cette méthode appelle la méthode virtuelle [**CBaseAllocator :: Alloc**](cbaseallocator-alloc.md) pour allouer la mémoire pour les mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="433a1-121">This method calls the virtual method [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) to allocate the memory for the buffers.</span></span> <span data-ttu-id="433a1-122">Les classes dérivées peuvent substituer **Alloc**.</span><span class="sxs-lookup"><span data-stu-id="433a1-122">Derived classes can override **Alloc**.</span></span> <span data-ttu-id="433a1-123">Si une opération de dévalidation est en attente, elle est annulée.</span><span class="sxs-lookup"><span data-stu-id="433a1-123">If a decommit operation is pending, it is canceled.</span></span>

<span data-ttu-id="433a1-124">Vous devez appeler cette méthode avant d’appeler la méthode [**CBaseAllocator :: GetBuffer**](cbaseallocator-getbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="433a1-124">You must call this method before calling the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="433a1-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="433a1-125">Requirements</span></span>



| <span data-ttu-id="433a1-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="433a1-126">Requirement</span></span> | <span data-ttu-id="433a1-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="433a1-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="433a1-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="433a1-128">Header</span></span><br/>  | <dl> <span data-ttu-id="433a1-129"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="433a1-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="433a1-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="433a1-130">Library</span></span><br/> | <dl> <span data-ttu-id="433a1-131"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="433a1-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="433a1-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="433a1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="433a1-133">**CBaseAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="433a1-133">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




