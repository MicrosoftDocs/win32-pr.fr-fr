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
# <a name="step-7-transport-controls"></a>Étape 7 : contrôles de transport

Cette rubrique est l’étape 7 de la [lecture audio/vidéo du didacticiel dans DirectShow](audio-video-playback-in-directshow.md). Le code complet est présenté dans la rubrique [exemple de lecture DirectShow](directshow-playback-example.md).

La dernière étape consiste à ajouter des contrôles de transport (lecture, pause et arrêt). Pour lire le fichier, appelez [**IMediaControl :: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run).


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



Pour suspendre, appelez [**IMediaControl ::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause).


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



Pour arrêter, appelez [**IMediaControl :: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecture audio/vidéo dans DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[Exemple de lecture DirectShow](directshow-playback-example.md)
</dt> <dt>

[États de filtre](filter-states.md)
</dt> </dl>

 

 



