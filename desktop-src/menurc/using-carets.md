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
ms.openlocfilehash: e6450a3169588b3072d1fee271f4890a7cdeafd2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031132"
---
# <a name="using-carets"></a><span data-ttu-id="39631-120">Utilisation des signes d’insertion</span><span class="sxs-lookup"><span data-stu-id="39631-120">Using Carets</span></span>

<span data-ttu-id="39631-121">Cette section contient des exemples de code pour les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="39631-121">This section has code samples for the following tasks:</span></span>

-   [<span data-ttu-id="39631-122">Création et affichage d’un signe insertion</span><span class="sxs-lookup"><span data-stu-id="39631-122">Creating and Displaying a Caret</span></span>](#creating-and-displaying-a-caret)
-   [<span data-ttu-id="39631-123">Masquage d’un signe insertion</span><span class="sxs-lookup"><span data-stu-id="39631-123">Hiding a Caret</span></span>](#hiding-a-caret)
-   [<span data-ttu-id="39631-124">Destruction d’un signe insertion</span><span class="sxs-lookup"><span data-stu-id="39631-124">Destroying a Caret</span></span>](#destroying-a-caret)
-   [<span data-ttu-id="39631-125">Réglage de la durée de clignotement</span><span class="sxs-lookup"><span data-stu-id="39631-125">Adjusting the Blink Time</span></span>](#adjusting-the-blink-time)
-   [<span data-ttu-id="39631-126">Traitement de l’entrée au clavier</span><span class="sxs-lookup"><span data-stu-id="39631-126">Processing Keyboard Input</span></span>](#processing-keyboard-input)

## <a name="creating-and-displaying-a-caret"></a><span data-ttu-id="39631-127">Création et affichage d’un signe insertion</span><span class="sxs-lookup"><span data-stu-id="39631-127">Creating and Displaying a Caret</span></span>

<span data-ttu-id="39631-128">Lorsqu’il reçoit le focus clavier, la fenêtre doit créer et afficher le signe insertion.</span><span class="sxs-lookup"><span data-stu-id="39631-128">Upon receiving the keyboard focus, the window should create and display the caret.</span></span> <span data-ttu-id="39631-129">Utilisez la fonction [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) pour créer un signe insertion dans la fenêtre donnée.</span><span class="sxs-lookup"><span data-stu-id="39631-129">Use the [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) function to create a caret in the given window.</span></span> <span data-ttu-id="39631-130">Vous pouvez ensuite appeler [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) pour définir la position actuelle du signe insertion et [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) pour rendre le signe insertion visible.</span><span class="sxs-lookup"><span data-stu-id="39631-130">You can then call [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) to set the current position of the caret and [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) to make the caret visible.</span></span>

<span data-ttu-id="39631-131">Le système envoie le message [**WM \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus) à la fenêtre qui reçoit le focus clavier ; par conséquent, une application doit créer et afficher le signe insertion lors du traitement de ce message.</span><span class="sxs-lookup"><span data-stu-id="39631-131">The system sends the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message to the window receiving keyboard focus; therefore, an application should create and display the caret while processing this message.</span></span>


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



<span data-ttu-id="39631-132">Pour créer un signe insertion en fonction d’une image bitmap, vous devez spécifier un handle de bitmap lors de l’utilisation de [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret).</span><span class="sxs-lookup"><span data-stu-id="39631-132">To create a caret based on a bitmap, you must specify a bitmap handle when using [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret).</span></span> <span data-ttu-id="39631-133">Vous pouvez utiliser une application graphique pour créer l’image bitmap et un compilateur de ressources pour ajouter l’image bitmap aux ressources de votre application.</span><span class="sxs-lookup"><span data-stu-id="39631-133">You can use a graphics application to create the bitmap and a resource compiler to add the bitmap to your application's resources.</span></span> <span data-ttu-id="39631-134">Votre application peut ensuite utiliser la fonction [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) pour charger le descripteur de bitmap.</span><span class="sxs-lookup"><span data-stu-id="39631-134">Your application can then use the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function to load the bitmap handle.</span></span> <span data-ttu-id="39631-135">Par exemple, vous pouvez remplacer la ligne **CreateCaret** dans l’exemple précédent par les lignes suivantes pour créer un signe insertion de bitmap.</span><span class="sxs-lookup"><span data-stu-id="39631-135">For example, you could replace the **CreateCaret** line in the preceding example with the following lines to create a bitmap caret.</span></span>


```
// Load the application-defined caret resource. 
 
    hCaret = LoadBitmap(hinst, MAKEINTRESOURCE(120)); 
 
// Create a bitmap caret. 
 
    CreateCaret(hwnd, hCaret, 0, 0); 
```



<span data-ttu-id="39631-136">Vous pouvez également utiliser la fonction [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) ou [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) pour récupérer le handle de l’image bitmap du signe insertion.</span><span class="sxs-lookup"><span data-stu-id="39631-136">Alternatively, you can use the [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) or [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) function to retrieve the handle of the caret bitmap.</span></span> <span data-ttu-id="39631-137">Pour plus d’informations sur les bitmaps, consultez [bitmaps](/windows/desktop/gdi/bitmaps).</span><span class="sxs-lookup"><span data-stu-id="39631-137">For more information about bitmaps, see [Bitmaps](/windows/desktop/gdi/bitmaps).</span></span>

<span data-ttu-id="39631-138">Si votre application spécifie un descripteur de bitmap, [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) ignore les paramètres de largeur et de hauteur.</span><span class="sxs-lookup"><span data-stu-id="39631-138">If your application specifies a bitmap handle, [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) ignores the width and height parameters.</span></span> <span data-ttu-id="39631-139">La bitmap définit la taille du signe insertion.</span><span class="sxs-lookup"><span data-stu-id="39631-139">The bitmap defines the size of the caret.</span></span>

## <a name="hiding-a-caret"></a><span data-ttu-id="39631-140">Masquage d’un signe insertion</span><span class="sxs-lookup"><span data-stu-id="39631-140">Hiding a Caret</span></span>

<span data-ttu-id="39631-141">Chaque fois que votre application redessine un écran lors du traitement d’un message autre que [**WM \_ Paint**](/windows/desktop/gdi/wm-paint), elle doit rendre le signe insertion invisible à l’aide de la fonction [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) .</span><span class="sxs-lookup"><span data-stu-id="39631-141">Whenever your application redraws a screen while processing a message other than [**WM\_PAINT**](/windows/desktop/gdi/wm-paint), it must make the caret invisible by using the [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) function.</span></span> <span data-ttu-id="39631-142">Une fois le dessin terminé, réaffichez le signe insertion à l’aide de la fonction [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) .</span><span class="sxs-lookup"><span data-stu-id="39631-142">When your application is finished drawing, redisplay the caret by using the [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) function.</span></span> <span data-ttu-id="39631-143">Si votre application traite le message **WM \_ Paint** , il n’est pas nécessaire de masquer et de réafficher le signe insertion, car cette fonction effectue cette opération automatiquement.</span><span class="sxs-lookup"><span data-stu-id="39631-143">If your application processes the **WM\_PAINT** message, it is not necessary to hide and redisplay the caret, because this function does this automatically.</span></span>

<span data-ttu-id="39631-144">L’exemple de code suivant montre comment faire en sorte que votre application masque le signe insertion tout en dessinant un caractère à l’écran et lors du traitement du message [**WM \_ char**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="39631-144">The following code sample shows how to have your application hide the caret while drawing a character on the screen and while processing the [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span>


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



<span data-ttu-id="39631-145">Si votre application appelle la fonction [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) plusieurs fois sans appeler [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret), le signe insertion n’est pas affiché tant que l’application n’a pas également appelé **ShowCaret** le même nombre de fois.</span><span class="sxs-lookup"><span data-stu-id="39631-145">If your application calls the [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) function several times without calling [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret), the caret will not be displayed until the application also calls **ShowCaret** the same number of times.</span></span>

## <a name="destroying-a-caret"></a><span data-ttu-id="39631-146">Destruction d’un signe insertion</span><span class="sxs-lookup"><span data-stu-id="39631-146">Destroying a Caret</span></span>

<span data-ttu-id="39631-147">Quand une fenêtre perd le focus clavier, le système envoie le message [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="39631-147">When a window loses the keyboard focus, the system sends the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message to the window.</span></span> <span data-ttu-id="39631-148">Votre application doit détruire le signe insertion lors du traitement de ce message à l’aide de la fonction [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) .</span><span class="sxs-lookup"><span data-stu-id="39631-148">Your application should destroy the caret while processing this message by using the [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) function.</span></span> <span data-ttu-id="39631-149">Le code suivant montre comment détruire un signe insertion dans une fenêtre qui n’a plus le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="39631-149">The following code shows how to destroy a caret in a window that no longer has the keyboard focus.</span></span>


```
case WM_KILLFOCUS: 
 
// The window is losing the keyboard focus, so destroy the caret. 
 
    DestroyCaret(); 
 
    break; 
```



## <a name="adjusting-the-blink-time"></a><span data-ttu-id="39631-150">Réglage de la durée de clignotement</span><span class="sxs-lookup"><span data-stu-id="39631-150">Adjusting the Blink Time</span></span>

<span data-ttu-id="39631-151">Dans Windows 16 bits, une application Windows peut appeler la fonction [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) pour enregistrer la durée de clignotement actuelle, puis appeler la fonction [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) pour ajuster la durée de clignotement lors du traitement du message [**WM \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="39631-151">In 16-bit Windows, a Windows-based application could call the [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) function to save the current blink time, then call the [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) function to adjust the blink time during its processing of the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span> <span data-ttu-id="39631-152">L’application restaure la durée de clignotement enregistrée pour l’utilisation d’autres applications en appelant **SetCaretBlinkTime** lors du traitement du message [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) .</span><span class="sxs-lookup"><span data-stu-id="39631-152">The application would restore the saved blink time for the use of other applications by calling **SetCaretBlinkTime** during its processing of the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message.</span></span> <span data-ttu-id="39631-153">Toutefois, cette technique ne fonctionne pas dans les environnements multithreads.</span><span class="sxs-lookup"><span data-stu-id="39631-153">However, this technique does not work in multithreaded environments.</span></span> <span data-ttu-id="39631-154">Plus précisément, la désactivation d’une application n’est pas synchronisée avec l’activation d’une autre application, de sorte que si une application se bloque, une autre application peut toujours être activée.</span><span class="sxs-lookup"><span data-stu-id="39631-154">Specifically, the deactivation of one application is not synchronized with the activation of another application, so that if one application hangs, another application can still be activated.</span></span>

<span data-ttu-id="39631-155">Les applications doivent respecter la durée de clignotement choisie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="39631-155">Applications should respect the blink time chosen by the user.</span></span> <span data-ttu-id="39631-156">La fonction [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) doit être appelée uniquement par une application qui permet à l’utilisateur de définir la durée de clignotement.</span><span class="sxs-lookup"><span data-stu-id="39631-156">The [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) function should only be called by an application that allows the user to set the blink time.</span></span>

## <a name="processing-keyboard-input"></a><span data-ttu-id="39631-157">Traitement de l’entrée au clavier</span><span class="sxs-lookup"><span data-stu-id="39631-157">Processing Keyboard Input</span></span>

<span data-ttu-id="39631-158">L’exemple suivant montre comment utiliser un signe insertion dans un simple éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="39631-158">The following example demonstrates how to use a caret in a simple text editor.</span></span> <span data-ttu-id="39631-159">L’exemple met à jour l’emplacement du signe insertion lorsque l’utilisateur tape des caractères imprimables et utilise différentes clés pour se déplacer dans la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="39631-159">The example updates the caret position as the user types printable characters and uses various keys to move through the client area.</span></span>


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



 

 