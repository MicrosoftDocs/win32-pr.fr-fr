---
description: La méthode SetOneShot spécifie si le filtre d’accrochage de l’exemple s’arrête une fois que le filtre a reçu un exemple.
ms.assetid: 7e3a3e8c-1834-425b-9657-279ab4451a2b
title: 'ISampleGrabber :: SetOneShot, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetOneShot
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72a6e0e1798bcb8e19807619e982f487b0f04e6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533049"
---
# <a name="isamplegrabbersetoneshot-method"></a><span data-ttu-id="c79eb-103">ISampleGrabber :: SetOneShot, méthode</span><span class="sxs-lookup"><span data-stu-id="c79eb-103">ISampleGrabber::SetOneShot method</span></span>

> [!Note]  
> <span data-ttu-id="c79eb-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="c79eb-104">\[Deprecated.</span></span> <span data-ttu-id="c79eb-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c79eb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c79eb-106">La méthode **SetOneShot** spécifie si le filtre d' [**accrochage**](sample-grabber-filter.md) de l’exemple s’arrête une fois que le filtre a reçu un exemple.</span><span class="sxs-lookup"><span data-stu-id="c79eb-106">The **SetOneShot** method specifies whether the [**Sample Grabber**](sample-grabber-filter.md) filter halts after the filter receives a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="c79eb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c79eb-107">Syntax</span></span>


```C++
HRESULT SetOneShot(
   BOOL OneShot
);
```



## <a name="parameters"></a><span data-ttu-id="c79eb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c79eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c79eb-109">*OneShot*</span><span class="sxs-lookup"><span data-stu-id="c79eb-109">*OneShot*</span></span> 
</dt> <dd>

<span data-ttu-id="c79eb-110">Valeur booléenne qui spécifie si le filtre d’accrochage de l’exemple s’arrête après avoir reçu un échantillon.</span><span class="sxs-lookup"><span data-stu-id="c79eb-110">A Boolean value that specifies whether the Sample Grabber filter halts after receiving a sample.</span></span>



| <span data-ttu-id="c79eb-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="c79eb-111">Value</span></span>                                                                                                                                    | <span data-ttu-id="c79eb-112">Signification</span><span class="sxs-lookup"><span data-stu-id="c79eb-112">Meaning</span></span>                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="c79eb-113"><dt>VRAI \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="c79eb-113"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="c79eb-114">L’exemple d’accrochage s’arrête après le premier échantillon.</span><span class="sxs-lookup"><span data-stu-id="c79eb-114">The Sample Grabber halts after the first sample.</span></span> <br/>                                                      |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="c79eb-115"><dt>FALSe \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="c79eb-115"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="c79eb-116">Après le premier exemple, la méthode d’accrochage continue à traiter les exemples.</span><span class="sxs-lookup"><span data-stu-id="c79eb-116">After the first sample, the Sample Grabber continues to process samples.</span></span> <span data-ttu-id="c79eb-117">Il s'agit du comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="c79eb-117">This is the default behavior.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c79eb-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c79eb-118">Return value</span></span>

<span data-ttu-id="c79eb-119">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c79eb-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c79eb-120">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c79eb-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c79eb-121">Notes</span><span class="sxs-lookup"><span data-stu-id="c79eb-121">Remarks</span></span>

<span data-ttu-id="c79eb-122">Utilisez cette méthode pour obtenir un seul échantillon du flux, comme suit :</span><span class="sxs-lookup"><span data-stu-id="c79eb-122">Use this method to get a single sample from the stream, as follows:</span></span>

1.  <span data-ttu-id="c79eb-123">Appelez **SetOneShot** avec la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="c79eb-123">Call **SetOneShot** with the value **TRUE**.</span></span>
2.  <span data-ttu-id="c79eb-124">Vous pouvez également utiliser l’interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) pour rechercher une position dans le flux.</span><span class="sxs-lookup"><span data-stu-id="c79eb-124">Optionally, use the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface to seek to a position in the stream.</span></span>
3.  <span data-ttu-id="c79eb-125">Appelez [**IMediaControl :: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) pour exécuter le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="c79eb-125">Call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the filter graph.</span></span>
4.  <span data-ttu-id="c79eb-126">Appelez [**IMediaEvent :: WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) pour attendre l’arrêt du graphique.</span><span class="sxs-lookup"><span data-stu-id="c79eb-126">Call [**IMediaEvent::WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) to wait for the graph to halt.</span></span> <span data-ttu-id="c79eb-127">Vous pouvez également appeler [**IMediaEvent :: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) pour obtenir les événements de graphique, jusqu’à ce que vous receviez l’événement [**ce \_ complet**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="c79eb-127">Alternatively, call [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) to get graph events, until you receive the [**EC\_COMPLETE**](ec-complete.md) event.</span></span>

<span data-ttu-id="c79eb-128">Après l’arrêt de la requête d’échantillonnage, le graphique de filtre est toujours en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c79eb-128">After the Sample Grabber halts, the filter graph is still in a running state.</span></span> <span data-ttu-id="c79eb-129">Vous pouvez rechercher ou suspendre le graphique pour obtenir un autre exemple.</span><span class="sxs-lookup"><span data-stu-id="c79eb-129">You can seek or pause the graph to get another sample.</span></span>

> [!Note]  
> <span data-ttu-id="c79eb-130">Une version antérieure de la documentation indiquait que le graphique de filtre s’arrête après la réception de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="c79eb-130">An earlier version of the documentation stated that the filter graph stops after the sample is received.</span></span> <span data-ttu-id="c79eb-131">Cela n’est pas exact.</span><span class="sxs-lookup"><span data-stu-id="c79eb-131">That is not accurate.</span></span> <span data-ttu-id="c79eb-132">Le flux se termine, mais le graphique reste à l’État en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c79eb-132">The stream ends, but the graph remains in the running state.</span></span>

 

<span data-ttu-id="c79eb-133">L’exemple d’accrochage implémente le mode à une seule capture en appelant [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sur le filtre en aval et en renvoyant S \_ false à partir de la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="c79eb-133">The Sample Grabber implements one-shot mode by calling [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on the downstream filter and returning S\_FALSE from the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method of it.</span></span>

> [!Note]  
> <span data-ttu-id="c79eb-134">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="c79eb-134">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c79eb-135">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c79eb-135">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c79eb-136">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c79eb-136">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c79eb-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c79eb-137">Requirements</span></span>



| <span data-ttu-id="c79eb-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c79eb-138">Requirement</span></span> | <span data-ttu-id="c79eb-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="c79eb-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c79eb-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="c79eb-140">Header</span></span><br/>  | <dl> <span data-ttu-id="c79eb-141"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c79eb-141"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c79eb-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c79eb-142">Library</span></span><br/> | <dl> <span data-ttu-id="c79eb-143"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c79eb-143"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c79eb-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c79eb-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c79eb-145">Utilisation de l’exemple d’accrochage</span><span class="sxs-lookup"><span data-stu-id="c79eb-145">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="c79eb-146">**Interface ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="c79eb-146">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




