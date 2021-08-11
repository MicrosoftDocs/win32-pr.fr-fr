---
title: Utilisation de l’entrée au clavier
description: Cette section traite des tâches associées à l’entrée au clavier.
ms.assetid: d08e7f12-6595-4234-bfc4-08daad93e4c4
keywords:
- entrée d’utilisateur, entrée au clavier
- capture de l’entrée utilisateur, entrée au clavier
- entrée au clavier
- messages de séquence de touches
- messages de caractères
- signes insertion, entrée au clavier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1be8753ec6a5f920f09f6e5376b7988a88de0f9a49551492408e84908bb0c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118248271"
---
# <a name="using-keyboard-input"></a>Utilisation de l’entrée au clavier

Une fenêtre reçoit une entrée au clavier sous la forme de messages de frappe de touche et de messages de type caractère. La boucle de message attachée à la fenêtre doit inclure du code pour convertir des messages de frappe en messages de caractères correspondants. Si la fenêtre affiche une entrée au clavier dans sa zone cliente, elle doit créer et afficher un signe insertion pour indiquer la position à laquelle le caractère suivant sera entré. Les sections suivantes décrivent le code impliqué dans la réception, le traitement et l’affichage de l’entrée au clavier :

-   [Traitement des messages de frappe](#processing-keystroke-messages)
-   [Conversion de messages de caractères](#translating-character-messages)
-   [Traitement des messages de caractères](#processing-character-messages)
-   [Utilisation du signe insertion](#using-the-caret)
-   [Affichage de l’entrée au clavier](#displaying-keyboard-input)

## <a name="processing-keystroke-messages"></a>Traitement des messages de frappe

La procédure de fenêtre de la fenêtre qui a le focus clavier reçoit des messages de frappe lorsque l’utilisateur tape le clavier. Les messages de séquence de touches sont [**WM \_**](wm-keydown.md)KeyOut, [**WM \_ KEYUP**](wm-keyup.md), [**WM \_ SYSKEYDOWN**](wm-syskeydown.md)et [**WM \_ SYSKEYUP**](wm-syskeyup.md). Une procédure de fenêtre classique ignore tous les messages de frappe à l’exception de **\_ la touche WM**. Le système publie le **message \_ WM** KeyOut lorsque l’utilisateur appuie sur une touche.

Lorsque la procédure de fenêtre reçoit le message WM KeyOut, elle doit examiner le code de la touche virtuelle qui accompagne le message pour déterminer comment traiter la séquence de touches. [**\_**](wm-keydown.md) Le code de la touche virtuelle se trouve dans le paramètre *wParam* du message. En règle générale, une application traite uniquement les séquences de touches générées par des touches autres que des caractères, y compris les touches de fonction, les touches de déplacement du curseur et les clés spéciales, telles que INS, DEL, orig et END.

L’exemple suivant montre l’infrastructure de procédure de fenêtre qu’une application classique utilise pour recevoir et traiter des messages de séquence de touches.


```
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_LEFT: 
                    
                    // Process the LEFT ARROW key. 
                     
                    break; 
 
                case VK_RIGHT: 
                    
                    // Process the RIGHT ARROW key. 
                     
                    break; 
 
                case VK_UP: 
                    
                    // Process the UP ARROW key. 
                     
                    break; 
 
                case VK_DOWN: 
                    
                    // Process the DOWN ARROW key. 
                     
                    break; 
 
                case VK_HOME: 
                    
                    // Process the HOME key. 
                     
                    break; 
 
                case VK_END: 
                    
                    // Process the END key. 
                     
                    break; 
 
                case VK_INSERT: 
                    
                    // Process the INS key. 
                     
                    break; 
 
                case VK_DELETE: 
                    
                    // Process the DEL key. 
                     
                    break; 
 
                case VK_F2: 
                    
                    // Process the F2 key. 
                    
                    break; 
 
                
                // Process other non-character keystrokes. 
                 
                default: 
                    break; 
            } 
```



## <a name="translating-character-messages"></a>Conversion de messages de caractères

Tout thread qui reçoit l’entrée de caractères de l’utilisateur doit inclure la fonction [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) dans sa boucle de message. Cette fonction examine le code de touche virtuelle d’un message de frappe et, si le code correspond à un caractère, place un message de caractère dans la file d’attente de messages. Le message de caractère est supprimé et distribué lors de l’itération suivante de la boucle de message. le paramètre *wParam* du message contient le code de caractère.

En général, la boucle de message d’un thread doit utiliser la fonction [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) pour traduire chaque message, pas seulement les messages de clé virtuelle. Bien que **TranslateMessage** n’ait aucun effet sur les autres types de messages, il garantit que l’entrée au clavier est correctement traduite. L’exemple suivant montre comment inclure la fonction **TranslateMessage** dans une boucle de message de thread classique.


```
MSG msg;
BOOL bRet;

while (( bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0) 
{
    if (bRet == -1);
    {
        // handle the error and possibly exit
    }
    else
    { 
        if (TranslateAccelerator(hwndMain, haccl, &msg) == 0) 
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



## <a name="processing-character-messages"></a>Traitement des messages de caractères

Une procédure de fenêtre reçoit un message de caractère lorsque la fonction [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) traduit un code de touche virtuelle correspondant à une touche de caractère. Les messages de caractères [**sont \_ WM char**](wm-char.md), [**WM \_ DEADCHAR**](wm-deadchar.md), [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar)et [**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md). Une procédure de fenêtre classique ignore tous les messages de type caractère, à l’exception de **WM \_ char**. La fonction **TranslateMessage** génère un message **WM \_ char** quand l’utilisateur appuie sur l’une des touches suivantes :

-   Toute touche de caractère
-   Ret.arr
-   ENTRÉE (retour chariot)
-   ÉCHAP
-   Maj + Entrée (saut de saut)
-   Tab

Quand une procédure de fenêtre reçoit le message [**WM \_ char**](wm-char.md) , elle doit examiner le code de caractère qui accompagne le message pour déterminer comment traiter le caractère. Le code de caractère se trouve dans le paramètre *wParam* du message.

L’exemple suivant montre l’infrastructure de procédure de fenêtre qu’une application classique utilise pour recevoir et traiter des messages de caractères.


```
        case WM_CHAR: 
            switch (wParam) 
            { 
                case 0x08: 
                    
                    // Process a backspace. 
                     
                    break; 
 
                case 0x0A: 
                    
                    // Process a linefeed. 
                     
                    break; 
 
                case 0x1B: 
                    
                    // Process an escape. 
                    
                    break; 
 
                case 0x09: 
                    
                    // Process a tab. 
                     
                    break; 
 
                case 0x0D: 
                    
                    // Process a carriage return. 
                     
                    break; 
 
                default: 
                    
                    // Process displayable characters. 
                     
                    break; 
            } 
```



## <a name="using-the-caret"></a>Utilisation du signe insertion

Une fenêtre qui reçoit l’entrée au clavier affiche généralement les caractères que l’utilisateur tape dans la zone cliente de la fenêtre. Une fenêtre doit utiliser un signe insertion pour indiquer la position dans la zone cliente où le caractère suivant apparaît. La fenêtre doit également créer et afficher le signe insertion lorsqu’elle reçoit le focus clavier, puis masquer et détruire le signe insertion lorsqu’il perd le focus. Une fenêtre peut effectuer ces opérations dans le traitement des messages [**WM \_ SetFocus**](wm-setfocus.md) et [**WM \_ KILLFOCUS**](wm-killfocus.md) . Pour plus d’informations sur les signes d’insertion, consultez les [signes](/windows/desktop/menurc/carets).

## <a name="displaying-keyboard-input"></a>Affichage de l’entrée au clavier

L’exemple de cette section montre comment une application peut recevoir des caractères du clavier, les afficher dans la zone cliente d’une fenêtre et mettre à jour la position du signe insertion avec chaque caractère tapé. Il montre également comment déplacer le signe insertion en réponse aux séquences de touches gauche, droite, début et fin, et montre comment mettre en surbrillance le texte sélectionné en réponse à la combinaison de touches Maj + Flèche droite.

Lors du traitement du message [**WM \_ Create**](/windows/desktop/winmsg/wm-create) , la procédure de fenêtre illustrée dans l’exemple alloue une mémoire tampon de 64 Ko pour le stockage de l’entrée au clavier. Elle récupère également les métriques de la police actuellement chargée, en enregistrant la hauteur et la largeur moyenne des caractères de la police. La hauteur et la largeur sont utilisées dans le traitement du message de [**\_ taille WM**](/windows/desktop/winmsg/wm-size) pour calculer la longueur de ligne et le nombre maximal de lignes, en fonction de la taille de la zone cliente.

La procédure de fenêtre crée et affiche le signe insertion lors du traitement du message [**WM \_ SetFocus**](wm-setfocus.md) . Il masque et supprime le signe insertion lors du traitement du message [**WM \_ KILLFOCUS**](wm-killfocus.md) .

Lors du traitement du message [**WM \_ char**](wm-char.md) , la procédure de fenêtre affiche les caractères, les stocke dans la mémoire tampon d’entrée et met à jour la position du signe insertion. La procédure de fenêtre convertit également les caractères de tabulation en quatre espaces consécutifs. Les caractères de retour arrière, de saut de ligne et d’échappement génèrent un signal sonore, mais ils ne sont pas traités autrement.

La procédure de fenêtre exécute les mouvements de gauche, de droite, de fin et de signe insertion de début lors du traitement du message [**\_ keyverse WM**](wm-keydown.md) . Lors du traitement de l’action de la touche de direction droite, la procédure de fenêtre vérifie l’état de la touche Maj et, si elle est déverrouillée, sélectionne le caractère à droite du signe insertion lorsque le signe insertion est déplacé.

Notez que le code suivant est écrit de façon à pouvoir être compilé au format Unicode ou ANSI. Si le code source définit UNICODE, les chaînes sont gérées en tant que caractères Unicode. dans le cas contraire, elles sont gérées en tant que caractères ANSI.


```
#define BUFSIZE 65535 
#define SHIFTED 0x8000 
 
LONG APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    HDC hdc;                   // handle to device context 
    TEXTMETRIC tm;             // structure for text metrics 
    static DWORD dwCharX;      // average width of characters 
    static DWORD dwCharY;      // height of characters 
    static DWORD dwClientX;    // width of client area 
    static DWORD dwClientY;    // height of client area 
    static DWORD dwLineLen;    // line length 
    static DWORD dwLines;      // text lines in client area 
    static int nCaretPosX = 0; // horizontal position of caret 
    static int nCaretPosY = 0; // vertical position of caret 
    static int nCharWidth = 0; // width of a character 
    static int cch = 0;        // characters in buffer 
    static int nCurChar = 0;   // index of current character 
    static PTCHAR pchInputBuf; // input buffer 
    int i, j;                  // loop counters 
    int cCR = 0;               // count of carriage returns 
    int nCRIndex = 0;          // index of last carriage return 
    int nVirtKey;              // virtual-key code 
    TCHAR szBuf[128];          // temporary buffer 
    TCHAR ch;                  // current character 
    PAINTSTRUCT ps;            // required by BeginPaint 
    RECT rc;                   // output rectangle for DrawText 
    SIZE sz;                   // string dimensions 
    COLORREF crPrevText;       // previous text color 
    COLORREF crPrevBk;         // previous background color
    size_t * pcch;
    HRESULT hResult; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Get the metrics of the current font. 
 
            hdc = GetDC(hwndMain); 
            GetTextMetrics(hdc, &tm); 
            ReleaseDC(hwndMain, hdc); 
 
            // Save the average character width and height. 
 
            dwCharX = tm.tmAveCharWidth; 
            dwCharY = tm.tmHeight; 
 
            // Allocate a buffer to store keyboard input. 
 
            pchInputBuf = (LPTSTR) GlobalAlloc(GPTR, 
                BUFSIZE * sizeof(TCHAR)); 
            return 0; 
 
        case WM_SIZE: 
 
            // Save the new width and height of the client area. 
 
            dwClientX = LOWORD(lParam); 
            dwClientY = HIWORD(lParam); 
 
            // Calculate the maximum width of a line and the 
            // maximum number of lines in the client area. 
            
            dwLineLen = dwClientX - dwCharX; 
            dwLines = dwClientY / dwCharY; 
            break; 
 
 
        case WM_SETFOCUS: 
 
            // Create, position, and display the caret when the 
            // window receives the keyboard focus. 
 
            CreateCaret(hwndMain, (HBITMAP) 1, 0, dwCharY); 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            ShowCaret(hwndMain); 
            break; 
 
        case WM_KILLFOCUS: 
 
            // Hide and destroy the caret when the window loses the 
            // keyboard focus. 
 
            HideCaret(hwndMain); 
            DestroyCaret(); 
            break; 
 
        case WM_CHAR:
        // check if current location is close enough to the
        // end of the buffer that a buffer overflow may
        // occur. If so, add null and display contents. 
    if (cch > BUFSIZE-5)
    {
        pchInputBuf[cch] = 0x00;
        SendMessage(hwndMain, WM_PAINT, 0, 0);
    } 
            switch (wParam) 
            { 
                case 0x08:  // backspace 
                case 0x0A:  // linefeed 
                case 0x1B:  // escape 
                    MessageBeep((UINT) -1); 
                    return 0; 
 
                case 0x09:  // tab 
 
                    // Convert tabs to four consecutive spaces. 
 
                    for (i = 0; i < 4; i++) 
                        SendMessage(hwndMain, WM_CHAR, 0x20, 0); 
                    return 0; 
 
                case 0x0D:  // carriage return 
 
                    // Record the carriage return and position the 
                    // caret at the beginning of the new line.

                    pchInputBuf[cch++] = 0x0D; 
                    nCaretPosX = 0; 
                    nCaretPosY += 1; 
                    break; 
 
                default:    // displayable character 
 
                    ch = (TCHAR) wParam; 
                    HideCaret(hwndMain); 
 
                    // Retrieve the character's width and output 
                    // the character. 
 
                    hdc = GetDC(hwndMain); 
                    GetCharWidth32(hdc, (UINT) wParam, (UINT) wParam, 
                        &nCharWidth); 
                    TextOut(hdc, nCaretPosX, nCaretPosY * dwCharY, 
                        &ch, 1); 
                    ReleaseDC(hwndMain, hdc); 
 
                    // Store the character in the buffer.
 
                    pchInputBuf[cch++] = ch; 
 
                    // Calculate the new horizontal position of the 
                    // caret. If the position exceeds the maximum, 
                    // insert a carriage return and move the caret 
                    // to the beginning of the next line. 
 
                    nCaretPosX += nCharWidth; 
                    if ((DWORD) nCaretPosX > dwLineLen) 
                    { 
                        nCaretPosX = 0;
                        pchInputBuf[cch++] = 0x0D; 
                        ++nCaretPosY; 
                    } 
                    nCurChar = cch; 
                    ShowCaret(hwndMain); 
                    break; 
            } 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            break; 
 
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_LEFT:   // LEFT ARROW 
 
                    // The caret can move only to the beginning of 
                    // the current line. 
 
                    if (nCaretPosX > 0) 
                    { 
                        HideCaret(hwndMain); 
 
                        // Retrieve the character to the left of 
                        // the caret, calculate the character's 
                        // width, then subtract the width from the 
                        // current horizontal position of the caret 
                        // to obtain the new position. 
 
                        ch = pchInputBuf[--nCurChar]; 
                        hdc = GetDC(hwndMain); 
                        GetCharWidth32(hdc, ch, ch, &nCharWidth); 
                        ReleaseDC(hwndMain, hdc); 
                        nCaretPosX = max(nCaretPosX - nCharWidth, 
                            0); 
                        ShowCaret(hwndMain); 
                    } 
                    break; 
 
                case VK_RIGHT:  // RIGHT ARROW 
 
                    // Caret moves to the right or, when a carriage 
                    // return is encountered, to the beginning of 
                    // the next line. 
 
                    if (nCurChar < cch) 
                    { 
                        HideCaret(hwndMain); 
 
                        // Retrieve the character to the right of 
                        // the caret. If it's a carriage return, 
                        // position the caret at the beginning of 
                        // the next line. 
 
                        ch = pchInputBuf[nCurChar]; 
                        if (ch == 0x0D) 
                        { 
                            nCaretPosX = 0; 
                            nCaretPosY++; 
                        } 
 
                        // If the character isn't a carriage 
                        // return, check to see whether the SHIFT 
                        // key is down. If it is, invert the text 
                        // colors and output the character. 
 
                        else 
                        { 
                            hdc = GetDC(hwndMain); 
                            nVirtKey = GetKeyState(VK_SHIFT); 
                            if (nVirtKey & SHIFTED) 
                            { 
                                crPrevText = SetTextColor(hdc, 
                                    RGB(255, 255, 255)); 
                                crPrevBk = SetBkColor(hdc, 
                                    RGB(0,0,0)); 
                                TextOut(hdc, nCaretPosX, 
                                    nCaretPosY * dwCharY, 
                                    &ch, 1); 
                                SetTextColor(hdc, crPrevText); 
                                SetBkColor(hdc, crPrevBk); 
                            } 
 
                            // Get the width of the character and 
                            // calculate the new horizontal 
                            // position of the caret. 
 
                            GetCharWidth32(hdc, ch, ch, &nCharWidth); 
                            ReleaseDC(hwndMain, hdc); 
                            nCaretPosX = nCaretPosX + nCharWidth; 
                        } 
                        nCurChar++; 
                        ShowCaret(hwndMain); 
                        break; 
                    } 
                    break; 
 
                case VK_UP:     // UP ARROW 
                case VK_DOWN:   // DOWN ARROW 
                    MessageBeep((UINT) -1); 
                    return 0; 
 
                case VK_HOME:   // HOME 
 
                    // Set the caret's position to the upper left 
                    // corner of the client area. 
 
                    nCaretPosX = nCaretPosY = 0; 
                    nCurChar = 0; 
                    break; 
 
                case VK_END:    // END  
 
                    // Move the caret to the end of the text. 
 
                    for (i=0; i < cch; i++) 
                    { 
                        // Count the carriage returns and save the 
                        // index of the last one. 
 
                        if (pchInputBuf[i] == 0x0D) 
                        { 
                            cCR++; 
                            nCRIndex = i + 1; 
                        } 
                    } 
                    nCaretPosY = cCR; 
 
                    // Copy all text between the last carriage 
                    // return and the end of the keyboard input 
                    // buffer to a temporary buffer. 
 
                    for (i = nCRIndex, j = 0; i < cch; i++, j++) 
                        szBuf[j] = pchInputBuf[i]; 
                    szBuf[j] = TEXT('\0'); 
 
                    // Retrieve the text extent and use it 
                    // to set the horizontal position of the 
                    // caret. 
 
                    hdc = GetDC(hwndMain);
                    hResult = StringCchLength(szBuf, 128, pcch);
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
                    GetTextExtentPoint32(hdc, szBuf, *pcch, 
                        &sz); 
                    nCaretPosX = sz.cx; 
                    ReleaseDC(hwndMain, hdc); 
                    nCurChar = cch; 
                    break; 
 
                default: 
                    break; 
            } 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            break; 
 
        case WM_PAINT: 
            if (cch == 0)       // nothing in input buffer 
                break; 
 
            hdc = BeginPaint(hwndMain, &ps); 
            HideCaret(hwndMain); 
 
            // Set the clipping rectangle, and then draw the text 
            // into it. 
 
            SetRect(&rc, 0, 0, dwLineLen, dwClientY); 
            DrawText(hdc, pchInputBuf, -1, &rc, DT_LEFT); 
 
            ShowCaret(hwndMain); 
            EndPaint(hwndMain, &ps); 
            break; 
        
        // Process other messages. 
        
        case WM_DESTROY: 
            PostQuitMessage(0); 
 
            // Free the input buffer. 
 
            GlobalFree((HGLOBAL) pchInputBuf); 
            UnregisterHotKey(hwndMain, 0xAAAA); 
            break; 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



 

 