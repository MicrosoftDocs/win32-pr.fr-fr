---
description: Cette rubrique est l’étape 7 du didacticiel comment lire des fichiers multimédias avec Media Foundation.
ms.assetid: c31444df-8717-4ca8-a9ec-72cbb0ee4125
title: 'Étape 7 : arrêter la session multimédia'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa1eec6e798ee260c83fc1532c2012aed8a53625b12195848ac00fcdcf8fae3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721942"
---
# <a name="step-7-shut-down-the-media-session"></a>Étape 7 : arrêter la session multimédia

Cette rubrique est l’étape 7 du didacticiel [Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md). Le code complet est présenté dans la rubrique [exemple de lecture de session multimédia](media-session-playback-example.md).

Pour arrêter la [session multimédia](media-session.md), procédez comme suit :

1.  Appelez [**IMFMediaSession :: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) pour fermer la présentation actuelle.
2.  Attendez l’événement [MESessionClosed](mesessionclosed.md) . Cet événement est garanti comme étant le dernier événement de la session multimédia.
3.  Appelez [**IMFMediaSession :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown). Cette méthode amène les sessions multimédia à libérer des ressources.
4.  Appelez [**IMFMediaSource :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) sur la source du média en cours.

La méthode suivante arrête la session multimédia. Elle utilise un descripteur d’événement (*m \_ hCloseEvent*) pour attendre l’événement [MESessionClosed](mesessionclosed.md) . Consultez [étape 5 : gérer les événements de session multimédia](step-5--handle-media-session-events.md).


```C++
//  Close the media session. 
HRESULT CPlayer::CloseSession()
{
    //  The IMFMediaSession::Close method is asynchronous, but the 
    //  CPlayer::CloseSession method waits on the MESessionClosed event.
    //  
    //  MESessionClosed is guaranteed to be the last event that the 
    //  media session fires.

    HRESULT hr = S_OK;

    SafeRelease(&m_pVideoDisplay);

    // First close the media session.
    if (m_pSession)
    {
        DWORD dwWaitResult = 0;

        m_state = Closing;
           
        hr = m_pSession->Close();
        // Wait for the close operation to complete
        if (SUCCEEDED(hr))
        {
            dwWaitResult = WaitForSingleObject(m_hCloseEvent, 5000);
            if (dwWaitResult == WAIT_TIMEOUT)
            {
                assert(FALSE);
            }
            // Now there will be no more events from this session.
        }
    }

    // Complete shutdown operations.
    if (SUCCEEDED(hr))
    {
        // Shut down the media source. (Synchronous operation, no events.)
        if (m_pSource)
        {
            (void)m_pSource->Shutdown();
        }
        // Shut down the media session. (Synchronous operation, no events.)
        if (m_pSession)
        {
            (void)m_pSession->Shutdown();
        }
    }

    SafeRelease(&m_pSource);
    SafeRelease(&m_pSession);
    m_state = Closed;
    return hr;
}
```



Avant de quitter l’application, arrêtez la session multimédia, puis appelez [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) pour arrêter la plateforme Microsoft Media Foundation.


```C++
//  Release all resources held by this object.
HRESULT CPlayer::Shutdown()
{
    // Close the session
    HRESULT hr = CloseSession();

    // Shutdown the Media Foundation platform
    MFShutdown();

    if (m_hCloseEvent)
    {
        CloseHandle(m_hCloseEvent);
        m_hCloseEvent = NULL;
    }

    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecture audio/vidéo](audio-video-playback.md)
</dt> <dt>

[Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



