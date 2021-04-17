---
description: Vous pouvez utiliser un pinceau pour peindre l’intérieur de pratiquement n’importe quelle forme à l’aide d’une fonction GDI (Graphics Device Interface).
ms.assetid: 64cd6e82-7a0d-4b5e-b491-450f37eea43a
title: Utilisation de pinceaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b65ad4b14ba445642f224b0002eb1e7517c1008b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528821"
---
# <a name="using-brushes"></a><span data-ttu-id="a83b7-103">Utilisation de pinceaux</span><span class="sxs-lookup"><span data-stu-id="a83b7-103">Using Brushes</span></span>

<span data-ttu-id="a83b7-104">Vous pouvez utiliser un pinceau pour peindre l’intérieur de pratiquement n’importe quelle forme à l’aide d’une fonction GDI (Graphics Device Interface).</span><span class="sxs-lookup"><span data-stu-id="a83b7-104">You can use a brush to paint the interior of virtually any shape by using a graphics device interface (GDI) function.</span></span> <span data-ttu-id="a83b7-105">Cela comprend l’intérieur des rectangles, des ellipses, des polygones et des tracés.</span><span class="sxs-lookup"><span data-stu-id="a83b7-105">This includes the interiors of rectangles, ellipses, polygons, and paths.</span></span> <span data-ttu-id="a83b7-106">Selon les exigences de votre application, vous pouvez utiliser un pinceau plein d’une couleur spécifiée, un pinceau boursier, un pinceau hachuré ou un pinceau de motif.</span><span class="sxs-lookup"><span data-stu-id="a83b7-106">Depending on the requirements of your application, you can use a solid brush of a specified color, a stock brush, a hatch brush, or a pattern brush.</span></span>

<span data-ttu-id="a83b7-107">Cette section contient des exemples de code qui illustrent la création d’une boîte de dialogue de pinceau personnalisée.</span><span class="sxs-lookup"><span data-stu-id="a83b7-107">This section contains code samples that demonstrate the creation of a custom brush dialog box.</span></span> <span data-ttu-id="a83b7-108">La boîte de dialogue contient une grille qui représente l’image bitmap que le système utilise comme pinceau.</span><span class="sxs-lookup"><span data-stu-id="a83b7-108">The dialog box contains a grid that represents the bitmap the system uses as a brush.</span></span> <span data-ttu-id="a83b7-109">Un utilisateur peut utiliser cette grille pour créer une bitmap de pinceau de motif, puis afficher le modèle personnalisé en cliquant sur le bouton **modèle de test** .</span><span class="sxs-lookup"><span data-stu-id="a83b7-109">A user can use this grid to create a pattern-brush bitmap and then view the custom pattern by clicking the **Test Pattern** button.</span></span>

<span data-ttu-id="a83b7-110">L’illustration suivante montre un modèle créé à l’aide de la boîte de dialogue **pinceau personnalisé** .</span><span class="sxs-lookup"><span data-stu-id="a83b7-110">The following illustration shows a pattern created by using the **Custom Brush** dialog box.</span></span>

![capture d’écran de la boîte de dialogue pinceau personnalisé](images/custbrush.png)

<span data-ttu-id="a83b7-112">Pour afficher une boîte de dialogue, vous devez d’abord créer un modèle de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="a83b7-112">To display a dialog box, you must first create a dialog box template.</span></span> <span data-ttu-id="a83b7-113">Le modèle de boîte de dialogue suivant définit la boîte de dialogue **pinceau personnalisé** .</span><span class="sxs-lookup"><span data-stu-id="a83b7-113">The following dialog box template defines the **Custom Brush** dialog box.</span></span>


```C++
CustBrush DIALOG 6, 18, 160, 118 
STYLE WS_DLGFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION 
CAPTION "Custom Brush" 
FONT 8, "MS Sans Serif" 
BEGIN 
    CONTROL         "", IDD_GRID, "Static", SS_BLACKFRAME | 
                    WS_CHILD, 3, 2, 83, 79 
    CONTROL         "", IDD_RECT, "Static", SS_BLACKFRAME | 
                    WS_CHILD, 96, 11, 57, 28 
    PUSHBUTTON      "Test Pattern", IDD_PAINTRECT, 96, 47, 57, 14 
    PUSHBUTTON      "OK", IDD_OK, 29, 98, 40, 14 
    PUSHBUTTON      "Cancel", IDD_CANCEL, 92, 98, 40, 14 
END 
```



