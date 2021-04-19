---
description: 'La méthode GetStopPosition récupère l’heure à laquelle la lecture s’arrête, par rapport à la durée du flux. Cette méthode implémente la méthode IMediaSeeking :: GetStopPosition.'
ms.assetid: 11486371-da0a-4b83-956b-ef6b92721e74
title: Méthode CPosPassThru. GetStopPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ee704a47074db032badfa1f02ffbf2db8c7efa4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539257"
---
# <a name="cpospassthrugetstopposition-method"></a><span data-ttu-id="430c8-104">Méthode CPosPassThru. GetStopPosition</span><span class="sxs-lookup"><span data-stu-id="430c8-104">CPosPassThru.GetStopPosition method</span></span>

<span data-ttu-id="430c8-105">La `GetStopPosition` méthode récupère l’heure à laquelle la lecture s’arrêtera, par rapport à la durée du flux.</span><span class="sxs-lookup"><span data-stu-id="430c8-105">The `GetStopPosition` method retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="430c8-106">Cette méthode implémente la méthode [**IMediaSeeking :: GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) .</span><span class="sxs-lookup"><span data-stu-id="430c8-106">This method implements the [**IMediaSeeking::GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="430c8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="430c8-107">Syntax</span></span>


```C++
HRESULT GetStopPosition(
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="430c8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="430c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="430c8-109">*pStop*</span><span class="sxs-lookup"><span data-stu-id="430c8-109">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="430c8-110">Pointeur vers une variable qui reçoit l’heure d’arrêt, en unités du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="430c8-110">Pointer to a variable that receives the stop time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="430c8-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="430c8-111">Return value</span></span>

<span data-ttu-id="430c8-112">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="430c8-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="430c8-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="430c8-113">Requirements</span></span>



| <span data-ttu-id="430c8-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="430c8-114">Requirement</span></span> | <span data-ttu-id="430c8-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="430c8-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="430c8-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="430c8-116">Header</span></span><br/>  | <dl> <span data-ttu-id="430c8-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="430c8-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="430c8-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="430c8-118">Library</span></span><br/> | <dl> <span data-ttu-id="430c8-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="430c8-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="430c8-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="430c8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="430c8-121">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="430c8-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




