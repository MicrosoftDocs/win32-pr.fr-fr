---
description: 'La méthode GetTime récupère les temps de flux auxquels cet exemple doit commencer et se terminer. Cette méthode implémente la méthode IMediaSample :: GetTime.'
ms.assetid: ddb0df1c-707d-405d-9e73-0d5a59f487b6
title: CMediaSample. GetTime, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ff2035ede3e49feb2bc14a7aa31cfc18f2e7d23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537337"
---
# <a name="cmediasamplegettime-method"></a><span data-ttu-id="48465-104">CMediaSample. GetTime, méthode</span><span class="sxs-lookup"><span data-stu-id="48465-104">CMediaSample.GetTime method</span></span>

<span data-ttu-id="48465-105">La `GetTime` méthode récupère les temps de flux auxquels cet exemple doit commencer et se terminer.</span><span class="sxs-lookup"><span data-stu-id="48465-105">The `GetTime` method retrieves the stream times at which this sample should begin and finish.</span></span> <span data-ttu-id="48465-106">Cette méthode implémente la méthode [**IMediaSample :: getTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) .</span><span class="sxs-lookup"><span data-stu-id="48465-106">This method implements the [**IMediaSample::GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="48465-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="48465-107">Syntax</span></span>


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a><span data-ttu-id="48465-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="48465-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48465-109">*pTimeStart*</span><span class="sxs-lookup"><span data-stu-id="48465-109">*pTimeStart*</span></span> 
</dt> <dd>

<span data-ttu-id="48465-110">Pointeur vers une variable qui reçoit le temps de flux de début, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="48465-110">Pointer to a variable that receives the beginning stream time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="48465-111">*pTimeEnd*</span><span class="sxs-lookup"><span data-stu-id="48465-111">*pTimeEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="48465-112">Pointeur vers une variable qui reçoit le temps de flux de fin, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="48465-112">Pointer to a variable that receives the ending stream time, in 100-nanosecond units.</span></span> <span data-ttu-id="48465-113">Si l’exemple n’a pas de temps d’arrêt, la valeur est définie sur l’heure de début plus un.</span><span class="sxs-lookup"><span data-stu-id="48465-113">If the sample has no stop time, the value is set to the start time plus one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48465-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="48465-114">Return value</span></span>

<span data-ttu-id="48465-115">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="48465-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="48465-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="48465-116">Return code</span></span>                                                                                                   | <span data-ttu-id="48465-117">Description</span><span class="sxs-lookup"><span data-stu-id="48465-117">Description</span></span>                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="48465-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="48465-118"><dt>**S\_OK**</dt></span></span> </dl>                          | <span data-ttu-id="48465-119">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="48465-119">Success.</span></span><br/>                                         |
| <dl> <span data-ttu-id="48465-120"><dt>**VFW \_ S \_ sans \_ heure d’arrêt \_**</dt></span><span class="sxs-lookup"><span data-stu-id="48465-120"><dt>**VFW\_S\_NO\_STOP\_TIME**</dt></span></span> </dl>         | <span data-ttu-id="48465-121">L’exemple a une heure de début valide, mais aucune heure d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="48465-121">Sample has a valid start time, but no stop time.</span></span><br/> |
| <dl> <span data-ttu-id="48465-122"><dt>**\_exemple de temps d’échantillonnage VFW E \_ \_ \_ non \_ défini**</dt></span><span class="sxs-lookup"><span data-stu-id="48465-122"><dt>**VFW\_E\_SAMPLE\_TIME\_NOT\_SET**</dt></span></span> </dl> | <span data-ttu-id="48465-123">L’exemple n’a pas de datage valide.</span><span class="sxs-lookup"><span data-stu-id="48465-123">Sample does not have valid time stamps.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="48465-124">Notes</span><span class="sxs-lookup"><span data-stu-id="48465-124">Remarks</span></span>

<span data-ttu-id="48465-125">Les variables de membre de fin [**CMediaSample :: m \_ Start**](cmediasample-m-start.md) et [**CMediaSample :: m \_**](cmediasample-m-end.md) spécifient les horodatages.</span><span class="sxs-lookup"><span data-stu-id="48465-125">The [**CMediaSample::m\_Start**](cmediasample-m-start.md) and [**CMediaSample::m\_End**](cmediasample-m-end.md) member variables specify the time stamps.</span></span> <span data-ttu-id="48465-126">La variable de membre [**CMediaSample :: m \_ dwFlags**](cmediasample-m-dwflags.md) spécifie si les horodatages sont valides.</span><span class="sxs-lookup"><span data-stu-id="48465-126">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies whether the time stamps are valid.</span></span>

<span data-ttu-id="48465-127">Pour plus d’informations sur les horodatages, consultez [heure et horloges dans DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="48465-127">For information about time stamps, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="48465-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="48465-128">Requirements</span></span>



| <span data-ttu-id="48465-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="48465-129">Requirement</span></span> | <span data-ttu-id="48465-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="48465-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48465-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="48465-131">Header</span></span><br/>  | <dl> <span data-ttu-id="48465-132"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="48465-132"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="48465-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="48465-133">Library</span></span><br/> | <dl> <span data-ttu-id="48465-134"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="48465-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48465-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48465-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48465-136">**CMediaSample, classe**</span><span class="sxs-lookup"><span data-stu-id="48465-136">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




