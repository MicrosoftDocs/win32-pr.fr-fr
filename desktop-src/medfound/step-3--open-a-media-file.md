---
description: Cette rubrique est l’étape 3 du didacticiel comment lire des fichiers multimédias avec Media Foundation.
ms.assetid: cc0d2b60-64d7-49f3-844f-97487cab8466
title: 'Étape 3 : ouvrir un fichier multimédia'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b50f036b84806f96e4349f77a3f06e02e08764
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104042950"
---
# <a name="step-3-open-a-media-file"></a>Étape 3 : ouvrir un fichier multimédia

Cette rubrique est l’étape 3 du didacticiel [Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md). Le code complet est présenté dans la rubrique [exemple de lecture de session multimédia](media-session-playback-example.md).

La `CPlayer::OpenURL` méthode ouvre un fichier multimédia à partir d’une URL.


```C++
//  Open a URL for playback.
HRESULT CPlayer::OpenURL(const WCHAR *sURL)
{
    // 1. Create a new media session.
    // 2. Create the media source.
    // 3. Create the topology.
    // 4. Queue the topology [asynchronous]
    // 5. Start playback [asynchronous - does not happen in this method.]

    IMFTopology *pTopology = NULL;
    IMFPresentationDescriptor* pSourcePD = NULL;

    // Create the media session.
    HRESULT hr = CreateSession();
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the media source.
    hr = CreateMediaSource(sURL, &m_pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the presentation descriptor for the media source.
    hr = m_pSource->CreatePresentationDescriptor(&pSourcePD);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a partial topology.
    hr = CreatePlaybackTopology(m_pSource, pSourcePD, m_hwndVideo, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the topology on the media session.
    hr = m_pSession->SetTopology(0, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = OpenPending;

    // If SetTopology succeeds, the media session will queue an 
    // MESessionTopologySet event.

done:
    if (FAILED(hr))
    {
        m_state = Closed;
    }

    SafeRelease(&pSourcePD);
    SafeRelease(&pTopology);
    return hr;
}
```



Cette méthode effectue les étapes suivantes :

1.  Appelle **CPlayer :: CreateSession** pour créer une nouvelle instance de la session multimédia. Consultez [Step 4 : Create the Media session](step-4--create-the-media-session.md).
2.  Crée une source de média à partir de l’URL. Le code complet de cette étape est présenté dans la rubrique [utilisation du programme de résolution source](using-the-source-resolver.md).
3.  Appelle [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) pour récupérer le descripteur de présentation de la source du média. Le descripteur de présentation décrit chaque flux du fichier source.
4.  Crée la topologie de lecture. Le code pour cette étape est présenté dans la rubrique [création de topologies de lecture](creating-playback-topologies.md).
5.  Appelle [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) pour définir la topologie sur la session multimédia.

La méthode [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) se termine de façon asynchrone. Une fois l’opération terminée, la méthode [**IMFAsyncCallback :: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) de l’objet CPlayer est appelée ; consultez [étape 5 : gérer les événements de session multimédia](step-5--handle-media-session-events.md).

Suivant : [étape 4 : créer la session multimédia](step-4--create-the-media-session.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecture audio/vidéo](audio-video-playback.md)
</dt> <dt>

[Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



