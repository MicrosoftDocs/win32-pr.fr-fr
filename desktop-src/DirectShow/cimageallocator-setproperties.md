---
description: 'La méthode SetProperties spécifie le nombre de mémoires tampons à allouer et la taille de chaque mémoire tampon. Cette méthode remplace la méthode CBaseAllocator :: SetProperties.'
ms.assetid: 8d419432-a9a7-44fb-b916-8dacd08eb6ec
title: CImageAllocator. SetProperties, méthode (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c04501fe3511d9cdd45f3513c68082d2ffece0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537999"
---
# <a name="cimageallocatorsetproperties-method"></a><span data-ttu-id="ea994-104">CImageAllocator. SetProperties, méthode</span><span class="sxs-lookup"><span data-stu-id="ea994-104">CImageAllocator.SetProperties method</span></span>

<span data-ttu-id="ea994-105">La `SetProperties` méthode spécifie le nombre de mémoires tampons à allouer et la taille de chaque mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="ea994-105">The `SetProperties` method specifies the number of buffers to allocate and the size of each buffer.</span></span> <span data-ttu-id="ea994-106">Cette méthode remplace la méthode [**CBaseAllocator :: SetProperties**](cbaseallocator-setproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="ea994-106">This method overrides the [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea994-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea994-107">Syntax</span></span>


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a><span data-ttu-id="ea994-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea994-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea994-109">*pRequest*</span><span class="sxs-lookup"><span data-stu-id="ea994-109">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="ea994-110">Pointeur vers une structure de [**\_ Propriétés Allocator**](/windows/win32/api/strmif/ns-strmif-allocator_properties) qui contient les exigences de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="ea994-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the buffer requirements.</span></span>

</dd> <dt>

<span data-ttu-id="ea994-111">*pActual*</span><span class="sxs-lookup"><span data-stu-id="ea994-111">*pActual*</span></span> 
</dt> <dd>

<span data-ttu-id="ea994-112">Pointeur vers une structure de **\_ Propriétés Allocator** qui reçoit les propriétés de mémoire tampon réelles.</span><span class="sxs-lookup"><span data-stu-id="ea994-112">Pointer to an **ALLOCATOR\_PROPERTIES** structure that receives the actual buffer properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea994-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea994-113">Return value</span></span>

<span data-ttu-id="ea994-114">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ea994-114">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea994-115">Notes</span><span class="sxs-lookup"><span data-stu-id="ea994-115">Remarks</span></span>

<span data-ttu-id="ea994-116">Cette méthode appelle [**CImageAllocator :: CheckSizes**](cimageallocator-checksizes.md) pour valider la taille de mémoire tampon demandée.</span><span class="sxs-lookup"><span data-stu-id="ea994-116">This method calls [**CImageAllocator::CheckSizes**](cimageallocator-checksizes.md) to validate the requested buffer size.</span></span> <span data-ttu-id="ea994-117">Il appelle également la version de classe de base de `SetProperties` .</span><span class="sxs-lookup"><span data-stu-id="ea994-117">It also calls the base-class version of `SetProperties`.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea994-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea994-118">Requirements</span></span>



| <span data-ttu-id="ea994-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea994-119">Requirement</span></span> | <span data-ttu-id="ea994-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea994-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea994-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea994-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ea994-122"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea994-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ea994-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ea994-123">Library</span></span><br/> | <dl> <span data-ttu-id="ea994-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ea994-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea994-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea994-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea994-126">**CImageAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="ea994-126">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




