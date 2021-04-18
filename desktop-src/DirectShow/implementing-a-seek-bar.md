---
description: Implémentation d’une barre de recherche
ms.assetid: 384f0732-e0c5-4b1f-b590-195e0acf90e1
title: Implémentation d’une barre de recherche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd3f2440c011267c792c79c8bc3550926c5767f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522212"
---
# <a name="implementing-a-seek-bar"></a><span data-ttu-id="abac2-103">Implémentation d’une barre de recherche</span><span class="sxs-lookup"><span data-stu-id="abac2-103">Implementing a Seek Bar</span></span>

<span data-ttu-id="abac2-104">Cette section décrit comment implémenter une barre de recherche pour une application de lecteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="abac2-104">This section describes how to implement a seek bar for a media-player application.</span></span> <span data-ttu-id="abac2-105">La barre de recherche est implémentée en tant que contrôle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="abac2-105">The seek bar is implemented as a trackbar control.</span></span> <span data-ttu-id="abac2-106">Pour obtenir une vue d’ensemble de la recherche dans DirectShow, consultez [recherche du graphique de filtre](seeking-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="abac2-106">For an overview of seeking in DirectShow, see [Seeking the Filter Graph](seeking-the-filter-graph.md).</span></span>

<span data-ttu-id="abac2-107">Lorsque l’application démarre, initialisez le TrackBar :</span><span class="sxs-lookup"><span data-stu-id="abac2-107">When the application starts, initialize the trackbar:</span></span>


```C++
void InitSlider(HWND hwnd) 
{
    // Initialize the trackbar range, but disable the 
    // control until the user opens a file.
    hScroll = GetDlgItem(hwnd, IDC_SLIDER1);
    EnableWindow(hScroll, FALSE);
    SendMessage(hScroll, TBM_SETRANGE, TRUE, MAKELONG(0, 100));
}
```



<span data-ttu-id="abac2-108">Le TrackBar est désactivé jusqu’à ce que l’utilisateur ouvre un fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="abac2-108">The trackbar is disabled until the user opens a media file.</span></span> <span data-ttu-id="abac2-109">La plage TrackBar est définie entre 0 et 100.</span><span class="sxs-lookup"><span data-stu-id="abac2-109">The trackbar range is set from 0 to 100.</span></span> <span data-ttu-id="abac2-110">Pendant la lecture du fichier, l’application calcule la position de lecture en pourcentage de la durée du fichier et met à jour la barre de TrackBar en conséquence.</span><span class="sxs-lookup"><span data-stu-id="abac2-110">During file playback, the application will calculate the playback position as a percentage of the file duration, and update the trackbar accordingly.</span></span> <span data-ttu-id="abac2-111">Par exemple, la position TrackBar « 50 » correspond toujours au milieu du fichier.</span><span class="sxs-lookup"><span data-stu-id="abac2-111">For example, trackbar position "50" always corresponds to the middle of the file.</span></span>

<span data-ttu-id="abac2-112">Lorsque l’utilisateur ouvre un fichier, générez un graphique de lecture de fichier à l’aide de **RenderFile**.</span><span class="sxs-lookup"><span data-stu-id="abac2-112">When the user opens a file, build a file-playback graph using **RenderFile**.</span></span> <span data-ttu-id="abac2-113">Le code correspondant est illustré dans [Comment lire un fichier](how-to-play-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="abac2-113">The code for this is shown in [How To Play a File](how-to-play-a-file.md).</span></span> <span data-ttu-id="abac2-114">Interrogez ensuite le gestionnaire de graphe de filtre de l’interface **IMediaSeeking** et stockez le pointeur d’interface :</span><span class="sxs-lookup"><span data-stu-id="abac2-114">Then query the Filter Graph Manager for the **IMediaSeeking** interface and store the interface pointer:</span></span>


```C++
IMediaSeeking *g_pSeek = 0;
hr = pGraph->QueryInterface(IID_IMediaSeeking, (void**)&g_pSeek);
```



<span data-ttu-id="abac2-115">Pour déterminer si le fichier peut être recherché, appelez la méthode [**IMediaSeeking :: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) ou la méthode [**IMediaSeeking :: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="abac2-115">To determine whether the file is seekable, call either the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method or the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span> <span data-ttu-id="abac2-116">Ces méthodes ont presque la même signification, mais leur sémantique est légèrement différente.</span><span class="sxs-lookup"><span data-stu-id="abac2-116">These methods do almost the same thing, but their semantics are slightly different.</span></span> <span data-ttu-id="abac2-117">L’exemple suivant utilise **CheckCapabilites**:</span><span class="sxs-lookup"><span data-stu-id="abac2-117">The following example uses **CheckCapabilites**:</span></span>


```C++
// Determine if the source is seekable.
BOOL  bCanSeek = FALSE;
DWORD caps = AM_SEEKING_CanSeekAbsolute | AM_SEEKING_CanGetDuration; 
bCanSeek = (S_OK == pSeek->CheckCapabilities(&caps));
if (bCanSeek)
{
    // Enable the trackbar.
    EnableWindow(hScroll, TRUE);

    // Find the file duration.
    pSeek->GetDuration(&g_rtTotalTime);
}
```



<span data-ttu-id="abac2-118">L' \_ indicateur AM recherchant \_ CanSeekAbsolute vérifie si le fichier source peut être recherché, et l’indicateur AM Seek \_ \_ CanGetDuration vérifie si la durée du fichier peut être déterminée à l’avance.</span><span class="sxs-lookup"><span data-stu-id="abac2-118">The AM\_SEEKING\_CanSeekAbsolute flag checks whether the source file is seekable, and the AM\_SEEKING\_CanGetDuration flag checks whether the duration of the file can be determined in advance.</span></span> <span data-ttu-id="abac2-119">Si les deux fonctions sont prises en charge, l’application active le TrackBar et récupère la durée du fichier.</span><span class="sxs-lookup"><span data-stu-id="abac2-119">If both of the capabilities are supported, the application enables the trackbar and retrieves the file duration.</span></span>

<span data-ttu-id="abac2-120">Si le graphique est recherché, l’application utilise un minuteur pour mettre à jour la position de la barre de déroulement lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="abac2-120">If the graph is seekable, the application will use a timer to update the trackbar position during playback.</span></span> <span data-ttu-id="abac2-121">Lorsque vous exécutez le graphique de filtre pour lire le fichier, démarrez l’événement du minuteur en appelant l’une des fonctions du minuteur Windows, telles que **SetTimer**.</span><span class="sxs-lookup"><span data-stu-id="abac2-121">When you run the filter graph to play the file, start the timer event by calling one of the Windows timer functions, such as **SetTimer**.</span></span> <span data-ttu-id="abac2-122">Pour plus d’informations sur les minuteries, consultez la rubrique « timers » dans le kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="abac2-122">For more information about timers, see the topic "Timers" in the Platform SDK.</span></span>


```C++
void StartPlayback(HWND hwnd) 
{
    pControl->Run();
    if (bCanSeek)
    {
        StopTimer(); // Make sure an old timer is not still active.
        nTimerID = SetTimer(hwnd, IDT_TIMER1, TICK_FREQ, (TIMERPROC)NULL);
        if (nTimerID == 0)
        {
            /* Handle Error */
        }
    }
}

void StopTimer() 
{
    if (wTimerID != 0)
    {
        KillTimer(g_hwnd, wTimerID);
        wTimerID = 0;
    }
}
```



<span data-ttu-id="abac2-123">Utilisez l’événement du minuteur pour mettre à jour la position du TrackBar.</span><span class="sxs-lookup"><span data-stu-id="abac2-123">Use the timer event to update the position of the trackbar.</span></span> <span data-ttu-id="abac2-124">Appelez [**IMediaSeeking :: getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) pour récupérer la position de lecture Currant, puis calculez la position comme un pourcentage de la durée du fichier :</span><span class="sxs-lookup"><span data-stu-id="abac2-124">Call [**IMediaSeeking::GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) to retrieve the currant playback position, and then calculate the position as a percentage of the file duration:</span></span>


```C++
case WM_TIMER:
    if (wParam == IDT_TIMER1)
    {
        // Timer should not be running unless we really can seek.
        ASSERT(bCanSeek == TRUE);

        REFERENCE_TIME timeNow;
        if (SUCCEEDED(pSeek->GetCurrentPosition(&timeNow)))
        {
            long sliderTick = (long)((timeNow * 100) / g_rtTotalTime);
            SendMessage( hScroll, TBM_SETPOS, TRUE, sliderTick );
        }
    }
    break;
```



<span data-ttu-id="abac2-125">L’utilisateur peut également déplacer la barre de TrackBar pour rechercher le fichier.</span><span class="sxs-lookup"><span data-stu-id="abac2-125">The user can also move the trackbar to seek the file.</span></span> <span data-ttu-id="abac2-126">Quand l’utilisateur fait glisser ou clique sur le contrôle TrackBar, l’application reçoit un \_ événement WM HSCROLL.</span><span class="sxs-lookup"><span data-stu-id="abac2-126">When the user drags or clicks the trackbar control, the application receives a WM\_HSCROLL event.</span></span> <span data-ttu-id="abac2-127">Le mot de poids faible du paramètre *wParam* est le message de notification TrackBar.</span><span class="sxs-lookup"><span data-stu-id="abac2-127">The low word of the *wParam* parameter is the trackbar notification message.</span></span> <span data-ttu-id="abac2-128">Par exemple, to \_ ENDTRACK est envoyé à la fin de l’action TrackBar, et to \_ THUMBTRACK est envoyé en continu pendant que l’utilisateur fait glisser le TrackBar.</span><span class="sxs-lookup"><span data-stu-id="abac2-128">For example, TB\_ENDTRACK is sent at the end of the trackbar action, and TB\_THUMBTRACK is sent continuously while the user drags the trackbar.</span></span> <span data-ttu-id="abac2-129">Le code suivant illustre une manière de gérer le \_ message WM HSCROLL :</span><span class="sxs-lookup"><span data-stu-id="abac2-129">The following code shows one way to handle the WM\_HSCROLL message:</span></span>


```C++
static OAFilterState state;
static BOOL bStartOfScroll = TRUE;

case WM_HSCROLL:
    short int userReq = LOWORD(wParam);
    if (userReq == TB_ENDTRACK || userReq == TB_THUMBTRACK)
    {
        DWORD dwPosition  = SendMessage(hTrackbar, TBM_GETPOS, 0, 0);
        // Pause when the scroll action begins.
        if (bStartOfScroll) 
        {
            pControl->GetState(10, &state);
            bStartOfScroll = FALSE;
            pControl->Pause();
        }
        // Update the position continuously.
        REFERENCE_TIME newTime = (g_rtTotalTime/100) * dwPosition;
        pSeek->SetPositions(&newTime, AM_SEEKING_AbsolutePositioning,
            NULL, AM_SEEKING_NoPositioning);

        // Restore the state at the end.
        if (userReq == TB_ENDTRACK)
        {
            if (state == State_Stopped)
                pControl->Stop();
            else if (state == State_Running) 
                pControl->Run();
            bStartOfScroll = TRUE;
        }
    }
}
```



<span data-ttu-id="abac2-130">Si l’utilisateur fait glisser le TrackBar, l’application émet une série de commandes Seek, une pour chaque \_ message THUMBTRACK to qu’il reçoit.</span><span class="sxs-lookup"><span data-stu-id="abac2-130">If the user drags the trackbar, the application issues a series of seek commands, one for each TB\_THUMBTRACK message that it receives.</span></span> <span data-ttu-id="abac2-131">Pour que les opérations de recherche soient aussi lisses que possible, l’application met en pause le graphique.</span><span class="sxs-lookup"><span data-stu-id="abac2-131">To make the seek operations as smooth as possible, the application pauses the graph.</span></span> <span data-ttu-id="abac2-132">La suspension du graphique interrompt la lecture, mais garantit la mise à jour de la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="abac2-132">Pausing the graph halts playback but ensures that the video window is updated.</span></span> <span data-ttu-id="abac2-133">Lorsque l’application reçoit le \_ message ENDTRACK to, elle rétablit l’état d’origine du graphique.</span><span class="sxs-lookup"><span data-stu-id="abac2-133">When the application receives the TB\_ENDTRACK message, it restores the graph to its original state.</span></span>

 

 