<span data-ttu-id="a83b7-114">La boîte de dialogue **pinceau personnalisé** contient cinq contrôles : une fenêtre de grille de bitmap, une fenêtre d’affichage de modèles et trois boutons de commande, étiquetés **modèle de test**, **OK** et **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="a83b7-114">The **Custom Brush** dialog box contains five controls: a bitmap-grid window, a pattern-viewing window, and three push buttons, labeled **Test Pattern**, **OK**, and **Cancel**.</span></span> <span data-ttu-id="a83b7-115">Le bouton de commande Push du **modèle de test** permet à l’utilisateur d’afficher le modèle.</span><span class="sxs-lookup"><span data-stu-id="a83b7-115">The **Test Pattern** push button enables the user to view the pattern.</span></span> <span data-ttu-id="a83b7-116">Le modèle de boîte de dialogue spécifie les dimensions globales de la fenêtre de boîte de dialogue, assigne une valeur à chaque contrôle, spécifie l’emplacement de chaque contrôle, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="a83b7-116">The dialog box template specifies the overall dimensions of the dialog box window, assigns a value to each control, specifies the location of each control, and so forth.</span></span> <span data-ttu-id="a83b7-117">Pour plus d’informations, consultez [boîtes de dialogue](../dlgbox/dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="a83b7-117">For more information, see [Dialog Boxes](../dlgbox/dialog-boxes.md).</span></span>

<span data-ttu-id="a83b7-118">Les valeurs de contrôle dans le modèle de boîte de dialogue sont des constantes définies comme suit dans le fichier d’en-tête de l’application.</span><span class="sxs-lookup"><span data-stu-id="a83b7-118">The control values in the dialog box template are constants that have been defined as follows in the application's header file.</span></span>


```C++
#define IDD_GRID      120 
#define IDD_RECT      121 
#define IDD_PAINTRECT 122 
#define IDD_OK        123 
#define IDD_CANCEL    124 
```



<span data-ttu-id="a83b7-119">Après avoir créé un modèle de boîte de dialogue et l’avoir inclus dans le fichier de définition de ressources de l’application, vous devez écrire une procédure de dialogue.</span><span class="sxs-lookup"><span data-stu-id="a83b7-119">After you create a dialog box template and include it in the application's resource-definition file, you must write a dialog procedure.</span></span> <span data-ttu-id="a83b7-120">Cette procédure traite les messages que le système envoie à la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="a83b7-120">This procedure processes messages that the system sends to the dialog box.</span></span> <span data-ttu-id="a83b7-121">L’extrait suivant du code source d’une application montre la procédure de boîte de dialogue de la boîte de dialogue **pinceau personnalisée** et les deux fonctions définies par l’application qu’elle appelle.</span><span class="sxs-lookup"><span data-stu-id="a83b7-121">The following excerpt from an application's source code shows the dialog box procedure for the **Custom Brush** dialog box and the two application-defined functions it calls.</span></span>


```C++
BOOL CALLBACK BrushDlgProc( HWND hdlg, UINT message, LONG wParam, 
                            LONG lParam) 
{ 
    static HWND hwndGrid;       // grid-window control  
    static HWND hwndBrush;      // pattern-brush control  
    static RECT rctGrid;        // grid-window rectangle  
    static RECT rctBrush;       // pattern-brush rectangle  
    static UINT bBrushBits[8];  // bitmap bits  
    static RECT rect[64];       // grid-cell array  
    static HBITMAP hbm;         // bitmap handle  
    HBRUSH hbrush;              // current brush  
    HBRUSH hbrushOld;           // default brush  
    HRGN hrgnCell;              // test-region handle  
    HDC hdc;                    // device context (DC) handle  
    int x, y, deltaX, deltaY;   // drawing coordinates  
    POINTS ptlHit;              // mouse coordinates  
    int i;                      // count variable  
 
    switch (message) 
        { 
        case WM_INITDIALOG: 
 
            // Retrieve a window handle for the grid-window and  
            // pattern-brush controls.  
 
            hwndGrid = GetDlgItem(hdlg, IDD_GRID); 
            hwndBrush = GetDlgItem(hdlg, IDD_RECT); 
 
            // Initialize the array of bits that defines the  
            // custom brush pattern with the value 1 to produce a  
            // solid white brush.  

            for (i=0; i<8; i++) 
                bBrushBits[i] = 0xFF; 
 
            // Retrieve dimensions for the grid-window and pattern- 
            // brush controls.  
 
            GetClientRect(hwndGrid, &rctGrid); 
            GetClientRect(hwndBrush, &rctBrush); 
 
            // Determine the width and height of a single cell.  
 
            deltaX = (rctGrid.right - rctGrid.left)/8; 
            deltaY = (rctGrid.bottom - rctGrid.top)/8; 
 
            // Initialize the array of cell rectangles.  
 
            for (y=rctGrid.top, i=0; y < rctGrid.bottom; y += deltaY)
            { 
                for(x=rctGrid.left; x < (rctGrid.right - 8) && i < 64; 
                        x += deltaX, i++) 
                { 
                    rect[i].left = x; rect[i].top = y; 
                    rect[i].right = x + deltaX; 
                    rect[i].bottom = y + deltaY; 
                } 
            } 
            return FALSE; 
 
 
        case WM_PAINT: 

            // Draw the grid.  
 
            hdc = GetDC(hwndGrid); 
 
            for (i=rctGrid.left; i<rctGrid.right; 
                 i+=(rctGrid.right - rctGrid.left)/8)
            { 
                 MoveToEx(hdc, i, rctGrid.top, NULL); 
                 LineTo(hdc, i, rctGrid.bottom); 
            } 
            for (i=rctGrid.top; i<rctGrid.bottom; 
                 i+=(rctGrid.bottom - rctGrid.top)/8)
            { 
                 MoveToEx(hdc, rctGrid.left, i, NULL); 
                 LineTo(hdc, rctGrid.right, i); 
            } 
            ReleaseDC(hwndGrid, hdc); 
            return FALSE; 
 
 
        case WM_LBUTTONDOWN: 
 
            // Store the mouse coordinates in a POINT structure.  
 
            ptlHit = MAKEPOINTS((POINTS FAR *)lParam); 
 
            // Create a rectangular region with dimensions and  
            // coordinates that correspond to those of the grid  
            // window.  
 
            hrgnCell = CreateRectRgn(rctGrid.left, rctGrid.top, 
                        rctGrid.right, rctGrid.bottom); 
 
            // Retrieve a window DC for the grid window.  
 
            hdc = GetDC(hwndGrid); 
 
            // Select the region into the DC.  
 
            SelectObject(hdc, hrgnCell); 
 
            // Test for a button click in the grid-window rectangle.  
 
            if (PtInRegion(hrgnCell, ptlHit.x, ptlHit.y))
            { 
                // A button click occurred in the grid-window  
                // rectangle; isolate the cell in which it occurred.  
 
                for(i=0; i<64; i++)
                { 
                    DeleteObject(hrgnCell); 
 
                    hrgnCell = CreateRectRgn(rect[i].left,  
                               rect[i].top, 
                               rect[i].right, rect[i].bottom); 
 
                    if (PtInRegion(hrgnCell, ptlHit.x, ptlHit.y))
                    { 
                        InvertRgn(hdc, hrgnCell); 
 
                        // Set the appropriate brush bits.  
 
                         if (i % 8 == 0) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x80; 
                         else if (i % 8 == 1) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x40; 
                         else if (i % 8 == 2) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x20; 
                         else if (i % 8 == 3) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x10; 
                         else if (i % 8 == 4) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x08; 
                         else if (i % 8 == 5) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x04; 
                         else if (i % 8 == 6) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x02; 
                         else if (i % 8 == 7) 
                            bBrushBits[i/8] = bBrushBits[i/8] ^ 0x01; 
 
                      // Exit the "for" loop after the bit is set.  
 
                         break; 
                    } // end if  
 
                } // end for  
 
            } // end if  
 
            // Release the DC for the control.  
 
            ReleaseDC(hwndGrid, hdc); 
            return TRUE; 
 
 
        case WM_COMMAND: 
            switch (wParam)
            { 
               case IDD_PAINTRECT: 
 
                    hdc = GetDC(hwndBrush); 
 
                    // Create a monochrome bitmap.  
 
                    hbm = CreateBitmap(8, 8, 1, 1, 
                          (LPBYTE)bBrushBits); 
 
                    // Select the custom brush into the DC.  
 
                    hbrush = CreatePatternBrush(hbm); 
 
                    hbrushOld = SelectObject(hdc, hbrush); 
 
                    // Use the custom brush to fill the rectangle.  
 
                    Rectangle(hdc, rctBrush.left, rctBrush.top, 
                              rctBrush.right, rctBrush.bottom); 
 
                    // Clean up memory.  
                    SelectObject(hdc, hbrushOld); 
                    DeleteObject(hbrush); 
                    DeleteObject(hbm); 
 
                    ReleaseDC(hwndBrush, hdc); 
                    return TRUE; 
 
                case IDD_OK: 
 
                case IDD_CANCEL: 
                    EndDialog(hdlg, TRUE); 
                    return TRUE; 
 
            } // end switch  
            break; 
        default: 
            return FALSE; 
        } 
} 
 
 
int GetStrLngth(LPTSTR cArray) 
{ 
    int i = 0; 
 
    while (cArray[i++] != 0); 
    return i-1; 
 
} 
 
DWORD RetrieveWidth(LPTSTR cArray, int iLength) 
{ 
    int i, iTmp; 
    double dVal, dCount; 
 
    dVal = 0.0; 
    dCount = (double)(iLength-1); 
    for (i=0; i<iLength; i++)
    { 
        iTmp = cArray[i] - 0x30; 
        dVal = dVal + (((double)iTmp) * pow(10.0, dCount--)); 
    } 
 
    return (DWORD)dVal; 
} 
```



<span data-ttu-id="a83b7-122">La procédure de boîte de dialogue de la boîte de dialogue **pinceau personnalisé** traite quatre messages, comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a83b7-122">The dialog box procedure for the **Custom Brush** dialog box processes four messages, as described in the following table.</span></span>



| <span data-ttu-id="a83b7-123">Message</span><span class="sxs-lookup"><span data-stu-id="a83b7-123">Message</span></span>                                          | <span data-ttu-id="a83b7-124">Action</span><span class="sxs-lookup"><span data-stu-id="a83b7-124">Action</span></span>                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a83b7-125">**\_INITDIALOG WM**</span><span class="sxs-lookup"><span data-stu-id="a83b7-125">**WM\_INITDIALOG**</span></span>](../dlgbox/wm-initdialog.md)   | <span data-ttu-id="a83b7-126">Récupère un handle de fenêtre et des dimensions pour les contrôles Grid-Window et Pattern-Brush, calcule les dimensions d’une cellule unique dans le contrôle Grid-Window et initialise un tableau de coordonnées de cellule de grille.</span><span class="sxs-lookup"><span data-stu-id="a83b7-126">Retrieves a window handle and dimensions for the grid-window and pattern-brush controls, computes the dimensions of a single cell in the grid-window control, and initializes an array of grid-cell coordinates.</span></span>                                                                                           |
| [<span data-ttu-id="a83b7-127">**\_peinture WM**</span><span class="sxs-lookup"><span data-stu-id="a83b7-127">**WM\_PAINT**</span></span>](wm-paint.md)                    | <span data-ttu-id="a83b7-128">Dessine le modèle de grille dans le contrôle Grid-Window.</span><span class="sxs-lookup"><span data-stu-id="a83b7-128">Draws the grid pattern in the grid-window control.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="a83b7-129">**\_LBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="a83b7-129">**WM\_LBUTTONDOWN**</span></span>](../inputdev/wm-lbuttondown.md) | <span data-ttu-id="a83b7-130">Détermine si le curseur se trouve dans le contrôle de fenêtre de grille lorsque l’utilisateur appuie sur le bouton gauche de la souris.</span><span class="sxs-lookup"><span data-stu-id="a83b7-130">Determines whether the cursor is within the grid-window control when the user presses the left mouse button.</span></span> <span data-ttu-id="a83b7-131">Si c’est le cas, la procédure de la boîte de dialogue inverse la cellule de grille appropriée et enregistre l’état de cette cellule dans un tableau de bits utilisé pour créer l’image bitmap du pinceau personnalisé.</span><span class="sxs-lookup"><span data-stu-id="a83b7-131">If so, the dialog box procedure inverts the appropriate grid cell and records the state of that cell in an array of bits that is used to create the bitmap for the custom brush.</span></span>              |
| [<span data-ttu-id="a83b7-132">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="a83b7-132">**WM\_COMMAND**</span></span>](../menurc/wm-command.md)         | <span data-ttu-id="a83b7-133">Traite l’entrée pour les trois contrôles de bouton de commande.</span><span class="sxs-lookup"><span data-stu-id="a83b7-133">Processes input for the three push button controls.</span></span> <span data-ttu-id="a83b7-134">Si l’utilisateur clique sur le bouton **modèle de test** , la procédure de boîte de dialogue peint le contrôle de modèle de test avec le nouveau modèle de pinceau personnalisé.</span><span class="sxs-lookup"><span data-stu-id="a83b7-134">If the user clicks the **Test Pattern** button, the dialog box procedure paints the Test Pattern control with the new custom brush pattern.</span></span> <span data-ttu-id="a83b7-135">Si l’utilisateur clique sur le bouton **OK** ou **Annuler** , la procédure de la boîte de dialogue effectue des actions en conséquence.</span><span class="sxs-lookup"><span data-stu-id="a83b7-135">If the user clicks the **OK** or **Cancel** button, the dialog box procedure performs actions accordingly.</span></span> |



 

