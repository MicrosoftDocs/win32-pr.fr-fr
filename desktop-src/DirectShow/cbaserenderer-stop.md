---
description: La méthode Stop arrête le filtre.
ms.assetid: 80eac207-5db3-4b06-bbae-eca72e37d09d
title: CBaseRenderer. Stop, méthode (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ddd8194bbf76c4a4311aa90335f94d1e7548a356
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530015"
---
# <a name="cbaserendererstop-method"></a><span data-ttu-id="56440-103">CBaseRenderer. Stop, méthode</span><span class="sxs-lookup"><span data-stu-id="56440-103">CBaseRenderer.Stop method</span></span>

<span data-ttu-id="56440-104">La `Stop` méthode arrête le filtre.</span><span class="sxs-lookup"><span data-stu-id="56440-104">The `Stop` method stops the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="56440-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56440-105">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="56440-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56440-106">Parameters</span></span>

<span data-ttu-id="56440-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="56440-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="56440-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56440-108">Return value</span></span>

<span data-ttu-id="56440-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="56440-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="56440-110">Notes</span><span class="sxs-lookup"><span data-stu-id="56440-110">Remarks</span></span>

<span data-ttu-id="56440-111">Cette méthode remplace la méthode [**CBaseFilter :: Stop**](cbasefilter-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="56440-111">This method overrides the [**CBaseFilter::Stop**](cbasefilter-stop.md) method.</span></span> <span data-ttu-id="56440-112">Il effectue les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="56440-112">It performs the following actions:</span></span>

-   <span data-ttu-id="56440-113">Appelle [**CBaseFilter :: Stop**](cbasefilter-stop.md).</span><span class="sxs-lookup"><span data-stu-id="56440-113">Calls [**CBaseFilter::Stop**](cbasefilter-stop.md).</span></span>
-   <span data-ttu-id="56440-114">Annule la validation de l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="56440-114">Decommits the allocator.</span></span> <span data-ttu-id="56440-115">(Voir [**IMemAllocator ::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit).)</span><span class="sxs-lookup"><span data-stu-id="56440-115">(See [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit).)</span></span>
-   <span data-ttu-id="56440-116">Annule tout rendu planifié et libère le thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="56440-116">Cancels any scheduled rendering and releases the streaming thread.</span></span>
-   <span data-ttu-id="56440-117">Attend la fin d’un appel de **réception** en attente.</span><span class="sxs-lookup"><span data-stu-id="56440-117">Waits for any pending **Receive** call to complete.</span></span>

## <a name="requirements"></a><span data-ttu-id="56440-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56440-118">Requirements</span></span>



| <span data-ttu-id="56440-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56440-119">Requirement</span></span> | <span data-ttu-id="56440-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="56440-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56440-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="56440-121">Header</span></span><br/>  | <dl> <span data-ttu-id="56440-122"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56440-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="56440-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="56440-123">Library</span></span><br/> | <dl> <span data-ttu-id="56440-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="56440-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56440-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56440-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56440-126">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="56440-126">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




