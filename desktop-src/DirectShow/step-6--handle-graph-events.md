---
description: Cette rubrique est l’étape 6 de la lecture audio/vidéo du didacticiel dans DirectShow.
ms.assetid: febfe7fa-e5f1-4b37-942a-ed9f8c7c60c1
title: 'Étape 6 : gérer les événements graphiques'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3660e270a542a060ed5e5eee79d5c78c107fea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541226"
---
# <a name="step-6-handle-graph-events"></a><span data-ttu-id="5f37c-103">Étape 6 : gérer les événements graphiques</span><span class="sxs-lookup"><span data-stu-id="5f37c-103">Step 6: Handle Graph Events</span></span>

<span data-ttu-id="5f37c-104">Cette rubrique est l’étape 6 de la [lecture audio/vidéo du didacticiel dans DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="5f37c-104">This topic is step 6 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="5f37c-105">Le code complet est présenté dans la rubrique [exemple de lecture DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="5f37c-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="5f37c-106">Lorsque l’application crée une nouvelle instance du gestionnaire de graphes de filtre, l’application appelle [**IMediaEventEx :: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow).</span><span class="sxs-lookup"><span data-stu-id="5f37c-106">When the application creates a new instance of the Filter Graph Manager, the application calls [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow).</span></span> <span data-ttu-id="5f37c-107">Cette méthode inscrit la fenêtre d’application pour recevoir des événements du graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="5f37c-107">This method registers the application window to receive events from the filter graph.</span></span>


```C++
    hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&m_pEvent));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set up event notification.
    hr = m_pEvent->SetNotifyWindow((OAHWND)m_hwnd, WM_GRAPH_EVENT, NULL);
    if (FAILED(hr))
    {
        goto done;
    }
```



<span data-ttu-id="5f37c-108">La valeur `WM_GRAPH_EVENT` est un message de fenêtre privée.</span><span class="sxs-lookup"><span data-stu-id="5f37c-108">The value `WM_GRAPH_EVENT` is a private window message.</span></span> <span data-ttu-id="5f37c-109">Chaque fois que l’application reçoit ce message, elle appelle la `DShowPlayer::HandleGraphEvent` méthode.</span><span class="sxs-lookup"><span data-stu-id="5f37c-109">Whenever the application receives this message, it calls the `DShowPlayer::HandleGraphEvent` method.</span></span>


```C++
    case WM_GRAPH_EVENT:
       g_pPlayer->HandleGraphEvent(OnGraphEvent);
       return 0;
```



<span data-ttu-id="5f37c-110">La méthode `DShowPlayer::HandleGraphEvent` effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="5f37c-110">The `DShowPlayer::HandleGraphEvent` method does the following:</span></span>

1.  <span data-ttu-id="5f37c-111">Appelle [**IMediaEvent :: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) dans une boucle pour obtenir tous les événements mis en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="5f37c-111">Calls [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) in a loop to get all of the queued events.</span></span>
2.  <span data-ttu-id="5f37c-112">Appelle une fonction de rappel (*pfnOnGraphEvent*).</span><span class="sxs-lookup"><span data-stu-id="5f37c-112">Invokes a callback function (*pfnOnGraphEvent*).</span></span>
3.  <span data-ttu-id="5f37c-113">Appelle [**IMediaEvent :: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) pour libérer les données associées à chaque événement.</span><span class="sxs-lookup"><span data-stu-id="5f37c-113">Calls [**IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) to free the data associated with each event.</span></span>


```C++
// Respond to a graph event.
//
// The owning window should call this method when it receives the window
// message that the application specified when it called SetEventWindow.
//
// Caution: Do not tear down the graph from inside the callback.

HRESULT DShowPlayer::HandleGraphEvent(GraphEventFN pfnOnGraphEvent)
{
    if (!m_pEvent)
    {
        return E_UNEXPECTED;
    }

    long evCode = 0;
    LONG_PTR param1 = 0, param2 = 0;

    HRESULT hr = S_OK;

    // Get the events from the queue.
    while (SUCCEEDED(m_pEvent->GetEvent(&evCode, &param1, &param2, 0)))
    {
        // Invoke the callback.
        pfnOnGraphEvent(m_hwnd, evCode, param1, param2);

        // Free the event data.
        hr = m_pEvent->FreeEventParams(evCode, param1, param2);
        if (FAILED(hr))
        {
            break;
        }
    }
    return hr;
}
```



<span data-ttu-id="5f37c-114">Le code suivant illustre la fonction de rappel qui est passée à `DShowPlayer::HandleGraphEvent` .</span><span class="sxs-lookup"><span data-stu-id="5f37c-114">The following code shows the callback function that is passed to `DShowPlayer::HandleGraphEvent`.</span></span> <span data-ttu-id="5f37c-115">La fonction gère le nombre minimal d’événements de graphe ([**EC \_ Complete**](ec-complete.md), [**EC \_ ERRORABORT**](ec-errorabort.md)et [**EC \_ USERABORT**](ec-userabort.md)); vous pouvez développer la fonction pour gérer des événements supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="5f37c-115">The function handles the minimum number of graph events ([**EC\_COMPLETE**](ec-complete.md), [**EC\_ERRORABORT**](ec-errorabort.md), and [**EC\_USERABORT**](ec-userabort.md)); you could expand the function to handle additional events.</span></span>


```C++
void CALLBACK OnGraphEvent(HWND hwnd, long evCode, LONG_PTR param1, LONG_PTR param2)
{
    switch (evCode)
    {
    case EC_COMPLETE:
    case EC_USERABORT:
        g_pPlayer->Stop();
        break;

    case EC_ERRORABORT:
        NotifyError(hwnd, L"Playback error.");
        g_pPlayer->Stop();
        break;
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="5f37c-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5f37c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f37c-117">Lecture audio/vidéo dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="5f37c-117">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="5f37c-118">Exemple de lecture DirectShow</span><span class="sxs-lookup"><span data-stu-id="5f37c-118">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="5f37c-119">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="5f37c-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="5f37c-120">Réponse aux événements</span><span class="sxs-lookup"><span data-stu-id="5f37c-120">Responding to Events</span></span>](responding-to-events.md)
</dt> </dl>

 

 



