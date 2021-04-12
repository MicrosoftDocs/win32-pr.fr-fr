---
description: Définit un rappel qui crée la session de média PMP pendant la résolution de la source.
ms.assetid: 7277C5E0-BB91-4EEA-9529-64E66D179CDC
title: MFPKEY_PMP_Creation_Callback, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2b18e04a15e035a9e4dc04a4039ce230342031a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202340"
---
# <a name="mfpkey_pmp_creation_callback-property"></a><span data-ttu-id="58608-103">\_Propriété de \_ rappel de création PMP MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="58608-103">MFPKEY\_PMP\_Creation\_Callback property</span></span>

<span data-ttu-id="58608-104">Définit un rappel qui crée la [session de média PMP](pmp-media-session.md) pendant la résolution de la source.</span><span class="sxs-lookup"><span data-stu-id="58608-104">Sets a callback that creates the [PMP Media Session](pmp-media-session.md) during source resolution.</span></span>



<span data-ttu-id="58608-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="58608-105">Data type</span></span>

<span data-ttu-id="58608-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="58608-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="58608-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="58608-107">PROPVARIANT member</span></span>

<span data-ttu-id="58608-108">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="58608-108">\**IUnknown\** _</span></span>

<span data-ttu-id="58608-109">VT \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="58608-109">VT\_UNKNOWN</span></span>

<span data-ttu-id="58608-110">_ *punkVal*\*</span><span class="sxs-lookup"><span data-stu-id="58608-110">_ *punkVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="58608-111">Notes</span><span class="sxs-lookup"><span data-stu-id="58608-111">Remarks</span></span>

<span data-ttu-id="58608-112">Certains contenus protégés peuvent nécessiter l’utilisation de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="58608-112">Some protected content might require the use of this property.</span></span> <span data-ttu-id="58608-113">Dans ce cas, le processus de résolution source échoue avec le code d’erreur **MF \_ E \_ Resolution \_ requiert un \_ \_ \_ rappel de création PMP**.</span><span class="sxs-lookup"><span data-stu-id="58608-113">If so, the source resolution process fails with the error code **MF\_E\_RESOLUTION\_REQUIRES\_PMP\_CREATION\_CALLBACK**.</span></span>

<span data-ttu-id="58608-114">Pour utiliser cette propriété, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="58608-114">To use this property, do the following.</span></span>

1.  <span data-ttu-id="58608-115">Appelez [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) pour créer une banque de propriétés.</span><span class="sxs-lookup"><span data-stu-id="58608-115">Call [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) to create a property store.</span></span>
2.  <span data-ttu-id="58608-116">Implémentez l’interface de rappel [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="58608-116">Implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) callback interface.</span></span>
3.  <span data-ttu-id="58608-117">Définissez la \_ \_ \_ propriété de rappel de création MFPKEY PMP sur la Banque de propriétés.</span><span class="sxs-lookup"><span data-stu-id="58608-117">Set the MFPKEY\_PMP\_Creation\_Callback property on the property store.</span></span> <span data-ttu-id="58608-118">La valeur est un pointeur vers l’implémentation de [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="58608-118">The value is a pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) implementation.</span></span>
4.  <span data-ttu-id="58608-119">Appelez [**IMFSourceResolver :: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span><span class="sxs-lookup"><span data-stu-id="58608-119">Call [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span></span> <span data-ttu-id="58608-120">Transmettez un pointeur vers la Banque de propriétés dans le paramètre *pProps* .</span><span class="sxs-lookup"><span data-stu-id="58608-120">Pass in a pointer to the property store in the *pProps* parameter.</span></span>

<span data-ttu-id="58608-121">Dans la méthode [**IMFAsyncCallback :: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) de votre interface de rappel, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="58608-121">In the [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method of your callback interface, do the following.</span></span>

1.  <span data-ttu-id="58608-122">Appelez [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) pour créer la [session de média PMP](pmp-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="58608-122">Call [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) to create the [PMP Media Session](pmp-media-session.md).</span></span>
2.  <span data-ttu-id="58608-123">Appelez [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) sur la session de média PMP sur un pointeur vers l’interface [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) .</span><span class="sxs-lookup"><span data-stu-id="58608-123">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the PMP Media Session to a pointer to the [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) interface.</span></span>
3.  <span data-ttu-id="58608-124">Appelez [**IMFAsyncResult :: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate) sur l’objet de résultat qui est passé dans le paramètre *pAsyncResult* de [**IMFAsyncCallback :: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span><span class="sxs-lookup"><span data-stu-id="58608-124">Call [**IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate) on the result object that is passed in the *pAsyncResult* parameter of [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span></span> <span data-ttu-id="58608-125">Interrogez le pointeur [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) retourné pour l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="58608-125">Query the returned [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer for the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
4.  <span data-ttu-id="58608-126">Appelez [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="58608-126">Call [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) with the following parameters:</span></span>
    -   <span data-ttu-id="58608-127">*dwQueue*: **\_ \_ file d’attente \_ de rappel MFASYNC standard**</span><span class="sxs-lookup"><span data-stu-id="58608-127">*dwQueue*: **MFASYNC\_CALLBACK\_QUEUE\_STANDARD**</span></span>
    -   <span data-ttu-id="58608-128">*pCallback*: pointeur [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) obtenu à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="58608-128">*pCallback*: The [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) pointer obtained in step 3.</span></span>
    -   <span data-ttu-id="58608-129">*pState*: pointeur [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) obtenu à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="58608-129">*pState*: The [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) pointer obtained in step 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="58608-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58608-130">Requirements</span></span>



| <span data-ttu-id="58608-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58608-131">Requirement</span></span> | <span data-ttu-id="58608-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="58608-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="58608-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58608-133">Minimum supported client</span></span><br/> | <span data-ttu-id="58608-134">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="58608-134">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="58608-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58608-135">Minimum supported server</span></span><br/> | <span data-ttu-id="58608-136">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="58608-136">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="58608-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="58608-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="58608-138"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="58608-138"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58608-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58608-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58608-140">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="58608-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="58608-141">Session média PMP</span><span class="sxs-lookup"><span data-stu-id="58608-141">PMP Media Session</span></span>](pmp-media-session.md)
</dt> <dt>

[<span data-ttu-id="58608-142">Chemin du média protégé</span><span class="sxs-lookup"><span data-stu-id="58608-142">Protected Media Path</span></span>](protected-media-path.md)
</dt> <dt>

[<span data-ttu-id="58608-143">Résolveur source</span><span class="sxs-lookup"><span data-stu-id="58608-143">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 
