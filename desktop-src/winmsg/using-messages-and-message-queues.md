---
description: les exemples de code suivants montrent comment effectuer les tâches suivantes associées aux messages Windows et aux files d’attente de messages.
ms.assetid: 62b4616c-37bf-4d9f-8891-7010c7035d18
title: Utilisation des messages et des files d’attente de messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee617f2c48325eccf5a2fdb07741bb88b47738dea812d372acda1454c9dd3d9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028337"
---
# <a name="using-messages-and-message-queues"></a>Utilisation des messages et des files d’attente de messages

les exemples de code suivants montrent comment effectuer les tâches suivantes associées aux messages Windows et aux files d’attente de messages.

-   [Création d’une boucle de message](#creating-a-message-loop)
-   [Examen d’une file d’attente de messages](#examining-a-message-queue)
-   [Publication d’un message](#posting-a-message)
-   [Envoi d’un message](#sending-a-message)

## <a name="creating-a-message-loop"></a>Création d’une boucle de message

Le système ne crée pas automatiquement une file d’attente de messages pour chaque thread. Au lieu de cela, le système crée une file d’attente de messages uniquement pour les threads qui effectuent des opérations qui nécessitent une file d’attente de messages. Si le thread crée une ou plusieurs fenêtres, une boucle de message doit être fournie. Cette boucle de messages récupère les messages de la file d’attente de messages du thread et les distribue aux procédures de fenêtre appropriées.

Étant donné que le système dirige les messages vers des fenêtres individuelles dans une application, un thread doit créer au moins une fenêtre avant de démarrer sa boucle de message. La plupart des applications contiennent un seul thread qui crée des fenêtres. Une application classique inscrit la classe de fenêtre pour sa fenêtre principale, crée et affiche la fenêtre principale, puis démarre sa boucle de messages, le tout dans la fonction [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) .

Vous créez une boucle de messages à l’aide des fonctions [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) et [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) . Si votre application doit obtenir une entrée de caractères de la part de l’utilisateur, incluez la fonction [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) dans la boucle. **TranslateMessage** traduit les messages de clé virtuelle en messages de caractères. l’exemple suivant illustre la boucle de message dans la fonction [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) d’une application simple basée sur Windows.


```
HINSTANCE hinst; 
HWND hwndMain; 
 
int PASCAL WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, 
    LPSTR lpszCmdLine, int nCmdShow) 
{ 
    MSG msg;
    BOOL bRet; 
    WNDCLASS wc; 
    UNREFERENCED_PARAMETER(lpszCmdLine); 
 
    // Register the window class for the main window. 
 
    if (!hPrevInstance) 
    { 
        wc.style = 0; 
        wc.lpfnWndProc = (WNDPROC) WndProc; 
        wc.cbClsExtra = 0; 
        wc.cbWndExtra = 0; 
        wc.hInstance = hInstance; 
        wc.hIcon = LoadIcon((HINSTANCE) NULL, 
            IDI_APPLICATION); 
        wc.hCursor = LoadCursor((HINSTANCE) NULL, 
            IDC_ARROW); 
        wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
        wc.lpszMenuName =  "MainMenu"; 
        wc.lpszClassName = "MainWndClass"; 
 
        if (!RegisterClass(&wc)) 
            return FALSE; 
    } 
 
    hinst = hInstance;  // save instance handle 
 
    // Create the main window. 
 
    hwndMain = CreateWindow("MainWndClass", "Sample", 
        WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, (HWND) NULL, 
        (HMENU) NULL, hinst, (LPVOID) NULL); 
 
    // If the main window cannot be created, terminate 
    // the application. 
 
    if (!hwndMain) 
        return FALSE; 
 
    // Show the window and paint its contents. 
 
    ShowWindow(hwndMain, nCmdShow); 
    UpdateWindow(hwndMain); 
 
    // Start the message loop. 
 
    while( (bRet = GetMessage( &msg, NULL, 0, 0 )) != 0)
    { 
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        {
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        }
    } 
 
    // Return the exit code to the system. 
 
    return msg.wParam; 
} 
```



L’exemple suivant montre une boucle de messages pour un thread qui utilise des accélérateurs et affiche une boîte de dialogue non modale. Lorsque [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) ou [**IsDialogMessage**](/windows/win32/api/winuser/nf-winuser-isdialogmessagea) retourne **true** (indiquant que le message a été traité), [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) et [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) ne sont pas appelés. Cela est dû au fait que **TranslateAccelerator** et **IsDialogMessage** effectuent la traduction et la distribution des messages nécessaires.


```
HWND hwndMain; 
HWND hwndDlgModeless = NULL; 
MSG msg;
BOOL bRet; 
HACCEL haccel; 
// 
// Perform initialization and create a main window. 
// 
 
while( (bRet = GetMessage( &msg, NULL, 0, 0 )) != 0)
{ 
    if (bRet == -1)
    {
        // handle the error and possibly exit
    }
    else
    {
        if (hwndDlgModeless == (HWND) NULL || 
                !IsDialogMessage(hwndDlgModeless, &msg) && 
                !TranslateAccelerator(hwndMain, haccel, 
                    &msg)) 
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        }
    } 
} 
```



## <a name="examining-a-message-queue"></a>Examen d’une file d’attente de messages

Parfois, une application doit examiner le contenu de la file d’attente de messages d’un thread à partir de l’extérieur de la boucle de message du thread. Par exemple, si la procédure de fenêtre d’une application exécute une longue opération de dessin, vous souhaiterez peut-être que l’utilisateur soit en mesure d’interrompre l’opération. À moins que votre application n’examine régulièrement la file d’attente de messages pendant l’opération pour les messages de souris et de clavier, elle ne répond pas à l’entrée d’utilisateur tant que l’opération n’est pas terminée. Cela est dû au fait que la fonction [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) dans la boucle de message du thread ne retourne pas de réponse tant que la procédure de fenêtre n’a pas terminé le traitement d’un message.

Vous pouvez utiliser la fonction [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) pour examiner une file d’attente de messages pendant une opération de longue durée. **PeekMessage** est similaire à la fonction [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ; Vérifiez une file d’attente de messages pour un message qui correspond aux critères de filtre, puis copiez le message dans une structure [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) . La principale différence entre les deux fonctions est que **GetMessage** ne retourne aucun résultat tant qu’un message correspondant aux critères de filtre n’a pas été placé dans la file d’attente, tandis que **PeekMessage** est retourné immédiatement, qu’un message se trouve dans la file d’attente ou non.

L’exemple suivant montre comment utiliser [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) pour examiner une file d’attente de messages pour les clics de souris et l’entrée au clavier pendant une longue opération.


```
HWND hwnd; 
BOOL fDone; 
MSG msg; 
 
// Begin the operation and continue until it is complete 
// or until the user clicks the mouse or presses a key. 
 
fDone = FALSE; 
while (!fDone) 
{ 
    fDone = DoLengthyOperation(); // application-defined function 
 
    // Remove any messages that may be in the queue. If the 
    // queue contains any mouse or keyboard 
    // messages, end the operation. 
 
    while (PeekMessage(&msg, hwnd,  0, 0, PM_REMOVE)) 
    { 
        switch(msg.message) 
        { 
            case WM_LBUTTONDOWN: 
            case WM_RBUTTONDOWN: 
            case WM_KEYDOWN: 
                // 
                // Perform any required cleanup. 
                // 
                fDone = TRUE; 
        } 
    } 
} 
```



D’autres fonctions, notamment [**GetQueueStatus**](/windows/win32/api/winuser/nf-winuser-getqueuestatus) et [**GetInputState**](/windows/win32/api/winuser/nf-winuser-getinputstate), vous permettent également d’examiner le contenu de la file d’attente de messages d’un thread. **GetQueueStatus** retourne un tableau d’indicateurs qui indique les types de messages dans la file d’attente ; son utilisation est le moyen le plus rapide de déterminer si la file d’attente contient des messages. **GetInputState** retourne la **valeur true** si la file d’attente contient des messages de souris ou de clavier. Ces deux fonctions peuvent être utilisées pour déterminer si la file d’attente contient des messages qui doivent être traités.

## <a name="posting-a-message"></a>Publication d’un message

Vous pouvez poster un message dans une file d’attente de messages à l’aide de la fonction [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) . **PostMessage** place un message à la fin de la file d’attente de messages d’un thread et le retourne immédiatement, sans attendre que le thread traite le message. Les paramètres de la fonction incluent un handle de fenêtre, un identificateur de message et deux paramètres de message. Le système copie ces paramètres dans une structure [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) , remplit les membres **Time** et **PT** de la structure et place la structure dans la file d’attente de messages.

Le système utilise le handle de fenêtre passé avec la fonction [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) pour déterminer quelle file d’attente de messages de thread doit recevoir le message. Si le handle est **le \_ plus HWND**, le système publie le message dans les files d’attente de messages de thread de toutes les fenêtres de niveau supérieur.

Vous pouvez utiliser la fonction [**PostThreadMessage**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea) pour envoyer un message à une file d’attente de messages de thread spécifique. **PostThreadMessage** est similaire à [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea), sauf que le premier paramètre est un identificateur de thread plutôt qu’un handle de fenêtre. Vous pouvez récupérer l’identificateur de thread en appelant la fonction [**GetCurrentThreadID**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) .

Utilisez la fonction [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) pour quitter une boucle de message. **PostQuitMessage** publie le message [**WM \_ Quit**](wm-quit.md) sur le thread en cours d’exécution. La boucle de message du thread se termine et retourne le contrôle au système lorsqu’il rencontre le message **WM \_ Quit** . Une application appelle généralement **PostQuitMessage** en réponse au message [**WM \_ Destroy**](wm-destroy.md) , comme illustré dans l’exemple suivant.


```
case WM_DESTROY: 
 
    // Perform cleanup tasks. 
 
    PostQuitMessage(0); 
    break; 
```



## <a name="sending-a-message"></a>Envoi d’un message

La fonction [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) est utilisée pour envoyer un message directement à une procédure de fenêtre. **SendMessage** appelle une procédure de fenêtre et attend que cette procédure traite le message et retourne un résultat.

Un message peut être envoyé à n’importe quelle fenêtre du système ; tout ce qui est obligatoire est un handle de fenêtre. Le système utilise le handle pour déterminer la procédure de fenêtre qui doit recevoir le message.

Avant de traiter un message qui a pu être envoyé à partir d’un autre thread, une procédure de fenêtre doit d’abord appeler la fonction [**InSendMessage**](/windows/win32/api/winuser/nf-winuser-insendmessage) . Si cette fonction retourne la **valeur true**, la procédure de fenêtre doit appeler [**replyMessage**](/windows/win32/api/winuser/nf-winuser-replymessage) avant toute fonction qui amène le thread à donner le contrôle, comme illustré dans l’exemple suivant.


```
case WM_USER + 5: 
    if (InSendMessage()) 
        ReplyMessage(TRUE); 
 
    DialogBox(hInst, "MyDialogBox", hwndMain, (DLGPROC) MyDlgProc); 
    break; 
```



Un certain nombre de messages peuvent être envoyés à des contrôles dans une boîte de dialogue. Ces messages de contrôle définissent l’apparence, le comportement et le contenu des contrôles ou récupèrent des informations sur les contrôles. Par exemple, le message [**CB \_ ADDSTRING**](../controls/cb-addstring.md) peut ajouter une chaîne à une zone de liste déroulante, et le message [**\_ SETCHECK BM**](../controls/bm-setcheck.md) peut définir l’état d’activation d’une case à cocher ou d’une case d’option.

Utilisez la fonction [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea) pour envoyer un message à un contrôle, en spécifiant l’identificateur du contrôle et le handle de la fenêtre de la boîte de dialogue qui contient le contrôle. L’exemple suivant, extrait d’une procédure de boîte de dialogue, copie une chaîne du contrôle d’édition d’une zone de liste déroulante dans sa zone de liste. L’exemple utilise **SendDlgItemMessage** pour envoyer un message [**CB \_ ADDSTRING**](../controls/cb-addstring.md) à la zone de liste déroulante.


```
HWND hwndCombo; 
int cTxtLen; 
PSTR pszMem; 
 
switch (uMsg) 
{ 
    case WM_COMMAND: 
        switch (LOWORD(wParam)) 
        { 
            case IDD_ADDCBITEM: 
                // Get the handle of the combo box and the 
                // length of the string in the edit control 
                // of the combo box. 
 
                hwndCombo = GetDlgItem(hwndDlg, IDD_COMBO); 
                cTxtLen = GetWindowTextLength(hwndCombo); 
 
                // Allocate memory for the string and copy 
                // the string into the memory. 
 
                pszMem = (PSTR) VirtualAlloc((LPVOID) NULL, 
                    (DWORD) (cTxtLen + 1), MEM_COMMIT, 
                    PAGE_READWRITE); 
                GetWindowText(hwndCombo, pszMem, 
                    cTxtLen + 1); 
 
                // Add the string to the list box of the 
                // combo box and remove the string from the 
                // edit control of the combo box. 
 
                if (pszMem != NULL) 
                { 
                    SendDlgItemMessage(hwndDlg, IDD_COMBO, 
                        CB_ADDSTRING, 0, 
                        (DWORD) ((LPSTR) pszMem)); 
                    SetWindowText(hwndCombo, (LPSTR) NULL); 
                } 
 
                // Free the memory and return. 
 
                VirtualFree(pszMem, 0, MEM_RELEASE); 
                return TRUE; 
            // 
            // Process other dialog box commands. 
            // 
 
        } 
    // 
    // Process other dialog box messages. 
    // 
 
}
```



 

 
