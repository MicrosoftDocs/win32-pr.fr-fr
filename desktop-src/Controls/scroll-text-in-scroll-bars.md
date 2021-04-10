---
title: Comment faire défiler le texte
description: Cette section décrit les modifications que vous pouvez apporter à la procédure de fenêtre principale d’une application pour permettre à un utilisateur de faire défiler le texte.
ms.assetid: ACB4FF34-38EF-4F3D-9395-D48D58A72C0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ef9a2eea9490beac7b6ff5048b70de61eb635f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842746"
---
# <a name="how-to-scroll-text"></a><span data-ttu-id="7e492-103">Comment faire défiler le texte</span><span class="sxs-lookup"><span data-stu-id="7e492-103">How to Scroll Text</span></span>

<span data-ttu-id="7e492-104">Cette section décrit les modifications que vous pouvez apporter à la procédure de fenêtre principale d’une application pour permettre à un utilisateur de faire défiler le texte.</span><span class="sxs-lookup"><span data-stu-id="7e492-104">This section describes the changes you can make to an application's main window procedure to enable a user to scroll text.</span></span> <span data-ttu-id="7e492-105">L’exemple de cette section crée et affiche un tableau de chaînes de texte, puis traite les messages de la barre de défilement [**WM \_ HSCROLL**](wm-hscroll.md) et [**WM \_ VSCROLL**](wm-vscroll.md) pour permettre à l’utilisateur de faire défiler le texte à la fois verticalement et horizontalement.</span><span class="sxs-lookup"><span data-stu-id="7e492-105">The example in this section creates and displays an array of text strings, and processes [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md) scroll bar messages so that the user can scroll text both vertically and horizontally.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="7e492-106">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="7e492-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7e492-107">Technologies</span><span class="sxs-lookup"><span data-stu-id="7e492-107">Technologies</span></span>

