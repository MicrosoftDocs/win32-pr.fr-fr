---
description: Cette rubrique est l’étape 7 de la lecture audio/vidéo du didacticiel dans DirectShow.
ms.assetid: 2e542a2d-fc71-41d5-9abd-0dfa70719c0f
title: 'Étape 7 : contrôles de transport'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b974ccc8c186b1915d2a6564870a0b177073544e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518829"
---
# <a name="step-7-transport-controls"></a><span data-ttu-id="cce19-103">Étape 7 : contrôles de transport</span><span class="sxs-lookup"><span data-stu-id="cce19-103">Step 7: Transport Controls</span></span>

<span data-ttu-id="cce19-104">Cette rubrique est l’étape 7 de la [lecture audio/vidéo du didacticiel dans DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="cce19-104">This topic is step 7 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="cce19-105">Le code complet est présenté dans la rubrique [exemple de lecture DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="cce19-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="cce19-106">La dernière étape consiste à ajouter des contrôles de transport (lecture, pause et arrêt).</span><span class="sxs-lookup"><span data-stu-id="cce19-106">The last step is to add transport controls (play, pause, and stop).</span></span> <span data-ttu-id="cce19-107">Pour lire le fichier, appelez [**IMediaControl :: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run).</span><span class="sxs-lookup"><span data-stu-id="cce19-107">To play the file, call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run).</span></span>


```C++
HRESULT DShowPlayer::Play()
{
    if (m_state != STATE_PAUSED && m_state != STATE_STOPPED)
    {
        return VFW_E_WRONG_STATE;
    }

    HRESULT hr = m_pControl->Run();
    if (SUCCEEDED(hr))
    {
        m_state = STATE_RUNNING;
    }
    return hr;
}
```



<span data-ttu-id="cce19-108">Pour suspendre, appelez [**IMediaControl ::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause).</span><span class="sxs-lookup"><span data-stu-id="cce19-108">To pause, call [**IMediaControl::Pause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause).</span></span>


```C++
HRESULT DShowPlayer::Pause()
{
    if (m_state != STATE_RUNNING)
    {
        return VFW_E_WRONG_STATE;
    }

    HRESULT hr = m_pControl->Pause();
    if (SUCCEEDED(hr))
    {
        m_state = STATE_PAUSED;
    }
    return hr;
}
```



<span data-ttu-id="cce19-109">Pour arrêter, appelez [**IMediaControl :: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).</span><span class="sxs-lookup"><span data-stu-id="cce19-109">To stop, call [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).</span></span>


```C++
HRESULT DShowPlayer::Stop()
{
    if (m_state != STATE_RUNNING && m_state != STATE_PAUSED)
    {
        return VFW_E_WRONG_STATE;
    }

    HRESULT hr = m_pControl->Stop();
    if (SUCCEEDED(hr))
    {
        m_state = STATE_STOPPED;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="cce19-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cce19-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cce19-111">Lecture audio/vidéo dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="cce19-111">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="cce19-112">Exemple de lecture DirectShow</span><span class="sxs-lookup"><span data-stu-id="cce19-112">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="cce19-113">États de filtre</span><span class="sxs-lookup"><span data-stu-id="cce19-113">Filter States</span></span>](filter-states.md)
</dt> </dl>

 

 



