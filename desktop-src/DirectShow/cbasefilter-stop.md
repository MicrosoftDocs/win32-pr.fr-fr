---
description: 'La méthode Stop arrête le filtre. Cette méthode implémente la méthode IMediaFilter :: Stop.'
ms.assetid: 68d77f9a-95a2-4a71-bbe1-28be76fbc538
title: CBaseFilter. Stop, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b4c4893edcf02fa18da3dc207a49f87c91b2a9ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528521"
---
# <a name="cbasefilterstop-method"></a><span data-ttu-id="60593-104">CBaseFilter. Stop, méthode</span><span class="sxs-lookup"><span data-stu-id="60593-104">CBaseFilter.Stop method</span></span>

<span data-ttu-id="60593-105">La `Stop` méthode arrête le filtre.</span><span class="sxs-lookup"><span data-stu-id="60593-105">The `Stop` method stops the filter.</span></span> <span data-ttu-id="60593-106">Cette méthode implémente la méthode [**IMediaFilter :: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .</span><span class="sxs-lookup"><span data-stu-id="60593-106">This method implements the [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="60593-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60593-107">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="60593-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60593-108">Parameters</span></span>

<span data-ttu-id="60593-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="60593-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="60593-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="60593-110">Return value</span></span>

<span data-ttu-id="60593-111">Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="60593-111">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="60593-112">Notes</span><span class="sxs-lookup"><span data-stu-id="60593-112">Remarks</span></span>

<span data-ttu-id="60593-113">Cette méthode appelle la méthode [**CBasePin :: inactive**](cbasepin-inactive.md) sur chacune des broches connectées du filtre.</span><span class="sxs-lookup"><span data-stu-id="60593-113">This method calls the [**CBasePin::Inactive**](cbasepin-inactive.md) method on each of the filter's connected pins.</span></span> <span data-ttu-id="60593-114">Il définit également l’état du filtre sur état \_ arrêté.</span><span class="sxs-lookup"><span data-stu-id="60593-114">It also sets the filter's state to State\_Stopped.</span></span>

<span data-ttu-id="60593-115">Quand le filtre s’arrête, il doit rejeter les exemples en amont, arrêter la diffusion des exemples en aval, arrêter les threads de travail et libérer toutes les ressources qu’il utilisait pour la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="60593-115">When the filter stops, it should reject samples from upstream, stop delivering samples downstream, shut down worker threads, and free any resources that it used for streaming.</span></span>

## <a name="requirements"></a><span data-ttu-id="60593-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60593-116">Requirements</span></span>



| <span data-ttu-id="60593-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60593-117">Requirement</span></span> | <span data-ttu-id="60593-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="60593-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60593-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="60593-119">Header</span></span><br/>  | <dl> <span data-ttu-id="60593-120"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="60593-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="60593-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="60593-121">Library</span></span><br/> | <dl> <span data-ttu-id="60593-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="60593-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60593-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60593-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60593-124">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="60593-124">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




