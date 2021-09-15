---
description: Implémentation d’une barre de recherche
ms.assetid: 384f0732-e0c5-4b1f-b590-195e0acf90e1
title: Implémentation d’une barre de recherche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd3f2440c011267c792c79c8bc3550926c5767f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413977"
---
# <a name="implementing-a-seek-bar"></a>Implémentation d’une barre de recherche

Cette section décrit comment implémenter une barre de recherche pour une application de lecteur multimédia. La barre de recherche est implémentée en tant que contrôle TrackBar. pour obtenir une vue d’ensemble de la recherche dans DirectShow, consultez [recherche du Graph de filtre](seeking-the-filter-graph.md).

Lorsque l’application démarre, initialisez le TrackBar :


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



Le TrackBar est désactivé jusqu’à ce que l’utilisateur ouvre un fichier multimédia. La plage TrackBar est définie entre 0 et 100. Pendant la lecture du fichier, l’application calcule la position de lecture en pourcentage de la durée du fichier et met à jour la barre de TrackBar en conséquence. Par exemple, la position TrackBar « 50 » correspond toujours au milieu du fichier.

Lorsque l’utilisateur ouvre un fichier, générez un graphique de lecture de fichier à l’aide de **RenderFile**. Le code correspondant est illustré dans [Comment lire un fichier](how-to-play-a-file.md). interrogez ensuite le gestionnaire de Graph de filtre de l’interface **IMediaSeeking** et stockez le pointeur d’interface :


```C++
IMediaSeeking *g_pSeek = 0;
hr = pGraph->QueryInterface(IID_IMediaSeeking, (void**)&g_pSeek);
```



Pour déterminer si le fichier peut être recherché, appelez la méthode [**IMediaSeeking :: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) ou la méthode [**IMediaSeeking :: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) . Ces méthodes ont presque la même signification, mais leur sémantique est légèrement différente. L’exemple suivant utilise **CheckCapabilites**:


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



L' \_ indicateur AM recherchant \_ CanSeekAbsolute vérifie si le fichier source peut être recherché, et l’indicateur AM Seek \_ \_ CanGetDuration vérifie si la durée du fichier peut être déterminée à l’avance. Si les deux fonctions sont prises en charge, l’application active le TrackBar et récupère la durée du fichier.

Si le graphique est recherché, l’application utilise un minuteur pour mettre à jour la position de la barre de déroulement lors de la lecture. lorsque vous exécutez le graphique de filtre pour lire le fichier, démarrez l’événement du minuteur en appelant l’une des fonctions de minuterie Windows, telles que **SetTimer**. Pour plus d’informations sur les minuteries, consultez la rubrique « timers » dans le kit de développement Platform SDK.


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



Utilisez l’événement du minuteur pour mettre à jour la position du TrackBar. Appelez [**IMediaSeeking :: getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) pour récupérer la position de lecture Currant, puis calculez la position comme un pourcentage de la durée du fichier :


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



L’utilisateur peut également déplacer la barre de TrackBar pour rechercher le fichier. Quand l’utilisateur fait glisser ou clique sur le contrôle TrackBar, l’application reçoit un \_ événement WM HSCROLL. Le mot de poids faible du paramètre *wParam* est le message de notification TrackBar. Par exemple, to \_ ENDTRACK est envoyé à la fin de l’action TrackBar, et to \_ THUMBTRACK est envoyé en continu pendant que l’utilisateur fait glisser le TrackBar. Le code suivant illustre une manière de gérer le \_ message WM HSCROLL :


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



Si l’utilisateur fait glisser le TrackBar, l’application émet une série de commandes Seek, une pour chaque \_ message THUMBTRACK to qu’il reçoit. Pour que les opérations de recherche soient aussi lisses que possible, l’application met en pause le graphique. La suspension du graphique interrompt la lecture, mais garantit la mise à jour de la fenêtre vidéo. Lorsque l’application reçoit le \_ message ENDTRACK to, elle rétablit l’état d’origine du graphique.

 

 



