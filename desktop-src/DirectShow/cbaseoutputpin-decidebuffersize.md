---
description: La méthode DecideBufferSize définit les exigences de la mémoire tampon.
ms.assetid: 1f7a3424-18ba-4a10-b09f-947ee8585ffa
title: Méthode CBaseOutputPin. DecideBufferSize (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dcb3328b56a7e203575a3abbaab64cda6a9b87f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526423"
---
# <a name="cbaseoutputpindecidebuffersize-method"></a><span data-ttu-id="09795-103">Méthode CBaseOutputPin. DecideBufferSize</span><span class="sxs-lookup"><span data-stu-id="09795-103">CBaseOutputPin.DecideBufferSize method</span></span>

<span data-ttu-id="09795-104">La `DecideBufferSize` méthode définit les spécifications de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="09795-104">The `DecideBufferSize` method sets the buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="09795-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09795-105">Syntax</span></span>


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="09795-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09795-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09795-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="09795-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="09795-108">Pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="09795-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="09795-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="09795-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="09795-110">Pointeur vers une structure de [**\_ Propriétés Allocator**](/windows/win32/api/strmif/ns-strmif-allocator_properties) qui contient les exigences de mémoire tampon du code confidentiel d’entrée.</span><span class="sxs-lookup"><span data-stu-id="09795-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span> <span data-ttu-id="09795-111">Si la broche d’entrée n’a pas de spécifications, l’appelant doit zéro les membres de cette structure avant d’appeler la méthode.</span><span class="sxs-lookup"><span data-stu-id="09795-111">If the input pin does not have any requirements, the caller should zero out the members of this structure before calling the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09795-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="09795-112">Return value</span></span>

<span data-ttu-id="09795-113">Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="09795-113">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="09795-114">Notes</span><span class="sxs-lookup"><span data-stu-id="09795-114">Remarks</span></span>

<span data-ttu-id="09795-115">Substituez cette méthode dans votre classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="09795-115">Override this method in your derived class.</span></span> <span data-ttu-id="09795-116">Appelez la méthode [**IMemAllocator :: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) pour spécifier vos exigences en matière de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="09795-116">Call the [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) method to specify your buffer requirements.</span></span> <span data-ttu-id="09795-117">En règle générale, la classe dérivée honore les exigences de mémoire tampon du pin d’entrée, mais elle n’est pas requise pour.</span><span class="sxs-lookup"><span data-stu-id="09795-117">Typically, the derived class will honor the input pin's buffer requirements, but it is not required to.</span></span>

## <a name="requirements"></a><span data-ttu-id="09795-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09795-118">Requirements</span></span>



| <span data-ttu-id="09795-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09795-119">Requirement</span></span> | <span data-ttu-id="09795-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="09795-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09795-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="09795-121">Header</span></span><br/>  | <dl> <span data-ttu-id="09795-122"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09795-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="09795-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="09795-123">Library</span></span><br/> | <dl> <span data-ttu-id="09795-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="09795-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09795-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09795-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09795-126">**CBaseOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="09795-126">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




