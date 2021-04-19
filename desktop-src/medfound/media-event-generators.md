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
# <a name="media-event-generators"></a>Générateurs d’événements de média

Media Foundation offre un moyen cohérent aux objets d’envoyer des événements. Un objet peut utiliser des événements pour signaler l’achèvement d’une méthode asynchrone ou pour notifier l’application d’une modification de l’état de l’objet.

Si un objet envoie des événements, il expose l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Chaque fois que l’objet envoie un nouvel événement, l’événement est placé dans une file d’attente. L’application peut demander l’événement suivant à partir de la file d’attente en appelant l’une des méthodes suivantes :

-   [**IMFMediaEventGenerator :: GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent)

-   [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent)

La méthode [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) est synchrone. Si un événement se trouve déjà dans la file d’attente, la méthode est immédiatement retournée. S’il n’y a pas d’événement dans la file d’attente, la méthode échoue immédiatement ou se bloque jusqu’à ce que l’événement suivant soit mis en file d’attente, en fonction de l’indicateur que vous transmettez à **GetEvent**.

La méthode [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) est asynchrone et ne bloque donc jamais. Cette méthode prend un pointeur vers l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , que l’application doit implémenter. Lorsque le rappel est appelé, l’application appelle [**IMFMediaEventGenerator :: EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) pour récupérer l’événement à partir de la file d’attente. Pour plus d’informations sur **IMFAsyncCallback**, consultez [méthodes de rappel asynchrones](asynchronous-callback-methods.md).

Les événements sont représentés par l’interface [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) . Cette interface comprend les méthodes suivantes :

-   [**GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype): récupère le type d’événement. Le type d’événement indique ce qui s’est produit lors du déclenchement de l’événement.

-   [**GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus): récupère une valeur **HRESULT** indiquant si l’opération qui a déclenché l’événement a réussi. Si une opération échoue de façon asynchrone, **GetStatus** retourne un code d’échec.

-   [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue): récupère un **PROPVARIANT** qui contient les données d’événement. Les données d’événement dépendent du type d’événement. Certains événements n’ont pas de données.

-   [**GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype): récupère un **GUID**. Cette méthode s’applique à l' [événement MEExtendedType](meextendedtype.md)et fournit un moyen de définir des événements personnalisés.

L’interface [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) hérite également de l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Certains événements contiennent des informations supplémentaires en tant qu’attributs.

Pour obtenir la liste des types d’événements et leurs données et attributs associés, consultez [Media Foundation des événements](media-foundation-events.md).

## <a name="implementing-imfmediaeventgenerator"></a>Implémentation de IMFMediaEventGenerator

Si vous écrivez un composant de plug-in pour Media Foundation, tel qu’une source multimédia personnalisée ou un récepteur multimédia, vous devrez peut-être implémenter [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator). Pour faciliter cette opération, Media Foundation fournit un objet d’assistance qui implémente une file d’attente d’événements. Créez la file d’attente d’événements en appelant la fonction [**MFCreateEventQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateeventqueue) . La file d’attente d’événements expose l’interface [**IMFMediaEventQueue**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue) . Dans l’implémentation de l’objet des méthodes **IMFMediaEventGenerator** , appelez la méthode correspondante sur la file d’attente d’événements.

L’objet de file d’attente d’événements est thread-safe. Ne conservez jamais le même objet de section critique lors de l’appel de [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-getevent) et [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent), car **GetEvent** peut bloquer indéfiniment l’attente de [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent). Si vous conservez la même section critique pour les deux méthodes, cela provoque un interblocage.

Avant de libérer la file d’attente d’événements, appelez [**IMFMediaEventQueue :: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) pour libérer les ressources que l’objet contient.

Lorsque votre objet doit déclencher un événement, appelez l’une des méthodes suivantes dans la file d’attente des événements :

-   [**IMFMediaEventQueue::QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent)

-   [**IMFMediaEventQueue::QueueEventParamVar**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamvar)

-   [**IMFMediaEventQueue::QueueEventParamUnk**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamunk)

Ces méthodes placent un nouvel événement dans la file d’attente et signalent tout appelant qui attend l’événement suivant.

Le code suivant illustre une classe qui implémente [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) à l’aide de cet objet d’assistance. Cette classe définit une méthode d' **arrêt** public qui arrête la file d’attente des événements et libère le pointeur de la file d’attente des événements. Ce comportement est courant pour les sources multimédias et les récepteurs multimédia, qui ont toujours une méthode **Shutdown** .


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API de plateforme Media Foundation](media-foundation-platform-apis.md)
</dt> </dl>

 

 



