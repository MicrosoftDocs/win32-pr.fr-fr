---
description: La méthode GetDeliveryBuffer récupère un exemple de média qui contient une mémoire tampon vide.
ms.assetid: 5a20c11b-50f8-443e-a4d5-6bcffde741d5
title: Méthode CBaseOutputPin. GetDeliveryBuffer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.GetDeliveryBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 332fad740c1ea904feee1a437273f21eb4c1def0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526840"
---
# <a name="cbaseoutputpingetdeliverybuffer-method"></a><span data-ttu-id="f7554-103">Méthode CBaseOutputPin. GetDeliveryBuffer</span><span class="sxs-lookup"><span data-stu-id="f7554-103">CBaseOutputPin.GetDeliveryBuffer method</span></span>

<span data-ttu-id="f7554-104">La `GetDeliveryBuffer` méthode récupère un exemple de média qui contient une mémoire tampon vide.</span><span class="sxs-lookup"><span data-stu-id="f7554-104">The `GetDeliveryBuffer` method retrieves a media sample that contains an empty buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7554-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7554-105">Syntax</span></span>


```C++
virtual HRESULT GetDeliveryBuffer(
   IMediaSample   **ppSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="f7554-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7554-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7554-107">*ppSample*</span><span class="sxs-lookup"><span data-stu-id="f7554-107">*ppSample*</span></span> 
</dt> <dd>

<span data-ttu-id="f7554-108">Adresse d’une variable qui reçoit un pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="f7554-108">Address of a variable that receives a pointer to the buffer's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="f7554-109">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="f7554-109">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="f7554-110">Pointeur désignant l’heure de début de l’exemple, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="f7554-110">Pointer to the start time of the sample, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f7554-111">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="f7554-111">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="f7554-112">Pointeur vers l’heure de fin de l’exemple, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="f7554-112">Pointer to the ending time of the sample, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f7554-113">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="f7554-113">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="f7554-114">Combinaison d’opérations de bits des indicateurs pris en charge par l’interface [**IMemAllocator :: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) .</span><span class="sxs-lookup"><span data-stu-id="f7554-114">Bitwise combination of flags supported by the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7554-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f7554-115">Return value</span></span>

<span data-ttu-id="f7554-116">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f7554-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f7554-117">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f7554-117">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="f7554-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f7554-118">Return code</span></span>                                                                                   | <span data-ttu-id="f7554-119">Description</span><span class="sxs-lookup"><span data-stu-id="f7554-119">Description</span></span>                        |
|-----------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="f7554-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f7554-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f7554-121">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="f7554-121">Success.</span></span><br/>                |
| <dl> <span data-ttu-id="f7554-122"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="f7554-122"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="f7554-123">Aucun allocateur disponible.</span><span class="sxs-lookup"><span data-stu-id="f7554-123">No allocator available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f7554-124">Notes</span><span class="sxs-lookup"><span data-stu-id="f7554-124">Remarks</span></span>

<span data-ttu-id="f7554-125">Cette méthode appelle la méthode **IMemAllocator :: GetBuffer** sur l’allocateur et passe les paramètres à cette méthode.</span><span class="sxs-lookup"><span data-stu-id="f7554-125">This method calls the **IMemAllocator::GetBuffer** method on the allocator, and passes the parameters to that method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7554-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7554-126">Requirements</span></span>



| <span data-ttu-id="f7554-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7554-127">Requirement</span></span> | <span data-ttu-id="f7554-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7554-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7554-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7554-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f7554-130"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f7554-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f7554-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f7554-131">Library</span></span><br/> | <dl> <span data-ttu-id="f7554-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f7554-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7554-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7554-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7554-134">**CBaseOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="f7554-134">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




