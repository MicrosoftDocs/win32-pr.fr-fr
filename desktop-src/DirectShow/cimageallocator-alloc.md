---
description: 'La méthode Alloc alloue de la mémoire pour les mémoires tampons. Cette méthode remplace la méthode CBaseAllocator :: Alloc.'
ms.assetid: 4a246b4e-93b3-4adb-9f10-6b92d9f479eb
title: CImageAllocator. Alloc, méthode (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7acd13e2d2d09e6e491a2f338aef2fe7564b82b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545551"
---
# <a name="cimageallocatoralloc-method"></a><span data-ttu-id="b9421-104">CImageAllocator. Alloc, méthode</span><span class="sxs-lookup"><span data-stu-id="b9421-104">CImageAllocator.Alloc method</span></span>

<span data-ttu-id="b9421-105">La `Alloc` méthode alloue de la mémoire pour les mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="b9421-105">The `Alloc` method allocates memory for the buffers.</span></span> <span data-ttu-id="b9421-106">Cette méthode remplace la méthode [**CBaseAllocator :: Alloc**](cbaseallocator-alloc.md) .</span><span class="sxs-lookup"><span data-stu-id="b9421-106">This method overrides the [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9421-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9421-107">Syntax</span></span>


```C++
HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="b9421-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9421-108">Parameters</span></span>

<span data-ttu-id="b9421-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b9421-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b9421-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b9421-110">Return value</span></span>

<span data-ttu-id="b9421-111">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b9421-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b9421-112">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="b9421-112">Possible values include the following.</span></span>



| <span data-ttu-id="b9421-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b9421-113">Return code</span></span>                                                                                   | <span data-ttu-id="b9421-114">Description</span><span class="sxs-lookup"><span data-stu-id="b9421-114">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="b9421-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b9421-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b9421-116">Succès</span><span class="sxs-lookup"><span data-stu-id="b9421-116">Success</span></span><br/>             |
| <dl> <span data-ttu-id="b9421-117"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="b9421-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b9421-118">Mémoire insuffisante</span><span class="sxs-lookup"><span data-stu-id="b9421-118">Insufficient memory</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b9421-119">Notes</span><span class="sxs-lookup"><span data-stu-id="b9421-119">Remarks</span></span>

<span data-ttu-id="b9421-120">Cette méthode est appelée par la méthode [**CBaseAllocator :: Commit**](cbaseallocator-commit.md) , lorsque le filtre valide l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="b9421-120">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method, when the filter commits the allocator.</span></span>

<span data-ttu-id="b9421-121">Cette méthode crée une liste d’exemples de médias, qui sont implémentés en tant qu’objets [**CImageSample**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="b9421-121">This method creates a list of media samples, which are implemented as [**CImageSample**](cimagesample.md) objects.</span></span> <span data-ttu-id="b9421-122">Chaque exemple contient une image bitmap indépendante du périphérique GDI, à l’aide de la fonction GDI **CreateDIBSection** .</span><span class="sxs-lookup"><span data-stu-id="b9421-122">Each sample contains a GDI device-independent bitmap, using the GDI **CreateDIBSection** function.</span></span>

<span data-ttu-id="b9421-123">En interne, cette méthode appelle [**CImageAllocator :: CreateDIB**](cimageallocator-createdib.md) pour créer chaque DIB, et [**CImageAllocator :: CreateImageSample**](cimageallocator-createimagesample.md) pour créer chaque exemple.</span><span class="sxs-lookup"><span data-stu-id="b9421-123">Internally this method calls [**CImageAllocator::CreateDIB**](cimageallocator-createdib.md) to create each DIB, and [**CImageAllocator::CreateImageSample**](cimageallocator-createimagesample.md) to create each sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9421-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9421-124">Requirements</span></span>



| <span data-ttu-id="b9421-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9421-125">Requirement</span></span> | <span data-ttu-id="b9421-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9421-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9421-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="b9421-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b9421-128"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b9421-128"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b9421-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b9421-129">Library</span></span><br/> | <dl> <span data-ttu-id="b9421-130"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b9421-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9421-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9421-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9421-132">**CImageAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="b9421-132">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




