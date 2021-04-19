---
description: La méthode StreamTime récupère le temps de flux actuel.
ms.assetid: 88a2939d-fb51-49fd-af71-21c99511de43
title: Méthode CBaseFilter. StreamTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f4370758eb4ab15a9e53a5157550ee2129783c7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530344"
---
# <a name="cbasefilterstreamtime-method"></a><span data-ttu-id="23d5c-103">Méthode CBaseFilter. StreamTime</span><span class="sxs-lookup"><span data-stu-id="23d5c-103">CBaseFilter.StreamTime method</span></span>

<span data-ttu-id="23d5c-104">La méthode **StreamTime** récupère le temps de flux actuel.</span><span class="sxs-lookup"><span data-stu-id="23d5c-104">The **StreamTime** method retrieves the current stream time.</span></span>

## <a name="syntax"></a><span data-ttu-id="23d5c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23d5c-105">Syntax</span></span>


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a><span data-ttu-id="23d5c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23d5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23d5c-107">*rtStream* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="23d5c-107">*rtStream* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="23d5c-108">Référence à un objet [**CRefTime**](creftime.md) qui reçoit le temps de flux actuel.</span><span class="sxs-lookup"><span data-stu-id="23d5c-108">Reference to a [**CRefTime**](creftime.md) object that receives the current stream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23d5c-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="23d5c-109">Return value</span></span>

<span data-ttu-id="23d5c-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="23d5c-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="23d5c-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="23d5c-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="23d5c-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="23d5c-112">Return code</span></span>                                                                                      | <span data-ttu-id="23d5c-113">Description</span><span class="sxs-lookup"><span data-stu-id="23d5c-113">Description</span></span>                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="23d5c-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="23d5c-114"><dt>**S\_OK**</dt></span></span> </dl>             | <span data-ttu-id="23d5c-115">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="23d5c-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="23d5c-116"><dt>**VFW \_ E \_ pas d' \_ horloge**</dt></span><span class="sxs-lookup"><span data-stu-id="23d5c-116"><dt>**VFW\_E\_NO\_CLOCK**</dt></span></span> </dl> | <span data-ttu-id="23d5c-117">Aucune horloge de référence n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="23d5c-117">No reference clock is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="23d5c-118">Notes</span><span class="sxs-lookup"><span data-stu-id="23d5c-118">Remarks</span></span>

<span data-ttu-id="23d5c-119">Le temps de flux est défini comme le temps de référence actuel (comme indiqué par l’horloge de référence) moins l’heure de début (spécifiée par [**CBaseFilter :: m \_ tStart**](cbasefilter-m-tstart.md)).</span><span class="sxs-lookup"><span data-stu-id="23d5c-119">Stream time is defined as the current reference time (as given by the reference clock) minus the start time (specified by [**CBaseFilter::m\_tStart**](cbasefilter-m-tstart.md)).</span></span> <span data-ttu-id="23d5c-120">L' *horodatage* d’un exemple de média spécifie l’heure du flux de temps quand il doit être rendu.</span><span class="sxs-lookup"><span data-stu-id="23d5c-120">A media sample's *time stamp* specifies the stream time when it should be rendered.</span></span> <span data-ttu-id="23d5c-121">Si un échantillon dont l’horodatage est inférieur à l’heure actuelle du flux n’a pas encore été affiché, il est tardif.</span><span class="sxs-lookup"><span data-stu-id="23d5c-121">If a sample with a time stamp less than the current stream time has not yet been rendered, it is late.</span></span>

<span data-ttu-id="23d5c-122">Cette méthode obtient le temps de flux en appelant [**IReferenceClock :: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) pour obtenir le temps de référence actuel, puis en soustrayant l’heure de début initiale.</span><span class="sxs-lookup"><span data-stu-id="23d5c-122">This method gets the stream time by calling [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) to get the current reference time, and then subtracting the initial start time.</span></span>

## <a name="requirements"></a><span data-ttu-id="23d5c-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23d5c-123">Requirements</span></span>



| <span data-ttu-id="23d5c-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23d5c-124">Requirement</span></span> | <span data-ttu-id="23d5c-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="23d5c-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23d5c-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="23d5c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="23d5c-127"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="23d5c-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="23d5c-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="23d5c-128">Library</span></span><br/> | <dl> <span data-ttu-id="23d5c-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="23d5c-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23d5c-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23d5c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23d5c-131">Temps et horloges dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="23d5c-131">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="23d5c-132">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="23d5c-132">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




