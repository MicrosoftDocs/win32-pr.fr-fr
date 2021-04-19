---
description: 'La méthode GetStopPosition récupère l’heure à laquelle la lecture s’arrête, par rapport à la durée du flux. Cette méthode implémente la méthode IMediaSeeking :: GetStopPosition.'
ms.assetid: 83928f62-7acc-43b9-9537-49131ed0b0d4
title: Méthode CSourceSeeking. GetStopPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d9f61ad26c32cfeec285874edfcc26038d57b117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535279"
---
# <a name="csourceseekinggetstopposition-method"></a><span data-ttu-id="c26e9-104">Méthode CSourceSeeking. GetStopPosition</span><span class="sxs-lookup"><span data-stu-id="c26e9-104">CSourceSeeking.GetStopPosition method</span></span>

<span data-ttu-id="c26e9-105">La `GetStopPosition` méthode récupère l’heure à laquelle la lecture s’arrêtera, par rapport à la durée du flux.</span><span class="sxs-lookup"><span data-stu-id="c26e9-105">The `GetStopPosition` method retrieves the time when playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="c26e9-106">Cette méthode implémente la méthode [**IMediaSeeking :: GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) .</span><span class="sxs-lookup"><span data-stu-id="c26e9-106">This method implements the [**IMediaSeeking::GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c26e9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c26e9-107">Syntax</span></span>


```C++
HRESULT GetStopPosition(
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="c26e9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c26e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c26e9-109">*pStop*</span><span class="sxs-lookup"><span data-stu-id="c26e9-109">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="c26e9-110">Pointeur vers une variable qui reçoit l’heure d’arrêt, en unités du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="c26e9-110">Pointer to a variable that receives the stop time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c26e9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c26e9-111">Return value</span></span>

<span data-ttu-id="c26e9-112">Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c26e9-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="c26e9-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c26e9-113">Return code</span></span>                                                                               | <span data-ttu-id="c26e9-114">Description</span><span class="sxs-lookup"><span data-stu-id="c26e9-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="c26e9-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c26e9-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="c26e9-116">Succès</span><span class="sxs-lookup"><span data-stu-id="c26e9-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="c26e9-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="c26e9-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="c26e9-118">Valeur de pointeur **null**</span><span class="sxs-lookup"><span data-stu-id="c26e9-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c26e9-119">Notes</span><span class="sxs-lookup"><span data-stu-id="c26e9-119">Remarks</span></span>

<span data-ttu-id="c26e9-120">L’heure d’arrêt est spécifiée par la variable membre [**CSourceSeeking :: m \_ rtStop**](csourceseeking-m-rtstop.md) .</span><span class="sxs-lookup"><span data-stu-id="c26e9-120">The stop time is specified by the [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="c26e9-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c26e9-121">Requirements</span></span>



| <span data-ttu-id="c26e9-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c26e9-122">Requirement</span></span> | <span data-ttu-id="c26e9-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c26e9-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c26e9-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="c26e9-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c26e9-125"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c26e9-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c26e9-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c26e9-126">Library</span></span><br/> | <dl> <span data-ttu-id="c26e9-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c26e9-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c26e9-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c26e9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c26e9-129">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="c26e9-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




