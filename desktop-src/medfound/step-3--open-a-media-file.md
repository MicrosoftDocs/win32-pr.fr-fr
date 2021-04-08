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
# <a name="step-3-open-a-media-file"></a><span data-ttu-id="44c50-103">Étape 3 : ouvrir un fichier multimédia</span><span class="sxs-lookup"><span data-stu-id="44c50-103">Step 3: Open a Media File</span></span>

<span data-ttu-id="44c50-104">Cette rubrique est l’étape 3 du didacticiel [Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="44c50-104">This topic is step 3 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="44c50-105">Le code complet est présenté dans la rubrique [exemple de lecture de session multimédia](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="44c50-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="44c50-106">La `CPlayer::OpenURL` méthode ouvre un fichier multimédia à partir d’une URL.</span><span class="sxs-lookup"><span data-stu-id="44c50-106">The `CPlayer::OpenURL` method opens a media file from a URL.</span></span>


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



<span data-ttu-id="44c50-107">Cette méthode effectue les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="44c50-107">This method performs the following steps:</span></span>

1.  <span data-ttu-id="44c50-108">Appelle **CPlayer :: CreateSession** pour créer une nouvelle instance de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="44c50-108">Calls **CPlayer::CreateSession** to create a new instance of the Media Session.</span></span> <span data-ttu-id="44c50-109">Consultez [Step 4 : Create the Media session](step-4--create-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="44c50-109">See [Step 4: Create the Media Session](step-4--create-the-media-session.md).</span></span>
2.  <span data-ttu-id="44c50-110">Crée une source de média à partir de l’URL.</span><span class="sxs-lookup"><span data-stu-id="44c50-110">Creates a media source from the URL.</span></span> <span data-ttu-id="44c50-111">Le code complet de cette étape est présenté dans la rubrique [utilisation du programme de résolution source](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="44c50-111">The complete code for this step is shown in the topic [Using the Source Resolver](using-the-source-resolver.md).</span></span>
3.  <span data-ttu-id="44c50-112">Appelle [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) pour récupérer le descripteur de présentation de la source du média.</span><span class="sxs-lookup"><span data-stu-id="44c50-112">Calls [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) to get the media source's presentation descriptor.</span></span> <span data-ttu-id="44c50-113">Le descripteur de présentation décrit chaque flux du fichier source.</span><span class="sxs-lookup"><span data-stu-id="44c50-113">The presentation descriptor describes each streams in the source file.</span></span>
4.  <span data-ttu-id="44c50-114">Crée la topologie de lecture.</span><span class="sxs-lookup"><span data-stu-id="44c50-114">Creates the playback topology.</span></span> <span data-ttu-id="44c50-115">Le code pour cette étape est présenté dans la rubrique [création de topologies de lecture](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="44c50-115">Code for this step is shown in the topic [Creating Playback Topologies](creating-playback-topologies.md).</span></span>
5.  <span data-ttu-id="44c50-116">Appelle [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) pour définir la topologie sur la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="44c50-116">Calls [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the topology on the Media Session.</span></span>

<span data-ttu-id="44c50-117">La méthode [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) se termine de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="44c50-117">The [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method completes asynchronously.</span></span> <span data-ttu-id="44c50-118">Une fois l’opération terminée, la méthode [**IMFAsyncCallback :: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) de l’objet CPlayer est appelée ; consultez [étape 5 : gérer les événements de session multimédia](step-5--handle-media-session-events.md).</span><span class="sxs-lookup"><span data-stu-id="44c50-118">When it completes, the CPlayer object's [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method is called; see [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md).</span></span>

<span data-ttu-id="44c50-119">Suivant : [étape 4 : créer la session multimédia](step-4--create-the-media-session.md)</span><span class="sxs-lookup"><span data-stu-id="44c50-119">Next: [Step 4: Create the Media Session](step-4--create-the-media-session.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="44c50-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="44c50-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44c50-121">Lecture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="44c50-121">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="44c50-122">Comment lire des fichiers multimédias avec Media Foundation</span><span class="sxs-lookup"><span data-stu-id="44c50-122">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



