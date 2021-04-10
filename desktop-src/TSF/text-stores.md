---
title: Magasins de texte
description: Magasins de texte
ms.assetid: c827999a-0b74-4e5d-901e-4c2fa1d74929
keywords:
- Text Services Framework (TSF), magasins de texte
- TSF (Text Services Framework), magasins de texte
- Applications compatibles TSF, magasins de texte
- magasins de texte
- Text Services Framework (TSF), position caractère d’application (ACP)
- TSF (Text Services Framework), ACP (application Character position)
- Applications compatibles TSF, position de caractère d’application (ACP)
- Position du caractère d’application (ACP)
- ACP (position du caractère d’application)
- Text Services Framework (TSF), ancres
- TSF (Text Services Framework), ancres
- Applications compatibles TSF, ancres
- Points d’ancrage
- Text Services Framework (TSF), verrous de document
- TSF (Text Services Framework), verrous de document
- Applications compatibles TSF, verrous de document
- verrous de document
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1234f71fa799cf911ff7ede89915068f69417a00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031430"
---
# <a name="text-stores"></a><span data-ttu-id="8f72f-120">Magasins de texte</span><span class="sxs-lookup"><span data-stu-id="8f72f-120">Text Stores</span></span>

## <a name="application-character-position-acp"></a><span data-ttu-id="8f72f-121">Position du caractère d’application (ACP)</span><span class="sxs-lookup"><span data-stu-id="8f72f-121">Application Character Position (ACP)</span></span>

<span data-ttu-id="8f72f-122">Un ACP est l’emplacement d’un ou de plusieurs caractères dans un flux de texte exprimé sous la forme du nombre de caractères à partir du début du flux de texte.</span><span class="sxs-lookup"><span data-stu-id="8f72f-122">An ACP is the location of a character, or characters, in a text stream that is expressed as the number of characters from the start of the text stream.</span></span> <span data-ttu-id="8f72f-123">Étant donné que le modèle ACP est de base zéro, le premier caractère d’un flux de texte a un ACP égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="8f72f-123">Because the ACP model is zero-based, the first character in a text stream has an ACP of zero.</span></span> <span data-ttu-id="8f72f-124">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="8f72f-124">For example:</span></span>


```C++
Text Stream  H | e | l | l | o |   | W | o | r | l | d
ACP          0   1   2   3   4   5   6   7   8   9   10
```



<span data-ttu-id="8f72f-125">Un magasin de texte implémente un objet qui prend en charge l’interface [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) , ce qui permet d’exprimer le flux de texte dans un ACP.</span><span class="sxs-lookup"><span data-stu-id="8f72f-125">A text store implements an object that supports the [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) interface, which enables the text stream to be expressed in an ACP.</span></span> <span data-ttu-id="8f72f-126">Les méthodes d’interface **ITextStoreACP** utilisent la plage ACP du flux de texte pour modifier le texte.</span><span class="sxs-lookup"><span data-stu-id="8f72f-126">The **ITextStoreACP** interface methods use the ACP range of the text stream to modify the text.</span></span>

## <a name="anchor-based-applications"></a><span data-ttu-id="8f72f-127">Applications Anchor-Based</span><span class="sxs-lookup"><span data-stu-id="8f72f-127">Anchor-Based Applications</span></span>

<span data-ttu-id="8f72f-128">Le gestionnaire utilise les méthodes basées sur ACP en mode natif pour manipuler du texte.</span><span class="sxs-lookup"><span data-stu-id="8f72f-128">The manager uses the ACP-based methods natively to manipulate text.</span></span> <span data-ttu-id="8f72f-129">Toutefois, une approche basée sur l’ancre est disponible pour les clients [Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md) qui prennent en charge les [ancres](ranges.md), où le gestionnaire utilise les méthodes [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) et [ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink) pour encapsuler les méthodes [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) et [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) .</span><span class="sxs-lookup"><span data-stu-id="8f72f-129">However, an anchor-based approach is available for [Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md) clients that support [anchors](ranges.md), whereby the manager uses [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) and [ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink) methods to wrap the [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) and [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) methods.</span></span>

