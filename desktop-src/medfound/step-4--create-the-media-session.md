---
description: Cette rubrique est l’étape 4 du didacticiel comment lire des fichiers multimédias avec Media Foundation.
ms.assetid: fe5e852f-fe0c-439d-b0c5-d32593b587cb
title: 'Étape 4 : créer la session multimédia'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b4c6c9e36552247cb294a7d0d6996fcc0b8a6ec
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953472"
---
# <a name="step-4-create-the-media-session"></a><span data-ttu-id="f04e6-103">Étape 4 : créer la session multimédia</span><span class="sxs-lookup"><span data-stu-id="f04e6-103">Step 4: Create the Media Session</span></span>

<span data-ttu-id="f04e6-104">Cette rubrique est l’étape 4 du didacticiel [Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="f04e6-104">This topic is step 4 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="f04e6-105">Le code complet est présenté dans la rubrique [exemple de lecture de session multimédia](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="f04e6-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="f04e6-106">`CPlayer::CreateSession`Crée une nouvelle instance de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="f04e6-106">The `CPlayer::CreateSession` creates a new instance of the Media Session.</span></span>


```C++
//  Create a new instance of the media session.
HRESULT CPlayer::CreateSession()
{
    // Close the old session, if any.
    HRESULT hr = CloseSession();
    if (FAILED(hr))
    {
        goto done;
    }

    assert(m_state == Closed);

    // Create the media session.
    hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    // Start pulling events from the media session
    hr = m_pSession->BeginGetEvent((IMFAsyncCallback*)this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = Ready;

done:
    return hr;
}
```



<span data-ttu-id="f04e6-107">Cette méthode effectue les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f04e6-107">This method performs the following steps:</span></span>

1.  <span data-ttu-id="f04e6-108">Appelle `CPlayer::CloseSession` pour fermer toute instance précédente de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="f04e6-108">Calls `CPlayer::CloseSession` to close any previous instance of the Media Session.</span></span>
2.  <span data-ttu-id="f04e6-109">Appelle [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) pour créer une nouvelle instance de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="f04e6-109">Calls [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create a new instance of the Media Session.</span></span>
3.  <span data-ttu-id="f04e6-110">Appelle la méthode [**IMFMediaEventGenerator :: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) pour demander l’événement suivant à partir de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="f04e6-110">Calls the [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method to request the next event from the Media Session.</span></span> <span data-ttu-id="f04e6-111">Le premier paramètre de **BeginGetEvent** est un pointeur vers l’objet **CPlayer** lui-même, qui implents l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="f04e6-111">The first parameter to **BeginGetEvent** is a pointer to the **CPlayer** object itself, which implents the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>

<span data-ttu-id="f04e6-112">La gestion des événements est décrite à l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="f04e6-112">Event handling is described in step 5.</span></span>

<span data-ttu-id="f04e6-113">Suivant : [étape 5 : gérer les événements de session multimédia](step-5--handle-media-session-events.md)</span><span class="sxs-lookup"><span data-stu-id="f04e6-113">Next: [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="f04e6-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f04e6-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f04e6-115">Lecture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="f04e6-115">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="f04e6-116">Comment lire des fichiers multimédias avec Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f04e6-116">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



