---
description: Générateurs d’événements de média
ms.assetid: 2e003ad4-9fcb-4834-a335-e4969ffd3a00
title: Générateurs d’événements de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 125bf165740b0260f9131e0df8af420c8a669d97
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106544383"
---
# <a name="media-event-generators"></a><span data-ttu-id="35bf0-103">Générateurs d’événements de média</span><span class="sxs-lookup"><span data-stu-id="35bf0-103">Media Event Generators</span></span>

<span data-ttu-id="35bf0-104">Media Foundation offre un moyen cohérent aux objets d’envoyer des événements.</span><span class="sxs-lookup"><span data-stu-id="35bf0-104">Media Foundation provides a consistent way for objects to send events.</span></span> <span data-ttu-id="35bf0-105">Un objet peut utiliser des événements pour signaler l’achèvement d’une méthode asynchrone ou pour notifier l’application d’une modification de l’état de l’objet.</span><span class="sxs-lookup"><span data-stu-id="35bf0-105">An object can use events to signal the completion of an asynchronous method, or to notify the application about a change in the object's state.</span></span>

<span data-ttu-id="35bf0-106">Si un objet envoie des événements, il expose l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="35bf0-106">If an object sends events, it exposes the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="35bf0-107">Chaque fois que l’objet envoie un nouvel événement, l’événement est placé dans une file d’attente.</span><span class="sxs-lookup"><span data-stu-id="35bf0-107">Whenever the object sends a new event, the event is placed in a queue.</span></span> <span data-ttu-id="35bf0-108">L’application peut demander l’événement suivant à partir de la file d’attente en appelant l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="35bf0-108">The application can request the next event from the queue by calling one of the following methods:</span></span>

-   [<span data-ttu-id="35bf0-109">**IMFMediaEventGenerator :: GetEvent**</span><span class="sxs-lookup"><span data-stu-id="35bf0-109">**IMFMediaEventGenerator::GetEvent**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent)

-   [<span data-ttu-id="35bf0-110">**IMFMediaEventGenerator::BeginGetEvent**</span><span class="sxs-lookup"><span data-stu-id="35bf0-110">**IMFMediaEventGenerator::BeginGetEvent**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent)

<span data-ttu-id="35bf0-111">La méthode [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) est synchrone.</span><span class="sxs-lookup"><span data-stu-id="35bf0-111">The [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) method is synchronous.</span></span> <span data-ttu-id="35bf0-112">Si un événement se trouve déjà dans la file d’attente, la méthode est immédiatement retournée.</span><span class="sxs-lookup"><span data-stu-id="35bf0-112">If an event is already in the queue, the method returns immediately.</span></span> <span data-ttu-id="35bf0-113">S’il n’y a pas d’événement dans la file d’attente, la méthode échoue immédiatement ou se bloque jusqu’à ce que l’événement suivant soit mis en file d’attente, en fonction de l’indicateur que vous transmettez à **GetEvent**.</span><span class="sxs-lookup"><span data-stu-id="35bf0-113">If there is no event in the queue, the method either fails immediately, or blocks until the next event is queued, depending on which flag you pass into **GetEvent**.</span></span>