## <a name="document-access-control"></a><span data-ttu-id="8f72f-130">Access Control de documents</span><span class="sxs-lookup"><span data-stu-id="8f72f-130">Document Access Control</span></span>

<span data-ttu-id="8f72f-131">Le magasin de texte contrôle l’accès au flux de texte à l’aide de [verrous de document](document-locks.md).</span><span class="sxs-lookup"><span data-stu-id="8f72f-131">The text store controls access to the text stream by using [document locks](document-locks.md).</span></span> <span data-ttu-id="8f72f-132">Pour lire ou modifier le magasin de texte, le gestionnaire doit d’abord installer un récepteur de notifications qui prend en charge l’interface [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) en appelant la méthode [ITextStoreACP :: AdviseSink](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-advisesink) et en passant un pointeur vers un récepteur de notifications.</span><span class="sxs-lookup"><span data-stu-id="8f72f-132">To read or modify the text store, the manager must first install an advise sink that supports the [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) interface by calling the [ITextStoreACP::AdviseSink](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-advisesink) method and passing a pointer to an advise sink.</span></span> <span data-ttu-id="8f72f-133">Le récepteur de notifications permet au gestionnaire d’obtenir des verrous de document sur le magasin de texte et de recevoir des notifications lorsque le magasin de texte est modifié par un autre nom que le gestionnaire, tel que l’entrée d’utilisateur via l’application.</span><span class="sxs-lookup"><span data-stu-id="8f72f-133">The advise sink enables the manager to obtain a document locks on the text store and receive notifications when the text store is modified by something other than the manager, such as user input through the application.</span></span> <span data-ttu-id="8f72f-134">Les récepteurs de notification sont décrits plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="8f72f-134">Advise sinks are discussed later in this topic.</span></span>

## <a name="how-to-initialize-the-text-store"></a><span data-ttu-id="8f72f-135">Comment initialiser le magasin de texte</span><span class="sxs-lookup"><span data-stu-id="8f72f-135">How To Initialize the Text Store</span></span>

<span data-ttu-id="8f72f-136">Une application Initialise un magasin de texte en effectuant les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8f72f-136">An application initializes a text store by completing the following steps:</span></span>

1.  <span data-ttu-id="8f72f-137">Créez un objet de gestionnaire de threads basé sur l’interface [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) en appelant la fonction [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) avec un pointeur vers un objet de gestionnaire de threads.</span><span class="sxs-lookup"><span data-stu-id="8f72f-137">Create a thread manager object based on the [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) interface by calling the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function with a pointer to a thread manager object.</span></span> <span data-ttu-id="8f72f-138">L’exemple de code suivant illustre l’implémentation d’un objet de gestionnaire de threads.</span><span class="sxs-lookup"><span data-stu-id="8f72f-138">The following is a code example of implementing a thread manager object.</span></span>
    ```C++
    hr = CoCreateInstance (CLSID_TF_ThreadMgr, NULL, CLSCTX_INPROC_SERVER, 
                            IID_ITfThreadMgr, (void**)&pThreadMgr);
    ```

    

