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
# <a name="getting-started-with-mfplay"></a><span data-ttu-id="1d904-103">Prise en main avec MFPlay</span><span class="sxs-lookup"><span data-stu-id="1d904-103">Getting Started with MFPlay</span></span>

<span data-ttu-id="1d904-104">\[MFPlay peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="1d904-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1d904-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1d904-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="1d904-106">\]</span><span class="sxs-lookup"><span data-stu-id="1d904-106">\]</span></span>

<span data-ttu-id="1d904-107">MFPlay est une API permettant de créer des applications de lecture multimédia en C++.</span><span class="sxs-lookup"><span data-stu-id="1d904-107">MFPlay is an API for creating media playback applications in C++.</span></span>

<span data-ttu-id="1d904-108">Cette rubrique contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="1d904-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="1d904-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d904-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="1d904-110">À propos de MFPlay</span><span class="sxs-lookup"><span data-stu-id="1d904-110">About MFPlay</span></span>](#about-mfplay)
-   [<span data-ttu-id="1d904-111">Lit un fichier multimédia</span><span class="sxs-lookup"><span data-stu-id="1d904-111">Playing a Media File</span></span>](#playing-a-media-file)
-   [<span data-ttu-id="1d904-112">Contrôle de la lecture</span><span class="sxs-lookup"><span data-stu-id="1d904-112">Controlling Playback</span></span>](#controlling-playback)
-   [<span data-ttu-id="1d904-113">Réception d’événements à partir du lecteur</span><span class="sxs-lookup"><span data-stu-id="1d904-113">Receiving Events From the Player</span></span>](#receiving-events-from-the-player)
-   [<span data-ttu-id="1d904-114">Obtention d’informations sur un fichier multimédia</span><span class="sxs-lookup"><span data-stu-id="1d904-114">Getting Information About a Media File</span></span>](#getting-information-about-a-media-file)
-   [<span data-ttu-id="1d904-115">Gestion de la lecture vidéo</span><span class="sxs-lookup"><span data-stu-id="1d904-115">Managing Video Playback</span></span>](#managing-video-playback)
-   [<span data-ttu-id="1d904-116">Limitations de MFPlay</span><span class="sxs-lookup"><span data-stu-id="1d904-116">Limitations of MFPlay</span></span>](#limitations-of-mfplay)
-   [<span data-ttu-id="1d904-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1d904-117">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="1d904-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d904-118">Requirements</span></span>

<span data-ttu-id="1d904-119">MFPlay requiert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1d904-119">MFPlay requires Windows 7.</span></span>

## <a name="about-mfplay"></a><span data-ttu-id="1d904-120">À propos de MFPlay</span><span class="sxs-lookup"><span data-stu-id="1d904-120">About MFPlay</span></span>

<span data-ttu-id="1d904-121">MFPlay a un modèle de programmation simple, tout en fournissant l’ensemble principal de fonctionnalités dont la plupart des applications de lecture ont besoin.</span><span class="sxs-lookup"><span data-stu-id="1d904-121">MFPlay has a simple programming model, while providing the core set of features that most playback applications need.</span></span> <span data-ttu-id="1d904-122">Une application crée un objet *Player* qui contrôle la lecture.</span><span class="sxs-lookup"><span data-stu-id="1d904-122">An application creates a *player* object that controls playback.</span></span> <span data-ttu-id="1d904-123">Pour lire un fichier multimédia, l’objet Player crée un *élément multimédia*, qui peut être utilisé pour obtenir des informations sur le contenu du fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="1d904-123">To play a media file, the player object creates a *media item*, which can be used to get information about the contents of the media file.</span></span> <span data-ttu-id="1d904-124">L’application contrôle la lecture via des méthodes sur l’interface [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) de l’objet Player.</span><span class="sxs-lookup"><span data-stu-id="1d904-124">The application controls playback through methods on the player object's [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface.</span></span> <span data-ttu-id="1d904-125">Si vous le souhaitez, l’application peut obtenir des notifications d’événements par le biais d’une interface de rappel. le diagramme suivant illustre ce processus.</span><span class="sxs-lookup"><span data-stu-id="1d904-125">Optionally, the application can get event notifications through a callback interface The following diagram illustrates this process.</span></span>

![Diagramme conceptuel : l’application et le joueur pointent les uns sur les autres, pointent vers un élément multimédia, qui pointe vers un fichier multimédia](images/mfplay.png)

## <a name="playing-a-media-file"></a><span data-ttu-id="1d904-127">Lit un fichier multimédia</span><span class="sxs-lookup"><span data-stu-id="1d904-127">Playing a Media File</span></span>

<span data-ttu-id="1d904-128">Pour lire un fichier multimédia, appelez la fonction [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) .</span><span class="sxs-lookup"><span data-stu-id="1d904-128">To play a media file, call the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function.</span></span>


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



<span data-ttu-id="1d904-129">La fonction [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) crée une nouvelle instance de l’objet MFPlay Player.</span><span class="sxs-lookup"><span data-stu-id="1d904-129">The [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function creates a new instance of the MFPlay player object.</span></span> <span data-ttu-id="1d904-130">La fonction accepte les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="1d904-130">The function takes the following parameters:</span></span>

-   <span data-ttu-id="1d904-131">Le premier paramètre est l’URL du fichier à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="1d904-131">The first parameter is the URL of the file to open.</span></span> <span data-ttu-id="1d904-132">Il peut s’agir d’un fichier local ou d’un fichier sur un serveur multimédia.</span><span class="sxs-lookup"><span data-stu-id="1d904-132">This can be a local file or a file on a media server.</span></span>
-   <span data-ttu-id="1d904-133">Le deuxième paramètre spécifie si la lecture démarre automatiquement.</span><span class="sxs-lookup"><span data-stu-id="1d904-133">The second parameter specifies whether playback starts automatically.</span></span> <span data-ttu-id="1d904-134">En affectant la **valeur true** à ce paramètres, le fichier est lu dès que MFPlay le charge.</span><span class="sxs-lookup"><span data-stu-id="1d904-134">By setting this paremeter to **TRUE**, the file will play as soon as MFPlay loads it.</span></span>
-   <span data-ttu-id="1d904-135">Le troisième paramètre définit diverses options.</span><span class="sxs-lookup"><span data-stu-id="1d904-135">The third parameter sets various options.</span></span> <span data-ttu-id="1d904-136">Pour les options par défaut, transmettez zéro (0).</span><span class="sxs-lookup"><span data-stu-id="1d904-136">For the default options, pass zero (0).</span></span>
-   <span data-ttu-id="1d904-137">Le quatrième paramètre est un pointeur vers une interface de rappel facultative.</span><span class="sxs-lookup"><span data-stu-id="1d904-137">The fourth parameter is a pointer to an optional callback interface.</span></span> <span data-ttu-id="1d904-138">Ce paramètre peut avoir la **valeur null**, comme indiqué.</span><span class="sxs-lookup"><span data-stu-id="1d904-138">This parameter can be **NULL**, as shown.</span></span> <span data-ttu-id="1d904-139">Le rappel est décrit dans la section [réception d’événements du lecteur](#receiving-events-from-the-player).</span><span class="sxs-lookup"><span data-stu-id="1d904-139">The callback is described in the section [Receiving Events From the Player](#receiving-events-from-the-player).</span></span>
-   <span data-ttu-id="1d904-140">Le cinquième paramètre est un handle de la fenêtre d’application.</span><span class="sxs-lookup"><span data-stu-id="1d904-140">The fifth parameter is a handle to the application window.</span></span> <span data-ttu-id="1d904-141">Si le fichier multimédia contient un flux vidéo, la vidéo s’affiche à l’intérieur de la zone cliente de cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="1d904-141">If the media file contains a video stream, the video will appear inside the client area of this window.</span></span> <span data-ttu-id="1d904-142">Pour la lecture audio uniquement, ce paramètre peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="1d904-142">For audio-only playback, this parameter can be **NULL**.</span></span>

<span data-ttu-id="1d904-143">Le dernier paramètre reçoit un pointeur vers l’interface [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) de l’objet Player.</span><span class="sxs-lookup"><span data-stu-id="1d904-143">The last parameter receives a pointer to the player object's [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface.</span></span>

<span data-ttu-id="1d904-144">Avant que l’application s’arrête, assurez-vous de libérer le pointeur [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) .</span><span class="sxs-lookup"><span data-stu-id="1d904-144">Before the application shuts down, be sure to release the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) pointer.</span></span> <span data-ttu-id="1d904-145">Vous pouvez le faire dans le gestionnaire de messages de **\_ fermeture WM** .</span><span class="sxs-lookup"><span data-stu-id="1d904-145">You can do this in your **WM\_CLOSE** message handler.</span></span>


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



> [!Note]  
> <span data-ttu-id="1d904-146">Cet exemple utilise la fonction [SafeRelease](saferelease.md) pour libérer des pointeurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="1d904-146">This example uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

<span data-ttu-id="1d904-147">Pour une lecture vidéo simple, c’est tout le code dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="1d904-147">For simple video playback, that's all the code you need.</span></span> <span data-ttu-id="1d904-148">Le reste de ce didacticiel montre comment ajouter d’autres fonctionnalités, en commençant par la façon de contrôler la lecture.</span><span class="sxs-lookup"><span data-stu-id="1d904-148">The rest of this tutorial will show how to add more features, starting with how to control playback.</span></span>

## <a name="controlling-playback"></a><span data-ttu-id="1d904-149">Contrôle de la lecture</span><span class="sxs-lookup"><span data-stu-id="1d904-149">Controlling Playback</span></span>

<span data-ttu-id="1d904-150">Le code présenté dans la section précédente lira le fichier multimédia jusqu’à ce qu’il atteigne la fin du fichier.</span><span class="sxs-lookup"><span data-stu-id="1d904-150">The code shown in the previous section will play the media file until it reaches the end of the file.</span></span> <span data-ttu-id="1d904-151">Vous pouvez arrêter et démarrer la lecture en appelant les méthodes suivantes sur l’interface [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) :</span><span class="sxs-lookup"><span data-stu-id="1d904-151">You can stop and start playback by calling the following methods on the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface:</span></span>

-   <span data-ttu-id="1d904-152">[**IMFPMediaPlayer ::P ause**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-pause) interrompt la lecture.</span><span class="sxs-lookup"><span data-stu-id="1d904-152">[**IMFPMediaPlayer::Pause**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-pause) pauses playback.</span></span> <span data-ttu-id="1d904-153">Pendant que la lecture est suspendue, l’image vidéo la plus récente est affichée et l’audio est en mode silencieux.</span><span class="sxs-lookup"><span data-stu-id="1d904-153">While playback is paused, the most recent video frame is displayed, and audio is silent.</span></span>
-   <span data-ttu-id="1d904-154">[**IMFPMediaPlayer :: Stop**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-stop) arrête la lecture.</span><span class="sxs-lookup"><span data-stu-id="1d904-154">[**IMFPMediaPlayer::Stop**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-stop) stops playback.</span></span> <span data-ttu-id="1d904-155">Aucune vidéo ne s’affiche et la position de lecture se réinitialise au début du fichier.</span><span class="sxs-lookup"><span data-stu-id="1d904-155">No video is displayed, and the playback position resets to the start of the file.</span></span>
-   <span data-ttu-id="1d904-156">[**IMFPMediaPlayer ::P**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) marque reprend la lecture après l’arrêt ou la suspension.</span><span class="sxs-lookup"><span data-stu-id="1d904-156">[**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) resumes playback after stopping or pausing.</span></span>

<span data-ttu-id="1d904-157">Le code suivant suspend ou reprend la lecture lorsque vous appuyez sur la **barre d’espace**.</span><span class="sxs-lookup"><span data-stu-id="1d904-157">The following code pauses or resumes playback when you press the **SPACEBAR**.</span></span>


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



<span data-ttu-id="1d904-158">Cet exemple appelle la méthode [**IMFPMediaPlayer :: GetState**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getstate) pour récupérer l’état actuel de lecture (suspendu, arrêté ou en cours d’exécution), puis s’interrompt ou reprend en conséquence.</span><span class="sxs-lookup"><span data-stu-id="1d904-158">This example calls the [**IMFPMediaPlayer::GetState**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getstate) method to get the current playback state (paused, stopped, or playing) and pauses or resumes accordingly.</span></span>

## <a name="receiving-events-from-the-player"></a><span data-ttu-id="1d904-159">Réception d’événements à partir du lecteur</span><span class="sxs-lookup"><span data-stu-id="1d904-159">Receiving Events From the Player</span></span>

<span data-ttu-id="1d904-160">MFPlay utilise une interface de rappel pour envoyer des événements à votre application.</span><span class="sxs-lookup"><span data-stu-id="1d904-160">MFPlay uses a callback interface to send events to your application.</span></span> <span data-ttu-id="1d904-161">Il existe deux raisons pour ce rappel :</span><span class="sxs-lookup"><span data-stu-id="1d904-161">There are two reasons for this callback:</span></span>

-   <span data-ttu-id="1d904-162">La lecture se produit sur un thread séparé.</span><span class="sxs-lookup"><span data-stu-id="1d904-162">Playback occurs on a separate thread.</span></span> <span data-ttu-id="1d904-163">Pendant la lecture, certains événements peuvent se produire, tels que l’atteinte de la fin du fichier.</span><span class="sxs-lookup"><span data-stu-id="1d904-163">During playback, certain events might occur, such as reaching the end of the file.</span></span> <span data-ttu-id="1d904-164">MFPlay utilise le rappel pour notifier votre application de l’événement.</span><span class="sxs-lookup"><span data-stu-id="1d904-164">MFPlay uses the callback to notify your application of the event.</span></span>
-   <span data-ttu-id="1d904-165">La plupart des méthodes [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) sont asynchrones, ce qui signifie qu’elles sont retournées avant la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="1d904-165">Many of the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) methods are asynchronous, meaning they return before the operation completes.</span></span> <span data-ttu-id="1d904-166">Les méthodes asynchrones vous permettent de démarrer une opération à partir de votre thread d’interface utilisateur qui peut prendre beaucoup de temps, sans entraîner le blocage de votre interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1d904-166">Asynchronous methods let you start an operation from your UI thread that might take a long time to complete, without it causing your UI to block.</span></span> <span data-ttu-id="1d904-167">Une fois l’opération terminée, MFPlay signale le rappel.</span><span class="sxs-lookup"><span data-stu-id="1d904-167">After the operation completes, MFPlay signals the callback.</span></span>

<span data-ttu-id="1d904-168">Pour recevoir des notifications de rappel, implémentez l’interface [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) .</span><span class="sxs-lookup"><span data-stu-id="1d904-168">To receive callback notifications, implement the [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface.</span></span> <span data-ttu-id="1d904-169">Cette interface hérite de **IUnknown** et définit une méthode unique, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span><span class="sxs-lookup"><span data-stu-id="1d904-169">This interface inherits **IUnknown** and defines a single method, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span></span> <span data-ttu-id="1d904-170">Pour configurer le rappel, transmettez un pointeur vers votre implémentation de **IMFPMediaPlayerCallback** dans le paramètre *pCallback* de la fonction [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) .</span><span class="sxs-lookup"><span data-stu-id="1d904-170">To set up the callback, pass a pointer to your **IMFPMediaPlayerCallback** implementation in the *pCallback* parameter of the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function.</span></span>

<span data-ttu-id="1d904-171">Voici le premier exemple de ce didacticiel, modifié pour inclure le rappel.</span><span class="sxs-lookup"><span data-stu-id="1d904-171">Here is the first example from this tutorial, modified to include the callback.</span></span>


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



<span data-ttu-id="1d904-172">La méthode [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) a un seul paramètre, qui est un pointeur vers la structure d' [**\_ \_ en-tête d’événement MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) .</span><span class="sxs-lookup"><span data-stu-id="1d904-172">The [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) method has a single parameter, which is a pointer to the [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure.</span></span> <span data-ttu-id="1d904-173">Le membre **eEventType** de cette structure vous indique quel événement s’est produit.</span><span class="sxs-lookup"><span data-stu-id="1d904-173">The **eEventType** member of this structure tells you which event occurred.</span></span> <span data-ttu-id="1d904-174">Par exemple, lors du démarrage de la lecture, MFPlay envoie l’événement de **\_ lecture de \_ type \_ d’événement MFP** .</span><span class="sxs-lookup"><span data-stu-id="1d904-174">For example, when playback starts, MFPlay sends the **MFP\_EVENT\_TYPE\_PLAY** event.</span></span>

<span data-ttu-id="1d904-175">Chaque type d’événement a une structure de données correspondante qui contient des informations pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="1d904-175">Each event type has a corresponding data structure that contains information for that event.</span></span> <span data-ttu-id="1d904-176">Chacune de ces structures commence par une structure d' [**\_ \_ en-tête d’événement MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) .</span><span class="sxs-lookup"><span data-stu-id="1d904-176">Each of these structures starts with an [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure.</span></span> <span data-ttu-id="1d904-177">Dans votre rappel, effectuez un cast du pointeur d' **\_ \_ en-tête d’événement MFP** vers la structure de données spécifique à l’événement.</span><span class="sxs-lookup"><span data-stu-id="1d904-177">In your callback, cast the **MFP\_EVENT\_HEADER** pointer to the event-specific data structure.</span></span> <span data-ttu-id="1d904-178">Par exemple, si le type d’événement **est \_ \_ événement MFP Play**, la structure de données est un [**\_ \_ événement MFP Play**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event).</span><span class="sxs-lookup"><span data-stu-id="1d904-178">For example, if the event type is **MFP\_PLAY\_EVENT**, the data structure is [**MFP\_PLAY\_EVENT**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event).</span></span> <span data-ttu-id="1d904-179">Le code suivant montre comment gérer cet événement dans le rappel.</span><span class="sxs-lookup"><span data-stu-id="1d904-179">The following code shows how to handle this event in the callback.</span></span>


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



<span data-ttu-id="1d904-180">Cet exemple utilise l’événement de lecture de l’événement [**MFP \_ \_ Play \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event) pour effectuer un cast du pointeur *pEventHeader* en structure d' [**\_ \_ événement**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) de type MFP.</span><span class="sxs-lookup"><span data-stu-id="1d904-180">This example uses the [**MFP\_GET\_PLAY\_EVENT**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event) event to cast the *pEventHeader* pointer to an [**MFP\_PLAY\_EVENT**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) structure.</span></span> <span data-ttu-id="1d904-181">Le **HRESULT** de l’opération qui a déclenché l’événement est stocké dans le champ **hrEvent** de la structure.</span><span class="sxs-lookup"><span data-stu-id="1d904-181">The **HRESULT** from the operation that triggered the event is stored in the **hrEvent** field of the structure.</span></span>

<span data-ttu-id="1d904-182">Pour obtenir la liste de tous les types d’événements et les structures de données correspondantes, consultez [**\_ \_ type d’événement MFP**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).</span><span class="sxs-lookup"><span data-stu-id="1d904-182">For a list of all the event types and the corresponding data structures, see [**MFP\_EVENT\_TYPE**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).</span></span>

<span data-ttu-id="1d904-183">Remarque sur le Threading : par défaut, MFPlay appelle le rappel à partir du même thread que celui qui a appelé [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer).</span><span class="sxs-lookup"><span data-stu-id="1d904-183">A note about threading: By default, MFPlay invokes the callback from the same thread that called [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer).</span></span> <span data-ttu-id="1d904-184">Ce thread doit avoir une boucle de message.</span><span class="sxs-lookup"><span data-stu-id="1d904-184">This thread must have a message loop.</span></span> <span data-ttu-id="1d904-185">Vous pouvez également passer l’option MFP Free repartage de l’indicateur de **\_ \_ \_ \_ rappel de thread** dans le paramètre *creationOptions* de **MFPCreateMediaPlayer**.</span><span class="sxs-lookup"><span data-stu-id="1d904-185">Alternatively, you can pass the **MFP\_OPTION\_FREE\_THREADED\_CALLBACK** flag in the *creationOptions* parameter of **MFPCreateMediaPlayer**.</span></span> <span data-ttu-id="1d904-186">Cet indicateur Force MFPlay à appeler des rappels à partir d’un thread distinct.</span><span class="sxs-lookup"><span data-stu-id="1d904-186">This flag causes MFPlay to invoke callbacks from a separate thread.</span></span> <span data-ttu-id="1d904-187">Les deux options ont des implications pour votre application.</span><span class="sxs-lookup"><span data-stu-id="1d904-187">Either option has implications for your application.</span></span> <span data-ttu-id="1d904-188">L’option par défaut signifie que votre rappel ne peut rien faire qui attend la boucle de message, comme en attente d’une action d’interface utilisateur, car cela bloquera votre procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="1d904-188">The default option means your callback cannot do anything that waits on your message loop, such as waiting for a UI action, because that will block your window procedure.</span></span> <span data-ttu-id="1d904-189">L’option Free-Threaded signifie que vous devez utiliser des sections critiques pour protéger toutes les données auxquelles vous accédez dans votre rappel.</span><span class="sxs-lookup"><span data-stu-id="1d904-189">The free-threaded option means you need to use critical sections to protect any data that you access in your callback.</span></span> <span data-ttu-id="1d904-190">Dans la plupart des cas, l’option par défaut est la plus simple.</span><span class="sxs-lookup"><span data-stu-id="1d904-190">In most cases, the default option is simplest.</span></span>

## <a name="getting-information-about-a-media-file"></a><span data-ttu-id="1d904-191">Obtention d’informations sur un fichier multimédia</span><span class="sxs-lookup"><span data-stu-id="1d904-191">Getting Information About a Media File</span></span>

<span data-ttu-id="1d904-192">Lorsque vous ouvrez un fichier multimédia dans MFPlay, le lecteur crée un objet appelé *élément multimédia* qui représente le fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="1d904-192">When you open a media file in MFPlay, the player creates an object called a *media item* that represents the media file.</span></span> <span data-ttu-id="1d904-193">Cet objet expose l’interface [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) , que vous pouvez utiliser pour obtenir des informations sur le fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="1d904-193">This object exposes the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface, which you can use to get information about the media file.</span></span> <span data-ttu-id="1d904-194">La plupart des structures d’événements MFPlay contiennent un pointeur vers l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="1d904-194">Many of the MFPlay event structures contain a pointer to the current media item.</span></span> <span data-ttu-id="1d904-195">Vous pouvez également accéder à l’élément multimédia en cours en appelant [**IMFPMediaPlayer :: GetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmediaitem) sur le lecteur.</span><span class="sxs-lookup"><span data-stu-id="1d904-195">You can also get the current media item by calling [**IMFPMediaPlayer::GetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmediaitem) on the player.</span></span>

<span data-ttu-id="1d904-196">Les deux méthodes particulièrement utiles sont [**IMFPMediaItem :: HasVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasvideo) et [**IMFPMediaItem :: HasAudio**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasaudio).</span><span class="sxs-lookup"><span data-stu-id="1d904-196">Two particularly useful methods are [**IMFPMediaItem::HasVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasvideo) and [**IMFPMediaItem::HasAudio**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasaudio).</span></span> <span data-ttu-id="1d904-197">Ces méthodes interrogent si la source du média contient des données audio ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="1d904-197">These methods query whether the media source contains video or audio.</span></span>

<span data-ttu-id="1d904-198">Par exemple, le code suivant teste si le fichier multimédia actuel contient un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="1d904-198">For example, the following code tests whether the current media file contains a video stream.</span></span>


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



<span data-ttu-id="1d904-199">Si le fichier source contient un flux vidéo qui est sélectionné pour la lecture, *bHasVideo* et *bIsSelected* ont tous les deux la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="1d904-199">If the source file contains a video stream that is selected for playback, *bHasVideo* and *bIsSelected* are both set to **TRUE**.</span></span>

## <a name="managing-video-playback"></a><span data-ttu-id="1d904-200">Gestion de la lecture vidéo</span><span class="sxs-lookup"><span data-stu-id="1d904-200">Managing Video Playback</span></span>

<span data-ttu-id="1d904-201">Quand MFPlay lit un fichier vidéo, il dessine la vidéo dans la fenêtre que vous avez spécifiée dans la fonction [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) .</span><span class="sxs-lookup"><span data-stu-id="1d904-201">When MFPlay plays a video file, it draws the video in the window that you specified in the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function.</span></span> <span data-ttu-id="1d904-202">Cela se produit sur un thread distinct détenu par le pipeline de lecture Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="1d904-202">This occurs on a separate thread owned by the Microsoft Media Foundation playback pipeline.</span></span> <span data-ttu-id="1d904-203">La plupart du temps, votre application n’a pas besoin de gérer ce processus.</span><span class="sxs-lookup"><span data-stu-id="1d904-203">For the most part, your application does not need to manage this process.</span></span> <span data-ttu-id="1d904-204">Toutefois, il existe deux situations dans lesquelles l’application doit notifier MFPlay de mettre à jour la vidéo.</span><span class="sxs-lookup"><span data-stu-id="1d904-204">However, there are two situations where the application must notify MFPlay to update the video.</span></span>

-   <span data-ttu-id="1d904-205">Si la lecture est suspendue ou arrêtée, MFPlay doit être averti chaque fois que la fenêtre vidéo de l’application reçoit un \_ message de peinture WM.</span><span class="sxs-lookup"><span data-stu-id="1d904-205">If playback is paused or stopped, MFPlay must be notified whenever the application's video window receives a WM\_PAINT message.</span></span> <span data-ttu-id="1d904-206">Cela permet à MFPlay de repeindre la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="1d904-206">This allows MFPlay to repaint the window.</span></span>
-   <span data-ttu-id="1d904-207">Si la fenêtre est redimensionnée, MFPlay doit être notifié afin de pouvoir mettre la vidéo à l’échelle pour qu’elle corresponde à la nouvelle taille de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="1d904-207">If the window is resized, MFPlay must be notified so that it can scale the video to match the new window size.</span></span>

<span data-ttu-id="1d904-208">La méthode [**IMFPMediaPlayer :: UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) gère les deux cas.</span><span class="sxs-lookup"><span data-stu-id="1d904-208">The [**IMFPMediaPlayer::UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) method handles both cases.</span></span> <span data-ttu-id="1d904-209">Appelez cette méthode à la fois dans les \_ \_ gestionnaires de messages de la peinture WM et de la taille WM pour la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="1d904-209">Call this method inside both the WM\_PAINT and WM\_SIZE message handlers for the video window.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1d904-210">Appelez la fonction GDI **BeginPaint** avant d’appeler [**UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).</span><span class="sxs-lookup"><span data-stu-id="1d904-210">Call the GDI **BeginPaint** function before calling [**UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).</span></span>

 


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



<span data-ttu-id="1d904-211">À moins que vous ne spécifiiez sinon, MFPlay affiche la vidéo aux proportions correctes, en utilisant cadre si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1d904-211">Unless you specify otherwise, MFPlay shows the video at the correct aspect ratio, using letterboxing if needed.</span></span> <span data-ttu-id="1d904-212">Si vous ne souhaitez pas conserver les proportions, appelez [**IMFPMediaPlayer :: SetAspectRatioMode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setaspectratiomode) avec l’indicateur **MFVideoARMode \_ None** .</span><span class="sxs-lookup"><span data-stu-id="1d904-212">If you do not want to preserve the aspect ratio, call [**IMFPMediaPlayer::SetAspectRatioMode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setaspectratiomode) with the **MFVideoARMode\_None** flag.</span></span> <span data-ttu-id="1d904-213">MFPlay étire la vidéo pour remplir l’intégralité du rectangle, sans cadre.</span><span class="sxs-lookup"><span data-stu-id="1d904-213">This will cause MFPlay to stretch the video to fill the entire rectangle, with no letterboxing.</span></span> <span data-ttu-id="1d904-214">En général, vous devez utiliser le paramètre par défaut et laisser MFPlay la vidéo.</span><span class="sxs-lookup"><span data-stu-id="1d904-214">Typically you should use the default setting and let MFPlay letterbox the video.</span></span> <span data-ttu-id="1d904-215">La couleur par défaut des bandes noires est noire, mais vous pouvez modifier cela en appelant [**IMFPMediaPlayer :: SetBorderColor**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbordercolor).</span><span class="sxs-lookup"><span data-stu-id="1d904-215">The default letterbox color is black, but you can change this by calling [**IMFPMediaPlayer::SetBorderColor**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbordercolor).</span></span>

## <a name="limitations-of-mfplay"></a><span data-ttu-id="1d904-216">Limitations de MFPlay</span><span class="sxs-lookup"><span data-stu-id="1d904-216">Limitations of MFPlay</span></span>

<span data-ttu-id="1d904-217">La version actuelle de MFPlay présente les limitations suivantes :</span><span class="sxs-lookup"><span data-stu-id="1d904-217">The current version of MFPlay has the following limitations:</span></span>

-   <span data-ttu-id="1d904-218">MFPlay ne prend pas en charge le contenu protégé par DRM.</span><span class="sxs-lookup"><span data-stu-id="1d904-218">MFPlay does not support DRM-protected content.</span></span>
-   <span data-ttu-id="1d904-219">Par défaut, MFPlay ne prend pas en charge les protocoles de streaming réseau.</span><span class="sxs-lookup"><span data-stu-id="1d904-219">By default, MFPlay does not support network streaming protocols.</span></span> <span data-ttu-id="1d904-220">Pour plus d’informations, consultez [**IMFPMediaPlayer :: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).</span><span class="sxs-lookup"><span data-stu-id="1d904-220">For more information, see [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).</span></span>
-   <span data-ttu-id="1d904-221">MFPlay ne prend pas en charge les sélections côté serveur (SSPLs) ou d’autres types de sources qui lisent plusieurs segments.</span><span class="sxs-lookup"><span data-stu-id="1d904-221">MFPlay does not support server-side playlists (SSPLs) or other types of source that play more than one segment.</span></span> <span data-ttu-id="1d904-222">En termes techniques, MFPlay arrête la lecture après la première présentation et ignore tous les événements [MENewPresentation](menewpresentation.md) de la source du média.</span><span class="sxs-lookup"><span data-stu-id="1d904-222">In technical terms, MFPlay stops playback after the first presentation, and ignores any [MENewPresentation](menewpresentation.md) events from the media source.</span></span>
-   <span data-ttu-id="1d904-223">MFPlay ne prend pas en charge les transitions transparents entre les sources multimédias.</span><span class="sxs-lookup"><span data-stu-id="1d904-223">MFPlay does not support seamless transitions between media sources.</span></span>
-   <span data-ttu-id="1d904-224">MFPlay ne prend pas en charge le mélange de plusieurs flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="1d904-224">MFPlay does not support mixing multiple video streams.</span></span>
-   <span data-ttu-id="1d904-225">Seuls les formats multimédias pris en charge en mode natif dans Media Foundation sont pris en charge par MFPlay.</span><span class="sxs-lookup"><span data-stu-id="1d904-225">Only media formats supported natively in Media Foundation are supported by MFPlay.</span></span> <span data-ttu-id="1d904-226">(Cela comprend des composants de Media Foundation tiers qui peuvent être installés sur le système.)</span><span class="sxs-lookup"><span data-stu-id="1d904-226">(This includes third-party Media Foundation components that might be installed on the system.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d904-227">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1d904-227">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d904-228">Utilisation de MFPlay pour la lecture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="1d904-228">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