<span data-ttu-id="a83b7-136">Pour plus d’informations sur les messages et le traitement des messages, consultez [messages et files d’attente](../winmsg/messages-and-message-queues.md)de messages.</span><span class="sxs-lookup"><span data-stu-id="a83b7-136">For more information about messages and message processing, see [Messages and Message Queues](../winmsg/messages-and-message-queues.md).</span></span>

<span data-ttu-id="a83b7-137">Après avoir écrit la procédure de boîte de dialogue, incluez la définition de fonction pour la procédure dans le fichier d’en-tête de l’application, puis appelez la procédure de la boîte de dialogue au point approprié dans l’application.</span><span class="sxs-lookup"><span data-stu-id="a83b7-137">After you write the dialog box procedure, include the function definition for the procedure in the application's header file and then call the dialog box procedure at the appropriate point in the application.</span></span>

<span data-ttu-id="a83b7-138">L’extrait suivant du fichier d’en-tête de l’application montre la définition de fonction pour la procédure de boîte de dialogue et les deux fonctions qu’elle appelle.</span><span class="sxs-lookup"><span data-stu-id="a83b7-138">The following excerpt from the application's header file shows the function definition for the dialog box procedure and the two functions it calls.</span></span>


```C++
BOOL CALLBACK BrushDlgProc(HWND, UINT, WPARAM, LPARAM); 
int GetStrLngth(LPTSTR); 
DWORD RetrieveWidth(LPTSTR, int); 
```



<span data-ttu-id="a83b7-139">Enfin, le code suivant montre comment la procédure de boîte de dialogue est appelée à partir du fichier de code source de l’application.</span><span class="sxs-lookup"><span data-stu-id="a83b7-139">Finally, the following code shows how the dialog box procedure is called from the application's source-code file.</span></span>


```C++
    DialogBox((HANDLE)GetModuleHandle(NULL), 
        (LPTSTR)"CustBrush", 
        hWnd, 
        (DLGPROC) BrushDlgProc); 
```



<span data-ttu-id="a83b7-140">Cet appel est généralement effectué en réponse à l’utilisateur en choisissant une option dans le menu de l’application.</span><span class="sxs-lookup"><span data-stu-id="a83b7-140">This call is usually made in response to the user choosing an option from the application's menu.</span></span>

 

 
