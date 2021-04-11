---
title: Utilisation de l’entrée de souris
description: Cette section traite des tâches associées à l’entrée de souris.
ms.assetid: b96d0046-a507-4733-bcf3-fcf757beec7f
keywords:
- entrée utilisateur, entrée de la souris
- capture de l’entrée utilisateur, entrée de la souris
- entrées de la souris
- curseurs, entrée de la souris
- curseur de la souris
- double-cliquez sur traitement des messages
- roulette de la souris
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50b34f180aad6aec6120bf4e3ffa997eba13e760
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314945"
---
# <a name="using-mouse-input"></a><span data-ttu-id="f686e-110">Utilisation de l’entrée de souris</span><span class="sxs-lookup"><span data-stu-id="f686e-110">Using Mouse Input</span></span>

<span data-ttu-id="f686e-111">Cette section traite des tâches associées à l’entrée de souris.</span><span class="sxs-lookup"><span data-stu-id="f686e-111">This section covers tasks associated with mouse input.</span></span>

-   [<span data-ttu-id="f686e-112">Suivi du curseur de la souris</span><span class="sxs-lookup"><span data-stu-id="f686e-112">Tracking the Mouse Cursor</span></span>](#tracking-the-mouse-cursor)
-   [<span data-ttu-id="f686e-113">Dessin de lignes à l’aide de la souris</span><span class="sxs-lookup"><span data-stu-id="f686e-113">Drawing Lines with the Mouse</span></span>](#drawing-lines-with-the-mouse)
-   [<span data-ttu-id="f686e-114">Traitement d’un message de double-clic</span><span class="sxs-lookup"><span data-stu-id="f686e-114">Processing a Double Click Message</span></span>](#processing-a-double-click-message)
-   [<span data-ttu-id="f686e-115">Sélection d’une ligne de texte</span><span class="sxs-lookup"><span data-stu-id="f686e-115">Selecting a Line of Text</span></span>](#selecting-a-line-of-text)
-   [<span data-ttu-id="f686e-116">Utilisation d’une roulette de souris dans un document avec des objets incorporés</span><span class="sxs-lookup"><span data-stu-id="f686e-116">Using a Mouse Wheel in a Document with Embedded Objects</span></span>](#using-a-mouse-wheel-in-a-document-with-embedded-objects)
-   [<span data-ttu-id="f686e-117">Récupération du nombre de lignes de défilement de la roulette de la souris</span><span class="sxs-lookup"><span data-stu-id="f686e-117">Retrieving the Number of Mouse Wheel Scroll Lines</span></span>](#retrieving-the-number-of-mouse-wheel-scroll-lines)

## <a name="tracking-the-mouse-cursor"></a><span data-ttu-id="f686e-118">Suivi du curseur de la souris</span><span class="sxs-lookup"><span data-stu-id="f686e-118">Tracking the Mouse Cursor</span></span>

<span data-ttu-id="f686e-119">Les applications effectuent souvent des tâches qui impliquent le suivi de la position du curseur de la souris.</span><span class="sxs-lookup"><span data-stu-id="f686e-119">Applications often perform tasks that involve tracking the position of the mouse cursor.</span></span> <span data-ttu-id="f686e-120">La plupart des applications de dessin, par exemple, effectuent le suivi de la position du curseur de la souris pendant les opérations de dessin, ce qui permet à l’utilisateur de dessiner dans la zone cliente d’une fenêtre en faisant glisser la souris.</span><span class="sxs-lookup"><span data-stu-id="f686e-120">Most drawing applications, for example, track the position of the mouse cursor during drawing operations, allowing the user to draw in a window's client area by dragging the mouse.</span></span> <span data-ttu-id="f686e-121">Les applications de traitement de texte suivent également le curseur, ce qui permet à l’utilisateur de sélectionner un mot ou un bloc de texte en cliquant et en faisant glisser la souris.</span><span class="sxs-lookup"><span data-stu-id="f686e-121">Word-processing applications also track the cursor, enabling the user to select a word or block of text by clicking and dragging the mouse.</span></span>

<span data-ttu-id="f686e-122">Le suivi du curseur implique généralement le traitement des messages [**WM \_ LBUTTONDOWN**](wm-lbuttondown.md), [**WM \_ MOUSEMOVE**](wm-mousemove.md)et [**WM \_ LBUTTONUP**](wm-lbuttonup.md) .</span><span class="sxs-lookup"><span data-stu-id="f686e-122">Tracking the cursor typically involves processing the [**WM\_LBUTTONDOWN**](wm-lbuttondown.md), [**WM\_MOUSEMOVE**](wm-mousemove.md), and [**WM\_LBUTTONUP**](wm-lbuttonup.md) messages.</span></span> <span data-ttu-id="f686e-123">Une fenêtre détermine quand commencer le suivi du curseur en vérifiant la position du curseur fournie dans le paramètre *lParam* du message **WM \_ LBUTTONDOWN** .</span><span class="sxs-lookup"><span data-stu-id="f686e-123">A window determines when to begin tracking the cursor by checking the cursor position provided in the *lParam* parameter of the **WM\_LBUTTONDOWN** message.</span></span> <span data-ttu-id="f686e-124">Par exemple, une application de traitement de texte commence à suivre le curseur uniquement si le message **WM \_ LBUTTONDOWN** s’est produit alors que le curseur se trouvait sur une ligne de texte, mais pas s’il se trouvait au-delà de la fin du document.</span><span class="sxs-lookup"><span data-stu-id="f686e-124">For example, a word-processing application would begin tracking the cursor only if the **WM\_LBUTTONDOWN** message occurred while the cursor was on a line of text, but not if it was past the end of the document.</span></span>

<span data-ttu-id="f686e-125">Une fenêtre effectue le suivi de la position du curseur en traitant le flux des messages [**WM \_ MOUSEMOVE**](wm-mousemove.md) postés dans la fenêtre à mesure que la souris se déplace.</span><span class="sxs-lookup"><span data-stu-id="f686e-125">A window tracks the position of the cursor by processing the stream of [**WM\_MOUSEMOVE**](wm-mousemove.md) messages posted to the window as the mouse moves.</span></span> <span data-ttu-id="f686e-126">Le traitement du message **WM \_ MOUSEMOVE** implique généralement une opération de peinture ou de dessin répétée dans la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="f686e-126">Processing the **WM\_MOUSEMOVE** message typically involves a repetitive painting or drawing operation in the client area.</span></span> <span data-ttu-id="f686e-127">Par exemple, une application de dessin peut redessiner une ligne à plusieurs reprises à mesure que la souris se déplace.</span><span class="sxs-lookup"><span data-stu-id="f686e-127">For example, a drawing application might redraw a line repeatedly as the mouse moves.</span></span> <span data-ttu-id="f686e-128">Une fenêtre utilise le message [**WM \_ LBUTTONUP**](wm-lbuttonup.md) comme signal pour arrêter le suivi du curseur.</span><span class="sxs-lookup"><span data-stu-id="f686e-128">A window uses the [**WM\_LBUTTONUP**](wm-lbuttonup.md) message as a signal to stop tracking the cursor.</span></span>

<span data-ttu-id="f686e-129">En outre, une application peut appeler la fonction [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) pour que le système envoie d’autres messages utiles pour le suivi du curseur.</span><span class="sxs-lookup"><span data-stu-id="f686e-129">In addition, an application can call the [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) function to have the system send other messages that are useful for tracking the cursor.</span></span> <span data-ttu-id="f686e-130">Le système publie le message [**WM \_ MOUSEHOVER**](wm-mousehover.md) quand le curseur pointe sur la zone cliente pendant une certaine période.</span><span class="sxs-lookup"><span data-stu-id="f686e-130">The system posts the [**WM\_MOUSEHOVER**](wm-mousehover.md) message when the cursor hovers over the client area for a certain time period.</span></span> <span data-ttu-id="f686e-131">Il publie le message [**WM \_ MOUSELEAVE**](wm-mouseleave.md) lorsque le curseur quitte la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="f686e-131">It posts the [**WM\_MOUSELEAVE**](wm-mouseleave.md) message when the cursor leaves the client area.</span></span> <span data-ttu-id="f686e-132">Les messages [**WM \_ NCMOUSEHOVER**](wm-ncmousehover.md) et [**WM \_ NCMOUSELEAVE**](wm-ncmouseleave.md) sont les messages correspondants pour les zones non clientes.</span><span class="sxs-lookup"><span data-stu-id="f686e-132">The [**WM\_NCMOUSEHOVER**](wm-ncmousehover.md) and [**WM\_NCMOUSELEAVE**](wm-ncmouseleave.md) messages are the corresponding messages for the nonclient areas.</span></span>

## <a name="drawing-lines-with-the-mouse"></a><span data-ttu-id="f686e-133">Dessin de lignes à l’aide de la souris</span><span class="sxs-lookup"><span data-stu-id="f686e-133">Drawing Lines with the Mouse</span></span>

<span data-ttu-id="f686e-134">L’exemple de cette section montre comment suivre le curseur de la souris.</span><span class="sxs-lookup"><span data-stu-id="f686e-134">The example in this section demonstrates how to track the mouse cursor.</span></span> <span data-ttu-id="f686e-135">Elle contient des parties d’une procédure de fenêtre qui permet à l’utilisateur de dessiner des lignes dans la zone cliente d’une fenêtre en faisant glisser la souris.</span><span class="sxs-lookup"><span data-stu-id="f686e-135">It contains portions of a window procedure that enables the user to draw lines in a window's client area by dragging the mouse.</span></span>

<span data-ttu-id="f686e-136">Lorsque la procédure de fenêtre reçoit un message [**WM \_ LBUTTONDOWN**](wm-lbuttondown.md) , elle capture la souris et enregistre les coordonnées du curseur, en utilisant les coordonnées comme point de départ de la ligne.</span><span class="sxs-lookup"><span data-stu-id="f686e-136">When the window procedure receives a [**WM\_LBUTTONDOWN**](wm-lbuttondown.md) message, it captures the mouse and saves the coordinates of the cursor, using the coordinates as the starting point of the line.</span></span> <span data-ttu-id="f686e-137">Elle utilise également la fonction [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) pour limiter le curseur à la zone cliente pendant l’opération de dessin de ligne.</span><span class="sxs-lookup"><span data-stu-id="f686e-137">It also uses the [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) function to confine the cursor to the client area during the line drawing operation.</span></span>

<span data-ttu-id="f686e-138">Pendant le premier message [**WM \_ MOUSEMOVE**](wm-mousemove.md) , la procédure de fenêtre dessine une ligne à partir du point de départ jusqu’à la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="f686e-138">During the first [**WM\_MOUSEMOVE**](wm-mousemove.md) message, the window procedure draws a line from the starting point to the current position of the cursor.</span></span> <span data-ttu-id="f686e-139">Lors des messages de la **\_ souris WM** suivants, la procédure de fenêtre efface la ligne précédente en dessinant avec une couleur de stylet inversée.</span><span class="sxs-lookup"><span data-stu-id="f686e-139">During subsequent **WM\_MOUSEMOVE** messages, the window procedure erases the previous line by drawing over it with an inverted pen color.</span></span> <span data-ttu-id="f686e-140">Elle dessine ensuite une nouvelle ligne à partir du point de départ jusqu’à la nouvelle position du curseur.</span><span class="sxs-lookup"><span data-stu-id="f686e-140">Then it draws a new line from the starting point to the new position of the cursor.</span></span>

<span data-ttu-id="f686e-141">Le message [**WM \_ LBUTTONUP**](wm-lbuttonup.md) signale la fin de l’opération de dessin.</span><span class="sxs-lookup"><span data-stu-id="f686e-141">The [**WM\_LBUTTONUP**](wm-lbuttonup.md) message signals the end of the drawing operation.</span></span> <span data-ttu-id="f686e-142">La procédure de fenêtre libère la capture de la souris et libère la souris à partir de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="f686e-142">The window procedure releases the mouse capture and frees the mouse from the client area.</span></span>


```
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    HDC hdc;                       // handle to device context 
    RECT rcClient;                 // client area rectangle 
    POINT ptClientUL;              // client upper left corner 
    POINT ptClientLR;              // client lower right corner 
    static POINTS ptsBegin;        // beginning point 
    static POINTS ptsEnd;          // new endpoint 
    static POINTS ptsPrevEnd;      // previous endpoint 
    static BOOL fPrevLine = FALSE; // previous line flag 
 
    switch (uMsg) 
    { 
       case WM_LBUTTONDOWN: 
 
            // Capture mouse input. 
 
            SetCapture(hwndMain); 
 
            // Retrieve the screen coordinates of the client area, 
            // and convert them into client coordinates. 
 
            GetClientRect(hwndMain, &rcClient); 
            ptClientUL.x = rcClient.left; 
            ptClientUL.y = rcClient.top; 
 
            // Add one to the right and bottom sides, because the 
            // coordinates retrieved by GetClientRect do not 
            // include the far left and lowermost pixels. 
 
            ptClientLR.x = rcClient.right + 1; 
            ptClientLR.y = rcClient.bottom + 1; 
            ClientToScreen(hwndMain, &ptClientUL); 
            ClientToScreen(hwndMain, &ptClientLR); 
 
            // Copy the client coordinates of the client area 
            // to the rcClient structure. Confine the mouse cursor 
            // to the client area by passing the rcClient structure 
            // to the ClipCursor function. 
 
            SetRect(&rcClient, ptClientUL.x, ptClientUL.y, 
                ptClientLR.x, ptClientLR.y); 
            ClipCursor(&rcClient); 
 
            // Convert the cursor coordinates into a POINTS 
            // structure, which defines the beginning point of the 
            // line drawn during a WM_MOUSEMOVE message. 
 
            ptsBegin = MAKEPOINTS(lParam); 
            return 0; 
 
        case WM_MOUSEMOVE: 
 
            // When moving the mouse, the user must hold down 
            // the left mouse button to draw lines. 
 
            if (wParam & MK_LBUTTON) 
            { 
 
                // Retrieve a device context (DC) for the client area. 
 
                hdc = GetDC(hwndMain); 
 
                // The following function ensures that pixels of 
                // the previously drawn line are set to white and 
                // those of the new line are set to black. 
 
                SetROP2(hdc, R2_NOTXORPEN); 
 
                // If a line was drawn during an earlier WM_MOUSEMOVE 
                // message, draw over it. This erases the line by 
                // setting the color of its pixels to white. 
 
                if (fPrevLine) 
                { 
                    MoveToEx(hdc, ptsBegin.x, ptsBegin.y, 
                        (LPPOINT) NULL); 
                    LineTo(hdc, ptsPrevEnd.x, ptsPrevEnd.y); 
                } 
 
                // Convert the current cursor coordinates to a 
                // POINTS structure, and then draw a new line. 
 
                ptsEnd = MAKEPOINTS(lParam); 
                MoveToEx(hdc, ptsBegin.x, ptsBegin.y, (LPPOINT) NULL); 
                LineTo(hdc, ptsEnd.x, ptsEnd.y); 
 
                // Set the previous line flag, save the ending 
                // point of the new line, and then release the DC. 
 
                fPrevLine = TRUE; 
                ptsPrevEnd = ptsEnd; 
                ReleaseDC(hwndMain, hdc); 
            } 
            break; 
 
        case WM_LBUTTONUP: 
 
            // The user has finished drawing the line. Reset the 
            // previous line flag, release the mouse cursor, and 
            // release the mouse capture. 
 
            fPrevLine = FALSE; 
            ClipCursor(NULL); 
            ReleaseCapture(); 
            return 0; 
 
        case WM_DESTROY: 
            PostQuitMessage(0); 
            break; 
 
        // Process other messages. 
        
```



## <a name="processing-a-double-click-message"></a><span data-ttu-id="f686e-143">Traitement d’un message de double-clic</span><span class="sxs-lookup"><span data-stu-id="f686e-143">Processing a Double Click Message</span></span>

<span data-ttu-id="f686e-144">Pour recevoir des messages de double-clic, une fenêtre doit appartenir à une classe de fenêtre qui a le style de classe [**cs \_ DBLCLKS**](/windows/desktop/winmsg/about-window-classes) .</span><span class="sxs-lookup"><span data-stu-id="f686e-144">To receive double-click messages, a window must belong to a window class that has the [**CS\_DBLCLKS**](/windows/desktop/winmsg/about-window-classes) class style.</span></span> <span data-ttu-id="f686e-145">Vous définissez ce style lors de l’inscription de la classe de fenêtre, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="f686e-145">You set this style when registering the window class, as shown in the following example.</span></span>


```
BOOL InitApplication(HINSTANCE hInstance) 
{ 
    WNDCLASS wc; 
 
    wc.style = CS_DBLCLKS | CS_HREDRAW | CS_VREDRAW; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hInstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_IBEAM); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName = "MainMenu"; 
    wc.lpszClassName = "MainWClass"; 
 
    return RegisterClass(&wc); 
} 
```



<span data-ttu-id="f686e-146">Un message de double-clic est toujours précédé d’un message de bouton.</span><span class="sxs-lookup"><span data-stu-id="f686e-146">A double-click message is always preceded by a button-down message.</span></span> <span data-ttu-id="f686e-147">Pour cette raison, les applications utilisent généralement un message de double-clic pour étendre une tâche lancée lors d’un message de bouton.</span><span class="sxs-lookup"><span data-stu-id="f686e-147">For this reason, applications typically use a double-click message to extend a task that it began during a button-down message.</span></span>

## <a name="selecting-a-line-of-text"></a><span data-ttu-id="f686e-148">Sélection d’une ligne de texte</span><span class="sxs-lookup"><span data-stu-id="f686e-148">Selecting a Line of Text</span></span>

<span data-ttu-id="f686e-149">L’exemple de cette section provient d’une application de traitement de texte simple.</span><span class="sxs-lookup"><span data-stu-id="f686e-149">The example in this section is taken from a simple word-processing application.</span></span> <span data-ttu-id="f686e-150">Il comprend du code qui permet à l’utilisateur de définir la position du signe insertion en cliquant n’importe où sur une ligne de texte et de sélectionner (mettre en surbrillance) une ligne de texte en double-cliquant n’importe où sur la ligne.</span><span class="sxs-lookup"><span data-stu-id="f686e-150">It includes code that enables the user to set the position of the caret by clicking anywhere on a line of text, and to select (highlight) a line of text by double-clicking anywhere on the line.</span></span>


```
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    HDC hdc;                     // handle to device context 
    TEXTMETRIC tm;               // font size data 
    int i, j;                    // loop counters 
    int cCR = 0;                 // count of carriage returns 
    char ch;                     // character from input buffer 
    static int nBegLine;         // beginning of selected line 
    static int nCurrentLine = 0; // currently selected line 
    static int nLastLine = 0;    // last text line 
    static int nCaretPosX = 0;   // x-coordinate of caret 
    static int cch = 0;          // number of characters entered 
    static int nCharWidth = 0;   // exact width of a character 
    static char szHilite[128];   // text string to highlight 
    static DWORD dwCharX;        // average width of characters 
    static DWORD dwLineHeight;   // line height 
    static POINTS ptsCursor;     // coordinates of mouse cursor 
    static COLORREF crPrevText;  // previous text color 
    static COLORREF crPrevBk;    // previous background color 
    static PTCHAR pchInputBuf;   // pointer to input buffer 
    static BOOL fTextSelected = FALSE; // text-selection flag 
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
            dwLineHeight = tm.tmHeight; 
 
            // Allocate a buffer to store keyboard input. 
 
            pchInputBuf = (LPSTR) GlobalAlloc(GPTR, 
                BUFSIZE * sizeof(TCHAR)); 
 
            return 0; 
 
        case WM_CHAR: 
            switch (wParam) 
            { 
                case 0x08:  // backspace 
                case 0x0A:  // linefeed 
                case 0x1B:  // escape 
                    MessageBeep( (UINT) -1); 
                    return 0; 
 
                case 0x09:  // tab 
 
                    // Convert tabs to four consecutive spaces. 
 
                    for (i = 0; i < 4; i++) 
                        SendMessage(hwndMain, WM_CHAR, 0x20, 0); 
                    return 0; 
 
                case 0x0D:  // carriage return 
 
                    // Record the carriage return, and position the 
                    // caret at the beginning of the new line. 
 
                    pchInputBuf[cch++] = 0x0D; 
                    nCaretPosX = 0; 
                    nCurrentLine += 1; 
                    break; 
 
                default:    / displayable character 
 
                    ch = (char) wParam; 
                    HideCaret(hwndMain); 
 
                    // Retrieve the character's width, and display the 
                    // character. 
 
                    hdc = GetDC(hwndMain); 
                    GetCharWidth32(hdc, (UINT) wParam, (UINT) wParam, 
                        &nCharWidth); 
                    TextOut(hdc, nCaretPosX, 
                        nCurrentLine * dwLineHeight, &ch, 1); 
                    ReleaseDC(hwndMain, hdc); 
 
                    // Store the character in the buffer. 
 
                    pchInputBuf[cch++] = ch; 
 
                    // Calculate the new horizontal position of the 
                    // caret. If the new position exceeds the maximum, 
                    // insert a carriage return and reposition the 
                    // caret at the beginning of the next line. 
 
                    nCaretPosX += nCharWidth; 
                    if ((DWORD) nCaretPosX > dwMaxCharX) 
                    { 
                        nCaretPosX = 0; 
                        pchInputBuf[cch++] = 0x0D; 
                        ++nCurrentLine; 
                    } 
 
                    ShowCaret(hwndMain); 
 
                    break; 
            } 
            SetCaretPos(nCaretPosX, nCurrentLine * dwLineHeight); 
            nLastLine = max(nLastLine, nCurrentLine); 
            break; 
 
        // Process other messages. 
 
        case WM_LBUTTONDOWN: 
 
            // If a line of text is currently highlighted, redraw 
            // the text to remove the highlighting. 
 
            if (fTextSelected) 
            { 
                hdc = GetDC(hwndMain); 
                SetTextColor(hdc, crPrevText); 
                SetBkColor(hdc, crPrevBk);
                hResult = StringCchLength(szHilite, 128/sizeof(TCHAR), pcch);
                if (FAILED(hResult))
                {
                // TODO: write error handler
                } 
                TextOut(hdc, 0, nCurrentLine * dwLineHeight, 
                    szHilite, *pcch); 
                ReleaseDC(hwndMain, hdc); 
                ShowCaret(hwndMain); 
                fTextSelected = FALSE; 
            } 
 
            // Save the current mouse-cursor coordinates. 
 
            ptsCursor = MAKEPOINTS(lParam); 
 
            // Determine which line the cursor is on, and save 
            // the line number. Do not allow line numbers greater 
            // than the number of the last line of text. The 
            // line number is later multiplied by the average height 
            // of the current font. The result is used to set the 
            // y-coordinate of the caret. 
 
            nCurrentLine = min((int)(ptsCursor.y / dwLineHeight), 
                nLastLine); 
 
            // Parse the text input buffer to find the first 
            // character in the selected line of text. Each 
            // line ends with a carriage return, so it is possible 
            // to count the carriage returns to find the selected 
            // line. 
 
            cCR = 0; 
            nBegLine = 0; 
            if (nCurrentLine != 0) 
            { 
                for (i = 0; (i < cch) && 
                        (cCR < nCurrentLine); i++) 
                { 
                    if (pchInputBuf[i] == 0x0D) 
                        ++cCR; 
                } 
                nBegLine = i; 
            } 
 
            // Starting at the beginning of the selected line, 
            // measure  the width of each character, summing the 
            // width with each character measured. Stop when the 
            // sum is greater than the x-coordinate of the cursor. 
            // The sum is used to set the x-coordinate of the caret. 
 
            hdc = GetDC(hwndMain); 
            nCaretPosX = 0; 
            for (i = nBegLine; 
                (pchInputBuf[i] != 0x0D) && (i < cch); i++) 
            { 
                ch = pchInputBuf[i]; 
                GetCharWidth32(hdc, (int) ch, (int) ch, &nCharWidth); 
                if ((nCaretPosX + nCharWidth) > ptsCursor.x) break; 
                else nCaretPosX += nCharWidth; 
            } 
            ReleaseDC(hwndMain, hdc); 
 
            // Set the caret to the user-selected position. 
 
            SetCaretPos(nCaretPosX, nCurrentLine * dwLineHeight); 
            break; 
 
        case WM_LBUTTONDBLCLK: 
 
            // Copy the selected line of text to a buffer. 
 
            for (i = nBegLine, j = 0; (pchInputBuf[i] != 0x0D) && 
                    (i < cch); i++) 
            {
                szHilite[j++] = pchInputBuf[i]; 
            }
            szHilite[j] = '\0'; 
 
            // Hide the caret, invert the background and foreground 
            // colors, and then redraw the selected line. 
 
            HideCaret(hwndMain); 
            hdc = GetDC(hwndMain); 
            crPrevText = SetTextColor(hdc, RGB(255, 255, 255)); 
            crPrevBk = SetBkColor(hdc, RGB(0, 0, 0));
            hResult = StringCchLength(szHilite, 128/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            } 
            TextOut(hdc, 0, nCurrentLine * dwLineHeight, szHilite, *pcch); 
            SetTextColor(hdc, crPrevText); 
            SetBkColor(hdc, crPrevBk); 
            ReleaseDC(hwndMain, hdc); 
 
            fTextSelected = TRUE; 
            break; 

            // Process other messages. 

        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



## <a name="using-a-mouse-wheel-in-a-document-with-embedded-objects"></a><span data-ttu-id="f686e-151">Utilisation d’une roulette de souris dans un document avec des objets incorporés</span><span class="sxs-lookup"><span data-stu-id="f686e-151">Using a Mouse Wheel in a Document with Embedded Objects</span></span>

<span data-ttu-id="f686e-152">Cet exemple suppose un document Microsoft Word avec divers objets incorporés :</span><span class="sxs-lookup"><span data-stu-id="f686e-152">This example assumes a Microsoft Word document with various embedded objects:</span></span>

-   <span data-ttu-id="f686e-153">Feuille de calcul Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="f686e-153">A Microsoft Excel spreadsheet</span></span>
-   <span data-ttu-id="f686e-154">Contrôle de zone de liste incorporé qui fait défiler la réponse à la roulette</span><span class="sxs-lookup"><span data-stu-id="f686e-154">An embedded list box control that scrolls in response to the wheel</span></span>
-   <span data-ttu-id="f686e-155">Contrôle de zone de texte incorporé qui ne répond pas à la roulette</span><span class="sxs-lookup"><span data-stu-id="f686e-155">An embedded text box control that does not respond to the wheel</span></span>

<span data-ttu-id="f686e-156">Le message [MSH \_ MOUSEWHEEL](about-mouse-input.md) est toujours envoyé à la fenêtre principale de Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="f686e-156">The [MSH\_MOUSEWHEEL](about-mouse-input.md) message is always sent to the main window in Microsoft Word.</span></span> <span data-ttu-id="f686e-157">Cela est vrai même si la feuille de calcul incorporée est active.</span><span class="sxs-lookup"><span data-stu-id="f686e-157">This is true even if the embedded spreadsheet is active.</span></span> <span data-ttu-id="f686e-158">Le tableau suivant explique comment le \_ message MSH MOUSEWHEEL est géré en fonction du focus.</span><span class="sxs-lookup"><span data-stu-id="f686e-158">The following table explains how the MSH\_MOUSEWHEEL message is handled according to the focus.</span></span>



| <span data-ttu-id="f686e-159">Le focus est activé</span><span class="sxs-lookup"><span data-stu-id="f686e-159">Focus is on</span></span>                | <span data-ttu-id="f686e-160">La gestion est la suivante :</span><span class="sxs-lookup"><span data-stu-id="f686e-160">Handling is as follows</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f686e-161">Document Word</span><span class="sxs-lookup"><span data-stu-id="f686e-161">Word document</span></span>              | <span data-ttu-id="f686e-162">Word fait défiler la fenêtre de document.</span><span class="sxs-lookup"><span data-stu-id="f686e-162">Word scrolls the document window.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="f686e-163">Feuille de calcul Excel incorporée</span><span class="sxs-lookup"><span data-stu-id="f686e-163">Embedded Excel spreadsheet</span></span> | <span data-ttu-id="f686e-164">Word publie le message dans Excel.</span><span class="sxs-lookup"><span data-stu-id="f686e-164">Word posts the message to Excel.</span></span> <span data-ttu-id="f686e-165">Vous devez décider si l’application incorporée doit répondre au message ou non.</span><span class="sxs-lookup"><span data-stu-id="f686e-165">You must decide if the embedded application should respond to the message or not.</span></span>                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="f686e-166">Contrôle incorporé</span><span class="sxs-lookup"><span data-stu-id="f686e-166">Embedded control</span></span>           | <span data-ttu-id="f686e-167">C’est à l’application d’envoyer le message à un contrôle incorporé qui a le focus et de vérifier le code de retour pour voir si le contrôle l’a géré.</span><span class="sxs-lookup"><span data-stu-id="f686e-167">It is up to the application to send the message to an embedded control that has the focus and check the return code to see if the control handled it.</span></span> <span data-ttu-id="f686e-168">Si le contrôle ne l’a pas géré, l’application doit faire défiler la fenêtre de document.</span><span class="sxs-lookup"><span data-stu-id="f686e-168">If the control did not handle it, then the application should scroll the document window.</span></span> <span data-ttu-id="f686e-169">Par exemple, si l’utilisateur a cliqué sur une zone de liste, puis a reporté la roue, ce contrôle défilerait en réponse à une rotation de roulette.</span><span class="sxs-lookup"><span data-stu-id="f686e-169">For example, if the user clicked a list box and then rolled the wheel, that control would scroll in response to a wheel rotation.</span></span> <span data-ttu-id="f686e-170">Si l’utilisateur a cliqué sur une zone de texte, puis a fait pivoter la roue, le document entier défilerait.</span><span class="sxs-lookup"><span data-stu-id="f686e-170">If the user clicked a text box and then rotated the wheel, the whole document would scroll.</span></span> |



 

<span data-ttu-id="f686e-171">L’exemple suivant montre comment une application peut gérer les deux messages de roulette.</span><span class="sxs-lookup"><span data-stu-id="f686e-171">This following example shows how an application might handle the two wheel messages.</span></span>


```
/************************************************
* this code deals with MSH_MOUSEWHEEL
*************************************************/
#include "zmouse.h"

//
// Mouse Wheel rotation stuff, only define if we are
// on a version of the OS that does not support
// WM_MOUSEWHEEL messages.
//
#ifndef WM_MOUSEWHEEL
#define WM_MOUSEWHEEL WM_MOUSELAST+1 
    // Message ID for IntelliMouse wheel
#endif

UINT uMSH_MOUSEWHEEL = 0;   // Value returned from
                            // RegisterWindowMessage()

/**************************************************

INT WINAPI WinMain(
         HINSTANCE hInst, 
         HINSTANCE hPrevInst, 
         LPSTR lpCmdLine, 
         INT nCmdShow)
{
    MSG msg;
    BOOL bRet;

    if (!InitInstance(hInst, nCmdShow))
        return FALSE;

    //
    // The new IntelliMouse uses a Registered message to transmit
    // wheel rotation info. So register for it!
 
    uMSH_MOUSEWHEEL =
     RegisterWindowMessage(MSH_MOUSEWHEEL); 
    if ( !uMSH_MOUSEWHEEL )
    {
        MessageBox(NULL,"
                   RegisterWindowMessag Failed!",
                   "Error",MB_OK);
        return msg.wParam;
    }
    
    while (( bRet = GetMessage(&msg, NULL, 0, 0)) != 0)
    {
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        {
            if (!TranslateAccelerator(ghwndApp,
                                      ghaccelTable,
                                      &msg))
            {
                TranslateMessage(&msg);
                DispatchMessage(&msg);
            }
        }
    }

    return msg.wParam;
}

/************************************************
* this code deals with WM_MOUSEWHEEL
*************************************************/
LONG APIENTRY MainWndProc(
    HWND hwnd,
    UINT msg,
    WPARAM wParam,
    LPARAM lParam)
{
    static int nZoom = 0;
    

    switch (msg)
    {
        //
        // Handle Mouse Wheel messages generated
        // by the operating systems that have built-in
        // support for the WM_MOUSEWHEEL message.
        //

        case WM_MOUSEWHEEL:
            ((short) HIWORD(wParam)< 0) ? nZoom-- : nZoom++;

            //
            // Do other wheel stuff...
            //

            break;

        default:
            //
            // uMSH_MOUSEWHEEL is a message registered by
            // the mswheel dll on versions of Windows that
            // do not support the new message in the OS.

            if( msg == uMSH_MOUSEWHEEL )
            {
               ((int)wParam < 0) ? nZoom-- : nZoom++;

                //
                // Do other wheel stuff...
                //
                break;
            }

            return DefWindowProc(hwnd,
                                 msg,
                                 wParam,
                                 lParam);
    }

    return 0L;
}
```



## <a name="retrieving-the-number-of-mouse-wheel-scroll-lines"></a><span data-ttu-id="f686e-172">Récupération du nombre de lignes de défilement de la roulette de la souris</span><span class="sxs-lookup"><span data-stu-id="f686e-172">Retrieving the Number of Mouse Wheel Scroll Lines</span></span>

<span data-ttu-id="f686e-173">Le code suivant permet à une application de récupérer le nombre de lignes de défilement à l’aide de la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) .</span><span class="sxs-lookup"><span data-stu-id="f686e-173">The following code allows an application to retrieve the number of scroll lines using the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>


```
#ifndef SPI_GETWHEELSCROLLLINES
#define SPI_GETWHEELSCROLLLINES   104
#endif

#include "zmouse.h"

/*********************************************************
* FUNCTION: GetNumScrollLines
* Purpose : An OS independent method to retrieve the 
*           number of wheel scroll lines
* Params  : none
* Returns : UINT:  Number of scroll lines where WHEEL_PAGESCROLL 
*           indicates to scroll a page at a time.
*********************************************************/
UINT GetNumScrollLines(void)
{
   HWND hdlMsWheel;
   UINT ucNumLines=3;  // 3 is the default
   OSVERSIONINFO osversion;
   UINT uiMsh_MsgScrollLines;
   

   memset(&osversion, 0, sizeof(osversion));
   osversion.dwOSVersionInfoSize =sizeof(osversion);
   GetVersionEx(&osversion);

   if ((osversion.dwPlatformId == VER_PLATFORM_WIN32_WINDOWS) ||
       ( (osversion.dwPlatformId == VER_PLATFORM_WIN32_NT) && 
         (osversion.dwMajorVersion < 4) )   )
   {
        hdlMsWheel = FindWindow(MSH_WHEELMODULE_CLASS, 
                                MSH_WHEELMODULE_TITLE);
        if (hdlMsWheel)
        {
           uiMsh_MsgScrollLines = RegisterWindowMessage
                                     (MSH_SCROLL_LINES);
           if (uiMsh_MsgScrollLines)
                ucNumLines = (int)SendMessage(hdlMsWheel,
                                    uiMsh_MsgScrollLines, 
                                                       0, 
                                                       0);
        }
   }
   else if ( (osversion.dwPlatformId ==
                         VER_PLATFORM_WIN32_NT) &&
             (osversion.dwMajorVersion >= 4) )
   {
      SystemParametersInfo(SPI_GETWHEELSCROLLLINES,
                                          0,
                                    &ucNumLines, 0);
   }
   return(ucNumLines);
}
```



 

 