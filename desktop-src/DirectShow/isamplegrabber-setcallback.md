---
description: La méthode SetCallback spécifie une méthode de rappel à appeler sur les exemples entrants.
ms.assetid: b84d3f52-b986-492a-a8b9-1d98618dcdd3
title: 'ISampleGrabber :: SetCallback, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetCallback
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 46e0565c314bab86967ee0d5dabee6ba449a87dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539977"
---
# <a name="isamplegrabbersetcallback-method"></a><span data-ttu-id="67d43-103">ISampleGrabber :: SetCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="67d43-103">ISampleGrabber::SetCallback method</span></span>

> [!Note]  
> <span data-ttu-id="67d43-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="67d43-104">\[Deprecated.</span></span> <span data-ttu-id="67d43-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="67d43-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="67d43-106">La méthode **SetCallback** spécifie une méthode de rappel à appeler sur les exemples entrants.</span><span class="sxs-lookup"><span data-stu-id="67d43-106">The **SetCallback** method specifies a callback method to call on incoming samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="67d43-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67d43-107">Syntax</span></span>


```C++
HRESULT SetCallback(
   ISampleGrabberCB *pCallback,
   long             WhichMethodToCallback
);
```



## <a name="parameters"></a><span data-ttu-id="67d43-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67d43-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67d43-109">*pCallback*</span><span class="sxs-lookup"><span data-stu-id="67d43-109">*pCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="67d43-110">Pointeur vers une interface [**ISampleGrabberCB**](isamplegrabbercb.md) contenant la méthode de rappel, ou **null** pour annuler le rappel.</span><span class="sxs-lookup"><span data-stu-id="67d43-110">Pointer to an [**ISampleGrabberCB**](isamplegrabbercb.md) interface containing the callback method, or **NULL** to cancel the callback.</span></span>

</dd> <dt>

<span data-ttu-id="67d43-111">*WhichMethodToCallback*</span><span class="sxs-lookup"><span data-stu-id="67d43-111">*WhichMethodToCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="67d43-112">Index qui spécifie la méthode de rappel.</span><span class="sxs-lookup"><span data-stu-id="67d43-112">Index specifying the callback method.</span></span> <span data-ttu-id="67d43-113">Doit avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="67d43-113">Must be one of the following values.</span></span>



| <span data-ttu-id="67d43-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="67d43-114">Value</span></span> | <span data-ttu-id="67d43-115">Description</span><span class="sxs-lookup"><span data-stu-id="67d43-115">Description</span></span>                                                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67d43-116">0</span><span class="sxs-lookup"><span data-stu-id="67d43-116">0</span></span>     | <span data-ttu-id="67d43-117">L’exemple de filtre d’accrochage appelle la méthode [**ISampleGrabberCB :: SampleCB**](isamplegrabbercb-samplecb.md) .</span><span class="sxs-lookup"><span data-stu-id="67d43-117">The Sample Grabber filter calls the [**ISampleGrabberCB::SampleCB**](isamplegrabbercb-samplecb.md) method.</span></span> <span data-ttu-id="67d43-118">Cette méthode reçoit un pointeur [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .</span><span class="sxs-lookup"><span data-stu-id="67d43-118">This method receives an [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointer.</span></span>               |
| <span data-ttu-id="67d43-119">1</span><span class="sxs-lookup"><span data-stu-id="67d43-119">1</span></span>     | <span data-ttu-id="67d43-120">L’exemple de filtre d’accrochage appelle la méthode [**ISampleGrabberCB :: BufferCB**](isamplegrabbercb-buffercb.md) .</span><span class="sxs-lookup"><span data-stu-id="67d43-120">The Sample Grabber filter calls the [**ISampleGrabberCB::BufferCB**](isamplegrabbercb-buffercb.md) method.</span></span> <span data-ttu-id="67d43-121">Cette méthode reçoit un pointeur vers la mémoire tampon contenue dans l’exemple de média.</span><span class="sxs-lookup"><span data-stu-id="67d43-121">This method receives a pointer to the buffer that is contained in the media sample.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67d43-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="67d43-122">Return value</span></span>

<span data-ttu-id="67d43-123">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="67d43-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="67d43-124">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="67d43-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="67d43-125">Notes</span><span class="sxs-lookup"><span data-stu-id="67d43-125">Remarks</span></span>

<span data-ttu-id="67d43-126">Le thread de traitement des données se bloque jusqu’à ce que la méthode de rappel retourne.</span><span class="sxs-lookup"><span data-stu-id="67d43-126">The data processing thread blocks until the callback method returns.</span></span> <span data-ttu-id="67d43-127">Si le rappel ne retourne pas rapidement, il peut interférer avec la lecture.</span><span class="sxs-lookup"><span data-stu-id="67d43-127">If the callback does not return quickly, it can interfere with playback.</span></span>

<span data-ttu-id="67d43-128">Le filtre n’appelle pas la fonction de rappel pour les exemples de préroll, ou pour les exemples dans lesquels le membre **dwStreamId** de la structure de [**\_ \_ Propriétés am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) est autre chose que le \_ média de flux \_ .</span><span class="sxs-lookup"><span data-stu-id="67d43-128">The filter does not invoke the callback function for preroll samples, or for samples in which the **dwStreamId** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure is anything other than AM\_STREAM\_MEDIA.</span></span>

> [!Note]  
> <span data-ttu-id="67d43-129">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="67d43-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="67d43-130">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="67d43-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="67d43-131">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="67d43-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="67d43-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67d43-132">Requirements</span></span>



| <span data-ttu-id="67d43-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67d43-133">Requirement</span></span> | <span data-ttu-id="67d43-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="67d43-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67d43-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="67d43-135">Header</span></span><br/>  | <dl> <span data-ttu-id="67d43-136"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="67d43-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="67d43-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="67d43-137">Library</span></span><br/> | <dl> <span data-ttu-id="67d43-138"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67d43-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67d43-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67d43-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67d43-140">Utilisation de l’exemple d’accrochage</span><span class="sxs-lookup"><span data-stu-id="67d43-140">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="67d43-141">**Interface ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="67d43-141">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