<span data-ttu-id="35bf0-114">La méthode [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) est asynchrone et ne bloque donc jamais.</span><span class="sxs-lookup"><span data-stu-id="35bf0-114">The [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method is asynchronous, so it never blocks.</span></span> <span data-ttu-id="35bf0-115">Cette méthode prend un pointeur vers l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , que l’application doit implémenter.</span><span class="sxs-lookup"><span data-stu-id="35bf0-115">This method takes a pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface, which the application must implement.</span></span> <span data-ttu-id="35bf0-116">Lorsque le rappel est appelé, l’application appelle [**IMFMediaEventGenerator :: EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) pour récupérer l’événement à partir de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="35bf0-116">When the callback is invoked, the application calls [**IMFMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) to get the event from the queue.</span></span> <span data-ttu-id="35bf0-117">Pour plus d’informations sur **IMFAsyncCallback**, consultez [méthodes de rappel asynchrones](asynchronous-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="35bf0-117">For more information about **IMFAsyncCallback**, see [Asynchronous Callback Methods](asynchronous-callback-methods.md).</span></span>

<span data-ttu-id="35bf0-118">Les événements sont représentés par l’interface [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .</span><span class="sxs-lookup"><span data-stu-id="35bf0-118">Events are represented by the [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) interface.</span></span> <span data-ttu-id="35bf0-119">Cette interface comprend les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="35bf0-119">This interface has the following methods:</span></span>

-   <span data-ttu-id="35bf0-120">[**GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype): récupère le type d’événement.</span><span class="sxs-lookup"><span data-stu-id="35bf0-120">[**GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype): Retrieves the event type.</span></span> <span data-ttu-id="35bf0-121">Le type d’événement indique ce qui s’est produit lors du déclenchement de l’événement.</span><span class="sxs-lookup"><span data-stu-id="35bf0-121">The event type indicates what happened to trigger the event.</span></span>

-   <span data-ttu-id="35bf0-122">[**GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus): récupère une valeur **HRESULT** indiquant si l’opération qui a déclenché l’événement a réussi.</span><span class="sxs-lookup"><span data-stu-id="35bf0-122">[**GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus): Retrieves an **HRESULT** value, indicating whether the operation that triggered the event was successful.</span></span> <span data-ttu-id="35bf0-123">Si une opération échoue de façon asynchrone, **GetStatus** retourne un code d’échec.</span><span class="sxs-lookup"><span data-stu-id="35bf0-123">If an operation fails asynchronously, **GetStatus** returns a failure code.</span></span>

-   <span data-ttu-id="35bf0-124">[**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue): récupère un **PROPVARIANT** qui contient les données d’événement.</span><span class="sxs-lookup"><span data-stu-id="35bf0-124">[**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue): Retrieves a **PROPVARIANT** that contains event data.</span></span> <span data-ttu-id="35bf0-125">Les données d’événement dépendent du type d’événement.</span><span class="sxs-lookup"><span data-stu-id="35bf0-125">The event data depends on the event type.</span></span> <span data-ttu-id="35bf0-126">Certains événements n’ont pas de données.</span><span class="sxs-lookup"><span data-stu-id="35bf0-126">Some events do not have any data.</span></span>

-   <span data-ttu-id="35bf0-127">[**GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype): récupère un **GUID**.</span><span class="sxs-lookup"><span data-stu-id="35bf0-127">[**GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype): Retrieves a **GUID**.</span></span> <span data-ttu-id="35bf0-128">Cette méthode s’applique à l' [événement MEExtendedType](meextendedtype.md)et fournit un moyen de définir des événements personnalisés.</span><span class="sxs-lookup"><span data-stu-id="35bf0-128">This method applies to the [MEExtendedType Event](meextendedtype.md), and provides a way to define custom events.</span></span>

<span data-ttu-id="35bf0-129">L’interface [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) hérite également de l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="35bf0-129">The [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) interface also inherits the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="35bf0-130">Certains événements contiennent des informations supplémentaires en tant qu’attributs.</span><span class="sxs-lookup"><span data-stu-id="35bf0-130">Some events carry additional information as attributes.</span></span>

<span data-ttu-id="35bf0-131">Pour obtenir la liste des types d’événements et leurs données et attributs associés, consultez [Media Foundation des événements](media-foundation-events.md).</span><span class="sxs-lookup"><span data-stu-id="35bf0-131">For a list of event types and their associated data and attributes, see [Media Foundation Events](media-foundation-events.md).</span></span>

## <a name="implementing-imfmediaeventgenerator"></a><span data-ttu-id="35bf0-132">Implémentation de IMFMediaEventGenerator</span><span class="sxs-lookup"><span data-stu-id="35bf0-132">Implementing IMFMediaEventGenerator</span></span>

<span data-ttu-id="35bf0-133">Si vous écrivez un composant de plug-in pour Media Foundation, tel qu’une source multimédia personnalisée ou un récepteur multimédia, vous devrez peut-être implémenter [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator).</span><span class="sxs-lookup"><span data-stu-id="35bf0-133">If you are writing a plug-in component for Media Foundation, such as a custom media source or media sink, you might need to implement [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator).</span></span> <span data-ttu-id="35bf0-134">Pour faciliter cette opération, Media Foundation fournit un objet d’assistance qui implémente une file d’attente d’événements.</span><span class="sxs-lookup"><span data-stu-id="35bf0-134">To make this easier, Media Foundation provides a helper object that implements an event queue.</span></span> <span data-ttu-id="35bf0-135">Créez la file d’attente d’événements en appelant la fonction [**MFCreateEventQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateeventqueue) .</span><span class="sxs-lookup"><span data-stu-id="35bf0-135">Create the event queue by calling the [**MFCreateEventQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateeventqueue) function.</span></span> <span data-ttu-id="35bf0-136">La file d’attente d’événements expose l’interface [**IMFMediaEventQueue**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue) .</span><span class="sxs-lookup"><span data-stu-id="35bf0-136">The event queue exposes the [**IMFMediaEventQueue**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue) interface.</span></span> <span data-ttu-id="35bf0-137">Dans l’implémentation de l’objet des méthodes **IMFMediaEventGenerator** , appelez la méthode correspondante sur la file d’attente d’événements.</span><span class="sxs-lookup"><span data-stu-id="35bf0-137">In your object's implementation of the **IMFMediaEventGenerator** methods, call the corresponding method on the event queue.</span></span>

<span data-ttu-id="35bf0-138">L’objet de file d’attente d’événements est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="35bf0-138">The event queue object is thread safe.</span></span> <span data-ttu-id="35bf0-139">Ne conservez jamais le même objet de section critique lors de l’appel de [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-getevent) et [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent), car **GetEvent** peut bloquer indéfiniment l’attente de [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent).</span><span class="sxs-lookup"><span data-stu-id="35bf0-139">Never hold the same critical section object when calling [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-getevent) and [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent), because **GetEvent** might block indefinitely waiting for [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent).</span></span> <span data-ttu-id="35bf0-140">Si vous conservez la même section critique pour les deux méthodes, cela provoque un interblocage.</span><span class="sxs-lookup"><span data-stu-id="35bf0-140">If you hold the same critical section for both methods, it will cause a deadlock.</span></span>

<span data-ttu-id="35bf0-141">Avant de libérer la file d’attente d’événements, appelez [**IMFMediaEventQueue :: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) pour libérer les ressources que l’objet contient.</span><span class="sxs-lookup"><span data-stu-id="35bf0-141">Before releasing the event queue, call [**IMFMediaEventQueue::Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) to release the resources that the object holds.</span></span>

<span data-ttu-id="35bf0-142">Lorsque votre objet doit déclencher un événement, appelez l’une des méthodes suivantes dans la file d’attente des événements :</span><span class="sxs-lookup"><span data-stu-id="35bf0-142">When your object needs to raise an event, call one of the following methods on the event queue:</span></span>

-   [<span data-ttu-id="35bf0-143">**IMFMediaEventQueue::QueueEvent**</span><span class="sxs-lookup"><span data-stu-id="35bf0-143">**IMFMediaEventQueue::QueueEvent**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent)

-   [<span data-ttu-id="35bf0-144">**IMFMediaEventQueue::QueueEventParamVar**</span><span class="sxs-lookup"><span data-stu-id="35bf0-144">**IMFMediaEventQueue::QueueEventParamVar**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamvar)

-   [<span data-ttu-id="35bf0-145">**IMFMediaEventQueue::QueueEventParamUnk**</span><span class="sxs-lookup"><span data-stu-id="35bf0-145">**IMFMediaEventQueue::QueueEventParamUnk**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamunk)

<span data-ttu-id="35bf0-146">Ces méthodes placent un nouvel événement dans la file d’attente et signalent tout appelant qui attend l’événement suivant.</span><span class="sxs-lookup"><span data-stu-id="35bf0-146">These methods put a new event on the queue and signal any caller that is waiting for the next event.</span></span>

<span data-ttu-id="35bf0-147">Le code suivant illustre une classe qui implémente [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) à l’aide de cet objet d’assistance.</span><span class="sxs-lookup"><span data-stu-id="35bf0-147">The following code shows a class that implements [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) using this helper object.</span></span> <span data-ttu-id="35bf0-148">Cette classe définit une méthode d' **arrêt** public qui arrête la file d’attente des événements et libère le pointeur de la file d’attente des événements.</span><span class="sxs-lookup"><span data-stu-id="35bf0-148">This class defines a public **Shutdown** method that shuts down the event queue and releases the event queue pointer.</span></span> <span data-ttu-id="35bf0-149">Ce comportement est courant pour les sources multimédias et les récepteurs multimédia, qui ont toujours une méthode **Shutdown** .</span><span class="sxs-lookup"><span data-stu-id="35bf0-149">This behavior would be typical for media sources and media sinks, which always have a **Shutdown** method.</span></span>


```C++
class MyObject : public IMFMediaEventGenerator
{
private:
    long                m_nRefCount;    // Reference count.
    CRITICAL_SECTION    m_critSec;      // Critical section.
    IMFMediaEventQueue *m_pQueue;       // Event queue.
    BOOL                m_bShutdown;    // Is the object shut down?

    // CheckShutdown: Returns MF_E_SHUTDOWN if the object was shut down.
    HRESULT CheckShutdown() const 
    {
        return (m_bShutdown? MF_E_SHUTDOWN : S_OK);
    }

public:
    MyObject(HRESULT &hr) : m_nRefCount(0), m_pQueue(NULL), m_bShutdown(FALSE)
    {
        InitializeCriticalSection(&m_critSec);
        
        // Create the event queue.
        hr = MFCreateEventQueue(&m_pQueue);
    }

    // Shutdown: Shuts down this object.
    HRESULT Shutdown()
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            // Shut down the event queue.
            if (m_pQueue)
            {
                hr = m_pQueue->Shutdown();
            }

            // Release the event queue.
            SAFE_RELEASE(m_pQueue);
            // Release any other objects owned by the class (not shown).

            // Set the shutdown flag.
            m_bShutdown = TRUE;
        }

        LeaveCriticalSection(&m_critSec);
        return hr;
    }

    // TODO: Implement IUnknown (not shown).
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);

    // IMFMediaEventGenerator::BeginGetEvent
    STDMETHODIMP BeginGetEvent(IMFAsyncCallback* pCallback, IUnknown* pState)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->BeginGetEvent(pCallback, pState);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;    
    }

    // IMFMediaEventGenerator::EndGetEvent
    STDMETHODIMP EndGetEvent(IMFAsyncResult* pResult, IMFMediaEvent** ppEvent)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->EndGetEvent(pResult, ppEvent);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;    
    }

    // IMFMediaEventGenerator::GetEvent
    STDMETHODIMP GetEvent(DWORD dwFlags, IMFMediaEvent** ppEvent)
    {
        // Because GetEvent can block indefinitely, it requires
        // a slightly different locking strategy.
        IMFMediaEventQueue *pQueue = NULL;

        // Hold lock.
        EnterCriticalSection(&m_critSec);

        // Check shutdown
        HRESULT hr = CheckShutdown();

        // Store the pointer in a local variable, so that another thread
        // does not release it after we leave the critical section.
        if (SUCCEEDED(hr))
        {
            pQueue = m_pQueue;
            pQueue->AddRef();
        }

        // Release the lock.
        LeaveCriticalSection(&m_critSec);

        if (SUCCEEDED(hr))
        {
            hr = pQueue->GetEvent(dwFlags, ppEvent);
        }

        SAFE_RELEASE(pQueue);
        return hr;
    }

    // IMFMediaEventGenerator::QueueEvent
    STDMETHODIMP QueueEvent(
        MediaEventType met, REFGUID extendedType, 
        HRESULT hrStatus, const PROPVARIANT* pvValue)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->QueueEventParamVar(
                met, extendedType, hrStatus, pvValue);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;
    }

private:

    // The destructor is private. The caller must call Release.
    virtual ~MyObject()
    {
        assert(m_bShutdown);
        assert(m_nRefCount == 0);
    }
};
```



## <a name="related-topics"></a><span data-ttu-id="35bf0-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="35bf0-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35bf0-151">API de plateforme Media Foundation</span><span class="sxs-lookup"><span data-stu-id="35bf0-151">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



