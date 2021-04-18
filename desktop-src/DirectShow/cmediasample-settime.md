---
description: 'La méthode SetTime définit les temps de flux lorsque cet exemple doit commencer et se terminer. Cette méthode implémente la méthode IMediaSample :: SetTime.'
ms.assetid: cab4907f-eb6f-4444-9b41-1f95a6ecffed
title: CMediaSample. SetTime, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 935c4f3aa565b291e459d36e067805944b4fd6b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520369"
---
# <a name="cmediasamplesettime-method"></a><span data-ttu-id="686d7-104">CMediaSample. SetTime, méthode</span><span class="sxs-lookup"><span data-stu-id="686d7-104">CMediaSample.SetTime method</span></span>

<span data-ttu-id="686d7-105">La `SetTime` méthode définit les temps de flux lorsque cet exemple doit commencer et se terminer.</span><span class="sxs-lookup"><span data-stu-id="686d7-105">The `SetTime` method sets the stream times when this sample should begin and finish.</span></span> <span data-ttu-id="686d7-106">Cette méthode implémente la méthode [**IMediaSample :: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) .</span><span class="sxs-lookup"><span data-stu-id="686d7-106">This method implements the [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="686d7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="686d7-107">Syntax</span></span>


```C++
HRESULT SetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a><span data-ttu-id="686d7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="686d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="686d7-109">*pTimeStart*</span><span class="sxs-lookup"><span data-stu-id="686d7-109">*pTimeStart*</span></span> 
</dt> <dd>

<span data-ttu-id="686d7-110">Pointeur vers le temps de flux auquel l’échantillon commence, en unités de 100 nanosecondes, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="686d7-110">Pointer to the stream time at which the sample begins, in 100-nanosecond units, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="686d7-111">*pTimeEnd*</span><span class="sxs-lookup"><span data-stu-id="686d7-111">*pTimeEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="686d7-112">Pointeur vers le temps de flux auquel l’échantillon se termine, en unités de 100 nanosecondes, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="686d7-112">Pointer to the stream time at which the sample ends, in 100-nanosecond units, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="686d7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="686d7-113">Return value</span></span>

<span data-ttu-id="686d7-114">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="686d7-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="686d7-115">Notes</span><span class="sxs-lookup"><span data-stu-id="686d7-115">Remarks</span></span>

<span data-ttu-id="686d7-116">Cette méthode définit les variables de membre de fin [**CMediaSample :: m \_ Start**](cmediasample-m-start.md) et [**CMediaSample :: m \_**](cmediasample-m-end.md) , qui spécifient les horodatages.</span><span class="sxs-lookup"><span data-stu-id="686d7-116">This method sets the [**CMediaSample::m\_Start**](cmediasample-m-start.md) and [**CMediaSample::m\_End**](cmediasample-m-end.md) member variables, which specify the time stamps.</span></span> <span data-ttu-id="686d7-117">Il met également à jour la variable de membre [**CMediaSample :: m \_ dwFlags**](cmediasample-m-dwflags.md) , qui spécifie si les horodatages sont valides.</span><span class="sxs-lookup"><span data-stu-id="686d7-117">It also updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies whether the time stamps are valid.</span></span>

<span data-ttu-id="686d7-118">Pour plus d’informations sur les horodatages, consultez [heure et horloges dans DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="686d7-118">For information about time stamps, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="686d7-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="686d7-119">Requirements</span></span>



| <span data-ttu-id="686d7-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="686d7-120">Requirement</span></span> | <span data-ttu-id="686d7-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="686d7-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="686d7-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="686d7-122">Header</span></span><br/>  | <dl> <span data-ttu-id="686d7-123"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="686d7-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="686d7-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="686d7-124">Library</span></span><br/> | <dl> <span data-ttu-id="686d7-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="686d7-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="686d7-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="686d7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="686d7-127">**CMediaSample, classe**</span><span class="sxs-lookup"><span data-stu-id="686d7-127">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




