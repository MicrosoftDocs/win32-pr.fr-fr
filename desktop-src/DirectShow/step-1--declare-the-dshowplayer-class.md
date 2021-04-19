---
description: Cette rubrique est l’étape 1 de la lecture audio/vidéo du didacticiel dans DirectShow.
ms.assetid: 3ccd201d-e60d-40bf-a602-6d42df03b36b
title: 'Étape 1 : déclarer la classe DShowPlayer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22ff36a76be8017f7b468815cf572514900f8d11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530082"
---
# <a name="step-1-declare-the-dshowplayer-class"></a><span data-ttu-id="1fcfe-103">Étape 1 : déclarer la classe DShowPlayer</span><span class="sxs-lookup"><span data-stu-id="1fcfe-103">Step 1: Declare the DShowPlayer Class</span></span>

<span data-ttu-id="1fcfe-104">Cette rubrique est l’étape 1 de la [lecture audio/vidéo du didacticiel dans DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="1fcfe-104">This topic is step 1 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="1fcfe-105">Le code complet est présenté dans la rubrique [exemple de lecture DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="1fcfe-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="1fcfe-106">Dans ce didacticiel, la `DShowPlayer` classe gère toutes les fonctionnalités DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1fcfe-106">In this tutorial, the `DShowPlayer` class manages all DirectShow functionality.</span></span> <span data-ttu-id="1fcfe-107">Cette classe est déclarée en tant que folows.</span><span class="sxs-lookup"><span data-stu-id="1fcfe-107">This class is declared as folows.</span></span>


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





<span data-ttu-id="1fcfe-108">Remarques :</span><span class="sxs-lookup"><span data-stu-id="1fcfe-108">Notes:</span></span>

-   <span data-ttu-id="1fcfe-109">L' `PlaybackState` énumération décrit l’état actuel de l' `DShowPlayer` objet.</span><span class="sxs-lookup"><span data-stu-id="1fcfe-109">The `PlaybackState` enumeration describes the current state of the `DShowPlayer` object.</span></span>
-   <span data-ttu-id="1fcfe-110">L’événement de \_ graphe WM constant \_ définit un message de fenêtre privée.</span><span class="sxs-lookup"><span data-stu-id="1fcfe-110">The constant WM\_GRAPH\_EVENT defines a private window message.</span></span> <span data-ttu-id="1fcfe-111">Ce message est utilisé pour notifier l’application des événements de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="1fcfe-111">This message is used to notify the application about filter graph events.</span></span> <span data-ttu-id="1fcfe-112">Voir [étape 6 : gérer les événements de graphique](step-6--handle-graph-events.md).</span><span class="sxs-lookup"><span data-stu-id="1fcfe-112">See [Step 6: Handle Graph Events](step-6--handle-graph-events.md).</span></span>
-   <span data-ttu-id="1fcfe-113">`GraphEventFN` est un pointeur vers une fonction de rappel pour gérer les événements de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="1fcfe-113">`GraphEventFN` is a pointer to a callback function for handling filter graph events.</span></span> <span data-ttu-id="1fcfe-114">L’application implémente cette fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="1fcfe-114">The application implements this callback function.</span></span>
-   <span data-ttu-id="1fcfe-115">La variable membre *m \_ pVideo* fournit un wrapper pour les divers convertisseurs vidéo DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1fcfe-115">The *m\_pVideo* member variable provides a wrapper for the various DirectShow video renderers.</span></span> <span data-ttu-id="1fcfe-116">Voir [étape 2 : déclarer des CVideoRenderer et des classes dérivées](step-2--declare-cvideorenderer-and-derived-classes.md).</span><span class="sxs-lookup"><span data-stu-id="1fcfe-116">See [Step 2: Declare CVideoRenderer and Derived Classes](step-2--declare-cvideorenderer-and-derived-classes.md).</span></span>
-   <span data-ttu-id="1fcfe-117">Tout au long de ce didacticiel, la fonction [SafeRelease](../medfound/saferelease.md) est utilisée pour libérer des pointeurs d’interface com.</span><span class="sxs-lookup"><span data-stu-id="1fcfe-117">Throughout this tutorial, the [SafeRelease](../medfound/saferelease.md) function is used to release COM interface pointers.</span></span>

<span data-ttu-id="1fcfe-118">Ensuite : [étape 2 : déclarer des CVideoRenderer et des classes dérivées](step-2--declare-cvideorenderer-and-derived-classes.md).</span><span class="sxs-lookup"><span data-stu-id="1fcfe-118">Next: [Step 2: Declare CVideoRenderer and Derived Classes](step-2--declare-cvideorenderer-and-derived-classes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fcfe-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1fcfe-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fcfe-120">Lecture audio/vidéo dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="1fcfe-120">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> </dl>

 

 
