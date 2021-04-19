---
description: Cette rubrique est l’étape 2 du didacticiel comment lire des fichiers multimédias avec Media Foundation.
ms.assetid: b489312f-ab8c-4ec6-8070-f5848034087e
title: 'Étape 2 : créer l’objet CPlayer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021ffa383506c0ab1be8d6c1ca327f67ed8f52f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517737"
---
# <a name="step-2-create-the-cplayer-object"></a>Étape 2 : créer l’objet CPlayer

Cette rubrique est l’étape 2 du didacticiel [Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md). Le code complet est présenté dans la rubrique [exemple de lecture de session multimédia](media-session-playback-example.md).

Pour créer une instance de la `CPlayer` classe, l’application appelle la `CPlayer::CreateInstance` méthode statique. Cette méthode accepte les paramètres suivants :

-   *hVideo* spécifie la fenêtre qui affiche la vidéo.
-   *hEvent* spécifie une fenêtre pour recevoir des événements. Il est possible de passer le même handle pour les deux handles de fenêtre.
-   *ppPlayer* reçoit un pointeur vers une nouvelle `CPlayer` instance.

Le code suivant montre la méthode `CreateInstance` :


```C++
//  Static class method to create the CPlayer object.

HRESULT CPlayer::CreateInstance(
    HWND hVideo,                  // Video window.
    HWND hEvent,                  // Window to receive notifications.
    CPlayer **ppPlayer)           // Receives a pointer to the CPlayer object.
{
    if (ppPlayer == NULL)
    {
        return E_POINTER;
    }

    CPlayer *pPlayer = new (std::nothrow) CPlayer(hVideo, hEvent);
    if (pPlayer == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pPlayer->Initialize();
    if (SUCCEEDED(hr))
    {
        *ppPlayer = pPlayer;
    }
    else
    {
        pPlayer->Release();
    }
    return hr;
}

HRESULT CPlayer::Initialize()
{
    // Start up Media Foundation platform.
    HRESULT hr = MFStartup(MF_VERSION);
    if (SUCCEEDED(hr))
    {
        m_hCloseEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
        if (m_hCloseEvent == NULL)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
        }
    }
    return hr;
}
```



Le code suivant illustre le `CPlayer` constructeur :


```C++
CPlayer::CPlayer(HWND hVideo, HWND hEvent) : 
    m_pSession(NULL),
    m_pSource(NULL),
    m_pVideoDisplay(NULL),
    m_hwndVideo(hVideo),
    m_hwndEvent(hEvent),
    m_state(Closed),
    m_hCloseEvent(NULL),
    m_nRefCount(1)
{
}
```



Le constructeur effectue les opérations suivantes :

1.  Appelle [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) pour initialiser la plateforme Media Foundation.
2.  Crée un événement de réinitialisation automatique. Cet événement est utilisé lors de la fermeture de la session multimédia ; Voir [étape 7 : arrêter la session multimédia](step-7--shut-down-the-media-session.md).

Le destructeur arrête la session multimédia, comme décrit à [l’étape 7 : arrêter la session multimédia](step-7--shut-down-the-media-session.md).


```C++
CPlayer::~CPlayer()
{
    assert(m_pSession == NULL);  
    // If FALSE, the app did not call Shutdown().

    // When CPlayer calls IMediaEventGenerator::BeginGetEvent on the
    // media session, it causes the media session to hold a reference 
    // count on the CPlayer. 
    
    // This creates a circular reference count between CPlayer and the 
    // media session. Calling Shutdown breaks the circular reference 
    // count.

    // If CreateInstance fails, the application will not call 
    // Shutdown. To handle that case, call Shutdown in the destructor. 

    Shutdown();
}
```



Notez que le constructeur et le destructeur sont tous deux des méthodes de classe protégées. L’application crée l’objet à l’aide de la `CreateInstance` méthode statique. Elle détruit l’objet en appelant **IUnknown :: Release**, plutôt que de **supprimer** explicitement.

Suivant : [étape 3 : ouvrir un fichier multimédia](step-3--open-a-media-file.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecture audio/vidéo](audio-video-playback.md)
</dt> <dt>

[Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



