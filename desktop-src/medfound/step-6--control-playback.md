---
description: Cette rubrique est l’étape 6 du didacticiel comment lire des fichiers multimédias avec Media Foundation.
ms.assetid: e2e3e95b-41b2-45fb-b495-0e700220e5f5
title: 'Étape 6 : contrôler la lecture'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdfecea3484ac6b06cc44e23fd3bd1b3235324e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863410"
---
# <a name="step-6-control-playback"></a><span data-ttu-id="e257b-103">Étape 6 : contrôler la lecture</span><span class="sxs-lookup"><span data-stu-id="e257b-103">Step 6: Control Playback</span></span>

<span data-ttu-id="e257b-104">Cette rubrique est l’étape 6 du didacticiel [Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="e257b-104">This topic is step 6 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="e257b-105">Le code complet est présenté dans la rubrique [exemple de lecture de session multimédia](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="e257b-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="e257b-106">Cette rubrique contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="e257b-106">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="e257b-107">Démarrage de la lecture</span><span class="sxs-lookup"><span data-stu-id="e257b-107">Starting Playback</span></span>](#starting-playback)
-   [<span data-ttu-id="e257b-108">Suspension de la lecture</span><span class="sxs-lookup"><span data-stu-id="e257b-108">Pausing Playback</span></span>](#pausing-playback)
-   [<span data-ttu-id="e257b-109">Arrêt de la lecture</span><span class="sxs-lookup"><span data-stu-id="e257b-109">Stopping Playback</span></span>](#stopping-playback)
-   [<span data-ttu-id="e257b-110">Redessiner la fenêtre vidéo</span><span class="sxs-lookup"><span data-stu-id="e257b-110">Repainting the Video Window</span></span>](#repainting-the-video-window)
-   [<span data-ttu-id="e257b-111">Redimensionnement de la fenêtre vidéo</span><span class="sxs-lookup"><span data-stu-id="e257b-111">Resizing the Video Window</span></span>](#resizing-the-video-window)
-   [<span data-ttu-id="e257b-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e257b-112">Related topics</span></span>](#related-topics)

## <a name="starting-playback"></a><span data-ttu-id="e257b-113">Démarrage de la lecture</span><span class="sxs-lookup"><span data-stu-id="e257b-113">Starting Playback</span></span>

<span data-ttu-id="e257b-114">Pour démarrer la lecture, appelez [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="e257b-114">To start playback, call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span> <span data-ttu-id="e257b-115">Le code suivant montre comment démarrer à partir de la position de lecture actuelle.</span><span class="sxs-lookup"><span data-stu-id="e257b-115">The following code shows how to start from the current playback position.</span></span>


```C++
//  Start playback from the current position. 
HRESULT CPlayer::StartPlayback()
{
    assert(m_pSession != NULL);

    PROPVARIANT varStart;
    PropVariantInit(&varStart);

    HRESULT hr = m_pSession->Start(&GUID_NULL, &varStart);
    if (SUCCEEDED(hr))
    {
        // Note: Start is an asynchronous operation. However, we
        // can treat our state as being already started. If Start
        // fails later, we'll get an MESessionStarted event with
        // an error code, and we will update our state then.
        m_state = Started;
    }
    PropVariantClear(&varStart);
    return hr;
}

//  Start playback from paused or stopped.
HRESULT CPlayer::Play()
{
    if (m_state != Paused && m_state != Stopped)
    {
        return MF_E_INVALIDREQUEST;
    }
    if (m_pSession == NULL || m_pSource == NULL)
    {
        return E_UNEXPECTED;
    }
    return StartPlayback();
}

```



<span data-ttu-id="e257b-116">La méthode [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) peut également spécifier une position de départ par rapport au début du fichier ; Pour plus d’informations, consultez la rubrique de référence sur les API.</span><span class="sxs-lookup"><span data-stu-id="e257b-116">The [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method can also specify a starting position relative to the start of the file; see the API reference topic for more information.</span></span>

## <a name="pausing-playback"></a><span data-ttu-id="e257b-117">Suspension de la lecture</span><span class="sxs-lookup"><span data-stu-id="e257b-117">Pausing Playback</span></span>

<span data-ttu-id="e257b-118">Pour suspendre la lecture, appelez [**IMFMediaSession ::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause).</span><span class="sxs-lookup"><span data-stu-id="e257b-118">To pause playback, call [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause).</span></span>


```C++
//  Pause playback.
HRESULT CPlayer::Pause()    
{
    if (m_state != Started)
    {
        return MF_E_INVALIDREQUEST;
    }
    if (m_pSession == NULL || m_pSource == NULL)
    {
        return E_UNEXPECTED;
    }

    HRESULT hr = m_pSession->Pause();
    if (SUCCEEDED(hr))
    {
        m_state = Paused;
    }

    return hr;
}
```



## <a name="stopping-playback"></a><span data-ttu-id="e257b-119">Arrêt de la lecture</span><span class="sxs-lookup"><span data-stu-id="e257b-119">Stopping Playback</span></span>

<span data-ttu-id="e257b-120">Pour arrêter la lecture, appelez [**IMFMediaSession :: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span><span class="sxs-lookup"><span data-stu-id="e257b-120">To stop playback, call [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span></span> <span data-ttu-id="e257b-121">Pendant l’arrêt de la lecture, l’image vidéo est effacée et la fenêtre vidéo est peinte avec la couleur d’arrière-plan (noir par défaut).</span><span class="sxs-lookup"><span data-stu-id="e257b-121">While playback is stopped, the video image is cleared and the video window is painted with the background color (black by default).</span></span>


```C++
// Stop playback.
HRESULT CPlayer::Stop()
{
    if (m_state != Started && m_state != Paused)
    {
        return MF_E_INVALIDREQUEST;
    }
    if (m_pSession == NULL)
    {
        return E_UNEXPECTED;
    }

    HRESULT hr = m_pSession->Stop();
    if (SUCCEEDED(hr))
    {
        m_state = Stopped;
    }
    return hr;
}
```



## <a name="repainting-the-video-window"></a><span data-ttu-id="e257b-122">Redessiner la fenêtre vidéo</span><span class="sxs-lookup"><span data-stu-id="e257b-122">Repainting the Video Window</span></span>

<span data-ttu-id="e257b-123">Le [convertisseur vidéo amélioré](enhanced-video-renderer.md) (EVR) dessine la vidéo dans la fenêtre spécifiée par l’application.</span><span class="sxs-lookup"><span data-stu-id="e257b-123">The [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) draws the video in the window specified by the application.</span></span> <span data-ttu-id="e257b-124">Cela se produit sur un thread distinct et, pour l’essentiel, votre application n’a pas besoin de gérer ce processus.</span><span class="sxs-lookup"><span data-stu-id="e257b-124">This occurs on a separate thread, and for the most part, your application does not need to manage this process.</span></span> <span data-ttu-id="e257b-125">Toutefois, si la lecture est suspendue ou arrêtée, le EVR doit être notifié chaque fois que la fenêtre vidéo reçoit un message de [**\_ peinture WM**](../gdi/wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="e257b-125">If playback is paused or stopped, however, the EVR must be notified whenever the video window receives a [**WM\_PAINT**](../gdi/wm-paint.md) message.</span></span> <span data-ttu-id="e257b-126">Cela permet à EVR de repeindre la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e257b-126">This allows the EVR to repaint the window.</span></span> <span data-ttu-id="e257b-127">Pour notifier le EVR, appelez la méthode [**IMFVideoDisplayControl :: RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) :</span><span class="sxs-lookup"><span data-stu-id="e257b-127">To notify the EVR, call the [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) method:</span></span>


```C++
//  Repaint the video window. Call this method on WM_PAINT.

HRESULT CPlayer::Repaint()
{
    if (m_pVideoDisplay)
    {
        return m_pVideoDisplay->RepaintVideo();
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="e257b-128">Le code suivant montre le gestionnaire du message [**WM \_ Paint**](../gdi/wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="e257b-128">The following code shows the handler for the [**WM\_PAINT**](../gdi/wm-paint.md) message.</span></span> <span data-ttu-id="e257b-129">Cette fonction doit être appelée à partir de la boucle de message de l’application.</span><span class="sxs-lookup"><span data-stu-id="e257b-129">This function should be called from the application's message loop.</span></span>


```C++
//  Handler for WM_PAINT messages.
void OnPaint(HWND hwnd)
{
    PAINTSTRUCT ps;
    HDC hdc = BeginPaint(hwnd, &ps);

    if (g_pPlayer && g_pPlayer->HasVideo())
    {
        // Video is playing. Ask the player to repaint.
        g_pPlayer->Repaint();
    }
    else
    {
        // The video is not playing, so we must paint the application window.
        RECT rc;
        GetClientRect(hwnd, &rc);
        FillRect(hdc, &rc, (HBRUSH) COLOR_WINDOW);
    }
    EndPaint(hwnd, &ps);
}
```



<span data-ttu-id="e257b-130">La `HasVideo` méthode retourne la **valeur true** si l' `CPlayer` objet a un pointeur [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) valide.</span><span class="sxs-lookup"><span data-stu-id="e257b-130">The `HasVideo` method returns **TRUE** if the `CPlayer` object has a valid [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) pointer.</span></span> <span data-ttu-id="e257b-131">(Voir [étape 1 : déclarer la classe CPlayer](step-1--declare-the-cplayer-class.md).)</span><span class="sxs-lookup"><span data-stu-id="e257b-131">(See [Step 1: Declare the CPlayer Class](step-1--declare-the-cplayer-class.md).)</span></span>


```C++
    BOOL          HasVideo() const { return (m_pVideoDisplay != NULL);  }
```



## <a name="resizing-the-video-window"></a><span data-ttu-id="e257b-132">Redimensionnement de la fenêtre vidéo</span><span class="sxs-lookup"><span data-stu-id="e257b-132">Resizing the Video Window</span></span>

<span data-ttu-id="e257b-133">Si vous redimensionnez la fenêtre vidéo, mettez à jour le rectangle de destination sur le EVR en appelant la méthode [**IMFVideoDisplayControl :: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) :</span><span class="sxs-lookup"><span data-stu-id="e257b-133">If you resize the video window, update the destination rectangle on the EVR by calling the [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) method:</span></span>


```C++
//  Resize the video rectangle.
//
//  Call this method if the size of the video window changes.

HRESULT CPlayer::ResizeVideo(WORD width, WORD height)
{
    if (m_pVideoDisplay)
    {
        // Set the destination rectangle.
        // Leave the default source rectangle (0,0,1,1).

        RECT rcDest = { 0, 0, width, height };

        return m_pVideoDisplay->SetVideoPosition(NULL, &rcDest);
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="e257b-134">Suivant : [étape 7 : arrêter la session multimédia](step-7--shut-down-the-media-session.md)</span><span class="sxs-lookup"><span data-stu-id="e257b-134">Next: [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="e257b-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e257b-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e257b-136">Lecture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="e257b-136">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="e257b-137">Comment lire des fichiers multimédias avec Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e257b-137">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