2.  <span data-ttu-id="8f72f-139">Activez l’objet de gestionnaire de threads en appelant la méthode [ITfThreadMgr :: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) .</span><span class="sxs-lookup"><span data-stu-id="8f72f-139">Activate the thread manager object by calling the [ITfThreadMgr::Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) method.</span></span> <span data-ttu-id="8f72f-140">Cette méthode fournit un pointeur vers un [identificateur client](tfclientid.md) utilisé pour créer un objet de contexte.</span><span class="sxs-lookup"><span data-stu-id="8f72f-140">This method supplies a pointer to a [client identifier](tfclientid.md) used to create a context object.</span></span> <span data-ttu-id="8f72f-141">Le gestionnaire de thread est utilisé pour implémenter un objet du gestionnaire de documents.</span><span class="sxs-lookup"><span data-stu-id="8f72f-141">The thread manager is used to implement a document manager object.</span></span>
3.  <span data-ttu-id="8f72f-142">Créez un objet de gestionnaire de documents basé sur l’interface [ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) en appelant la méthode [ITfThreadMgr :: CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr) avec un pointeur vers l’objet du gestionnaire de documents.</span><span class="sxs-lookup"><span data-stu-id="8f72f-142">Create a document manager object based on the [ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) interface by calling the [ITfThreadMgr::CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr) method with a pointer to the document manager object.</span></span> <span data-ttu-id="8f72f-143">L’objet du gestionnaire de documents est utilisé pour implémenter un objet de contexte qui est le magasin de texte.</span><span class="sxs-lookup"><span data-stu-id="8f72f-143">The document manager object is used to implement a context object that is the text store.</span></span>
4.  <span data-ttu-id="8f72f-144">Créez un objet de contexte à partir du gestionnaire de documents en appelant la méthode [ITfDocumentMgr :: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext) avec le pointeur vers l’objet de magasin de texte et un pointeur vers l’identificateur de client à partir de l’activation du gestionnaire de thread.</span><span class="sxs-lookup"><span data-stu-id="8f72f-144">Create a context object from the document manager by calling the [ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext) method with the pointer to the text store object and a pointer to the client identifier from activating the thread manager.</span></span> <span data-ttu-id="8f72f-145">Voici un exemple de création d’un objet de contexte :</span><span class="sxs-lookup"><span data-stu-id="8f72f-145">The following is an example of creating a context object:</span></span>
    ```C++
    hr = pDocumentMgr->CreateContext(m_ClientID, 0, (ITextStoreACP*)this, 
                                    &pContext, pEditCookie);
    ```

    

5.  <span data-ttu-id="8f72f-146">Exécute un push de l’objet Context sur la pile avec la méthode [ITfDocumentMgr ::P par émission](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-push) .</span><span class="sxs-lookup"><span data-stu-id="8f72f-146">Push the context object onto the stack with the [ITfDocumentMgr::Push](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-push) method.</span></span> <span data-ttu-id="8f72f-147">Voici un exemple de transmission de l’objet de contexte sur la pile :</span><span class="sxs-lookup"><span data-stu-id="8f72f-147">The following is an example of pushing the context object onto the stack:</span></span>
    ```C++
    hr = pDocumentMgr->Push(pContext);
    ```

    

## <a name="how-to-modify-the-text-store"></a><span data-ttu-id="8f72f-148">Comment modifier le magasin de texte</span><span class="sxs-lookup"><span data-stu-id="8f72f-148">How To Modify the Text Store</span></span>

<span data-ttu-id="8f72f-149">La méthode **ITfDocumentMgr ::P par émission** appelle **ITextStoreACP :: AdviseSink** avec un pointeur vers l’interface du récepteur de notifications pour installer un nouveau récepteur de notifications ou modifier un récepteur de notifications existant.</span><span class="sxs-lookup"><span data-stu-id="8f72f-149">The **ITfDocumentMgr::Push** method calls **ITextStoreACP::AdviseSink** with a pointer to the advise sink interface to install a new advise sink or modify an existing advise sink.</span></span> <span data-ttu-id="8f72f-150">Le récepteur de notifications reçoit des notifications lorsque le magasin de texte est modifié par un autre nom que le gestionnaire, tel que l’entrée d’utilisateur dans l’application.</span><span class="sxs-lookup"><span data-stu-id="8f72f-150">The advise sink receives notifications when the text store is modified by something other than the manager, such as user input to the application.</span></span> <span data-ttu-id="8f72f-151">Les applications doivent appeler la méthode [ITfThreadMgrEventSink :: OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus) lorsque la méthode d’entrée obtient le focus.</span><span class="sxs-lookup"><span data-stu-id="8f72f-151">Applications must call the [ITfThreadMgrEventSink::OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus) method when the input method obtains the focus.</span></span> <span data-ttu-id="8f72f-152">D’autres notifications au gestionnaire de thread sont fournies en appelant les méthodes d’interface **ITextStoreACPSink** appropriées.</span><span class="sxs-lookup"><span data-stu-id="8f72f-152">Other notifications to the thread manager are provided by calling to the appropriate **ITextStoreACPSink** interface methods.</span></span>

