---
description: 'La méthode SetMediaTime définit les temps de support pour cet exemple. Cette méthode implémente la méthode IMediaSample :: SetMediaTime.'
ms.assetid: 768812f8-c044-4499-9149-7c334c51e539
title: Méthode CMediaSample. SetMediaTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0240ef40f4c37f6c5528c979b2e89b43b03b3451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530412"
---
# <a name="cmediasamplesetmediatime-method"></a><span data-ttu-id="b5a47-104">Méthode CMediaSample. SetMediaTime</span><span class="sxs-lookup"><span data-stu-id="b5a47-104">CMediaSample.SetMediaTime method</span></span>

<span data-ttu-id="b5a47-105">La `SetMediaTime` méthode définit les temps de support pour cet exemple.</span><span class="sxs-lookup"><span data-stu-id="b5a47-105">The `SetMediaTime` method sets the media times for this sample.</span></span> <span data-ttu-id="b5a47-106">Cette méthode implémente la méthode [**IMediaSample :: SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) .</span><span class="sxs-lookup"><span data-stu-id="b5a47-106">This method implements the [**IMediaSample::SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5a47-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5a47-107">Syntax</span></span>


```C++
HRESULT SetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a><span data-ttu-id="b5a47-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5a47-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5a47-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="b5a47-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="b5a47-110">Pointeur désignant l’heure de début du média, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="b5a47-110">Pointer to the media start time, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b5a47-111">*Attente*</span><span class="sxs-lookup"><span data-stu-id="b5a47-111">*pEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="b5a47-112">Pointeur désignant l’heure d’arrêt du support, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="b5a47-112">Pointer to the media stop time, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5a47-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b5a47-113">Return value</span></span>

<span data-ttu-id="b5a47-114">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b5a47-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5a47-115">Notes</span><span class="sxs-lookup"><span data-stu-id="b5a47-115">Remarks</span></span>

<span data-ttu-id="b5a47-116">L’heure d’arrêt du support doit être supérieure à l’heure de début du support.</span><span class="sxs-lookup"><span data-stu-id="b5a47-116">The media stop time must be greater than the media start time.</span></span> <span data-ttu-id="b5a47-117">Utilisez **null** pour invalider les temps de support.</span><span class="sxs-lookup"><span data-stu-id="b5a47-117">Use **NULL** to invalidate the media times.</span></span>

<span data-ttu-id="b5a47-118">Le paramètre en *attente* spécifie un temps de support absolu, mais la variable de membre [**CMediaSample :: m \_ MediaEnd**](cmediasample-m-mediaend.md) est calculée comme un décalage par rapport à *pstart*.</span><span class="sxs-lookup"><span data-stu-id="b5a47-118">The *pEnd* parameter specifies an absolute media time, but the [**CMediaSample::m\_MediaEnd**](cmediasample-m-mediaend.md) member variable is calculated as an offset from *pStart*.</span></span> <span data-ttu-id="b5a47-119">En d’autres termes, **m \_ MediaEnd**  =  \* *pTimeEnd* \* *pTimeStart*.  </span><span class="sxs-lookup"><span data-stu-id="b5a47-119">In other words, **m\_MediaEnd** = \**pTimeEnd*  \**pTimeStart*.</span></span>

<span data-ttu-id="b5a47-120">Pour plus d’informations sur les temps de support, consultez [heure et horloges dans DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="b5a47-120">For information about media times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5a47-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5a47-121">Requirements</span></span>



| <span data-ttu-id="b5a47-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5a47-122">Requirement</span></span> | <span data-ttu-id="b5a47-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5a47-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5a47-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5a47-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b5a47-125"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b5a47-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b5a47-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b5a47-126">Library</span></span><br/> | <dl> <span data-ttu-id="b5a47-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b5a47-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5a47-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5a47-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5a47-129">**CMediaSample, classe**</span><span class="sxs-lookup"><span data-stu-id="b5a47-129">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




