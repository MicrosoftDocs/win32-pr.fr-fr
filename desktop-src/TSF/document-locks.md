---
title: Verrous de document
description: Verrous de document
ms.assetid: 3c623c44-b0d3-4b03-8de9-25f1062b5726
keywords:
- Text Services Framework (TSF), verrous de document
- TSF (Text Services Framework), verrous de document
- Applications compatibles TSF, verrous de document
- verrous de document
- Text Services Framework (TSF), position caractère d’application (ACP)
- TSF (Text Services Framework), ACP (application Character position)
- Applications compatibles TSF, position de caractère d’application (ACP)
- Position du caractère d’application (ACP)
- ACP (position du caractère d’application)
- Text Services Framework (TSF), ancres
- TSF (Text Services Framework), ancres
- Applications compatibles TSF, ancres
- Points d’ancrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 438e22d7c77a45d798dfd6d5d7c43eaafa3e09c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196528"
---
# <a name="document-locks"></a><span data-ttu-id="ab47f-116">Verrous de document</span><span class="sxs-lookup"><span data-stu-id="ab47f-116">Document Locks</span></span>

## <a name="the-document-lock-protocol"></a><span data-ttu-id="ab47f-117">Protocole de verrouillage de document</span><span class="sxs-lookup"><span data-stu-id="ab47f-117">The Document Lock Protocol</span></span>

<span data-ttu-id="ab47f-118">Pour demander un verrou de document pour les applications basées sur ACP, le gestionnaire TSF appelle [ITextStoreACP :: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock).</span><span class="sxs-lookup"><span data-stu-id="ab47f-118">To request a document lock for ACP-based applications, the TSF manager calls [ITextStoreACP::RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock).</span></span> <span data-ttu-id="ab47f-119">Pour les applications basées sur l’ancre, le gestionnaire TSF appelle [ITextStoreAnchor :: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock).</span><span class="sxs-lookup"><span data-stu-id="ab47f-119">For anchor-based applications, the TSF manager calls [ITextStoreAnchor::RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock).</span></span> <span data-ttu-id="ab47f-120">L’application accorde le verrou de document en appelant [ITextStoreACPSink :: Onlockgranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted) (applications basées sur ACP) ou [ITextStoreAnchorSink :: Onlockgranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted) (applications basées sur une ancre) à l’intérieur de **RequestLock**.</span><span class="sxs-lookup"><span data-stu-id="ab47f-120">The application grants the document lock by calling [ITextStoreACPSink::OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted) (ACP-based applications) or [ITextStoreAnchorSink::OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted) (anchor-based applications) inside of **RequestLock**.</span></span> <span data-ttu-id="ab47f-121">Le verrou est uniquement valide pendant l’appel **Onlockgranted** .</span><span class="sxs-lookup"><span data-stu-id="ab47f-121">The lock is only valid during the **OnLockGranted** call.</span></span> <span data-ttu-id="ab47f-122">Quand **Onlockgranted** retourne, le document est considéré comme déverrouillé.</span><span class="sxs-lookup"><span data-stu-id="ab47f-122">When **OnLockGranted** returns, the document is considered unlocked.</span></span>

## <a name="types-of-document-locks"></a><span data-ttu-id="ab47f-123">Types de verrous de document</span><span class="sxs-lookup"><span data-stu-id="ab47f-123">Types of Document Locks</span></span>

<span data-ttu-id="ab47f-124">Il existe deux types de verrous de document, en lecture seule et en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ab47f-124">There are two types of document locks, read-only and read/write.</span></span> <span data-ttu-id="ab47f-125">Un verrou en lecture seule permet au responsable de lire le texte, mais il ne peut pas modifier ou insérer du texte.</span><span class="sxs-lookup"><span data-stu-id="ab47f-125">A read-only lock enables the manager to read the text, but it cannot modify or insert text.</span></span> <span data-ttu-id="ab47f-126">Un verrou en lecture/écriture permet au gestionnaire de lire, modifier et insérer du texte.</span><span class="sxs-lookup"><span data-stu-id="ab47f-126">A read/write lock enables the manager to read, modify, and insert text.</span></span> <span data-ttu-id="ab47f-127">Un verrou en lecture seule est demandé en spécifiant le saut de la variable TS \_ \_ lu dans *dwFlags*.</span><span class="sxs-lookup"><span data-stu-id="ab47f-127">A read-only lock is requested by specifying TS\_LF\_READ in *dwFlags*.</span></span> <span data-ttu-id="ab47f-128">Un verrou en lecture/écriture est demandé en spécifiant TS \_ LF \_ ReadWrite dans *dwFlags*.</span><span class="sxs-lookup"><span data-stu-id="ab47f-128">A read/write lock is requested by specifying TS\_LF\_READWRITE in *dwFlags*.</span></span>

