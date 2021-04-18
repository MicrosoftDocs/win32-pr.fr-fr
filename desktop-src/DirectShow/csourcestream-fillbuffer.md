---
description: La méthode FillBuffer remplit un échantillon de média avec des données.
ms.assetid: dddad8c7-44f1-4ba3-8fb1-7e7e88e40941
title: Méthode CSourceStream. FillBuffer (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.FillBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3611ad8b590bb823abccdecf9d3d138c70441a07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540244"
---
# <a name="csourcestreamfillbuffer-method"></a><span data-ttu-id="c3950-103">Méthode CSourceStream. FillBuffer</span><span class="sxs-lookup"><span data-stu-id="c3950-103">CSourceStream.FillBuffer method</span></span>

<span data-ttu-id="c3950-104">La `FillBuffer` méthode remplit un échantillon de média avec des données.</span><span class="sxs-lookup"><span data-stu-id="c3950-104">The `FillBuffer` method fills a media sample with data.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3950-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3950-105">Syntax</span></span>


```C++
virtual HRESULT FillBuffer(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="c3950-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3950-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3950-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="c3950-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="c3950-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="c3950-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3950-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c3950-109">Return value</span></span>

<span data-ttu-id="c3950-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c3950-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c3950-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="c3950-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="c3950-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c3950-112">Return code</span></span>                                                                             | <span data-ttu-id="c3950-113">Description</span><span class="sxs-lookup"><span data-stu-id="c3950-113">Description</span></span>              |
|-----------------------------------------------------------------------------------------|--------------------------|
| <dl> <span data-ttu-id="c3950-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="c3950-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="c3950-115">Fin de flux</span><span class="sxs-lookup"><span data-stu-id="c3950-115">End of stream</span></span><br/> |
| <dl> <span data-ttu-id="c3950-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c3950-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="c3950-117">Succès</span><span class="sxs-lookup"><span data-stu-id="c3950-117">Success</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="c3950-118">Notes</span><span class="sxs-lookup"><span data-stu-id="c3950-118">Remarks</span></span>

<span data-ttu-id="c3950-119">La classe dérivée doit implémenter cette méthode.</span><span class="sxs-lookup"><span data-stu-id="c3950-119">The derived class must implement this method.</span></span>

<span data-ttu-id="c3950-120">L’exemple de support fourni à cette méthode n’a pas de datage.</span><span class="sxs-lookup"><span data-stu-id="c3950-120">The media sample given to this method has no time stamps.</span></span> <span data-ttu-id="c3950-121">La classe dérivée doit appeler la méthode [**IMediaSample :: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) pour définir les horodatages.</span><span class="sxs-lookup"><span data-stu-id="c3950-121">The derived class should call the [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) method to set the time stamps.</span></span> <span data-ttu-id="c3950-122">Si cela est approprié pour le type de média, la classe dérivée doit également définir les heures de média, en appelant la méthode [**IMediaSample :: SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) .</span><span class="sxs-lookup"><span data-stu-id="c3950-122">If appropriate for the media type, the derived class should also set the media times, by calling the [**IMediaSample::SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) method.</span></span> <span data-ttu-id="c3950-123">Pour plus d’informations, consultez [heure et horloges dans DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="c3950-123">For more information, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

<span data-ttu-id="c3950-124">Retourne S \_ false à la fin du flux.</span><span class="sxs-lookup"><span data-stu-id="c3950-124">Return S\_FALSE at the end of the stream.</span></span> <span data-ttu-id="c3950-125">Cela amène la classe **CSourceStream** à envoyer la notification de fin de flux et à arrêter la boucle de traitement de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c3950-125">This causes the **CSourceStream** class to send the end-of-stream notification and halt the buffer processing loop.</span></span> <span data-ttu-id="c3950-126">Pour plus d’informations, consultez [**CSourceStream ::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .</span><span class="sxs-lookup"><span data-stu-id="c3950-126">See [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) for more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3950-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3950-127">Requirements</span></span>



| <span data-ttu-id="c3950-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3950-128">Requirement</span></span> | <span data-ttu-id="c3950-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3950-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3950-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3950-130">Header</span></span><br/>  | <dl> <span data-ttu-id="c3950-131"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3950-131"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c3950-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c3950-132">Library</span></span><br/> | <dl> <span data-ttu-id="c3950-133"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c3950-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3950-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3950-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3950-135">**CSourceStream, classe**</span><span class="sxs-lookup"><span data-stu-id="c3950-135">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




