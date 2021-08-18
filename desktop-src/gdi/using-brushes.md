---
description: Vous pouvez utiliser un pinceau pour peindre l’intérieur de pratiquement n’importe quelle forme à l’aide d’une fonction GDI (Graphics Device Interface).
ms.assetid: 64cd6e82-7a0d-4b5e-b491-450f37eea43a
title: Utilisation de pinceaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42e09dc5731ceba7961dfd66b296df531897f2915cff53ccdacf1b5b5740160
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037497"
---
# <a name="using-brushes"></a>Utilisation de pinceaux

Vous pouvez utiliser un pinceau pour peindre l’intérieur de pratiquement n’importe quelle forme à l’aide d’une fonction GDI (Graphics Device Interface). Cela comprend l’intérieur des rectangles, des ellipses, des polygones et des tracés. Selon les exigences de votre application, vous pouvez utiliser un pinceau plein d’une couleur spécifiée, un pinceau boursier, un pinceau hachuré ou un pinceau de motif.

Cette section contient des exemples de code qui illustrent la création d’une boîte de dialogue de pinceau personnalisée. La boîte de dialogue contient une grille qui représente l’image bitmap que le système utilise comme pinceau. Un utilisateur peut utiliser cette grille pour créer une bitmap de pinceau de motif, puis afficher le modèle personnalisé en cliquant sur le bouton **modèle de test** .

L’illustration suivante montre un modèle créé à l’aide de la boîte de dialogue **pinceau personnalisé** .

![capture d’écran de la boîte de dialogue pinceau personnalisé](images/custbrush.png)

Pour afficher une boîte de dialogue, vous devez d’abord créer un modèle de boîte de dialogue. Le modèle de boîte de dialogue suivant définit la boîte de dialogue **pinceau personnalisé** .


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



La boîte de dialogue **pinceau personnalisé** contient cinq contrôles : une fenêtre de grille de bitmap, une fenêtre d’affichage de modèles et trois boutons de commande, étiquetés **modèle de test**, **OK** et **Annuler**. Le bouton de commande Push du **modèle de test** permet à l’utilisateur d’afficher le modèle. Le modèle de boîte de dialogue spécifie les dimensions globales de la fenêtre de boîte de dialogue, assigne une valeur à chaque contrôle, spécifie l’emplacement de chaque contrôle, et ainsi de suite. Pour plus d’informations, consultez [boîtes de dialogue](../dlgbox/dialog-boxes.md).

Les valeurs de contrôle dans le modèle de boîte de dialogue sont des constantes définies comme suit dans le fichier d’en-tête de l’application.


```C++
#define IDD_GRID      120 
#define IDD_RECT      121 
#define IDD_PAINTRECT 122 
#define IDD_OK        123 
#define IDD_CANCEL    124 
```



Après avoir créé un modèle de boîte de dialogue et l’avoir inclus dans le fichier de définition de ressources de l’application, vous devez écrire une procédure de dialogue. Cette procédure traite les messages que le système envoie à la boîte de dialogue. L’extrait suivant du code source d’une application montre la procédure de boîte de dialogue de la boîte de dialogue **pinceau personnalisée** et les deux fonctions définies par l’application qu’elle appelle.


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



La procédure de boîte de dialogue de la boîte de dialogue **pinceau personnalisé** traite quatre messages, comme décrit dans le tableau suivant.



| Message                                          | Action                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_INITDIALOG WM**](../dlgbox/wm-initdialog.md)   | Récupère un handle de fenêtre et des dimensions pour les contrôles Grid-Window et Pattern-Brush, calcule les dimensions d’une cellule unique dans le contrôle Grid-Window et initialise un tableau de coordonnées de cellule de grille.                                                                                           |
| [**\_peinture WM**](wm-paint.md)                    | Dessine le modèle de grille dans le contrôle Grid-Window.                                                                                                                                                                                                                                                         |
| [**\_LBUTTONDOWN WM**](../inputdev/wm-lbuttondown.md) | Détermine si le curseur se trouve dans le contrôle de fenêtre de grille lorsque l’utilisateur appuie sur le bouton gauche de la souris. Si c’est le cas, la procédure de la boîte de dialogue inverse la cellule de grille appropriée et enregistre l’état de cette cellule dans un tableau de bits utilisé pour créer l’image bitmap du pinceau personnalisé.              |
| [**WM, \_ commande**](../menurc/wm-command.md)         | Traite l’entrée pour les trois contrôles de bouton de commande. Si l’utilisateur clique sur le bouton **modèle de test** , la procédure de boîte de dialogue peint le contrôle de modèle de test avec le nouveau modèle de pinceau personnalisé. Si l’utilisateur clique sur le bouton **OK** ou **Annuler** , la procédure de la boîte de dialogue effectue des actions en conséquence. |



 

Pour plus d’informations sur les messages et le traitement des messages, consultez [messages et files d’attente](../winmsg/messages-and-message-queues.md)de messages.

Après avoir écrit la procédure de boîte de dialogue, incluez la définition de fonction pour la procédure dans le fichier d’en-tête de l’application, puis appelez la procédure de la boîte de dialogue au point approprié dans l’application.

L’extrait suivant du fichier d’en-tête de l’application montre la définition de fonction pour la procédure de boîte de dialogue et les deux fonctions qu’elle appelle.


```C++
BOOL CALLBACK BrushDlgProc(HWND, UINT, WPARAM, LPARAM); 
int GetStrLngth(LPTSTR); 
DWORD RetrieveWidth(LPTSTR, int); 
```



Enfin, le code suivant montre comment la procédure de boîte de dialogue est appelée à partir du fichier de code source de l’application.


```C++
    DialogBox((HANDLE)GetModuleHandle(NULL), 
        (LPTSTR)"CustBrush", 
        hWnd, 
        (DLGPROC) BrushDlgProc); 
```



Cet appel est généralement effectué en réponse à l’utilisateur en choisissant une option dans le menu de l’application.

 

 
