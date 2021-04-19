---
description: 'La méthode ReleaseBuffer retourne un exemple de support à la liste des exemples de supports gratuits. Cette méthode implémente la méthode IMemAllocator :: ReleaseBuffer.'
ms.assetid: 35e4e426-044c-4e57-af13-2fddf8501db7
title: Méthode CBaseAllocator. ReleaseBuffer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.ReleaseBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e339f3a8186e845e28261633806a61b1b15c281
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531074"
---
# <a name="cbaseallocatorreleasebuffer-method"></a><span data-ttu-id="c2151-104">Méthode CBaseAllocator. ReleaseBuffer</span><span class="sxs-lookup"><span data-stu-id="c2151-104">CBaseAllocator.ReleaseBuffer method</span></span>

<span data-ttu-id="c2151-105">La `ReleaseBuffer` méthode retourne un exemple de support à la liste des exemples de supports gratuits.</span><span class="sxs-lookup"><span data-stu-id="c2151-105">The `ReleaseBuffer` method returns a media sample to the list of free media samples.</span></span> <span data-ttu-id="c2151-106">Cette méthode implémente la méthode [**IMemAllocator :: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) .</span><span class="sxs-lookup"><span data-stu-id="c2151-106">This method implements the [**IMemAllocator::ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2151-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2151-107">Syntax</span></span>


```C++
HRESULT ReleaseBuffer(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="c2151-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2151-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2151-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="c2151-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="c2151-110">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’objet d’exemple de média.</span><span class="sxs-lookup"><span data-stu-id="c2151-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the media sample object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2151-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c2151-111">Return value</span></span>

<span data-ttu-id="c2151-112">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c2151-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2151-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c2151-113">Remarks</span></span>

<span data-ttu-id="c2151-114">Quand le nombre de références d’un exemple de média atteint zéro, l’exemple appelle **ReleaseBuffer** avec lui-même comme paramètre.</span><span class="sxs-lookup"><span data-stu-id="c2151-114">When a media sample's reference count reaches zero, the sample calls **ReleaseBuffer** with itself as the parameter.</span></span> <span data-ttu-id="c2151-115">Cette méthode effectue les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="c2151-115">This method performs the following actions.</span></span>

-   <span data-ttu-id="c2151-116">Retourne l’exemple de support à la liste libre ([**CBaseAllocator :: m \_ lFree**](cbaseallocator-m-lfree.md)).</span><span class="sxs-lookup"><span data-stu-id="c2151-116">Returns the media sample to the free list ([**CBaseAllocator::m\_lFree**](cbaseallocator-m-lfree.md)).</span></span>
-   <span data-ttu-id="c2151-117">Appelle la méthode [**CBaseAllocator :: NotifySample**](cbaseallocator-notifysample.md) , qui libère tous les threads qui sont bloqués lors des appels à la méthode [**CBaseAllocator :: GetBuffer**](cbaseallocator-getbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="c2151-117">Calls the [**CBaseAllocator::NotifySample**](cbaseallocator-notifysample.md) method, which releases any threads that are blocked on calls to the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method.</span></span>
-   <span data-ttu-id="c2151-118">Si la méthode [**CBaseAllocator :: SetNotify**](cbaseallocator-setnotify.md) a été appelée précédemment, appelle la méthode **IMemAllocatorNotifyCallbackTemp :: NotifyRelease** .</span><span class="sxs-lookup"><span data-stu-id="c2151-118">If the [**CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) method was called previously, calls the **IMemAllocatorNotifyCallbackTemp::NotifyRelease** method.</span></span>
-   <span data-ttu-id="c2151-119">Lorsque le dernier échantillon est publié, s’il y a un appel [**CBaseAllocator ::D ecommit**](cbaseallocator-decommit.md) , appelle la méthode [**CBaseAllocator :: Free**](cbaseallocator-free.md) pour libérer la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c2151-119">When the last sample is released, if there is a pending [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) call, calls the [**CBaseAllocator::Free**](cbaseallocator-free.md) method to release the buffer memory.</span></span> <span data-ttu-id="c2151-120">(Dans la classe de base, **Free** est une méthode virtuelle pure.)</span><span class="sxs-lookup"><span data-stu-id="c2151-120">(In the base class, **Free** is a pure virtual method.)</span></span>

## <a name="requirements"></a><span data-ttu-id="c2151-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2151-121">Requirements</span></span>



| <span data-ttu-id="c2151-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2151-122">Requirement</span></span> | <span data-ttu-id="c2151-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2151-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2151-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="c2151-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c2151-125"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2151-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c2151-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c2151-126">Library</span></span><br/> | <dl> <span data-ttu-id="c2151-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c2151-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2151-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2151-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2151-129">**CBaseAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="c2151-129">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




