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
# <a name="step-6-handle-graph-events"></a>Étape 6 : gérer les événements graphiques

Cette rubrique est l’étape 6 de la [lecture audio/vidéo du didacticiel dans DirectShow](audio-video-playback-in-directshow.md). Le code complet est présenté dans la rubrique [exemple de lecture DirectShow](directshow-playback-example.md).

Lorsque l’application crée une nouvelle instance du gestionnaire de graphes de filtre, l’application appelle [**IMediaEventEx :: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow). Cette méthode inscrit la fenêtre d’application pour recevoir des événements du graphique de filtre.


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



La valeur `WM_GRAPH_EVENT` est un message de fenêtre privée. Chaque fois que l’application reçoit ce message, elle appelle la `DShowPlayer::HandleGraphEvent` méthode.


```C++
    case WM_GRAPH_EVENT:
       g_pPlayer->HandleGraphEvent(OnGraphEvent);
       return 0;
```



La méthode `DShowPlayer::HandleGraphEvent` effectue les opérations suivantes :

1.  Appelle [**IMediaEvent :: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) dans une boucle pour obtenir tous les événements mis en file d’attente.
2.  Appelle une fonction de rappel (*pfnOnGraphEvent*).
3.  Appelle [**IMediaEvent :: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) pour libérer les données associées à chaque événement.


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



Le code suivant illustre la fonction de rappel qui est passée à `DShowPlayer::HandleGraphEvent` . La fonction gère le nombre minimal d’événements de graphe ([**EC \_ Complete**](ec-complete.md), [**EC \_ ERRORABORT**](ec-errorabort.md)et [**EC \_ USERABORT**](ec-userabort.md)); vous pouvez développer la fonction pour gérer des événements supplémentaires.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecture audio/vidéo dans DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[Exemple de lecture DirectShow](directshow-playback-example.md)
</dt> <dt>

[Notification d’événement dans DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Réponse aux événements](responding-to-events.md)
</dt> </dl>

 

 



