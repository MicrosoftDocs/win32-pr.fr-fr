---
description: Cette rubrique montre comment créer et détruire des minuteries, et comment utiliser un minuteur pour intercepter l’entrée de la souris à des intervalles spécifiés.
ms.assetid: eee54078-759f-4fd4-9cf4-10a8bde888b7
title: Utilisation de minuteurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7922be60012ae81ce1971afe6f2300f54689f7a6cc8d7f088df2fb126e834ab5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028307"
---
# <a name="using-timers"></a>Utilisation de minuteurs

Cette rubrique montre comment créer et détruire des minuteries, et comment utiliser un minuteur pour intercepter l’entrée de la souris à des intervalles spécifiés.

Cette rubrique contient les sections suivantes.

-   [Création d’un minuteur](#creating-a-timer)
-   [Destruction d’un minuteur](#destroying-a-timer)
-   [Utilisation des fonctions de minuterie pour intercepter l’entrée de la souris](#using-timer-functions-to-trap-mouse-input)
-   [Rubriques connexes](#related-topics)

## <a name="creating-a-timer"></a>Création d’un minuteur

L’exemple suivant utilise la fonction [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) pour créer deux minuteries. La première minuterie est définie toutes les 10 secondes, la seconde pour toutes les cinq minutes.


```
// Set two timers. 
 
SetTimer(hwnd,             // handle to main window 
    IDT_TIMER1,            // timer identifier 
    10000,                 // 10-second interval 
    (TIMERPROC) NULL);     // no timer callback 
 
SetTimer(hwnd,             // handle to main window 
    IDT_TIMER2,            // timer identifier 
    300000,                // five-minute interval 
    (TIMERPROC) NULL);     // no timer callback 
```



Pour traiter les messages du [**\_ minuteur WM**](wm-timer.md) générés par ces minuteurs, ajoutez une instruction de cas de **\_ minuterie WM** à la procédure de fenêtre pour le paramètre *HWND* .


```
case WM_TIMER: 
 
    switch (wParam) 
    { 
        case IDT_TIMER1: 
            // process the 10-second timer 
 
             return 0; 
 
        case IDT_TIMER2: 
            // process the five-minute timer 

            return 0; 
    } 
```



Une application peut également créer un minuteur dont les messages [**\_ du minuteur WM**](wm-timer.md) ne sont pas traités par la procédure de fenêtre principale, mais par une fonction de rappel définie par l’application, comme dans l’exemple de code suivant, qui crée un minuteur et utilise la fonction de rappel **MyTimerProc** pour traiter les messages du **\_ minuteur WM** de la minuterie.


```
// Set the timer. 
 
SetTimer(hwnd,                // handle to main window 
    IDT_TIMER3,               // timer identifier 
    5000,                     // 5-second interval 
    (TIMERPROC) MyTimerProc); // timer callback
```



La Convention d’appel pour **MyTimerProc** doit être basée sur la fonction de rappel [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) .

Si votre application crée un minuteur sans spécifier de handle de fenêtre, votre application doit surveiller la file d’attente de messages pour les messages [**\_ du minuteur WM**](wm-timer.md) et les distribuer à la fenêtre appropriée.


```
HWND hwndTimer;   // handle to window for timer messages 
MSG msg;          // message structure 
 
    while (GetMessage(&msg, // message structure 
            NULL,           // handle to window to receive the message 
               0,           // lowest message to examine 
               0))          // highest message to examine 
    { 
 
        // Post WM_TIMER messages to the hwndTimer procedure. 
 
        if (msg.message == WM_TIMER) 
        { 
            msg.hwnd = hwndTimer; 
        } 
 
        TranslateMessage(&msg); // translates virtual-key codes 
        DispatchMessage(&msg);  // dispatches message to window 
    } 
```



## <a name="destroying-a-timer"></a>Destruction d’un minuteur

Les applications doivent utiliser la fonction [**KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) pour détruire les minuteurs qui ne sont plus nécessaires. L’exemple ci-dessous détruit les minuteries identifiées par les constantes IDT \_ Timer1, IDT \_ TIMER2 et IDT \_ TIMER3.


```
// Destroy the timers. 
 
KillTimer(hwnd, IDT_TIMER1); 
KillTimer(hwnd, IDT_TIMER2); 
KillTimer(hwnd, IDT_TIMER3); 
```



## <a name="using-timer-functions-to-trap-mouse-input"></a>Utilisation des fonctions de minuterie pour intercepter l’entrée de la souris

Il est parfois nécessaire d’éviter une entrée supplémentaire pendant que vous avez un pointeur de souris sur l’écran. Une façon d’y parvenir consiste à créer une routine spéciale qui intercepte l’entrée de la souris jusqu’à ce qu’un événement spécifique se produise. De nombreux développeurs font référence à cette routine en tant que « construction d’un Mousetrap ».

L’exemple suivant utilise les fonctions [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) et [**KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) pour intercepter l’entrée de la souris. **SetTimer** crée un minuteur qui envoie un message de [**\_ minuteur WM**](wm-timer.md) toutes les 10 secondes. Chaque fois que l’application reçoit un message de **\_ minuteur WM** , il enregistre l’emplacement du pointeur de la souris. Si l’emplacement actuel est le même que l’emplacement précédent et que la fenêtre principale de l’application est réduite, l’application déplace le pointeur de la souris sur l’icône. Lorsque l’application se ferme, **KillTimer** arrête le minuteur.


```
HICON hIcon1;               // icon handle 
POINT ptOld;                // previous cursor location 
UINT uResult;               // SetTimer's return value 
HINSTANCE hinstance;        // handle to current instance 
 
//
// Perform application initialization here. 
//
 
wc.hIcon = LoadIcon(hinstance, MAKEINTRESOURCE(400)); 
wc.hCursor = LoadCursor(hinstance, MAKEINTRESOURCE(200)); 
 
// Record the initial cursor position. 
 
GetCursorPos(&ptOld); 
 
// Set the timer for the mousetrap. 
 
uResult = SetTimer(hwnd,             // handle to main window 
    IDT_MOUSETRAP,                   // timer identifier 
    10000,                           // 10-second interval 
    (TIMERPROC) NULL);               // no timer callback 
 
if (uResult == 0) 
{ 
    ErrorHandler("No timer is available."); 
} 
 
LONG APIENTRY MainWndProc( 
    HWND hwnd,          // handle to main window 
    UINT message,       // type of message 
    WPARAM  wParam,     // additional information 
    LPARAM  lParam)     // additional information 
{ 
 
    HDC hdc;        // handle to device context 
    POINT pt;       // current cursor location 
    RECT rc;        // location of minimized window 
 
    switch (message) 
    { 
        //
        // Process other messages. 
        // 
 
        case WM_TIMER: 
        // If the window is minimized, compare the current 
        // cursor position with the one from 10 seconds 
        // earlier. If the cursor position has not changed, 
        // move the cursor to the icon. 
 
            if (IsIconic(hwnd)) 
            { 
                GetCursorPos(&pt); 
 
                if ((pt.x == ptOld.x) && (pt.y == ptOld.y)) 
                { 
                    GetWindowRect(hwnd, &rc); 
                    SetCursorPos(rc.left, rc.top); 
                } 
                else 
                { 
                    ptOld.x = pt.x; 
                    ptOld.y = pt.y; 
                } 
            } 
 
            return 0; 
 
        case WM_DESTROY: 
 
        // Destroy the timer. 
 
            KillTimer(hwnd, IDT_MOUSETRAP); 
            PostQuitMessage(0); 
            break; 
 
        //
        // Process other messages. 
        // 
 
} 
```



Bien que l’exemple suivant montre également comment intercepter l’entrée de la souris, il traite le message du [**\_ minuteur WM**](wm-timer.md) via la fonction de rappel définie par l’application **MyTimerProc**, plutôt que via la file d’attente de messages de l’application.


```
UINT uResult;               // SetTimer's return value 
HICON hIcon1;               // icon handle 
POINT ptOld;                // previous cursor location 
HINSTANCE hinstance;        // handle to current instance 
 
//
// Perform application initialization here. 
//
 
wc.hIcon = LoadIcon(hinstance, MAKEINTRESOURCE(400)); 
wc.hCursor = LoadCursor(hinstance, MAKEINTRESOURCE(200)); 
 
// Record the current cursor position. 
 
GetCursorPos(&ptOld); 
 
// Set the timer for the mousetrap. 
 
uResult = SetTimer(hwnd,      // handle to main window 
    IDT_MOUSETRAP,            // timer identifier 
    10000,                    // 10-second interval 
    (TIMERPROC) MyTimerProc); // timer callback 
 
if (uResult == 0) 
{ 
    ErrorHandler("No timer is available."); 
} 
 
LONG APIENTRY MainWndProc( 
    HWND hwnd,          // handle to main window 
    UINT message,       // type of message 
    WPARAM  wParam,     // additional information 
    LPARAM   lParam)    // additional information 
{ 
 
    HDC hdc;            // handle to device context 
 
    switch (message) 
    { 
    // 
    // Process other messages. 
    // 
 
        case WM_DESTROY: 
        // Destroy the timer. 
 
            KillTimer(hwnd, IDT_MOUSETRAP); 
            PostQuitMessage(0); 
            break; 
 
        //
        // Process other messages. 
        // 
 
} 
 
// MyTimerProc is an application-defined callback function that 
// processes WM_TIMER messages. 
 
VOID CALLBACK MyTimerProc( 
    HWND hwnd,        // handle to window for timer messages 
    UINT message,     // WM_TIMER message 
    UINT idTimer,     // timer identifier 
    DWORD dwTime)     // current system time 
{ 
 
    RECT rc; 
    POINT pt; 
 
    // If the window is minimized, compare the current 
    // cursor position with the one from 10 seconds earlier. 
    // If the cursor position has not changed, move the 
    // cursor to the icon. 
 
    if (IsIconic(hwnd)) 
    { 
        GetCursorPos(&pt); 
 
        if ((pt.x == ptOld.x) && (pt.y == ptOld.y)) 
        { 
            GetWindowRect(hwnd, &rc); 
            SetCursorPos(rc.left, rc.top); 
        } 
        else 
        { 
            ptOld.x = pt.x; 
            ptOld.y = pt.y; 
        } 
    } 
} 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des minuteries](about-timers.md)
</dt> </dl>

 

 
