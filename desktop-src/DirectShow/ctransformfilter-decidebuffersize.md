---
description: La méthode DecideBufferSize définit les exigences de mémoire tampon de la broche de sortie.
ms.assetid: 33e41668-b4f6-4142-b22e-2ddfb96332df
title: Méthode CTransformFilter. DecideBufferSize (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71a506a9c9cd16a014418b24ad3fbd1186d6f48f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526528"
---
# <a name="ctransformfilterdecidebuffersize-method"></a><span data-ttu-id="c62de-103">Méthode CTransformFilter. DecideBufferSize</span><span class="sxs-lookup"><span data-stu-id="c62de-103">CTransformFilter.DecideBufferSize method</span></span>

<span data-ttu-id="c62de-104">La `DecideBufferSize` méthode définit les exigences de mémoire tampon de la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="c62de-104">The `DecideBufferSize` method sets the output pin's buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="c62de-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c62de-105">Syntax</span></span>


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="c62de-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c62de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c62de-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="c62de-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="c62de-108">Pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) sur l’allocateur de la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="c62de-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface on the output pin's allocator.</span></span>

</dd> <dt>

<span data-ttu-id="c62de-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="c62de-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="c62de-110">Pointeur vers une structure de [**\_ Propriétés Allocator**](/windows/win32/api/strmif/ns-strmif-allocator_properties) qui contient des exigences de mémoire tampon à partir de la broche d’entrée en aval.</span><span class="sxs-lookup"><span data-stu-id="c62de-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains buffer requirements from the downstream input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c62de-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c62de-111">Return value</span></span>

<span data-ttu-id="c62de-112">Retourne S \_ OK ou une autre valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c62de-112">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c62de-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c62de-113">Remarks</span></span>

<span data-ttu-id="c62de-114">La méthode [**CTransformOutputPin ::D ecidebuffersize**](ctransformoutputpin-decidebuffersize.md) de la broche de sortie appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="c62de-114">The output pin's [**CTransformOutputPin::DecideBufferSize**](ctransformoutputpin-decidebuffersize.md) method calls this method.</span></span> <span data-ttu-id="c62de-115">La classe dérivée doit implémenter cette méthode.</span><span class="sxs-lookup"><span data-stu-id="c62de-115">The derived class must implement this method.</span></span> <span data-ttu-id="c62de-116">Pour plus d’informations, consultez [**CBaseOutputPin ::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md).</span><span class="sxs-lookup"><span data-stu-id="c62de-116">For more information, see [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c62de-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c62de-117">Requirements</span></span>



| <span data-ttu-id="c62de-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c62de-118">Requirement</span></span> | <span data-ttu-id="c62de-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c62de-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c62de-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="c62de-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c62de-121"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c62de-121"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c62de-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c62de-122">Library</span></span><br/> | <dl> <span data-ttu-id="c62de-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c62de-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c62de-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c62de-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c62de-125">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="c62de-125">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




