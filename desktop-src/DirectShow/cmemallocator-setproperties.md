---
description: La méthode SetProperties spécifie le nombre de mémoires tampons à allouer et la taille de chaque mémoire tampon.
ms.assetid: 01f63379-1d66-4a72-b87c-de55504b0bb4
title: CMemAllocator. SetProperties, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8505916245cca81fdd84132e4523fe9dd03b971b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526527"
---
# <a name="cmemallocatorsetproperties-method"></a><span data-ttu-id="cb4c2-103">CMemAllocator. SetProperties, méthode</span><span class="sxs-lookup"><span data-stu-id="cb4c2-103">CMemAllocator.SetProperties method</span></span>

<span data-ttu-id="cb4c2-104">La `SetProperties` méthode spécifie le nombre de mémoires tampons à allouer et la taille de chaque mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="cb4c2-104">The `SetProperties` method specifies the number of buffers to allocate and the size of each buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb4c2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb4c2-105">Syntax</span></span>


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a><span data-ttu-id="cb4c2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb4c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb4c2-107">*pRequest*</span><span class="sxs-lookup"><span data-stu-id="cb4c2-107">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="cb4c2-108">Pointeur vers une structure de [**\_ Propriétés Allocator**](/windows/win32/api/strmif/ns-strmif-allocator_properties) qui contient les exigences de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="cb4c2-108">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the buffer requirements.</span></span>

</dd> <dt>

<span data-ttu-id="cb4c2-109">*pActual*</span><span class="sxs-lookup"><span data-stu-id="cb4c2-109">*pActual*</span></span> 
</dt> <dd>

<span data-ttu-id="cb4c2-110">Pointeur vers une structure de **\_ Propriétés Allocator** qui reçoit les propriétés de mémoire tampon réelles.</span><span class="sxs-lookup"><span data-stu-id="cb4c2-110">Pointer to an **ALLOCATOR\_PROPERTIES** structure that receives the actual buffer properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb4c2-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cb4c2-111">Return value</span></span>

<span data-ttu-id="cb4c2-112">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="cb4c2-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="cb4c2-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="cb4c2-113">Return code</span></span>                                                                                                 | <span data-ttu-id="cb4c2-114">Description</span><span class="sxs-lookup"><span data-stu-id="cb4c2-114">Description</span></span>                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="cb4c2-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cb4c2-115"><dt>**S\_OK**</dt></span></span> </dl>                        | <span data-ttu-id="cb4c2-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="cb4c2-116">Success.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="cb4c2-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="cb4c2-117"><dt>**E\_POINTER**</dt></span></span> </dl>                   | <span data-ttu-id="cb4c2-118">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="cb4c2-118">**NULL** pointer argument.</span></span><br/>                                 |
| <dl> <span data-ttu-id="cb4c2-119"><dt>**VFW \_ E \_ déjà \_ validé**</dt></span><span class="sxs-lookup"><span data-stu-id="cb4c2-119"><dt>**VFW\_E\_ALREADY\_COMMITTED**</dt></span></span> </dl>   | <span data-ttu-id="cb4c2-120">Impossible de modifier la mémoire allouée lorsque le filtre est actif.</span><span class="sxs-lookup"><span data-stu-id="cb4c2-120">Cannot change allocated memory while the filter is active.</span></span><br/> |
| <dl> <span data-ttu-id="cb4c2-121"><dt>**VFW \_ E \_ BADALIGN**</dt></span><span class="sxs-lookup"><span data-stu-id="cb4c2-121"><dt>**VFW\_E\_BADALIGN**</dt></span></span> </dl>             | <span data-ttu-id="cb4c2-122">Un alignement non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="cb4c2-122">An invalid alignment was specified.</span></span><br/>                        |
| <dl> <span data-ttu-id="cb4c2-123"><dt>**\_ \_ mémoires tampons VFW E en \_ suspens**</dt></span><span class="sxs-lookup"><span data-stu-id="cb4c2-123"><dt>**VFW\_E\_BUFFERS\_OUTSTANDING**</dt></span></span> </dl> | <span data-ttu-id="cb4c2-124">Une ou plusieurs mémoires tampons sont toujours actives.</span><span class="sxs-lookup"><span data-stu-id="cb4c2-124">One or more buffers are still active.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="cb4c2-125">Notes</span><span class="sxs-lookup"><span data-stu-id="cb4c2-125">Remarks</span></span>

<span data-ttu-id="cb4c2-126">Cette méthode remplace la méthode [**CBaseAllocator :: SetProperties**](cbaseallocator-setproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="cb4c2-126">This method overrides the [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method.</span></span>

<span data-ttu-id="cb4c2-127">L’alignement de la mémoire tampon, spécifié par le membre **cbAlign** de la structure de **\_ Propriétés Allocator** , doit être une puissance égale à deux.</span><span class="sxs-lookup"><span data-stu-id="cb4c2-127">The buffer alignment, specified by the **cbAlign** member of the **ALLOCATOR\_PROPERTIES** structure, must be an even power of two.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb4c2-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb4c2-128">Requirements</span></span>



| <span data-ttu-id="cb4c2-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb4c2-129">Requirement</span></span> | <span data-ttu-id="cb4c2-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb4c2-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb4c2-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb4c2-131">Header</span></span><br/>  | <dl> <span data-ttu-id="cb4c2-132"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb4c2-132"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cb4c2-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cb4c2-133">Library</span></span><br/> | <dl> <span data-ttu-id="cb4c2-134"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cb4c2-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb4c2-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb4c2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb4c2-136">**CMemAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="cb4c2-136">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