## <a name="asynchronous-and-synchronous-requests"></a><span data-ttu-id="ab47f-129">Requêtes asynchrones et synchrones</span><span class="sxs-lookup"><span data-stu-id="ab47f-129">Asynchronous and Synchronous Requests</span></span>

<span data-ttu-id="ab47f-130">Une demande de verrouillage peut être synchrone ou asynchrone.</span><span class="sxs-lookup"><span data-stu-id="ab47f-130">A lock request can be either synchronous or asynchronous.</span></span> <span data-ttu-id="ab47f-131">Le gestionnaire demande un verrou synchrone à l’aide de \_ l' \_ indicateur de synchronisation TS LF dans *dwFlags*.</span><span class="sxs-lookup"><span data-stu-id="ab47f-131">The manager requests a synchronous lock by using the TS\_LF\_SYNC flag in *dwFlags*.</span></span> <span data-ttu-id="ab47f-132">Si cet indicateur n’est pas présent, la demande est asynchrone.</span><span class="sxs-lookup"><span data-stu-id="ab47f-132">If this flag is not present, the request is asynchronous.</span></span>

## <a name="granting-the-lock"></a><span data-ttu-id="ab47f-133">Octroi du verrou</span><span class="sxs-lookup"><span data-stu-id="ab47f-133">Granting the Lock</span></span>

<span data-ttu-id="ab47f-134">Quand **RequestLock** est appelé, l’application doit déterminer si le document est actuellement verrouillé.</span><span class="sxs-lookup"><span data-stu-id="ab47f-134">When **RequestLock** is called, the application must determine if the document is currently locked.</span></span> <span data-ttu-id="ab47f-135">Si le document n’est pas verrouillé et qu’il n’existe aucune autre raison pour refuser le verrou, l’application doit définir *phrSession* sur S \_ OK et retourner s \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ab47f-135">If the document is not locked, and no other reason to deny the lock exists, the application should set *phrSession* to S\_OK and return S\_OK.</span></span>

<span data-ttu-id="ab47f-136">Si le document est verrouillé et que la demande de verrou est synchrone, l’application doit définir *phrSession* sur TS \_ E \_ Synchronous et retourner \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ab47f-136">If the document is locked and the lock request is synchronous, the application should set *phrSession* to TS\_E\_SYNCHRONOUS and return S\_OK.</span></span> <span data-ttu-id="ab47f-137">Cela indique qu’une demande synchrone ne peut pas être accordée.</span><span class="sxs-lookup"><span data-stu-id="ab47f-137">This indicates that a synchronous request cannot be granted.</span></span>