-   [<span data-ttu-id="7e492-108">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="7e492-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="7e492-109">Prérequis</span><span class="sxs-lookup"><span data-stu-id="7e492-109">Prerequisites</span></span>

-   <span data-ttu-id="7e492-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="7e492-110">C/C++</span></span>
-   <span data-ttu-id="7e492-111">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="7e492-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="7e492-112">Instructions</span><span class="sxs-lookup"><span data-stu-id="7e492-112">Instructions</span></span>

### <a name="processing-the-wm_create-message"></a><span data-ttu-id="7e492-113">Traitement du \_ message WM Create</span><span class="sxs-lookup"><span data-stu-id="7e492-113">Processing the WM\_CREATE Message</span></span>

<span data-ttu-id="7e492-114">Les unités de défilement sont généralement définies lors du traitement du message [**WM \_ Create**](/windows/desktop/winmsg/wm-create) .</span><span class="sxs-lookup"><span data-stu-id="7e492-114">Scrolling units are typically set while processing the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message.</span></span> <span data-ttu-id="7e492-115">Il est pratique de baser les unités de défilement sur les dimensions de la police associée au contexte de périphérique (DC) de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7e492-115">It is convenient to base the scrolling units on the dimensions of the font associated with the window's device context (DC).</span></span> <span data-ttu-id="7e492-116">Pour récupérer les dimensions de police d’un DC spécifique, utilisez la fonction [**GetTextMetrics**](/windows/desktop/api/wingdi/nf-wingdi-gettextmetrics) .</span><span class="sxs-lookup"><span data-stu-id="7e492-116">To retrieve the font dimensions for a specific DC, use the [**GetTextMetrics**](/windows/desktop/api/wingdi/nf-wingdi-gettextmetrics) function.</span></span>

<span data-ttu-id="7e492-117">Dans l’exemple de cette section, une unité de défilement vertical est équivalente à la hauteur d’une cellule de caractère, plus la valeur de début externe.</span><span class="sxs-lookup"><span data-stu-id="7e492-117">In the example in this section, one vertical scrolling unit is equivalent to the height of a character cell, plus external leading.</span></span> <span data-ttu-id="7e492-118">Une unité de défilement horizontal est équivalente à la largeur moyenne d’une cellule de caractère.</span><span class="sxs-lookup"><span data-stu-id="7e492-118">One horizontal scrolling unit is equivalent to the average width of a character cell.</span></span> <span data-ttu-id="7e492-119">Les positions de défilement horizontal, par conséquent, ne correspondent pas aux caractères réels, à moins que la police d’écran ne soit à largeur fixe.</span><span class="sxs-lookup"><span data-stu-id="7e492-119">The horizontal scrolling positions, therefore, do not correspond to actual characters, unless the screen font is fixed-width.</span></span>

### <a name="processing-the-wm_size-message"></a><span data-ttu-id="7e492-120">Traitement du \_ message de taille WM</span><span class="sxs-lookup"><span data-stu-id="7e492-120">Processing the WM\_SIZE Message</span></span>

<span data-ttu-id="7e492-121">Lors du traitement du message de [**\_ taille WM**](/windows/desktop/winmsg/wm-size) , il est commode d’ajuster la plage de défilement et la position de défilement pour refléter les dimensions de la zone cliente ainsi que le nombre de lignes de texte qui seront affichées.</span><span class="sxs-lookup"><span data-stu-id="7e492-121">When processing the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message, it is convenient to adjust the scrolling range and scrolling position to reflect the dimensions of the client area as well as the number of lines of text that will be displayed.</span></span>

<span data-ttu-id="7e492-122">La fonction [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) définit les valeurs de position minimale et maximale, la taille de la page et la position de défilement pour une barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="7e492-122">The [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) function sets the minimum and maximum position values, the page size, and the scrolling position for a scroll bar.</span></span>

### <a name="processing-the-wm_hscroll-and-wm_vscroll-messages"></a><span data-ttu-id="7e492-123">Traitement des \_ messages WM HSCROLL et WM \_ VSCROLL</span><span class="sxs-lookup"><span data-stu-id="7e492-123">Processing the WM\_HSCROLL and WM\_VSCROLL Messages</span></span>

<span data-ttu-id="7e492-124">La barre de défilement envoie les messages [**WM \_ HSCROLL**](wm-hscroll.md) et [**WM \_ VSCROLL**](wm-vscroll.md) à la procédure de fenêtre chaque fois que l’utilisateur clique sur la barre de défilement ou fait glisser la case de défilement.</span><span class="sxs-lookup"><span data-stu-id="7e492-124">The scroll bar sends [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md) messages to the window procedure whenever the user clicks the scroll bar or drags the scroll box.</span></span> <span data-ttu-id="7e492-125">Les mots de poids faible de **WM \_ VSCROLL** et **WM \_ HSCROLL** contiennent chacun un code de demande qui indique la direction et l’amplitude de l’action de défilement.</span><span class="sxs-lookup"><span data-stu-id="7e492-125">The low-order words of **WM\_VSCROLL** and **WM\_HSCROLL** each contain a request code that indicates the direction and magnitude of the scrolling action.</span></span>

<span data-ttu-id="7e492-126">Lorsque les messages [**WM \_ HSCROLL**](wm-hscroll.md) et [**WM \_ VSCROLL**](wm-vscroll.md) sont traités, le code de demande de la barre de défilement est examiné et l’incrément de défilement est calculé.</span><span class="sxs-lookup"><span data-stu-id="7e492-126">When the [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md) messages are processed, the scroll bar request code is examined and the scrolling increment is calculated.</span></span> <span data-ttu-id="7e492-127">Une fois l’incrément appliqué à la position de défilement actuelle, la fenêtre défile vers la nouvelle position à l’aide de la fonction [**ScrollWindowEx**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) , et la position de la case de défilement est ajustée à l’aide de la fonction [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="7e492-127">After the increment is applied to the current scrolling position, the window is scrolled to the new position by using the [**ScrollWindowEx**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) function, and the position of the scroll box is adjusted by using the [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) function.</span></span>

<span data-ttu-id="7e492-128">Une fois qu’une fenêtre a été défilée, une partie de sa zone cliente est rendue non valide.</span><span class="sxs-lookup"><span data-stu-id="7e492-128">After a window is scrolled, part of its client area is made invalid.</span></span> <span data-ttu-id="7e492-129">Pour vous assurer que la région non valide est mise à jour, la fonction [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) est utilisée pour générer un message [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="7e492-129">To ensure that the invalid region is updated, the [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) function is used to generate a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span>

### <a name="processing-the-wm_paint-message"></a><span data-ttu-id="7e492-130">Traitement du \_ message de peinture WM</span><span class="sxs-lookup"><span data-stu-id="7e492-130">Processing the WM\_PAINT Message</span></span>

<span data-ttu-id="7e492-131">Lors du traitement du message de [**\_ peinture WM**](/windows/desktop/gdi/wm-paint) , il est pratique de dessiner les lignes de texte que vous souhaitez voir apparaître dans la partie non valide de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7e492-131">When processing the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message, it is convenient to draw the lines of text that you want to appear in the invalid portion of the window.</span></span> <span data-ttu-id="7e492-132">L’exemple suivant utilise la position de défilement actuelle et les dimensions de la région non valide pour déterminer la plage de lignes dans la région non valide pour les afficher.</span><span class="sxs-lookup"><span data-stu-id="7e492-132">The following example uses the current scrolling position and the dimensions of the invalid region to determine the range of lines within the invalid region in order to display them.</span></span>

## <a name="example-of-scrolling-text"></a><span data-ttu-id="7e492-133">Exemple de texte défilant</span><span class="sxs-lookup"><span data-stu-id="7e492-133">Example of Scrolling Text</span></span>

<span data-ttu-id="7e492-134">L’exemple suivant est une procédure de fenêtre pour une fenêtre qui affiche du texte dans sa zone cliente.</span><span class="sxs-lookup"><span data-stu-id="7e492-134">The following example is a window procedure for a window that displays text in its client area.</span></span> <span data-ttu-id="7e492-135">L’exemple montre comment faire défiler le texte en réponse à l’entrée des barres de défilement horizontale et verticale.</span><span class="sxs-lookup"><span data-stu-id="7e492-135">The example demonstrates how to scroll the text in response to input from the horizontal and vertical scroll bars.</span></span>


```C++
#include "strsafe.h"

LRESULT CALLBACK MyTextWindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
HDC hdc; 
PAINTSTRUCT ps; 
TEXTMETRIC tm; 
SCROLLINFO si; 
 
// These variables are required to display text. 
static int xClient;     // width of client area 
static int yClient;     // height of client area 
static int xClientMax;  // maximum width of client area 
 
static int xChar;       // horizontal scrolling unit 
static int yChar;       // vertical scrolling unit 
static int xUpper;      // average width of uppercase letters 
 
static int xPos;        // current horizontal scrolling position 
static int yPos;        // current vertical scrolling position 
 
int i;                  // loop counter 
int x, y;               // horizontal and vertical coordinates
 
int FirstLine;          // first line in the invalidated area 
int LastLine;           // last line in the invalidated area 
HRESULT hr;
size_t abcLength;        // length of an abc[] item 

// Create an array of lines to display. 
#define LINES 28 
static TCHAR *abc[] = { 
       TEXT("anteater"),  TEXT("bear"),      TEXT("cougar"), 
       TEXT("dingo"),     TEXT("elephant"),  TEXT("falcon"), 
       TEXT("gazelle"),   TEXT("hyena"),     TEXT("iguana"), 
       TEXT("jackal"),    TEXT("kangaroo"),  TEXT("llama"), 
       TEXT("moose"),     TEXT("newt"),      TEXT("octopus"), 
       TEXT("penguin"),   TEXT("quail"),     TEXT("rat"), 
       TEXT("squid"),     TEXT("tortoise"),  TEXT("urus"), 
       TEXT("vole"),      TEXT("walrus"),    TEXT("xylophone"), 
       TEXT("yak"),       TEXT("zebra"),
       TEXT("This line contains words, but no character. Go figure."),
       TEXT("")
     }; 
 
switch (uMsg) 
{ 
    case WM_CREATE : 
        // Get the handle to the client area's device context. 
        hdc = GetDC (hwnd); 
 
        // Extract font dimensions from the text metrics. 
        GetTextMetrics (hdc, &tm); 
        xChar = tm.tmAveCharWidth; 
        xUpper = (tm.tmPitchAndFamily & 1 ? 3 : 2) * xChar/2; 
        yChar = tm.tmHeight + tm.tmExternalLeading; 
 
        // Free the device context. 
        ReleaseDC (hwnd, hdc); 
 
        // Set an arbitrary maximum width for client area. 
        // (xClientMax is the sum of the widths of 48 average 
        // lowercase letters and 12 uppercase letters.) 
        xClientMax = 48 * xChar + 12 * xUpper; 
 
        return 0; 
 
    case WM_SIZE: 
 
        // Retrieve the dimensions of the client area. 
        yClient = HIWORD (lParam); 
        xClient = LOWORD (lParam); 
 
        // Set the vertical scrolling range and page size
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = LINES - 1; 
        si.nPage  = yClient / yChar; 
        SetScrollInfo(hwnd, SB_VERT, &si, TRUE); 
 
        // Set the horizontal scrolling range and page size. 
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = 2 + xClientMax / xChar; 
        si.nPage  = xClient / xChar; 
        SetScrollInfo(hwnd, SB_HORZ, &si, TRUE); 
 
        return 0; 
    case WM_HSCROLL:
        // Get all the vertial scroll bar information.
        si.cbSize = sizeof (si);
        si.fMask  = SIF_ALL;

        // Save the position for comparison later on.
        GetScrollInfo (hwnd, SB_HORZ, &si);
        xPos = si.nPos;
        switch (LOWORD (wParam))
        {
        // User clicked the left arrow.
        case SB_LINELEFT: 
            si.nPos -= 1;
            break;
              
        // User clicked the right arrow.
        case SB_LINERIGHT: 
            si.nPos += 1;
            break;
              
        // User clicked the scroll bar shaft left of the scroll box.
        case SB_PAGELEFT:
            si.nPos -= si.nPage;
            break;
              
        // User clicked the scroll bar shaft right of the scroll box.
        case SB_PAGERIGHT:
            si.nPos += si.nPage;
            break;
              
        // User dragged the scroll box.
        case SB_THUMBTRACK: 
            si.nPos = si.nTrackPos;
            break;
              
        default :
            break;
        }

        // Set the position and then retrieve it.  Due to adjustments
        // by Windows it may not be the same as the value set.
        si.fMask = SIF_POS;
        SetScrollInfo (hwnd, SB_HORZ, &si, TRUE);
        GetScrollInfo (hwnd, SB_HORZ, &si);
         
        // If the position has changed, scroll the window.
        if (si.nPos != xPos)
        {
            ScrollWindow(hwnd, xChar * (xPos - si.nPos), 0, NULL, NULL);
        }

        return 0;
         
    case WM_VSCROLL:
        // Get all the vertial scroll bar information.
        si.cbSize = sizeof (si);
        si.fMask  = SIF_ALL;
        GetScrollInfo (hwnd, SB_VERT, &si);

        // Save the position for comparison later on.
        yPos = si.nPos;
        switch (LOWORD (wParam))
        {

        // User clicked the HOME keyboard key.
        case SB_TOP:
            si.nPos = si.nMin;
            break;
              
        // User clicked the END keyboard key.
        case SB_BOTTOM:
            si.nPos = si.nMax;
            break;
              
        // User clicked the top arrow.
        case SB_LINEUP:
            si.nPos -= 1;
            break;
              
        // User clicked the bottom arrow.
        case SB_LINEDOWN:
            si.nPos += 1;
            break;
              
        // User clicked the scroll bar shaft above the scroll box.
        case SB_PAGEUP:
            si.nPos -= si.nPage;
            break;
              
        // User clicked the scroll bar shaft below the scroll box.
        case SB_PAGEDOWN:
            si.nPos += si.nPage;
            break;
              
        // User dragged the scroll box.
        case SB_THUMBTRACK:
            si.nPos = si.nTrackPos;
            break;
              
        default:
            break; 
        }

        // Set the position and then retrieve it.  Due to adjustments
        // by Windows it may not be the same as the value set.
        si.fMask = SIF_POS;
        SetScrollInfo (hwnd, SB_VERT, &si, TRUE);
        GetScrollInfo (hwnd, SB_VERT, &si);

        // If the position has changed, scroll window and update it.
        if (si.nPos != yPos)
        {                    
            ScrollWindow(hwnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
            UpdateWindow (hwnd);
        }

        return 0;
         
    case WM_PAINT :
        // Prepare the window for painting.
        hdc = BeginPaint (hwnd, &ps);

        // Get vertical scroll bar position.
        si.cbSize = sizeof (si);
        si.fMask  = SIF_POS;
        GetScrollInfo (hwnd, SB_VERT, &si);
        yPos = si.nPos;

        // Get horizontal scroll bar position.
        GetScrollInfo (hwnd, SB_HORZ, &si);
        xPos = si.nPos;

        // Find painting limits.
        FirstLine = max (0, yPos + ps.rcPaint.top / yChar);
        LastLine = min (LINES - 1, yPos + ps.rcPaint.bottom / yChar);
         
        for (i = FirstLine; i <= LastLine; i++)
        {
            x = xChar * (1 - xPos);
            y = yChar * (i - yPos);
              
            // Note that "55" in the following depends on the 
            // maximum size of an abc[] item. Also, you must include
            // strsafe.h to use the StringCchLength function.
            hr = StringCchLength(abc[i], 55, &abcLength);
            if ((FAILED(hr))|(abcLength == NULL))
            {
                //
                // TODO: write error handler
                //
            }

            // Write a line of text to the client area.
            TextOut(hdc, x, y, abc[i], abcLength); 
        }

        // Indicate that painting is finished.
        EndPaint (hwnd, &ps);
        return 0;
         
    case WM_DESTROY :
        PostQuitMessage (0);
        return 0;
    }

    return DefWindowProc (hwnd, uMsg, wParam, lParam);
}
```



## <a name="related-topics"></a><span data-ttu-id="7e492-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7e492-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e492-137">Utilisation des barres de défilement</span><span class="sxs-lookup"><span data-stu-id="7e492-137">Using Scroll Bars</span></span>](using-scroll-bars.md)
</dt> <dt>

<span data-ttu-id="7e492-138">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="7e492-138">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 