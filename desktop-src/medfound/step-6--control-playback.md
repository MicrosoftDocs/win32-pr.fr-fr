---
description: Cette rubrique est l’étape 6 du didacticiel comment lire des fichiers multimédias avec Media Foundation.
ms.assetid: e2e3e95b-41b2-45fb-b495-0e700220e5f5
title: 'Étape 6 : contrôler la lecture'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eef0aa18f671c994837ba195cddba38976c3ffba990eb95748d2bede09141317
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887259"
---
# <a name="step-6-control-playback"></a>Étape 6 : contrôler la lecture

Cette rubrique est l’étape 6 du didacticiel [Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md). Le code complet est présenté dans la rubrique [exemple de lecture de session multimédia](media-session-playback-example.md).

Cette rubrique contient les sections suivantes :

-   [Démarrage de la lecture](#starting-playback)
-   [Suspension de la lecture](#pausing-playback)
-   [Arrêt de la lecture](#stopping-playback)
-   [Redessiner la fenêtre vidéo](#repainting-the-video-window)
-   [Redimensionnement de la fenêtre vidéo](#resizing-the-video-window)
-   [Rubriques connexes](#related-topics)

## <a name="starting-playback"></a>Démarrage de la lecture

Pour démarrer la lecture, appelez [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start). Le code suivant montre comment démarrer à partir de la position de lecture actuelle.


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



La méthode [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) peut également spécifier une position de départ par rapport au début du fichier ; Pour plus d’informations, consultez la rubrique de référence sur les API.

## <a name="pausing-playback"></a>Suspension de la lecture

Pour suspendre la lecture, appelez [**IMFMediaSession ::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause).


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



## <a name="stopping-playback"></a>Arrêt de la lecture

Pour arrêter la lecture, appelez [**IMFMediaSession :: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop). Pendant l’arrêt de la lecture, l’image vidéo est effacée et la fenêtre vidéo est peinte avec la couleur d’arrière-plan (noir par défaut).


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



## <a name="repainting-the-video-window"></a>Redessiner la fenêtre vidéo

Le [convertisseur vidéo amélioré](enhanced-video-renderer.md) (EVR) dessine la vidéo dans la fenêtre spécifiée par l’application. Cela se produit sur un thread distinct et, pour l’essentiel, votre application n’a pas besoin de gérer ce processus. Toutefois, si la lecture est suspendue ou arrêtée, le EVR doit être notifié chaque fois que la fenêtre vidéo reçoit un message de [**\_ peinture WM**](../gdi/wm-paint.md) . Cela permet à EVR de repeindre la fenêtre. Pour notifier le EVR, appelez la méthode [**IMFVideoDisplayControl :: RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) :


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



Le code suivant montre le gestionnaire du message [**WM \_ Paint**](../gdi/wm-paint.md) . Cette fonction doit être appelée à partir de la boucle de message de l’application.


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



La `HasVideo` méthode retourne la **valeur true** si l' `CPlayer` objet a un pointeur [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) valide. (Voir [étape 1 : déclarer la classe CPlayer](step-1--declare-the-cplayer-class.md).)


```C++
    BOOL          HasVideo() const { return (m_pVideoDisplay != NULL);  }
```



## <a name="resizing-the-video-window"></a>Redimensionnement de la fenêtre vidéo

Si vous redimensionnez la fenêtre vidéo, mettez à jour le rectangle de destination sur le EVR en appelant la méthode [**IMFVideoDisplayControl :: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) :


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



Suivant : [étape 7 : arrêter la session multimédia](step-7--shut-down-the-media-session.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecture audio/vidéo](audio-video-playback.md)
</dt> <dt>

[Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
