---
description: 'La méthode GetMediaTime récupère les temps de support pour cet exemple. Cette méthode implémente la méthode IMediaSample :: GetMediaTime.'
ms.assetid: f58a2162-5764-48f2-8984-ee4bba1229ab
title: Méthode CMediaSample. GetMediaTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9a41d29e46d29cff9023421a661cc90731d4c06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525191"
---
# <a name="cmediasamplegetmediatime-method"></a><span data-ttu-id="81247-104">Méthode CMediaSample. GetMediaTime</span><span class="sxs-lookup"><span data-stu-id="81247-104">CMediaSample.GetMediaTime method</span></span>

<span data-ttu-id="81247-105">La `GetMediaTime` méthode récupère les temps de support pour cet exemple.</span><span class="sxs-lookup"><span data-stu-id="81247-105">The `GetMediaTime` method retrieves the media times for this sample.</span></span> <span data-ttu-id="81247-106">Cette méthode implémente la méthode [**IMediaSample :: GetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatime) .</span><span class="sxs-lookup"><span data-stu-id="81247-106">This method implements the [**IMediaSample::GetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="81247-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81247-107">Syntax</span></span>


```C++
HRESULT GetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a><span data-ttu-id="81247-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81247-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81247-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="81247-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="81247-110">Pointeur vers une variable qui reçoit l’heure de début du média.</span><span class="sxs-lookup"><span data-stu-id="81247-110">Pointer to a variable that receives the media start time.</span></span>

</dd> <dt>

<span data-ttu-id="81247-111">*Attente*</span><span class="sxs-lookup"><span data-stu-id="81247-111">*pEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="81247-112">Pointeur vers une variable qui reçoit l’heure d’arrêt du support.</span><span class="sxs-lookup"><span data-stu-id="81247-112">Pointer to a variable that receives the media stop time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81247-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="81247-113">Return value</span></span>

<span data-ttu-id="81247-114">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="81247-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="81247-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="81247-115">Return code</span></span>                                                                                                  | <span data-ttu-id="81247-116">Description</span><span class="sxs-lookup"><span data-stu-id="81247-116">Description</span></span>                                         |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="81247-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="81247-117"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="81247-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="81247-118">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="81247-119"><dt>**\_heure du média VFW E \_ \_ \_ non \_ définie**</dt></span><span class="sxs-lookup"><span data-stu-id="81247-119"><dt>**VFW\_E\_MEDIA\_TIME\_NOT\_SET**</dt></span></span> </dl> | <span data-ttu-id="81247-120">Aucun temps de support n’a été défini pour cet exemple.</span><span class="sxs-lookup"><span data-stu-id="81247-120">No media times were set for this sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="81247-121">Notes</span><span class="sxs-lookup"><span data-stu-id="81247-121">Remarks</span></span>

<span data-ttu-id="81247-122">La variable de membre [**CMediaSample :: m \_ MediaEnd**](cmediasample-m-mediaend.md) spécifie un décalage à partir de [**CMediaSample :: m \_ MediaStart**](cmediasample-m-mediastart.md), mais la valeur reçue par le paramètre en *attente* est un temps de support absolu, calculé comme **m \_** MediaStart  +  **m \_ MediaEnd**.</span><span class="sxs-lookup"><span data-stu-id="81247-122">The [**CMediaSample::m\_MediaEnd**](cmediasample-m-mediaend.md) member variable specifies an offset from [**CMediaSample::m\_MediaStart**](cmediasample-m-mediastart.md), but the value received by the *pEnd* parameter is an absolute media time, calculated as **m\_MediaStart** + **m\_MediaEnd**.</span></span>

<span data-ttu-id="81247-123">Pour plus d’informations sur les temps de support, consultez [heure et horloges dans DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="81247-123">For information about media times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="81247-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81247-124">Requirements</span></span>



| <span data-ttu-id="81247-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81247-125">Requirement</span></span> | <span data-ttu-id="81247-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="81247-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81247-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="81247-127">Header</span></span><br/>  | <dl> <span data-ttu-id="81247-128"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81247-128"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="81247-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="81247-129">Library</span></span><br/> | <dl> <span data-ttu-id="81247-130"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="81247-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81247-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81247-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81247-132">**CMediaSample, classe**</span><span class="sxs-lookup"><span data-stu-id="81247-132">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




