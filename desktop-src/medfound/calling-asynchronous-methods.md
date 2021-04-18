---
description: Appeler des méthodes asynchrones
ms.assetid: 1d8688a5-d476-457d-a0ad-e4f106ac3484
title: Appeler des méthodes asynchrones
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bdd6e272aeb3203706f0c621b4634cf3e6c0562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524644"
---
# <a name="calling-asynchronous-methods"></a><span data-ttu-id="02543-103">Appeler des méthodes asynchrones</span><span class="sxs-lookup"><span data-stu-id="02543-103">Calling Asynchronous Methods</span></span>

<span data-ttu-id="02543-104">Dans Media Foundation, de nombreuses opérations sont exécutées de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="02543-104">In Media Foundation, many operations are performed asynchronously.</span></span> <span data-ttu-id="02543-105">Les opérations asynchrones peuvent améliorer les performances, car elles ne bloquent pas le thread appelant.</span><span class="sxs-lookup"><span data-stu-id="02543-105">Asynchronous operations can improve performance, because they do not block the calling thread.</span></span> <span data-ttu-id="02543-106">Une opération asynchrone dans Media Foundation est définie par une paire de méthodes avec la Convention d’affectation de noms **Begin..** . et **end...**.</span><span class="sxs-lookup"><span data-stu-id="02543-106">An asynchronous operation in Media Foundation is defined by a pair of methods with the naming convention **Begin...** and **End....**.</span></span> <span data-ttu-id="02543-107">Ensemble, ces deux méthodes définissent une opération de lecture asynchrone sur le flux.</span><span class="sxs-lookup"><span data-stu-id="02543-107">Together, these two methods define an asynchronous read operation on the stream.</span></span>

<span data-ttu-id="02543-108">Pour démarrer une opération asynchrone, appelez la méthode **Begin** .</span><span class="sxs-lookup"><span data-stu-id="02543-108">To start an asynchronous operation, call the **Begin** method.</span></span> <span data-ttu-id="02543-109">La méthode **Begin** contient toujours au moins deux paramètres :</span><span class="sxs-lookup"><span data-stu-id="02543-109">The **Begin** method always contains at least two parameters:</span></span>

-   <span data-ttu-id="02543-110">Pointeur vers l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="02543-110">A pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> <span data-ttu-id="02543-111">L’application doit implémenter cette interface.</span><span class="sxs-lookup"><span data-stu-id="02543-111">The application must implement this interface.</span></span>
-   <span data-ttu-id="02543-112">Pointeur vers un objet d’État facultatif.</span><span class="sxs-lookup"><span data-stu-id="02543-112">A pointer to an optional state object.</span></span>

