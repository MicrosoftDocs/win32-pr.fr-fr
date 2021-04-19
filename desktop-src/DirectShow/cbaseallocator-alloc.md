---
description: La méthode Alloc alloue de la mémoire pour les mémoires tampons.
ms.assetid: a22c97ef-6a8d-4cad-b5a5-3e6b225f5c81
title: CBaseAllocator. Alloc, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b7510a108e69eb218a894b67dd5b62d94bfdbe6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542218"
---
# <a name="cbaseallocatoralloc-method"></a><span data-ttu-id="e4732-103">CBaseAllocator. Alloc, méthode</span><span class="sxs-lookup"><span data-stu-id="e4732-103">CBaseAllocator.Alloc method</span></span>

<span data-ttu-id="e4732-104">La `Alloc` méthode alloue de la mémoire pour les mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="e4732-104">The `Alloc` method allocates memory for the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4732-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4732-105">Syntax</span></span>


```C++
virtual HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="e4732-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4732-106">Parameters</span></span>

<span data-ttu-id="e4732-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e4732-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e4732-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e4732-108">Return value</span></span>

<span data-ttu-id="e4732-109">Retourne l’une des valeurs **HRESULT** suivantes.</span><span class="sxs-lookup"><span data-stu-id="e4732-109">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="e4732-110">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e4732-110">Return code</span></span>                                                                                       | <span data-ttu-id="e4732-111">Description</span><span class="sxs-lookup"><span data-stu-id="e4732-111">Description</span></span>                                      |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="e4732-112"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="e4732-112"><dt>**S\_FALSE**</dt></span></span> </dl>           | <span data-ttu-id="e4732-113">Les exigences de mémoire tampon n’ont pas changé.</span><span class="sxs-lookup"><span data-stu-id="e4732-113">Buffer requirements have not changed.</span></span><br/> |
| <dl> <span data-ttu-id="e4732-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e4732-114"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="e4732-115">Les exigences en matière de mémoire tampon ont changé.</span><span class="sxs-lookup"><span data-stu-id="e4732-115">Buffer requirements have changed.</span></span><br/>     |
| <dl> <span data-ttu-id="e4732-116"><dt>**VFW \_ E \_ SIZENOTSET**</dt></span><span class="sxs-lookup"><span data-stu-id="e4732-116"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="e4732-117">Les exigences de mémoire tampon n’ont pas été définies.</span><span class="sxs-lookup"><span data-stu-id="e4732-117">Buffer requirements were not set.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="e4732-118">Notes</span><span class="sxs-lookup"><span data-stu-id="e4732-118">Remarks</span></span>

<span data-ttu-id="e4732-119">Cette méthode est appelée par la méthode [**CBaseAllocator :: Commit**](cbaseallocator-commit.md) .</span><span class="sxs-lookup"><span data-stu-id="e4732-119">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method.</span></span>

<span data-ttu-id="e4732-120">Dans la classe de base, cette méthode n’alloue pas de mémoire.</span><span class="sxs-lookup"><span data-stu-id="e4732-120">In the base class, this method does not allocate any memory.</span></span> <span data-ttu-id="e4732-121">Elle retourne une erreur si les exigences de la mémoire tampon n’ont pas été définies, S \_ false si les spécifications n’ont pas été modifiées et s \_ OK si les spécifications ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="e4732-121">It returns an error if the buffer requirements were not set, S\_FALSE if the requirements have not changed, and S\_OK if the requirements have changed.</span></span>

<span data-ttu-id="e4732-122">Une classe dérivée doit substituer cette méthode pour effectuer l’allocation de mémoire réelle.</span><span class="sxs-lookup"><span data-stu-id="e4732-122">A derived class should override this method to perform the actual memory allocation.</span></span> <span data-ttu-id="e4732-123">En règle générale, la classe dérivée effectue les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e4732-123">Typically, the derived class will perform the following steps:</span></span>

1.  <span data-ttu-id="e4732-124">Appelez l’implémentation de la classe de base pour déterminer si la mémoire doit être réellement allouée.</span><span class="sxs-lookup"><span data-stu-id="e4732-124">Call the base class implementation, to determine whether the memory truly needs allocating.</span></span>
2.  <span data-ttu-id="e4732-125">Allouez de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="e4732-125">Allocate memory.</span></span>
3.  <span data-ttu-id="e4732-126">Créez les objets [**CMediaSample**](cmediasample.md) qui contiennent des blocs de mémoire de l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="e4732-126">Create [**CMediaSample**](cmediasample.md) objects that contain chunks of memory from step 2.</span></span>
4.  <span data-ttu-id="e4732-127">Ajoutez chaque objet **CMediaSample** à la liste des exemples gratuits ([**CBaseAllocator :: m \_ lFree**](cbaseallocator-m-lfree.md)).</span><span class="sxs-lookup"><span data-stu-id="e4732-127">Add each **CMediaSample** object to the list of free samples ([**CBaseAllocator::m\_lFree**](cbaseallocator-m-lfree.md)).</span></span>

<span data-ttu-id="e4732-128">Pour obtenir un exemple, consultez [**CMemAllocator :: Alloc**](cmemallocator-alloc.md).</span><span class="sxs-lookup"><span data-stu-id="e4732-128">For an example, see [**CMemAllocator::Alloc**](cmemallocator-alloc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4732-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4732-129">Requirements</span></span>



| <span data-ttu-id="e4732-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4732-130">Requirement</span></span> | <span data-ttu-id="e4732-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4732-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4732-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="e4732-132">Header</span></span><br/>  | <dl> <span data-ttu-id="e4732-133"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4732-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e4732-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e4732-134">Library</span></span><br/> | <dl> <span data-ttu-id="e4732-135"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e4732-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4732-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4732-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4732-137">**CBaseAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="e4732-137">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