<span data-ttu-id="ab47f-138">Si le document est verrouillé et que la demande de verrou est asynchrone, l’application doit mettre la demande en file d’attente, définir *phrSession* sur TS \_ S \_ Async et retourner s \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ab47f-138">If the document is locked and the lock request is asynchronous, the application should queue the request, set *phrSession* to TS\_S\_ASYNC and return S\_OK.</span></span> <span data-ttu-id="ab47f-139">Lorsque le document devient disponible, l’application doit supprimer la demande de la file d’attente et appeler **Onlockgranted**.</span><span class="sxs-lookup"><span data-stu-id="ab47f-139">When the document becomes available, the application should remove the request from the queue and call **OnLockGranted**.</span></span> <span data-ttu-id="ab47f-140">Cette mise en file d’attente des demandes de verrou est facultative. une application doit prendre en charge un scénario.</span><span class="sxs-lookup"><span data-stu-id="ab47f-140">This queuing of lock requests is optional; there is one scenario that an application must support.</span></span> <span data-ttu-id="ab47f-141">Si le document a un verrou en lecture seule, la nouvelle demande de verrou est en lecture/écriture et la demande est asynchrone, l’application a appelé **Onlockgranted** , ce qui a provoqué un appel réentrant à **RequestLock**.</span><span class="sxs-lookup"><span data-stu-id="ab47f-141">If the document has a read-only lock, the new lock request is read/write and the request is asynchronous, the application has called into **OnLockGranted** , which has caused a reentrant call to **RequestLock**.</span></span> <span data-ttu-id="ab47f-142">L’application doit définir *phrSession* sur TS \_ s \_ Async et retourner s \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ab47f-142">The application should set *phrSession* to TS\_S\_ASYNC and return S\_OK.</span></span> <span data-ttu-id="ab47f-143">Une fois que l’appel à **Onlockgranted** a été retourné, l’application doit traiter la demande de mise à niveau en appelant à nouveau **Onlockgranted** avec TS \_ LF \_ ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="ab47f-143">After the call to **OnLockGranted** returns, the application should process the upgrade request by calling **OnLockGranted** again with TS\_LF\_READWRITE.</span></span>

## <a name="lock-enforcement"></a><span data-ttu-id="ab47f-144">Application de verrous</span><span class="sxs-lookup"><span data-stu-id="ab47f-144">Lock Enforcement</span></span>

<span data-ttu-id="ab47f-145">L’application doit s’assurer que le type de verrou approprié existe avant d’autoriser l’accès au document.</span><span class="sxs-lookup"><span data-stu-id="ab47f-145">The application must ensure that the proper type of lock exists before allowing access to the document.</span></span> <span data-ttu-id="ab47f-146">Par exemple, l’application doit vérifier qu’un document a au moins un verrou en lecture seule avant d’autoriser [ITextStoreACP :: gettext](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext) ou [ITextStoreAnchor :: gettext](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) à continuer.</span><span class="sxs-lookup"><span data-stu-id="ab47f-146">For example, the application should verify that a document has at least a read-only lock before allowing [ITextStoreACP::GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext) or [ITextStoreAnchor::GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) to proceed.</span></span> <span data-ttu-id="ab47f-147">Si le verrou approprié n’existe pas, l’application doit retourner TF \_ E \_ NOLOCK.</span><span class="sxs-lookup"><span data-stu-id="ab47f-147">If the proper lock does not exist, the application should return TF\_E\_NOLOCK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab47f-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ab47f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab47f-149">Magasins de texte</span><span class="sxs-lookup"><span data-stu-id="ab47f-149">Text Stores</span></span>](text-stores.md)
</dt> <dt>

[<span data-ttu-id="ab47f-150">ITextStoreACP :: RequestLock</span><span class="sxs-lookup"><span data-stu-id="ab47f-150">ITextStoreACP::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[<span data-ttu-id="ab47f-151">ITextStoreACPSink :: OnLockGranted</span><span class="sxs-lookup"><span data-stu-id="ab47f-151">ITextStoreACPSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[<span data-ttu-id="ab47f-152">ITextStoreACP :: GetText</span><span class="sxs-lookup"><span data-stu-id="ab47f-152">ITextStoreACP::GetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext)
</dt> <dt>

[<span data-ttu-id="ab47f-153">ITextStoreAnchor :: RequestLock</span><span class="sxs-lookup"><span data-stu-id="ab47f-153">ITextStoreAnchor::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[<span data-ttu-id="ab47f-154">ITextStoreAnchorSink :: OnLockGranted</span><span class="sxs-lookup"><span data-stu-id="ab47f-154">ITextStoreAnchorSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> <dt>

[<span data-ttu-id="ab47f-155">ITextStoreAnchor :: GetText</span><span class="sxs-lookup"><span data-stu-id="ab47f-155">ITextStoreAnchor::GetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext)
</dt> </dl>

 

 




