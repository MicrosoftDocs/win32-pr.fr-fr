---
description: Cette rubrique est l’étape 1 de la lecture audio/vidéo du didacticiel dans DirectShow.
ms.assetid: 3ccd201d-e60d-40bf-a602-6d42df03b36b
title: 'Étape 1 : déclarer la classe DShowPlayer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22ff36a76be8017f7b468815cf572514900f8d11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240642"
---
# <a name="step-1-declare-the-dshowplayer-class"></a>Étape 1 : déclarer la classe DShowPlayer

Cette rubrique est l’étape 1 de la [lecture audio/vidéo du didacticiel dans DirectShow](audio-video-playback-in-directshow.md). le code complet est présenté dans la rubrique [exemple de lecture DirectShow](directshow-playback-example.md).

dans ce didacticiel, la `DShowPlayer` classe gère toutes les fonctionnalités de DirectShow. Cette classe est déclarée en tant que folows.


```C++
#include <new>
#include <windows.h>
#include <dshow.h>


enum PlaybackState
{
    STATE_NO_GRAPH,
    STATE_RUNNING,
    STATE_PAUSED,
    STATE_STOPPED,
};

const UINT WM_GRAPH_EVENT = WM_APP + 1;

typedef void (CALLBACK *GraphEventFN)(HWND hwnd, long eventCode, LONG_PTR param1, LONG_PTR param2);

class DShowPlayer
{
public:
    DShowPlayer(HWND hwnd);
    ~DShowPlayer();

    PlaybackState State() const { return m_state; }

    HRESULT OpenFile(PCWSTR pszFileName);
    
    HRESULT Play();
    HRESULT Pause();
    HRESULT Stop();

    BOOL    HasVideo() const;
    HRESULT UpdateVideoWindow(const LPRECT prc);
    HRESULT Repaint(HDC hdc);
    HRESULT DisplayModeChanged();

    HRESULT HandleGraphEvent(GraphEventFN pfnOnGraphEvent);

private:
    HRESULT InitializeGraph();
    void    TearDownGraph();
    HRESULT CreateVideoRenderer();
    HRESULT RenderStreams(IBaseFilter *pSource);

    PlaybackState   m_state;

    HWND m_hwnd; // Video window. This window also receives graph events.

    IGraphBuilder   *m_pGraph;
    IMediaControl   *m_pControl;
    IMediaEventEx   *m_pEvent;
    CVideoRenderer  *m_pVideo;
};
```





Remarques :

-   L' `PlaybackState` énumération décrit l’état actuel de l' `DShowPlayer` objet.
-   L’événement de \_ graphe WM constant \_ définit un message de fenêtre privée. Ce message est utilisé pour notifier l’application des événements de graphique de filtre. consultez [Step 6 : Handle Graph events](step-6--handle-graph-events.md).
-   `GraphEventFN` est un pointeur vers une fonction de rappel pour gérer les événements de graphique de filtre. L’application implémente cette fonction de rappel.
-   la variable membre *m \_ pVideo* fournit un wrapper pour les différents convertisseurs vidéo DirectShow. Voir [étape 2 : déclarer des CVideoRenderer et des classes dérivées](step-2--declare-cvideorenderer-and-derived-classes.md).
-   Tout au long de ce didacticiel, la fonction [SafeRelease](../medfound/saferelease.md) est utilisée pour libérer des pointeurs d’interface com.

Ensuite : [étape 2 : déclarer des CVideoRenderer et des classes dérivées](step-2--declare-cvideorenderer-and-derived-classes.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecture audio/vidéo en DirectShow](audio-video-playback-in-directshow.md)
</dt> </dl>

 

 