<span data-ttu-id="8f72f-153">Toutefois, les applications ne doivent pas appeler les méthodes de l’interface **ITextStoreACPSink** en réponse aux méthodes de l’interface **ITextStoreACP** .</span><span class="sxs-lookup"><span data-stu-id="8f72f-153">However, applications should not call the **ITextStoreACPSink** interface methods in response to **ITextStoreACP** interface methods.</span></span> <span data-ttu-id="8f72f-154">Les applications doivent uniquement appeler les méthodes d’interface **ITextStoreACPSink** lorsque le magasin de texte est modifié par un autre nom que le responsable.</span><span class="sxs-lookup"><span data-stu-id="8f72f-154">Applications should only call **ITextStoreACPSink** interface methods when the text store is modified by something other than the manager.</span></span>

<span data-ttu-id="8f72f-155">Le contenu du magasin de texte peut être modifié à l’aide d’un état d’entrée temporaire appelé [composition](compositions.md).</span><span class="sxs-lookup"><span data-stu-id="8f72f-155">The contents of the text store can be modified with a temporary input state called a [composition](compositions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f72f-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8f72f-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f72f-157">Ancres</span><span class="sxs-lookup"><span data-stu-id="8f72f-157">Anchors</span></span>](ranges.md)
</dt> <dt>

[<span data-ttu-id="8f72f-158">Position</span><span class="sxs-lookup"><span data-stu-id="8f72f-158">Compositions</span></span>](compositions.md)
</dt> <dt>

[<span data-ttu-id="8f72f-159">Verrous de document</span><span class="sxs-lookup"><span data-stu-id="8f72f-159">Document Locks</span></span>](document-locks.md)
</dt> <dt>

[<span data-ttu-id="8f72f-160">ITextStoreACPSink</span><span class="sxs-lookup"><span data-stu-id="8f72f-160">ITextStoreACPSink</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink)
</dt> <dt>

[<span data-ttu-id="8f72f-161">ITextStoreACP</span><span class="sxs-lookup"><span data-stu-id="8f72f-161">ITextStoreACP</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[<span data-ttu-id="8f72f-162">ITextStoreAnchor</span><span class="sxs-lookup"><span data-stu-id="8f72f-162">ITextStoreAnchor</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor)
</dt> <dt>

[<span data-ttu-id="8f72f-163">ITextStoreAnchorSink</span><span class="sxs-lookup"><span data-stu-id="8f72f-163">ITextStoreAnchorSink</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink)
</dt> <dt>

[<span data-ttu-id="8f72f-164">ITfDocumentMgr</span><span class="sxs-lookup"><span data-stu-id="8f72f-164">ITfDocumentMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[<span data-ttu-id="8f72f-165">ITfThreadMgr</span><span class="sxs-lookup"><span data-stu-id="8f72f-165">ITfThreadMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[<span data-ttu-id="8f72f-166">ITfThreadMgrEventSink :: OnSetFocus</span><span class="sxs-lookup"><span data-stu-id="8f72f-166">ITfThreadMgrEventSink::OnSetFocus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus)
</dt> <dt>

[<span data-ttu-id="8f72f-167">TfClientId</span><span class="sxs-lookup"><span data-stu-id="8f72f-167">TfClientId</span></span>](tfclientid.md)
</dt> <dt>

[<span data-ttu-id="8f72f-168">Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="8f72f-168">Microsoft Active Accessibility</span></span>](../winauto/microsoft-active-accessibility.md)
</dt> </dl>

 

 