---
description: 'Méthode CTransformOutputPin. DecideBufferSize : la méthode DecideBufferSize définit les exigences de la mémoire tampon.'
ms.assetid: cdf9e384-623e-46a6-b123-d881fe21fb09
title: Méthode CTransformOutputPin. DecideBufferSize (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bc84eaf5e95a19436de5429ce018352cdaa286e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084837"
---
# <a name="ctransformoutputpindecidebuffersize-method"></a><span data-ttu-id="d0ec5-103">Méthode CTransformOutputPin. DecideBufferSize</span><span class="sxs-lookup"><span data-stu-id="d0ec5-103">CTransformOutputPin.DecideBufferSize method</span></span>

<span data-ttu-id="d0ec5-104">La `DecideBufferSize` méthode définit les spécifications de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-104">The `DecideBufferSize` method sets the buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0ec5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0ec5-105">Syntax</span></span>


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
);
```



## <a name="parameters"></a><span data-ttu-id="d0ec5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0ec5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0ec5-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="d0ec5-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="d0ec5-108">Pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="d0ec5-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="d0ec5-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="d0ec5-110">Pointeur d’une structure de [**\_ Propriétés Allocator**](/windows/win32/api/strmif/ns-strmif-allocator_properties) qui contient les exigences de mémoire tampon du code confidentiel d’entrée.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-110">Pointer an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0ec5-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d0ec5-111">Return value</span></span>

<span data-ttu-id="d0ec5-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d0ec5-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0ec5-113">Notes </span><span class="sxs-lookup"><span data-stu-id="d0ec5-113">Remarks</span></span>

<span data-ttu-id="d0ec5-114">Cette méthode remplace la méthode [**CBaseOutputPin ::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) .</span><span class="sxs-lookup"><span data-stu-id="d0ec5-114">This method overrides the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) method.</span></span> <span data-ttu-id="d0ec5-115">Elle appelle la méthode virtuelle pure [**CTransformFilter ::D ecidebuffersize**](ctransformfilter-decidebuffersize.md) du filtre, que la classe dérivée du filtre doit implémenter.</span><span class="sxs-lookup"><span data-stu-id="d0ec5-115">It calls the filter's pure virtual [**CTransformFilter::DecideBufferSize**](ctransformfilter-decidebuffersize.md) method, which the filter's derived class must implement.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0ec5-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0ec5-116">Requirements</span></span>



| <span data-ttu-id="d0ec5-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0ec5-117">Requirement</span></span> | <span data-ttu-id="d0ec5-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0ec5-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0ec5-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="d0ec5-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d0ec5-120"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0ec5-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d0ec5-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d0ec5-121">Library</span></span><br/> | <dl> <span data-ttu-id="d0ec5-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d0ec5-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




