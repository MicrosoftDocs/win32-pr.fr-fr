---
description: 'Méthode CTransformFilter. DecideBufferSize : la méthode DecideBufferSize définit les exigences de mémoire tampon de la broche de sortie.'
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
ms.openlocfilehash: f3276170f1256bba41aa075b0e5f06fb7becbcd2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095147"
---
# <a name="ctransformfilterdecidebuffersize-method"></a><span data-ttu-id="b624f-103">Méthode CTransformFilter. DecideBufferSize</span><span class="sxs-lookup"><span data-stu-id="b624f-103">CTransformFilter.DecideBufferSize method</span></span>

<span data-ttu-id="b624f-104">La `DecideBufferSize` méthode définit les exigences de mémoire tampon de la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="b624f-104">The `DecideBufferSize` method sets the output pin's buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="b624f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b624f-105">Syntax</span></span>


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="b624f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b624f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b624f-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="b624f-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="b624f-108">Pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) sur l’allocateur de la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="b624f-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface on the output pin's allocator.</span></span>

</dd> <dt>

<span data-ttu-id="b624f-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="b624f-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="b624f-110">Pointeur vers une structure de [**\_ Propriétés Allocator**](/windows/win32/api/strmif/ns-strmif-allocator_properties) qui contient des exigences de mémoire tampon à partir de la broche d’entrée en aval.</span><span class="sxs-lookup"><span data-stu-id="b624f-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains buffer requirements from the downstream input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b624f-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b624f-111">Return value</span></span>

<span data-ttu-id="b624f-112">Retourne S \_ OK ou une autre valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b624f-112">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b624f-113">Notes </span><span class="sxs-lookup"><span data-stu-id="b624f-113">Remarks</span></span>

<span data-ttu-id="b624f-114">La méthode [**CTransformOutputPin ::D ecidebuffersize**](ctransformoutputpin-decidebuffersize.md) de la broche de sortie appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b624f-114">The output pin's [**CTransformOutputPin::DecideBufferSize**](ctransformoutputpin-decidebuffersize.md) method calls this method.</span></span> <span data-ttu-id="b624f-115">La classe dérivée doit implémenter cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b624f-115">The derived class must implement this method.</span></span> <span data-ttu-id="b624f-116">Pour plus d’informations, consultez [**CBaseOutputPin ::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md).</span><span class="sxs-lookup"><span data-stu-id="b624f-116">For more information, see [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b624f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b624f-117">Requirements</span></span>



| <span data-ttu-id="b624f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b624f-118">Requirement</span></span> | <span data-ttu-id="b624f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b624f-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b624f-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="b624f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b624f-121"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b624f-121"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b624f-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b624f-122">Library</span></span><br/> | <dl> <span data-ttu-id="b624f-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b624f-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b624f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b624f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b624f-125">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="b624f-125">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




