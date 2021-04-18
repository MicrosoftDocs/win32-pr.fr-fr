---
description: La méthode InitializeOutputSample récupère un nouvel exemple de sortie et l’initialise.
ms.assetid: a4f8f514-cf1a-4f8f-ac17-17378705c2ea
title: CTransformFilter.Iniméthode tializeOutputSample (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.InitializeOutputSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: efe7e62936c6feb1984a339a67783cdbc1e4f124
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543284"
---
# <a name="ctransformfilterinitializeoutputsample-method"></a><span data-ttu-id="87e6c-103">CTransformFilter.Iniméthode tializeOutputSample</span><span class="sxs-lookup"><span data-stu-id="87e6c-103">CTransformFilter.InitializeOutputSample method</span></span>

<span data-ttu-id="87e6c-104">La `InitializeOutputSample` méthode récupère un nouvel exemple de sortie et l’initialise.</span><span class="sxs-lookup"><span data-stu-id="87e6c-104">The `InitializeOutputSample` method retrieves a new output sample and initializes it.</span></span>

## <a name="syntax"></a><span data-ttu-id="87e6c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87e6c-105">Syntax</span></span>


```C++
HRESULT InitializeOutputSample(
   IMediaSample *pSample,
   IMediaSample **ppOutSample
);
```



## <a name="parameters"></a><span data-ttu-id="87e6c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87e6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87e6c-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="87e6c-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="87e6c-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple d’entrée.</span><span class="sxs-lookup"><span data-stu-id="87e6c-108">Pointer to the input sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="87e6c-109">*ppOutSample*</span><span class="sxs-lookup"><span data-stu-id="87e6c-109">*ppOutSample*</span></span> 
</dt> <dd>

<span data-ttu-id="87e6c-110">Reçoit un pointeur vers l’interface **IMediaSample** de l’exemple de sortie.</span><span class="sxs-lookup"><span data-stu-id="87e6c-110">Receives a pointer to the output sample's **IMediaSample** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87e6c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="87e6c-111">Return value</span></span>

<span data-ttu-id="87e6c-112">Retourne S \_ OK ou une autre valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="87e6c-112">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="87e6c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="87e6c-113">Remarks</span></span>

<span data-ttu-id="87e6c-114">Cette méthode est appelée par la méthode [**CTransformFilter :: Receive**](ctransformfilter-receive.md) pour préparer l’exemple de sortie.</span><span class="sxs-lookup"><span data-stu-id="87e6c-114">This method is called by the [**CTransformFilter::Receive**](ctransformfilter-receive.md) method to prepare the output sample.</span></span> <span data-ttu-id="87e6c-115">En général, il n’est pas nécessaire d’appeler cette méthode dans votre classe dérivée, sauf si vous substituez la méthode **Receive** .</span><span class="sxs-lookup"><span data-stu-id="87e6c-115">Generally you do not have to call this method in your derived class, unless you override the **Receive** method.</span></span>

<span data-ttu-id="87e6c-116">Cette méthode récupère un nouvel exemple à partir de l’allocateur de la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="87e6c-116">This method retrieves a new sample from the output pin's allocator.</span></span> <span data-ttu-id="87e6c-117">Il copie ensuite les exemples de propriétés de l’exemple d’entrée dans l’exemple de sortie.</span><span class="sxs-lookup"><span data-stu-id="87e6c-117">Then it copies the sample properties from the input sample to the output sample.</span></span> <span data-ttu-id="87e6c-118">Les exemples de propriétés sont définis dans la structure de [**\_ \_ Propriétés am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .</span><span class="sxs-lookup"><span data-stu-id="87e6c-118">The sample properties are defined in the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="87e6c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87e6c-119">Requirements</span></span>



| <span data-ttu-id="87e6c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87e6c-120">Requirement</span></span> | <span data-ttu-id="87e6c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="87e6c-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87e6c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="87e6c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="87e6c-123"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87e6c-123"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="87e6c-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="87e6c-124">Library</span></span><br/> | <dl> <span data-ttu-id="87e6c-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="87e6c-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87e6c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87e6c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87e6c-127">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="87e6c-127">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