<span data-ttu-id="02543-113">L’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) avertit l’application lorsque l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="02543-113">The [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface notifies the application when the operation is completed.</span></span> <span data-ttu-id="02543-114">Pour obtenir un exemple d’implémentation de cette interface, consultez [implémentation du rappel asynchrone](implementing-the-asynchronous-callback.md).</span><span class="sxs-lookup"><span data-stu-id="02543-114">For an example of how to implement this interface, see [Implementing the Asynchronous Callback](implementing-the-asynchronous-callback.md).</span></span> <span data-ttu-id="02543-115">L’objet d’État est facultatif.</span><span class="sxs-lookup"><span data-stu-id="02543-115">The state object is optional.</span></span> <span data-ttu-id="02543-116">S’il est spécifié, il doit implémenter l’interface **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="02543-116">If specified, it must implement the **IUnknown** interface.</span></span> <span data-ttu-id="02543-117">Vous pouvez utiliser l’objet d’État pour stocker toutes les informations d’État requises par votre rappel.</span><span class="sxs-lookup"><span data-stu-id="02543-117">You can use the state object to store any state information that is needed by your callback.</span></span> <span data-ttu-id="02543-118">Si vous n’avez pas besoin d’informations d’État, vous pouvez définir ce paramètre sur la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="02543-118">If you do not need state information, you can set this parameter to **NULL**.</span></span> <span data-ttu-id="02543-119">La méthode **Begin** peut contenir des paramètres supplémentaires qui sont spécifiques à cette méthode.</span><span class="sxs-lookup"><span data-stu-id="02543-119">The **Begin** method might contain additional parameters that are specific to that method.</span></span>

<span data-ttu-id="02543-120">Si la méthode **Begin** retourne un code d’échec, cela signifie que l’opération a échoué immédiatement et que le rappel n’est pas appelé.</span><span class="sxs-lookup"><span data-stu-id="02543-120">If the **Begin** method returns a failure code, it means the operation has failed immediately, and the callback will not be invoked.</span></span> <span data-ttu-id="02543-121">Si la méthode **Begin** réussit, cela signifie que l’opération est en attente et que le rappel est appelé lorsque l’opération se termine.</span><span class="sxs-lookup"><span data-stu-id="02543-121">If the **Begin** method succeeds, it means the operation is pending, and the callback will be invoked when the operation completes.</span></span>

<span data-ttu-id="02543-122">Par exemple, la méthode [**IMFByteStream :: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) démarre une opération de lecture asynchrone sur un flux d’octets :</span><span class="sxs-lookup"><span data-stu-id="02543-122">For example, the [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) method starts an asynchronous read operation on a byte stream:</span></span>


```C++
    BYTE data[DATA_SIZE];
    ULONG cbRead = 0;

    CMyCallback *pCB = new (std::nothrow) CMyCallback(pStream, &hr);

    if (pCB == NULL)
    {
        hr = E_OUTOFMEMORY;
    }

    // Start an asynchronous request to read data.
    if (SUCCEEDED(hr))
    {
        hr = pStream->BeginRead(data, DATA_SIZE, pCB, NULL);
    }
```



<span data-ttu-id="02543-123">La méthode de rappel est [**IMFAsyncCallback :: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span><span class="sxs-lookup"><span data-stu-id="02543-123">The callback method is [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span></span> <span data-ttu-id="02543-124">Il possède un seul paramètre, *pAsyncResult*, qui est un pointeur vers l’interface [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) .</span><span class="sxs-lookup"><span data-stu-id="02543-124">It has a single parameter, *pAsyncResult*, which is a pointer to the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span> <span data-ttu-id="02543-125">Pour terminer l’opération asynchrone, appelez la méthode **end** qui correspond à la méthode **Begin** asynchrone.</span><span class="sxs-lookup"><span data-stu-id="02543-125">To complete the asynchronous operation, call the **End** method that matches the asynchronous **Begin** method.</span></span> <span data-ttu-id="02543-126">La méthode **end** prend toujours un pointeur **IMFAsyncResult** .</span><span class="sxs-lookup"><span data-stu-id="02543-126">The **End** method always takes an **IMFAsyncResult** pointer.</span></span> <span data-ttu-id="02543-127">Transmettez toujours le même pointeur que celui que vous avez reçu dans la méthode **Invoke** .</span><span class="sxs-lookup"><span data-stu-id="02543-127">Always pass in the same pointer that you received in the **Invoke** method.</span></span> <span data-ttu-id="02543-128">L’opération asynchrone n’est pas terminée tant que vous n’avez pas appelé la méthode **end** .</span><span class="sxs-lookup"><span data-stu-id="02543-128">The asynchronous operation is not complete until you call the **End** method.</span></span> <span data-ttu-id="02543-129">Vous pouvez appeler la méthode **end** à partir de la méthode **Invoke** , ou vous pouvez l’appeler à partir d’un autre thread.</span><span class="sxs-lookup"><span data-stu-id="02543-129">You may call the **End** method from inside the **Invoke** method, or you can call it from another thread.</span></span>

<span data-ttu-id="02543-130">Par exemple, pour terminer [**IMFByteStream :: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) sur un flux d’octets, appelez [**IMFByteStream :: EndRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endread):</span><span class="sxs-lookup"><span data-stu-id="02543-130">For example, to complete the [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) on a byte stream, call [**IMFByteStream::EndRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endread):</span></span>


```C++
    STDMETHODIMP Invoke(IMFAsyncResult* pResult)
    {
        m_hrStatus = m_pStream->EndRead(pResult, &m_cbRead);

        SetEvent(m_hEvent);

        return S_OK;
    }
```



<span data-ttu-id="02543-131">La valeur de retour de la méthode **end** indique l’état de l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="02543-131">The return value of the **End** method indicates the status of the asynchronous operation.</span></span> <span data-ttu-id="02543-132">Dans la plupart des cas, votre application effectue un travail après l’exécution de l’opération asynchrone, qu’elle se termine correctement ou non.</span><span class="sxs-lookup"><span data-stu-id="02543-132">In most cases, your application will perform some work after the asynchronous operation completes, whether it completes successfully or not.</span></span> <span data-ttu-id="02543-133">Vous disposez de plusieurs options :</span><span class="sxs-lookup"><span data-stu-id="02543-133">You have several options:</span></span>

-   <span data-ttu-id="02543-134">Effectuez le travail à l’intérieur de la méthode [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) .</span><span class="sxs-lookup"><span data-stu-id="02543-134">Do the work inside the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method.</span></span> <span data-ttu-id="02543-135">Cette approche est acceptable tant que votre application ne bloque jamais le thread appelant ou n’attend rien à l’intérieur de la méthode **Invoke** .</span><span class="sxs-lookup"><span data-stu-id="02543-135">This approach is acceptable as long as your application never blocks the calling thread or waits for anything inside the **Invoke** method.</span></span> <span data-ttu-id="02543-136">Si vous bloquez le thread appelant, vous risquez de bloquer le pipeline de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="02543-136">If you block the calling thread, you might block the streaming pipeline.</span></span> <span data-ttu-id="02543-137">Par exemple, vous pouvez mettre à jour certaines variables d’État, mais n’effectuez pas d’opération de lecture synchrone ou d’attente sur un objet Mutex.</span><span class="sxs-lookup"><span data-stu-id="02543-137">For example, you might update some state variables, but do not perform a synchronous read operation or wait on a mutex object.</span></span>
-   <span data-ttu-id="02543-138">Dans la méthode [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) , définissez un événement et retournez immédiatement.</span><span class="sxs-lookup"><span data-stu-id="02543-138">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, set an event and return immediately.</span></span> <span data-ttu-id="02543-139">Le thread appelant de l’application attend l’événement et effectue le travail lorsque l’événement est signalé.</span><span class="sxs-lookup"><span data-stu-id="02543-139">The application's calling thread waits for the event and does the work when the event is signaled.</span></span>
-   <span data-ttu-id="02543-140">Dans la méthode [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) , publiez un message de fenêtre privée dans la fenêtre de votre application et revenez immédiatement.</span><span class="sxs-lookup"><span data-stu-id="02543-140">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, post a private window message to your application window and return immediately.</span></span> <span data-ttu-id="02543-141">L’application effectue le travail sur sa boucle de message.</span><span class="sxs-lookup"><span data-stu-id="02543-141">The application does the work on its message loop.</span></span> <span data-ttu-id="02543-142">(Veillez à poster le message en appelant **PostMessage**, et non **SendMessage**, car **SendMessage** peut bloquer le thread de rappel.)</span><span class="sxs-lookup"><span data-stu-id="02543-142">(Make sure to post the message by calling **PostMessage**, not **SendMessage**, because **SendMessage** can block the callback thread.)</span></span>

<span data-ttu-id="02543-143">Il est important de se souvenir que [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) est appelé à partir d’un autre thread.</span><span class="sxs-lookup"><span data-stu-id="02543-143">It is important to remember that [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) is called from another thread.</span></span> <span data-ttu-id="02543-144">Votre application est chargée de s’assurer que tout travail effectué dans **Invoke** est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="02543-144">Your application is responsible for ensuring that any work performed inside **Invoke** is thread-safe.</span></span>

<span data-ttu-id="02543-145">Par défaut, le thread qui appelle [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) n’émet aucune hypothèse sur le comportement de votre objet de rappel.</span><span class="sxs-lookup"><span data-stu-id="02543-145">By default, the thread that calls [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) makes no assumptions about the behavior of your callback object.</span></span> <span data-ttu-id="02543-146">Si vous le souhaitez, vous pouvez implémenter la méthode [**IMFAsyncCallback :: GetParameters**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters) pour retourner des informations sur votre implémentation de rappel.</span><span class="sxs-lookup"><span data-stu-id="02543-146">Optionally, you can implement the [**IMFAsyncCallback::GetParameters**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters) method to return information about your callback implementation.</span></span> <span data-ttu-id="02543-147">Sinon, cette méthode peut retourner **E \_ NOTIMPL**:</span><span class="sxs-lookup"><span data-stu-id="02543-147">Otherwise, this method can return **E\_NOTIMPL**:</span></span>


```C++
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
```



<span data-ttu-id="02543-148">Si vous avez spécifié un objet d’État dans la méthode **Begin** , vous pouvez le récupérer à l’intérieur de votre méthode de rappel en appelant [**IMFAsyncResult :: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).</span><span class="sxs-lookup"><span data-stu-id="02543-148">If you specified a state object in the **Begin** method, you can retrieve it from inside your callback method by calling [**IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).</span></span>

## <a name="related-topics"></a><span data-ttu-id="02543-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="02543-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02543-150">Méthodes de rappel asynchrones</span><span class="sxs-lookup"><span data-stu-id="02543-150">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)
</dt> </dl>

 

 



