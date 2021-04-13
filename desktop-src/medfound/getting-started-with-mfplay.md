---
description: MFPlay est une API permettant de créer des applications de lecture multimédia en C++.
ms.assetid: 55612f49-5995-4bdf-aa12-8a853e5a2b24
title: Prise en main avec MFPlay
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9e0405d3138a22e0d20e94849d416b29d62945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484064"
---
# <a name="getting-started-with-mfplay"></a>Prise en main avec MFPlay

\[MFPlay peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. \]

MFPlay est une API permettant de créer des applications de lecture multimédia en C++.

Cette rubrique contient les sections suivantes :

-   [Configuration requise](#requirements)
-   [À propos de MFPlay](#about-mfplay)
-   [Lit un fichier multimédia](#playing-a-media-file)
-   [Contrôle de la lecture](#controlling-playback)
-   [Réception d’événements à partir du lecteur](#receiving-events-from-the-player)
-   [Obtention d’informations sur un fichier multimédia](#getting-information-about-a-media-file)
-   [Gestion de la lecture vidéo](#managing-video-playback)
-   [Limitations de MFPlay](#limitations-of-mfplay)
-   [Rubriques connexes](#related-topics)

## <a name="requirements"></a>Configuration requise

MFPlay requiert Windows 7.

## <a name="about-mfplay"></a>À propos de MFPlay

MFPlay a un modèle de programmation simple, tout en fournissant l’ensemble principal de fonctionnalités dont la plupart des applications de lecture ont besoin. Une application crée un objet *Player* qui contrôle la lecture. Pour lire un fichier multimédia, l’objet Player crée un *élément multimédia*, qui peut être utilisé pour obtenir des informations sur le contenu du fichier multimédia. L’application contrôle la lecture via des méthodes sur l’interface [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) de l’objet Player. Si vous le souhaitez, l’application peut obtenir des notifications d’événements par le biais d’une interface de rappel. le diagramme suivant illustre ce processus.

![Diagramme conceptuel : l’application et le joueur pointent les uns sur les autres, pointent vers un élément multimédia, qui pointe vers un fichier multimédia](images/mfplay.png)

## <a name="playing-a-media-file"></a>Lit un fichier multimédia

Pour lire un fichier multimédia, appelez la fonction [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) .


```C++
// Global variables
IMFPMediaPlayer *g_pPlayer = NULL;

const WCHAR *sURL = L"C:\\Users\\Public\\Videos\\example.wmv";

HRESULT PlayVideo(HWND hwnd, const WCHAR* sURL)
{
    // Create the player object and play a video file.

    return MFPCreateMediaPlayer(
        sURL,
        TRUE,   // Start playback automatically?
        0,      // Flags.
        NULL,   // Callback pointer.
        hwnd,
        &g_pPlayer
        );
}
```



La fonction [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) crée une nouvelle instance de l’objet MFPlay Player. La fonction accepte les paramètres suivants :

-   Le premier paramètre est l’URL du fichier à ouvrir. Il peut s’agir d’un fichier local ou d’un fichier sur un serveur multimédia.
-   Le deuxième paramètre spécifie si la lecture démarre automatiquement. En affectant la **valeur true** à ce paramètres, le fichier est lu dès que MFPlay le charge.
-   Le troisième paramètre définit diverses options. Pour les options par défaut, transmettez zéro (0).
-   Le quatrième paramètre est un pointeur vers une interface de rappel facultative. Ce paramètre peut avoir la **valeur null**, comme indiqué. Le rappel est décrit dans la section [réception d’événements du lecteur](#receiving-events-from-the-player).
-   Le cinquième paramètre est un handle de la fenêtre d’application. Si le fichier multimédia contient un flux vidéo, la vidéo s’affiche à l’intérieur de la zone cliente de cette fenêtre. Pour la lecture audio uniquement, ce paramètre peut avoir la **valeur null**.

Le dernier paramètre reçoit un pointeur vers l’interface [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) de l’objet Player.

Avant que l’application s’arrête, assurez-vous de libérer le pointeur [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) . Vous pouvez le faire dans le gestionnaire de messages de **\_ fermeture WM** .


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



> [!Note]  
> Cet exemple utilise la fonction [SafeRelease](saferelease.md) pour libérer des pointeurs d’interface.

 

Pour une lecture vidéo simple, c’est tout le code dont vous avez besoin. Le reste de ce didacticiel montre comment ajouter d’autres fonctionnalités, en commençant par la façon de contrôler la lecture.

## <a name="controlling-playback"></a>Contrôle de la lecture

Le code présenté dans la section précédente lira le fichier multimédia jusqu’à ce qu’il atteigne la fin du fichier. Vous pouvez arrêter et démarrer la lecture en appelant les méthodes suivantes sur l’interface [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) :

-   [**IMFPMediaPlayer ::P ause**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-pause) interrompt la lecture. Pendant que la lecture est suspendue, l’image vidéo la plus récente est affichée et l’audio est en mode silencieux.
-   [**IMFPMediaPlayer :: Stop**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-stop) arrête la lecture. Aucune vidéo ne s’affiche et la position de lecture se réinitialise au début du fichier.
-   [**IMFPMediaPlayer ::P**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) marque reprend la lecture après l’arrêt ou la suspension.

Le code suivant suspend ou reprend la lecture lorsque vous appuyez sur la **barre d’espace**.


```C++
//-------------------------------------------------------------------
// OnKeyDown
//
// Handles the WM_KEYDOWN message.
//-------------------------------------------------------------------

void OnKeyDown(HWND hwnd, UINT vk, BOOL fDown, int cRepeat, UINT flags)
{
    HRESULT hr = S_OK;

    switch (vk)
    {
    case VK_SPACE:

        // Toggle between playback and paused/stopped.
        if (g_pPlayer)
        {
            MFP_MEDIAPLAYER_STATE state = MFP_MEDIAPLAYER_STATE_EMPTY;
            
            g_pPlayer->GetState(&state);

            if (state == MFP_MEDIAPLAYER_STATE_PAUSED ||  
                state == MFP_MEDIAPLAYER_STATE_STOPPED)
            {
                g_pPlayer->Play();
            }
            else if (state == MFP_MEDIAPLAYER_STATE_PLAYING)
            {
                g_pPlayer->Pause();
            }
        }
        break;
    }
}
```



Cet exemple appelle la méthode [**IMFPMediaPlayer :: GetState**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getstate) pour récupérer l’état actuel de lecture (suspendu, arrêté ou en cours d’exécution), puis s’interrompt ou reprend en conséquence.

## <a name="receiving-events-from-the-player"></a>Réception d’événements à partir du lecteur

MFPlay utilise une interface de rappel pour envoyer des événements à votre application. Il existe deux raisons pour ce rappel :

-   La lecture se produit sur un thread séparé. Pendant la lecture, certains événements peuvent se produire, tels que l’atteinte de la fin du fichier. MFPlay utilise le rappel pour notifier votre application de l’événement.
-   La plupart des méthodes [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) sont asynchrones, ce qui signifie qu’elles sont retournées avant la fin de l’opération. Les méthodes asynchrones vous permettent de démarrer une opération à partir de votre thread d’interface utilisateur qui peut prendre beaucoup de temps, sans entraîner le blocage de votre interface utilisateur. Une fois l’opération terminée, MFPlay signale le rappel.

Pour recevoir des notifications de rappel, implémentez l’interface [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) . Cette interface hérite de **IUnknown** et définit une méthode unique, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent). Pour configurer le rappel, transmettez un pointeur vers votre implémentation de **IMFPMediaPlayerCallback** dans le paramètre *pCallback* de la fonction [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) .

Voici le premier exemple de ce didacticiel, modifié pour inclure le rappel.


```
// Global variables.
IMFPMediaPlayer *g_pPlayer = NULL;
IMFPMediaPlayerCallback *g_pCallback = NULL;

// Call an application-defined function to create the callback object.
hr = CreateMyCallback(&g_pCallback);

// Create the player object and play a video file.

const WCHAR *sURL = L"C:\\Users\\Public\\Videos\\example.wmv";

if (SUCCEEDED(hr))
{
    hr = MFPCreateMediaPlayer(
        sURL,
        TRUE,        // Start playback automatically?
        0,           // Flags.
        g_pCallback, // Callback pointer.
        hwnd,
        &g_pPlayer
        );
}
```



La méthode [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) a un seul paramètre, qui est un pointeur vers la structure d' [**\_ \_ en-tête d’événement MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) . Le membre **eEventType** de cette structure vous indique quel événement s’est produit. Par exemple, lors du démarrage de la lecture, MFPlay envoie l’événement de **\_ lecture de \_ type \_ d’événement MFP** .

Chaque type d’événement a une structure de données correspondante qui contient des informations pour cet événement. Chacune de ces structures commence par une structure d' [**\_ \_ en-tête d’événement MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) . Dans votre rappel, effectuez un cast du pointeur d' **\_ \_ en-tête d’événement MFP** vers la structure de données spécifique à l’événement. Par exemple, si le type d’événement **est \_ \_ événement MFP Play**, la structure de données est un [**\_ \_ événement MFP Play**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event). Le code suivant montre comment gérer cet événement dans le rappel.


```
void STDMETHODCALLTYPE MediaPlayerCallback::OnMediaPlayerEvent(
    MFP_EVENT_HEADER *pEventHeader
    )
{
    switch (pEventHeader->eEventType)
    {
    case MFP_EVENT_TYPE_PLAY:
        OnPlay(MFP_GET_PLAY_EVENT(pEventHeader));
        break;

    // Other event types (not shown).

    }
}

// Function to handle the event.
void OnPlay(MFP_PLAY_EVENT *pEvent)
{
    if (FAILED(pEvent->header.hrEvent))
    {  
        // Error occurred during playback.
    }  
}
```



Cet exemple utilise l’événement de lecture de l’événement [**MFP \_ \_ Play \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event) pour effectuer un cast du pointeur *pEventHeader* en structure d' [**\_ \_ événement**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) de type MFP. Le **HRESULT** de l’opération qui a déclenché l’événement est stocké dans le champ **hrEvent** de la structure.

Pour obtenir la liste de tous les types d’événements et les structures de données correspondantes, consultez [**\_ \_ type d’événement MFP**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).

Remarque sur le Threading : par défaut, MFPlay appelle le rappel à partir du même thread que celui qui a appelé [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer). Ce thread doit avoir une boucle de message. Vous pouvez également passer l’option MFP Free repartage de l’indicateur de **\_ \_ \_ \_ rappel de thread** dans le paramètre *creationOptions* de **MFPCreateMediaPlayer**. Cet indicateur Force MFPlay à appeler des rappels à partir d’un thread distinct. Les deux options ont des implications pour votre application. L’option par défaut signifie que votre rappel ne peut rien faire qui attend la boucle de message, comme en attente d’une action d’interface utilisateur, car cela bloquera votre procédure de fenêtre. L’option Free-Threaded signifie que vous devez utiliser des sections critiques pour protéger toutes les données auxquelles vous accédez dans votre rappel. Dans la plupart des cas, l’option par défaut est la plus simple.

## <a name="getting-information-about-a-media-file"></a>Obtention d’informations sur un fichier multimédia

Lorsque vous ouvrez un fichier multimédia dans MFPlay, le lecteur crée un objet appelé *élément multimédia* qui représente le fichier multimédia. Cet objet expose l’interface [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) , que vous pouvez utiliser pour obtenir des informations sur le fichier multimédia. La plupart des structures d’événements MFPlay contiennent un pointeur vers l’élément multimédia actuel. Vous pouvez également accéder à l’élément multimédia en cours en appelant [**IMFPMediaPlayer :: GetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmediaitem) sur le lecteur.

Les deux méthodes particulièrement utiles sont [**IMFPMediaItem :: HasVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasvideo) et [**IMFPMediaItem :: HasAudio**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasaudio). Ces méthodes interrogent si la source du média contient des données audio ou vidéo.

Par exemple, le code suivant teste si le fichier multimédia actuel contient un flux vidéo.


```
IMFPMediaItem *pItem;
BOOL bHasVideo = FALSE;
BOOL bIsSelected = FALSE;

hr = g_pPlayer->GetMediaItem(TRUE, &pItem);
if (SUCCEEDED(hr))
{
    hr = pItem->HasVideo(&bHasVideo, &bIsSelected);
    pItem->Release();
}
```



Si le fichier source contient un flux vidéo qui est sélectionné pour la lecture, *bHasVideo* et *bIsSelected* ont tous les deux la valeur **true**.

## <a name="managing-video-playback"></a>Gestion de la lecture vidéo

Quand MFPlay lit un fichier vidéo, il dessine la vidéo dans la fenêtre que vous avez spécifiée dans la fonction [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) . Cela se produit sur un thread distinct détenu par le pipeline de lecture Microsoft Media Foundation. La plupart du temps, votre application n’a pas besoin de gérer ce processus. Toutefois, il existe deux situations dans lesquelles l’application doit notifier MFPlay de mettre à jour la vidéo.

-   Si la lecture est suspendue ou arrêtée, MFPlay doit être averti chaque fois que la fenêtre vidéo de l’application reçoit un \_ message de peinture WM. Cela permet à MFPlay de repeindre la fenêtre.
-   Si la fenêtre est redimensionnée, MFPlay doit être notifié afin de pouvoir mettre la vidéo à l’échelle pour qu’elle corresponde à la nouvelle taille de fenêtre.

La méthode [**IMFPMediaPlayer :: UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) gère les deux cas. Appelez cette méthode à la fois dans les \_ \_ gestionnaires de messages de la peinture WM et de la taille WM pour la fenêtre vidéo.

> [!IMPORTANT]
> Appelez la fonction GDI **BeginPaint** avant d’appeler [**UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).

 


```
IMFPMediaPlayer *g_pPlayer;   // MFPlay player object

void OnSize(HWND hwnd, UINT state, int cx, int cy)
{
    HDC hdc;
    PAINTSTRUCT ps;

    if (g_pPlayer && (state == SIZE_RESTORED))
    {
        hdc = BeginPaint(hwnd, &ps);
        g_pPlayer->UpdateVideo();
         EndPaint(hwnd, &ps);
    }
}

void OnPaint(HWND hwnd)
{
    HDC hdc;
    PAINTSTRUCT ps;

    hdc = BeginPaint(hwnd, &ps);
    if (g_pPlayer)
    {
        g_pPlayer->UpdateVideo();
    }
      EndPaint(hwnd, &ps);
}
```



À moins que vous ne spécifiiez sinon, MFPlay affiche la vidéo aux proportions correctes, en utilisant cadre si nécessaire. Si vous ne souhaitez pas conserver les proportions, appelez [**IMFPMediaPlayer :: SetAspectRatioMode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setaspectratiomode) avec l’indicateur **MFVideoARMode \_ None** . MFPlay étire la vidéo pour remplir l’intégralité du rectangle, sans cadre. En général, vous devez utiliser le paramètre par défaut et laisser MFPlay la vidéo. La couleur par défaut des bandes noires est noire, mais vous pouvez modifier cela en appelant [**IMFPMediaPlayer :: SetBorderColor**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbordercolor).

## <a name="limitations-of-mfplay"></a>Limitations de MFPlay

La version actuelle de MFPlay présente les limitations suivantes :

-   MFPlay ne prend pas en charge le contenu protégé par DRM.
-   Par défaut, MFPlay ne prend pas en charge les protocoles de streaming réseau. Pour plus d’informations, consultez [**IMFPMediaPlayer :: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).
-   MFPlay ne prend pas en charge les sélections côté serveur (SSPLs) ou d’autres types de sources qui lisent plusieurs segments. En termes techniques, MFPlay arrête la lecture après la première présentation et ignore tous les événements [MENewPresentation](menewpresentation.md) de la source du média.
-   MFPlay ne prend pas en charge les transitions transparents entre les sources multimédias.
-   MFPlay ne prend pas en charge le mélange de plusieurs flux vidéo.
-   Seuls les formats multimédias pris en charge en mode natif dans Media Foundation sont pris en charge par MFPlay. (Cela comprend des composants de Media Foundation tiers qui peuvent être installés sur le système.)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de MFPlay pour la lecture audio/vidéo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



