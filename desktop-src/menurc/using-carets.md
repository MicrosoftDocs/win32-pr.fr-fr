---
title: Utilisation des signes d’insertion
description: Cette section fournit des exemples de code qui montrent comment effectuer des tâches liées aux signes d’insertion.
ms.assetid: 82b0a84c-49a9-4d9d-b4c8-7c4511d863eb
keywords:
- ressources, signes
- insertion, création
- signes insertion
- signes insertion, destruction
- signes insertion, masquage
- signes d’insertion et de clignotement
- lignes clignotantes
- blocs clignotants
- bitmaps clignotantes
- création de signes
- affichage des signes d’insertion
- masquage des signes
- destruction des signes d’insertion
- temps de clignotement
- entrée d’utilisateur, entrée au clavier
- capture de l’entrée utilisateur, entrée au clavier
- entrée au clavier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c930931df8ce401fbed8cc9af16db3cb52de08ebe9cf539109b426497318d5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472645"
---
# <a name="using-carets"></a>Utilisation des signes d’insertion

Cette section contient des exemples de code pour les tâches suivantes :

-   [Création et affichage d’un signe insertion](#creating-and-displaying-a-caret)
-   [Masquage d’un signe insertion](#hiding-a-caret)
-   [Destruction d’un signe insertion](#destroying-a-caret)
-   [Réglage de la durée de clignotement](#adjusting-the-blink-time)
-   [Traitement de l’entrée au clavier](#processing-keyboard-input)

## <a name="creating-and-displaying-a-caret"></a>Création et affichage d’un signe insertion

Lorsqu’il reçoit le focus clavier, la fenêtre doit créer et afficher le signe insertion. Utilisez la fonction [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) pour créer un signe insertion dans la fenêtre donnée. Vous pouvez ensuite appeler [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) pour définir la position actuelle du signe insertion et [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) pour rendre le signe insertion visible.

Le système envoie le message [**WM \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus) à la fenêtre qui reçoit le focus clavier ; par conséquent, une application doit créer et afficher le signe insertion lors du traitement de ce message.


```
HWND hwnd,       // window handle 
int x;           // horizontal coordinate of cursor 
int y;           // vertical coordinate of cursor 
int nWidth;      // width of cursor 
int nHeight;     // height of cursor 
char *lpszChar;  // pointer to character 
 
    case WM_SETFOCUS: 
 
    // Create a solid black caret. 
        CreateCaret(hwnd, (HBITMAP) NULL, nWidth, nHeight); 
 
    // Adjust the caret position, in client coordinates. 
        SetCaretPos(x, y); 
 
    // Display the caret. 
        ShowCaret(hwnd); 
 
        break; 
```



Pour créer un signe insertion en fonction d’une image bitmap, vous devez spécifier un handle de bitmap lors de l’utilisation de [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret). Vous pouvez utiliser une application graphique pour créer l’image bitmap et un compilateur de ressources pour ajouter l’image bitmap aux ressources de votre application. Votre application peut ensuite utiliser la fonction [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) pour charger le descripteur de bitmap. Par exemple, vous pouvez remplacer la ligne **CreateCaret** dans l’exemple précédent par les lignes suivantes pour créer un signe insertion de bitmap.


```
// Load the application-defined caret resource. 
 
    hCaret = LoadBitmap(hinst, MAKEINTRESOURCE(120)); 
 
// Create a bitmap caret. 
 
    CreateCaret(hwnd, hCaret, 0, 0); 
```



Vous pouvez également utiliser la fonction [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) ou [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) pour récupérer le handle de l’image bitmap du signe insertion. Pour plus d’informations sur les bitmaps, consultez [bitmaps](/windows/desktop/gdi/bitmaps).

Si votre application spécifie un descripteur de bitmap, [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) ignore les paramètres de largeur et de hauteur. La bitmap définit la taille du signe insertion.

## <a name="hiding-a-caret"></a>Masquage d’un signe insertion

Chaque fois que votre application redessine un écran lors du traitement d’un message autre que [**WM \_ Paint**](/windows/desktop/gdi/wm-paint), elle doit rendre le signe insertion invisible à l’aide de la fonction [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) . Une fois le dessin terminé, réaffichez le signe insertion à l’aide de la fonction [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) . Si votre application traite le message **WM \_ Paint** , il n’est pas nécessaire de masquer et de réafficher le signe insertion, car cette fonction effectue cette opération automatiquement.

L’exemple de code suivant montre comment faire en sorte que votre application masque le signe insertion tout en dessinant un caractère à l’écran et lors du traitement du message [**WM \_ char**](/windows/desktop/inputdev/wm-char) .


```
HWND hwnd,   // window handle 
HDC hdc;     // device context 
 
    case WM_CHAR: 
        switch (wParam) 
        { 
            case 0x08: 
             
             // Process a backspace. 
             
                break; 
 
            case 0x09: 
             
             // Process a tab.  
             
                break; 
 
            case 0x0D: 
             
             // Process a carriage return. 
             
                break; 
 
            case 0x1B: 
             
             // Process an escape. 
             
                break; 
 
            case 0x0A: 
             
             // Process a linefeed. 
             
                break; 
 
            default: 
                // Hide the caret. 
                HideCaret(hwnd); 
 
                // Draw the character on the screen. 
 
                hdc = GetDC(hwnd); 
                SelectObject(hdc, 
                    GetStockObject(SYSTEM_FIXED_FONT)); 
 
                TextOut(hdc, x, y, lpszChar, 1); 
 
                ReleaseDC(hwnd, hdc); 
 
                // Display the caret. 
 
                ShowCaret(hwnd); 
 
        } 
```



Si votre application appelle la fonction [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) plusieurs fois sans appeler [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret), le signe insertion n’est pas affiché tant que l’application n’a pas également appelé **ShowCaret** le même nombre de fois.

## <a name="destroying-a-caret"></a>Destruction d’un signe insertion

Quand une fenêtre perd le focus clavier, le système envoie le message [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) à la fenêtre. Votre application doit détruire le signe insertion lors du traitement de ce message à l’aide de la fonction [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) . Le code suivant montre comment détruire un signe insertion dans une fenêtre qui n’a plus le focus clavier.


```
case WM_KILLFOCUS: 
 
// The window is losing the keyboard focus, so destroy the caret. 
 
    DestroyCaret(); 
 
    break; 
```



## <a name="adjusting-the-blink-time"></a>Réglage de la durée de clignotement

en Windows 16 bits, une application basée sur des Windows peut appeler la fonction [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) pour enregistrer la durée de clignotement actuelle, puis appeler la fonction [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) pour ajuster la durée de clignotement lors du traitement du message [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) . L’application restaure la durée de clignotement enregistrée pour l’utilisation d’autres applications en appelant **SetCaretBlinkTime** lors du traitement du message [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) . Toutefois, cette technique ne fonctionne pas dans les environnements multithreads. Plus précisément, la désactivation d’une application n’est pas synchronisée avec l’activation d’une autre application, de sorte que si une application se bloque, une autre application peut toujours être activée.

Les applications doivent respecter la durée de clignotement choisie par l’utilisateur. La fonction [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) doit être appelée uniquement par une application qui permet à l’utilisateur de définir la durée de clignotement.

## <a name="processing-keyboard-input"></a>Traitement de l’entrée au clavier

L’exemple suivant montre comment utiliser un signe insertion dans un simple éditeur de texte. L’exemple met à jour l’emplacement du signe insertion lorsque l’utilisateur tape des caractères imprimables et utilise différentes clés pour se déplacer dans la zone cliente.


```
#define TEXTMATRIX(x, y) *(pTextMatrix + (y * nWindowCharsX) + x) 
// Global variables.
HINSTANCE hinst;                  // current instance 
HBITMAP hCaret;                   // caret bitmap 
HDC hdc;                          // device context  
PAINTSTRUCT ps;                   // client area paint info 
static char *pTextMatrix = NULL;  // points to text matrix 
static int  nCharX,               // width of char. in logical units 
            nCharY,               // height of char. in logical units 
            nWindowX,             // width of client area 
            nWindowY,             // height of client area 
            nWindowCharsX,        // width of client area 
            nWindowCharsY,        // height of client area 
            nCaretPosX,           // x-position of caret 
            nCaretPosY;           // y-position of caret 
static UINT uOldBlink;            // previous blink rate 
int x, y;                         // coordinates for text matrix 
TEXTMETRIC tm;                    // font information 
 
LONG APIENTRY MainWndProc( 
    HWND hwnd,            // window handle 
    UINT message,         // type of message 
    UINT wParam,          // additional information 
    LONG lParam)          // additional information 
{ 
 
    switch (message) 
    { 
        case WM_CREATE: 
        // Select a fixed-width system font, and get its text metrics.
 
            hdc = GetDC(hwnd); 
            SelectObject(hdc, 
                GetStockObject(SYSTEM_FIXED_FONT)); 
            GetTextMetrics(hdc, &tm); 
            ReleaseDC(hwnd, hdc); 
 
        // Save the avg. width and height of characters. 
 
            nCharX = tm.tmAveCharWidth; 
            nCharY = tm.tmHeight; 
 
            return 0; 
 
        case WM_SIZE: 
        // Determine the width of the client area, in pixels 
        // and in number of characters. 
 
            nWindowX = LOWORD(lParam); 
            nWindowCharsX = max(1, nWindowX/nCharX); 
 
            // Determine the height of the client area, in 
            // pixels and in number of characters. 
 
            nWindowY = HIWORD(lParam); 
            nWindowCharsY = max(1, nWindowY/nCharY); 
 
            // Clear the buffer that holds the text input. 
 
            if (pTextMatrix != NULL) 
                free(pTextMatrix); 
 
            // If there is enough memory, allocate space for the 
            // text input buffer. 
 
            pTextMatrix = malloc(nWindowCharsX * nWindowCharsY); 
 
            if (pTextMatrix == NULL) 
                ErrorHandler("Not enough memory."); 
            else 
                for (y = 0; y < nWindowCharsY; y++) 
                    for (x = 0; x < nWindowCharsX; x++) 
                        TEXTMATRIX(x, y) = ' '; 
 
            // Move the caret to the origin. 
 
            SetCaretPos(0, 0); 
 
            return 0; 
 
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_HOME:       // Home 
                    nCaretPosX = 0; 
                    break; 
 
                case VK_END:        // End 
                    nCaretPosX = nWindowCharsX - 1; 
                    break; 
 
                case VK_PRIOR:      // Page Up 
                    nCaretPosY = 0; 
                    break; 
 
                case VK_NEXT:       // Page Down 
                    nCaretPosY = nWindowCharsY -1; 
                    break; 
 
                case VK_LEFT:       // Left arrow 
                    nCaretPosX = max(nCaretPosX - 1, 0); 
                    break; 
 
                case VK_RIGHT:      // Right arrow 
                    nCaretPosX = min(nCaretPosX + 1, 
                        nWindowCharsX - 1); 
                    break; 
 
                case VK_UP:         // Up arrow 
                    nCaretPosY = max(nCaretPosY - 1, 0); 
                    break; 
 
                case VK_DOWN:       // Down arrow 
                    nCaretPosY = min(nCaretPosY + 1, 
                        nWindowCharsY - 1); 
                    break; 
 
                case VK_DELETE:     // Delete 
 
                // Move all the characters that followed the 
                // deleted character (on the same line) one 
                // space back (to the left) in the matrix. 
 
                    for (x = nCaretPosX; x < nWindowCharsX; x++) 
                        TEXTMATRIX(x, nCaretPosY) = 
                            TEXTMATRIX(x + 1, nCaretPosY); 
 
                    // Replace the last character on the 
                    // line with a space. 
 
                    TEXTMATRIX(nWindowCharsX - 1, 
                        nCaretPosY) = ' '; 
 
                    // The application will draw outside the 
                    // WM_PAINT message processing, so hide the caret. 
 
                    HideCaret(hwnd); 
 
                    // Redraw the line, adjusted for the 
                    // deleted character. 
 
                    hdc = GetDC(hwnd); 
                    SelectObject(hdc, 
                        GetStockObject(SYSTEM_FIXED_FONT)); 
 
                    TextOut(hdc, nCaretPosX * nCharX, 
                        nCaretPosY * nCharY, 
                        &TEXTMATRIX(nCaretPosX, nCaretPosY), 
                        nWindowCharsX - nCaretPosX); 
 
                    ReleaseDC(hwnd, hdc); 
 
                    // Display the caret. 
 
                    ShowCaret(hwnd); 
 
                    break; 
            } 
 
            // Adjust the caret position based on the 
            // virtual-key processing. 
 
            SetCaretPos(nCaretPosX * nCharX, 
                nCaretPosY * nCharY); 
 
            return 0; 
 
        case WM_CHAR: 
            switch (wParam) 
            { 
                case 0x08:          // Backspace 
                // Move the caret back one space, and then 
                // process this like the DEL key. 
 
                    if (nCaretPosX > 0) 
                    { 
                        nCaretPosX--; 
                        SendMessage(hwnd, WM_KEYDOWN, 
                            VK_DELETE, 1L); 
                    } 
                    break; 
 
                case 0x09:          // Tab 
                // Tab stops exist every four spaces, so add 
                // spaces until the user hits the next tab. 
 
                    do 
                    { 
                        SendMessage(hwnd, WM_CHAR, ' ', 1L); 
                    } while (nCaretPosX % 4 != 0); 
                    break; 
 
                case 0x0D:          // Carriage return 
                // Go to the beginning of the next line. 
                // The bottom line wraps around to the top. 
 
                    nCaretPosX = 0; 
 
                    if (++nCaretPosY == nWindowCharsY) 
                        nCaretPosY = 0; 
                    break; 
 
                case 0x1B:        // Escape 
                case 0x0A:        // Linefeed 
                    MessageBeep((UINT) -1); 
                    break; 
 
                default: 
                // Add the character to the text buffer. 
 
                    TEXTMATRIX(nCaretPosX, nCaretPosY) = 
                        (char) wParam; 
 
                // The application will draw outside the 
                // WM_PAINT message processing, so hide the caret. 
 
                    HideCaret(hwnd); 
 
                // Draw the character on the screen. 
 
                    hdc = GetDC(hwnd); 
                    SelectObject(hdc, 
                        GetStockObject(SYSTEM_FIXED_FONT)); 
 
                    TextOut(hdc, nCaretPosX * nCharX, 
                        nCaretPosY * nCharY, 
                        &TEXTMATRIX(nCaretPosX, nCaretPosY), 1); 
 
                    ReleaseDC(hwnd, hdc); 
 
                    // Display the caret. 
 
                    ShowCaret(hwnd); 
 
                    // Prepare to wrap around if you reached the 
                    // end of the line. 
 
                    if (++nCaretPosX == nWindowCharsX) 
                    { 
                        nCaretPosX = 0; 
                        if (++nCaretPosY == nWindowCharsY) 
                            nCaretPosY = 0; 
                    } 
                    break; 
            } 
 
            // Adjust the caret position based on the 
            // character processing. 
 
            SetCaretPos(nCaretPosX * nCharX, 
                nCaretPosY * nCharY); 
 
            return 0; 
 
        case WM_PAINT: 
        // Draw all the characters in the buffer, line by line. 
 
            hdc = BeginPaint(hwnd, &ps); 
 
            SelectObject(hdc, 
                GetStockObject(SYSTEM_FIXED_FONT)); 
 
            for (y = 0; y < nWindowCharsY; y++) 
                TextOut(hdc, 0, y * nCharY, &TEXTMATRIX(0, y), 
                    nWindowCharsX); 
 
            EndPaint(hwnd, &ps); 
 
        case WM_SETFOCUS: 
        // The window has the input focus. Load the 
        // application-defined caret resource. 
 
            hCaret = LoadBitmap(hinst, MAKEINTRESOURCE(120)); 
 
            // Create the caret. 
 
            CreateCaret(hwnd, hCaret, 0, 0); 
 
            // Adjust the caret position. 
 
            SetCaretPos(nCaretPosX * nCharX, 
                nCaretPosY * nCharY); 
 
            // Display the caret. 
 
            ShowCaret(hwnd); 
 
            break; 
 
        case WM_KILLFOCUS: 
        // The window is losing the input focus, 
        // so destroy the caret. 
 
            DestroyCaret(); 
 
            break; 
 
        default: 
            return DefWindowProc(hwnd, message, wParam, lParam); 
 
    } 
 
    return NULL; 
} 
```



 

 