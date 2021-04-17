---
title: Utilisation du presse-papiers
description: 'Cette section contient des exemples de code pour les tâches suivantes :'
ms.assetid: 377fb2cc-5b46-481a-8222-9291e504ae2c
keywords:
- presse-papiers, découper des données
- presse-papiers, copier des données
- presse-papiers, coller des données
- presse-papiers, sélectionner des données
- presse-papiers, commandes du menu Edition
- presse-papiers, visionneuses
- presse-papiers, fenêtres de visionneuse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d7c7e7d6db6f25bc1016eefbcc5afc9f5e0db44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315461"
---
# <a name="using-the-clipboard"></a>Utilisation du presse-papiers

Cette section contient des exemples de code pour les tâches suivantes :

-   [Implémentation des commandes Couper, copier et coller](#implementing-the-cut-copy-and-paste-commands)
    -   [Sélection de données](#selecting-data)
    -   [Création d’un menu Edition](#creating-an-edit-menu)
    -   [Traitement du \_ message WM INITMENUPOPUP](#processing-the-wm_initmenupopup-message)
    -   [Traitement du \_ message de commande WM](#processing-the-wm_command-message)
    -   [Copie d’informations dans le presse-papiers](#copying-information-to-the-clipboard)
    -   [Collage d’informations à partir du presse-papiers](#pasting-information-from-the-clipboard)
    -   [Inscription d’un format de presse-papiers](#registering-a-clipboard-format)
    -   [Traitement des \_ messages WM RENDERFORMAT et WM \_ RENDERALLFORMATS](#processing-the-wm_renderformat-and-wm_renderallformats-messages)
    -   [Traitement du \_ message WM DESTROYCLIPBOARD](#processing-the-wm_destroyclipboard-message)
    -   [Utilisation du format de presse-papiers Owner-Display](#using-the-owner-display-clipboard-format)
-   [Surveiller le contenu du presse-papiers](#monitoring-clipboard-contents)
-   [Interrogation du numéro de séquence du presse-papiers](#querying-the-clipboard-sequence-number)
-   [Création d’un écouteur de format de presse-papiers](#creating-a-clipboard-format-listener)
-   [Création d’une fenêtre de la visionneuse du presse-papiers](#creating-a-clipboard-viewer-window)
-   [Ajout d’une fenêtre à la chaîne de la visionneuse du presse-papiers](#adding-a-window-to-the-clipboard-viewer-chain)
    -   [Traitement du \_ message WM CHANGECBCHAIN](#processing-the-wm_changecbchain-message)
    -   [Suppression d’une fenêtre de la chaîne de la visionneuse du presse-papiers](#removing-a-window-from-the-clipboard-viewer-chain)
    -   [Traitement du \_ message WM DRAWCLIPBOARD](#processing-the-wm_drawclipboard-message)
    -   [Exemple de visionneuse du presse-papiers](#example-of-a-clipboard-viewer)

## <a name="implementing-the-cut-copy-and-paste-commands"></a>Implémentation des commandes Couper, copier et coller

Cette section décrit comment les commandes **couper**, **copier** et **coller** standard sont implémentées dans une application. L’exemple de cette section utilise ces méthodes pour placer des données dans le presse-papiers à l’aide d’un format de presse-papiers enregistré, du format **CF \_ OWNERDISPLAY** et du format de **\_ texte CF** . Le format enregistré est utilisé pour représenter des fenêtres de texte rectangulaires ou elliptiques, appelées étiquettes.

### <a name="selecting-data"></a>Sélection de données

Pour que les informations puissent être copiées dans le presse-papiers, l’utilisateur doit sélectionner des informations spécifiques à copier ou couper. Une application doit fournir à l’utilisateur un moyen de sélectionner des informations dans un document et un certain type de retour visuel pour indiquer les données sélectionnées.

### <a name="creating-an-edit-menu"></a>Création d’un menu Edition

Une application doit charger une table d’accélérateurs contenant les accélérateurs de clavier standard pour les commandes du menu **Edition** . La fonction [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) doit être ajoutée à la boucle de messages de l’application pour que les accélérateurs prennent effet. Pour plus d’informations sur les accélérateurs de clavier, consultez [accélérateurs clavier](/windows/desktop/menurc/keyboard-accelerators).

### <a name="processing-the-wm_initmenupopup-message"></a>Traitement du \_ message WM INITMENUPOPUP

Toutes les commandes du presse-papiers ne sont pas accessibles à l’utilisateur à un moment donné. Une application doit traiter le message [**WM \_ INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) pour activer les éléments de menu des commandes disponibles et désactiver les commandes non disponibles.

Voici le cas [**WM \_ INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) pour une application nommée label.


```
case WM_INITMENUPOPUP:
    InitMenu((HMENU) wParam);
    break;
```



La fonction InitMenu est définie comme suit.


```
void WINAPI InitMenu(HMENU hmenu) 
{ 
    int  cMenuItems = GetMenuItemCount(hmenu); 
    int  nPos; 
    UINT id; 
    UINT fuFlags; 
    PLABELBOX pbox = (hwndSelected == NULL) ? NULL : 
        (PLABELBOX) GetWindowLong(hwndSelected, 0); 
 
    for (nPos = 0; nPos < cMenuItems; nPos++) 
    { 
        id = GetMenuItemID(hmenu, nPos); 
 
        switch (id) 
        { 
            case IDM_CUT: 
            case IDM_COPY: 
            case IDM_DELETE: 
                if (pbox == NULL || !pbox->fSelected) 
                    fuFlags = MF_BYCOMMAND | MF_GRAYED; 
                else if (pbox->fEdit) 
                    fuFlags = (id != IDM_DELETE && pbox->ichSel 
                            == pbox->ichCaret) ? 
                        MF_BYCOMMAND | MF_GRAYED : 
                        MF_BYCOMMAND | MF_ENABLED; 
                else 
                    fuFlags = MF_BYCOMMAND | MF_ENABLED; 
 
                EnableMenuItem(hmenu, id, fuFlags); 
                break; 
 
            case IDM_PASTE: 
                if (pbox != NULL && pbox->fEdit) 
                    EnableMenuItem(hmenu, id, 
                        IsClipboardFormatAvailable(CF_TEXT) ? 
                            MF_BYCOMMAND | MF_ENABLED : 
                            MF_BYCOMMAND | MF_GRAYED 
                    ); 
                else 
                    EnableMenuItem(hmenu, id, 
                        IsClipboardFormatAvailable( 
                                uLabelFormat) ? 
                            MF_BYCOMMAND | MF_ENABLED : 
                            MF_BYCOMMAND | MF_GRAYED 
                    ); 
 
        } 
    } 
}
```



### <a name="processing-the-wm_command-message"></a>Traitement du \_ message de commande WM

Pour traiter les commandes de menu, ajoutez le cas de [**\_ commande WM**](/windows/desktop/menurc/wm-command) à la procédure de fenêtre principale de votre application. Voici le cas **de \_ commande WM** pour la procédure de fenêtre de l’application label.


```
case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_CUT: 
            if (EditCopy()) 
                EditDelete(); 
            break; 
 
        case IDM_COPY: 
            EditCopy(); 
            break; 
 
        case IDM_PASTE: 
            EditPaste(); 
            break; 
 
        case IDM_DELETE: 
            EditDelete(); 
            break; 
 
        case IDM_EXIT: 
            DestroyWindow(hwnd); 
    } 
    break; 
```



Pour exécuter les commandes **Copy** et **Cut** , la procédure de fenêtre appelle la fonction EditCopy définie par l’application. Pour plus d’informations, consultez [copie d’informations dans le presse-papiers](#copying-information-to-the-clipboard). Pour exécuter la commande de **Collage** , la procédure de fenêtre appelle la fonction EditPaste définie par l’application. Pour plus d’informations sur la fonction EditPaste, consultez [collage d’informations à partir du presse-papiers](#pasting-information-from-the-clipboard).

### <a name="copying-information-to-the-clipboard"></a>Copie d’informations dans le presse-papiers

Dans l’application label, la fonction EditCopy définie par l’application copie la sélection actuelle dans le presse-papiers. Cette fonction effectue les opérations suivantes :

1.  Ouvre le presse-papiers en appelant la fonction [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) .
2.  Vide le presse-papiers en appelant la fonction [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) .
3.  Appelle la fonction [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) une fois pour chaque format de presse-papiers fourni par l’application.
4.  Ferme le presse-papiers en appelant la fonction [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) .

Selon la sélection actuelle, la fonction EditCopy copie une plage de texte ou copie une structure définie par l’application représentant une étiquette entière. La structure, appelée LABELBOX, est définie comme suit.


```
#define BOX_ELLIPSE  0 
#define BOX_RECT     1 
 
#define CCH_MAXLABEL 80 
#define CX_MARGIN    12 
 
typedef struct tagLABELBOX {  // box 
    RECT rcText;    // coordinates of rectangle containing text 
    BOOL fSelected; // TRUE if the label is selected 
    BOOL fEdit;     // TRUE if text is selected 
    int nType;      // rectangular or elliptical 
    int ichCaret;   // caret position 
    int ichSel;     // with ichCaret, delimits selection 
    int nXCaret;    // window position corresponding to ichCaret 
    int nXSel;      // window position corresponding to ichSel 
    int cchLabel;   // length of text in atchLabel 
    TCHAR atchLabel[CCH_MAXLABEL]; 
} LABELBOX, *PLABELBOX;
```



Voici la fonction EditCopy.


```
BOOL WINAPI EditCopy(VOID) 
{ 
    PLABELBOX pbox; 
    LPTSTR  lptstrCopy; 
    HGLOBAL hglbCopy; 
    int ich1, ich2, cch; 
 
    if (hwndSelected == NULL) 
        return FALSE; 
 
    // Open the clipboard, and empty it. 
 
    if (!OpenClipboard(hwndMain)) 
        return FALSE; 
    EmptyClipboard(); 
 
    // Get a pointer to the structure for the selected label. 
 
    pbox = (PLABELBOX) GetWindowLong(hwndSelected, 0); 
 
    // If text is selected, copy it using the CF_TEXT format. 
 
    if (pbox->fEdit) 
    { 
        if (pbox->ichSel == pbox->ichCaret)     // zero length
        {   
            CloseClipboard();                   // selection 
            return FALSE; 
        } 
 
        if (pbox->ichSel < pbox->ichCaret) 
        { 
            ich1 = pbox->ichSel; 
            ich2 = pbox->ichCaret; 
        } 
        else 
        { 
            ich1 = pbox->ichCaret; 
            ich2 = pbox->ichSel; 
        } 
        cch = ich2 - ich1; 
 
        // Allocate a global memory object for the text. 
 
        hglbCopy = GlobalAlloc(GMEM_MOVEABLE, 
            (cch + 1) * sizeof(TCHAR)); 
        if (hglbCopy == NULL) 
        { 
            CloseClipboard(); 
            return FALSE; 
        } 
 
        // Lock the handle and copy the text to the buffer. 
 
        lptstrCopy = GlobalLock(hglbCopy); 
        memcpy(lptstrCopy, &pbox->atchLabel[ich1], 
            cch * sizeof(TCHAR)); 
        lptstrCopy[cch] = (TCHAR) 0;    // null character 
        GlobalUnlock(hglbCopy); 
 
        // Place the handle on the clipboard. 
 
        SetClipboardData(CF_TEXT, hglbCopy); 
    } 
 
    // If no text is selected, the label as a whole is copied. 
 
    else 
    { 
        // Save a copy of the selected label as a local memory 
        // object. This copy is used to render data on request. 
        // It is freed in response to the WM_DESTROYCLIPBOARD 
        // message. 
 
        pboxLocalClip = (PLABELBOX) LocalAlloc( 
            LMEM_FIXED, 
            sizeof(LABELBOX) 
        ); 
        if (pboxLocalClip == NULL) 
        { 
            CloseClipboard(); 
            return FALSE; 
        } 
        memcpy(pboxLocalClip, pbox, sizeof(LABELBOX)); 
        pboxLocalClip->fSelected = FALSE; 
        pboxLocalClip->fEdit = FALSE; 
 
        // Place a registered clipboard format, the owner-display 
        // format, and the CF_TEXT format on the clipboard using 
        // delayed rendering. 
 
        SetClipboardData(uLabelFormat, NULL); 
        SetClipboardData(CF_OWNERDISPLAY, NULL); 
        SetClipboardData(CF_TEXT, NULL); 
    } 
 
    // Close the clipboard. 
 
    CloseClipboard(); 
 
    return TRUE; 
}
```



### <a name="pasting-information-from-the-clipboard"></a>Collage d’informations à partir du presse-papiers

Dans l’application label, la fonction EditPaste définie par l’application colle le contenu du presse-papiers. Cette fonction effectue les opérations suivantes :

1.  Ouvre le presse-papiers en appelant la fonction [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) .
2.  Détermine les formats de presse-papiers disponibles à récupérer.
3.  Récupère le handle des données dans le format sélectionné en appelant la fonction [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) .
4.  Insère une copie des données dans le document.

    Le handle retourné par [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) est toujours détenu par le presse-papiers, de sorte qu’une application ne doit pas la libérer ou la conserver verrouillée.

5.  Ferme le presse-papiers en appelant la fonction [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) .

Si une étiquette est sélectionnée et contient un point d’insertion, la fonction EditPaste insère le texte à partir du presse-papiers au point d’insertion. S’il n’y a aucune sélection ou si une étiquette est sélectionnée, la fonction crée une nouvelle étiquette à l’aide de la structure LABELBOX définie par l’application sur le presse-papiers. La structure LABELBOX est placée dans le presse-papiers à l’aide d’un format de presse-papiers inscrit.

La structure, appelée LABELBOX, est définie comme suit.


```
#define BOX_ELLIPSE  0 
#define BOX_RECT     1 
 
#define CCH_MAXLABEL 80 
#define CX_MARGIN    12 
 
typedef struct tagLABELBOX {  // box 
    RECT rcText;    // coordinates of rectangle containing text 
    BOOL fSelected; // TRUE if the label is selected 
    BOOL fEdit;     // TRUE if text is selected 
    int nType;      // rectangular or elliptical 
    int ichCaret;   // caret position 
    int ichSel;     // with ichCaret, delimits selection 
    int nXCaret;    // window position corresponding to ichCaret 
    int nXSel;      // window position corresponding to ichSel 
    int cchLabel;   // length of text in atchLabel 
    TCHAR atchLabel[CCH_MAXLABEL]; 
} LABELBOX, *PLABELBOX;
```



Voici la fonction EditPaste.


```
VOID WINAPI EditPaste(VOID) 
{ 
    PLABELBOX pbox; 
    HGLOBAL   hglb; 
    LPTSTR    lptstr; 
    PLABELBOX pboxCopy; 
    int cx, cy; 
    HWND hwnd; 
 
    pbox = hwndSelected == NULL ? NULL : 
        (PLABELBOX) GetWindowLong(hwndSelected, 0); 
 
    // If the application is in edit mode, 
    // get the clipboard text. 
 
    if (pbox != NULL && pbox->fEdit) 
    { 
        if (!IsClipboardFormatAvailable(CF_TEXT)) 
            return; 
        if (!OpenClipboard(hwndMain)) 
            return; 
 
        hglb = GetClipboardData(CF_TEXT); 
        if (hglb != NULL) 
        { 
            lptstr = GlobalLock(hglb); 
            if (lptstr != NULL) 
            { 
                // Call the application-defined ReplaceSelection 
                // function to insert the text and repaint the 
                // window. 
 
                ReplaceSelection(hwndSelected, pbox, lptstr); 
                GlobalUnlock(hglb); 
            } 
        } 
        CloseClipboard(); 
 
        return; 
    } 
 
    // If the application is not in edit mode, 
    // create a label window. 
 
    if (!IsClipboardFormatAvailable(uLabelFormat)) 
        return; 
    if (!OpenClipboard(hwndMain)) 
        return; 
 
    hglb = GetClipboardData(uLabelFormat); 
    if (hglb != NULL) 
    { 
        pboxCopy = GlobalLock(hglb); 
        if (pboxCopy != NULL) 
        { 
            cx = pboxCopy->rcText.right + CX_MARGIN; 
            cy = pboxCopy->rcText.top * 2 + cyText; 
 
            hwnd = CreateWindowEx( 
                WS_EX_NOPARENTNOTIFY | WS_EX_TRANSPARENT, 
                atchClassChild, NULL, WS_CHILD, 0, 0, cx, cy, 
                hwndMain, NULL, hinst, NULL 
            ); 
            if (hwnd != NULL) 
            { 
                pbox = (PLABELBOX) GetWindowLong(hwnd, 0); 
                memcpy(pbox, pboxCopy, sizeof(LABELBOX)); 
                ShowWindow(hwnd, SW_SHOWNORMAL); 
                SetFocus(hwnd); 
            } 
            GlobalUnlock(hglb); 
        } 
    } 
    CloseClipboard(); 
}
```



### <a name="registering-a-clipboard-format"></a>Inscription d’un format de presse-papiers

Pour inscrire un format de presse-papiers, ajoutez un appel à la fonction [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) à la fonction d’initialisation d’instance de votre application, comme suit.


```
// Register a clipboard format. 
 
// We assume that atchTemp can contain the format name and
// a null-terminator, otherwise it is truncated.
//
LoadString(hinstCurrent, IDS_FORMATNAME, atchTemp, 
    sizeof(atchTemp)/sizeof(TCHAR)); 
uLabelFormat = RegisterClipboardFormat(atchTemp); 
if (uLabelFormat == 0) 
    return FALSE;
```



### <a name="processing-the-wm_renderformat-and-wm_renderallformats-messages"></a>Traitement des \_ messages WM RENDERFORMAT et WM \_ RENDERALLFORMATS

Si une fenêtre passe un handle **null** à la fonction [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) , elle doit traiter les messages [**WM \_ RENDERFORMAT**](wm-renderformat.md) et [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) pour restituer les données à la demande.

Si une fenêtre retarde le rendu d’un format spécifique, puis qu’une autre application demande des données dans ce format, un message [**WM \_ RENDERFORMAT**](wm-renderformat.md) est envoyé à la fenêtre. En outre, si une fenêtre retarde le rendu d’un ou de plusieurs formats, et si certains de ces formats restent non rendus lorsque la fenêtre est sur le lieu d’être détruite, un message [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) est envoyé à la fenêtre avant sa destruction.

Pour afficher un format de presse-papiers, la procédure de fenêtre doit placer un handle de données non **null** dans le presse-papiers à l’aide de la fonction [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) . Si la procédure de fenêtre restitue un format en réponse au message [**WM \_ RENDERFORMAT**](wm-renderformat.md) , il ne doit pas ouvrir le presse-papiers avant d’appeler **SetClipboardData**. Mais s’il affiche un ou plusieurs formats en réponse au message [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) , il doit ouvrir le presse-papiers et vérifier que la fenêtre possède toujours le presse-papiers avant d’appeler **SetClipboardData**, et il doit fermer le presse-papiers avant de retourner.

L’application label traite les messages [**WM \_ RENDERFORMAT**](wm-renderformat.md) et [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) comme suit.


```
case WM_RENDERFORMAT: 
    RenderFormat((UINT) wParam); 
    break; 
 
case WM_RENDERALLFORMATS:
    if (OpenClipboard(hwnd))
    {
        if (GetClipboardOwner() == hwnd)
        {
            RenderFormat(uLabelFormat);
            RenderFormat(CF_TEXT);
        }
        CloseClipboard();
    }
    break;
```



Dans les deux cas, la procédure de fenêtre appelle la fonction RenderFormat définie par l’application, définie comme suit.

La structure, appelée LABELBOX, est définie comme suit.


```
#define BOX_ELLIPSE  0 
#define BOX_RECT     1 
 
#define CCH_MAXLABEL 80 
#define CX_MARGIN    12 
 
typedef struct tagLABELBOX {  // box 
    RECT rcText;    // coordinates of rectangle containing text 
    BOOL fSelected; // TRUE if the label is selected 
    BOOL fEdit;     // TRUE if text is selected 
    int nType;      // rectangular or elliptical 
    int ichCaret;   // caret position 
    int ichSel;     // with ichCaret, delimits selection 
    int nXCaret;    // window position corresponding to ichCaret 
    int nXSel;      // window position corresponding to ichSel 
    int cchLabel;   // length of text in atchLabel 
    TCHAR atchLabel[CCH_MAXLABEL]; 
} LABELBOX, *PLABELBOX;
```




```
void WINAPI RenderFormat(UINT uFormat) 
{ 
    HGLOBAL hglb; 
    PLABELBOX pbox; 
    LPTSTR  lptstr; 
    int cch; 
 
    if (pboxLocalClip == NULL) 
        return; 
 
    if (uFormat == CF_TEXT) 
    { 
        // Allocate a buffer for the text. 
 
        cch = pboxLocalClip->cchLabel; 
        hglb = GlobalAlloc(GMEM_MOVEABLE, 
            (cch + 1) * sizeof(TCHAR)); 
        if (hglb == NULL) 
            return; 
 
        // Copy the text from pboxLocalClip. 
 
        lptstr = GlobalLock(hglb); 
        memcpy(lptstr, pboxLocalClip->atchLabel, 
            cch * sizeof(TCHAR)); 
        lptstr[cch] = (TCHAR) 0; 
        GlobalUnlock(hglb); 
 
        // Place the handle on the clipboard. 
 
        SetClipboardData(CF_TEXT, hglb); 
    } 
    else if (uFormat == uLabelFormat) 
    { 
        hglb = GlobalAlloc(GMEM_MOVEABLE, sizeof(LABELBOX)); 
        if (hglb == NULL) 
            return; 
        pbox = GlobalLock(hglb); 
        memcpy(pbox, pboxLocalClip, sizeof(LABELBOX)); 
        GlobalUnlock(hglb); 
 
        SetClipboardData(uLabelFormat, hglb); 
    } 
}
```



### <a name="processing-the-wm_destroyclipboard-message"></a>Traitement du \_ message WM DESTROYCLIPBOARD

Une fenêtre peut traiter le message [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) afin de libérer toutes les ressources qu’il a réservées pour prendre en charge le rendu retardé. Par exemple, l’application de l’étiquette, lors de la copie d’une étiquette dans le presse-papiers, alloue un objet mémoire local. Il libère ensuite cet objet en réponse au message **WM \_ DESTROYCLIPBOARD** , comme suit.


```
case WM_DESTROYCLIPBOARD: 
    if (pboxLocalClip != NULL) 
    { 
        LocalFree(pboxLocalClip); 
        pboxLocalClip = NULL; 
    } 
    break;
```



### <a name="using-the-owner-display-clipboard-format"></a>Utilisation du format de presse-papiers Owner-Display

Si une fenêtre place des informations dans le presse-papiers en utilisant le format de presse-papiers **CF \_ OWNERDISPLAY** , elle doit effectuer les opérations suivantes :

-   Traitez le message [**WM \_ PAINTCLIPBOARD**](wm-paintclipboard.md) . Ce message est envoyé au propriétaire du presse-papiers lorsqu’une partie de la fenêtre de la visionneuse du presse-papiers doit être repeinte.

-   Traitez le message [**WM \_ SIZECLIPBOARD**](wm-sizeclipboard.md) . Ce message est envoyé au propriétaire du presse-papiers lorsque la fenêtre de la visionneuse du presse-papiers a été redimensionnée ou que son contenu a changé.

    En règle générale, une fenêtre répond à ce message en définissant les positions et les plages de défilement pour la fenêtre de la visionneuse du presse-papiers. En réponse à ce message, l’application étiquette met également à jour une structure de [**taille**](/previous-versions//dd145106(v=vs.85)) pour la fenêtre de la visionneuse du presse-papiers.

-   Traitez les messages [**WM \_ HSCROLLCLIPBOARD**](wm-hscrollclipboard.md) et [**WM \_ VSCROLLCLIPBOARD**](wm-vscrollclipboard.md) . Ces messages sont envoyés au propriétaire du presse-papiers lorsqu’un événement de barre de défilement se produit dans la fenêtre de la visionneuse du presse-papiers.

-   Traitez le message [**WM \_ ASKCBFORMATNAME**](wm-askcbformatname.md) . La fenêtre de la visionneuse du presse-papiers envoie ce message à une application pour récupérer le nom du format d’affichage propriétaire.

La procédure de fenêtre pour l’application de l’étiquette traite ces messages, comme suit.


```
LRESULT CALLBACK MainWindowProc(hwnd, msg, wParam, lParam) 
HWND hwnd; 
UINT msg; 
WPARAM wParam; 
LPARAM lParam; 
{ 
    static RECT rcViewer; 
 
    RECT rc; 
    LPRECT lprc; 
    LPPAINTSTRUCT lpps; 
 
    switch (msg) 
    { 
        //
        // Handle other messages.
        //
        case WM_PAINTCLIPBOARD: 
            // Determine the dimensions of the label. 
 
            SetRect(&rc, 0, 0, 
                pboxLocalClip->rcText.right + CX_MARGIN, 
                pboxLocalClip->rcText.top * 2 + cyText 
            ); 
 
            // Center the image in the clipboard viewer window. 
 
            if (rc.right < rcViewer.right) 
            { 
                rc.left = (rcViewer.right - rc.right) / 2; 
                rc.right += rc.left; 
            } 
            if (rc.bottom < rcViewer.bottom) 
            { 
                rc.top = (rcViewer.bottom - rc.bottom) / 2; 
                rc.bottom += rc.top; 
            } 
 
            // Paint the image, using the specified PAINTSTRUCT 
            // structure, by calling the application-defined 
            // PaintLabel function. 
 
            lpps = (LPPAINTSTRUCT) GlobalLock((HGLOBAL) lParam); 
            PaintLabel(lpps, pboxLocalClip, &rc); 
            GlobalUnlock((HGLOBAL) lParam); 
            break; 
 
        case WM_SIZECLIPBOARD: 
            // Save the dimensions of the window in a static 
            // RECT structure. 
 
            lprc = (LPRECT) GlobalLock((HGLOBAL) lParam); 
            memcpy(&rcViewer, lprc, sizeof(RECT)); 
            GlobalUnlock((HGLOBAL) lParam); 
 
            // Set the scroll ranges to zero (thus eliminating 
            // the need to process the WM_HSCROLLCLIPBOARD and 
            // WM_VSCROLLCLIPBOARD messages). 
 
            SetScrollRange((HWND) wParam, SB_HORZ, 0, 0, TRUE); 
            SetScrollRange((HWND) wParam, SB_VERT, 0, 0, TRUE); 
 
            break; 
 
        case WM_ASKCBFORMATNAME: 
            LoadString(hinst, IDS_OWNERDISPLAY, 
                (LPSTR) lParam, wParam); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, msg, wParam, lParam); 
    } 
    return 0; 
}
```



## <a name="monitoring-clipboard-contents"></a>Surveiller le contenu du presse-papiers

Il existe trois façons de surveiller les modifications apportées au Presse-papiers. La méthode la plus ancienne consiste à créer une fenêtre de la visionneuse du presse-papiers. Windows 2000 a ajouté la possibilité d’interroger le numéro de séquence du presse-papiers, et Windows Vista a ajouté la prise en charge des écouteurs de format du presse-papiers. La visionneuse du presse-papiers Windows est prise en charge pour la compatibilité descendante avec les versions antérieures de Windows. Les nouveaux programmes doivent utiliser les écouteurs de format du presse-papiers ou le numéro de séquence du presse-papiers.

## <a name="querying-the-clipboard-sequence-number"></a>Interrogation du numéro de séquence du presse-papiers

Chaque fois que le contenu du presse-papiers change, une valeur 32 bits connue comme le numéro de séquence du presse-papiers est incrémentée. Un programme peut récupérer le numéro de séquence du presse-papiers actuel en appelant la fonction [**GetClipboardSequenceNumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) . En comparant la valeur retournée par rapport à une valeur retournée par un appel précédent à **GetClipboardSequenceNumber**, un programme peut déterminer si le contenu du presse-papiers a changé. Cette méthode est plus adaptée aux programmes qui cachent les résultats en fonction du contenu actuel du presse-papiers et doivent savoir si les calculs sont toujours valides avant d’utiliser les résultats de ce cache. Notez qu’il ne s’agit pas d’une méthode de notification et qu’elle ne doit pas être utilisée dans une boucle d’interrogation. Pour être averti lorsque le contenu du presse-papiers change, utilisez un écouteur de format du presse-papiers ou une visionneuse du presse-papiers.

## <a name="creating-a-clipboard-format-listener"></a>Création d’un écouteur de format de presse-papiers

Un écouteur de format de presse-papiers est une fenêtre qui s’est inscrite pour être averti lorsque le contenu du presse-papiers a changé. Cette méthode est recommandée par rapport à la création d’une fenêtre du presse-papiers, car elle est plus simple à implémenter et évite les problèmes si les programmes ne parviennent pas à gérer correctement la chaîne du presse-papiers ou si une fenêtre de la chaîne de la visionneuse du presse-papiers ne répond plus aux messages.

Une fenêtre s’inscrit comme un écouteur de format de presse-papiers en appelant la fonction [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) . Lorsque le contenu du presse-papiers change, la fenêtre est publiée dans un message [**WM \_ CLIPBOARDUPDATE**](wm-clipboardupdate.md) . L’inscription reste valide jusqu’à ce que la fenêtre annule son inscription en appelant la fonction [**RemoveClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener) .

## <a name="creating-a-clipboard-viewer-window"></a>Création d’une fenêtre de la visionneuse du presse-papiers

Une fenêtre de la visionneuse du presse-papiers affiche le contenu actuel du presse-papiers et reçoit des messages lorsque le contenu du presse-papiers change. Pour créer une fenêtre de la visionneuse du presse-papiers, votre application doit effectuer les opérations suivantes :

-   Ajoutez la fenêtre à la chaîne de la visionneuse du presse-papiers.
-   Traitez le message [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) .
-   Traitez le message [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) .
-   Supprime la fenêtre de la chaîne de la visionneuse du presse-papiers avant sa destruction.

## <a name="adding-a-window-to-the-clipboard-viewer-chain"></a>Ajout d’une fenêtre à la chaîne de la visionneuse du presse-papiers

Une fenêtre s’ajoute à la chaîne de la visionneuse du presse-papiers en appelant la fonction [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) . La valeur de retour est le handle de la fenêtre suivante dans la chaîne. Une fenêtre doit assurer le suivi de cette valeur, par exemple, en l’enregistrant dans une variable statique nommée *hwndNextViewer*.

L’exemple suivant ajoute une fenêtre à la chaîne de la visionneuse du presse-papiers en réponse au message [**WM \_ Create**](/windows/desktop/winmsg/wm-create) .


```
case WM_CREATE: 
 
    // Add the window to the clipboard viewer chain. 
 
    hwndNextViewer = SetClipboardViewer(hwnd); 
    break;
```



Les extraits de code sont affichés pour les tâches suivantes :

-   [Traitement du \_ message WM CHANGECBCHAIN](/windows)
-   [Suppression d’une fenêtre de la chaîne de la visionneuse du presse-papiers](#removing-a-window-from-the-clipboard-viewer-chain)
-   [Traitement du \_ message WM DRAWCLIPBOARD](/windows)
-   [Exemple de visionneuse du presse-papiers](#example-of-a-clipboard-viewer)

### <a name="processing-the-wm_changecbchain-message"></a>Traitement du \_ message WM CHANGECBCHAIN

Une fenêtre de la visionneuse du presse-papiers reçoit le message [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) lorsqu’une autre fenêtre se supprime lui-même de la chaîne du presse-papiers. Si la fenêtre en cours de suppression est la fenêtre suivante dans la chaîne, la fenêtre recevant le message doit dissocier la fenêtre suivante de la chaîne. Dans le cas contraire, ce message doit être passé à la fenêtre suivante dans la chaîne.

L’exemple suivant illustre le traitement du message [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) .


```
case WM_CHANGECBCHAIN: 
 
    // If the next window is closing, repair the chain. 
 
    if ((HWND) wParam == hwndNextViewer) 
        hwndNextViewer = (HWND) lParam; 
 
    // Otherwise, pass the message to the next link. 
 
    else if (hwndNextViewer != NULL) 
        SendMessage(hwndNextViewer, uMsg, wParam, lParam); 
 
    break;
```



### <a name="removing-a-window-from-the-clipboard-viewer-chain"></a>Suppression d’une fenêtre de la chaîne de la visionneuse du presse-papiers

Pour se supprimer de la chaîne de la visionneuse du presse-papiers, une fenêtre appelle la fonction [**ChangeClipboardChain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) . L’exemple suivant supprime une fenêtre de la chaîne de la visionneuse du presse-papiers en réponse au message [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) .


```
case WM_DESTROY: 
    ChangeClipboardChain(hwnd, hwndNextViewer); 
    PostQuitMessage(0); 
    break;
```



### <a name="processing-the-wm_drawclipboard-message"></a>Traitement du \_ message WM DRAWCLIPBOARD

Le message [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) avertit une fenêtre de la visionneuse du presse-papiers que le contenu du presse-papiers a changé. Une fenêtre doit effectuer les opérations suivantes lors du traitement du message **WM \_ DRAWCLIPBOARD** :

1.  Déterminez les formats de presse-papiers disponibles à afficher.
2.  Récupérer les données du presse-papiers et les afficher dans la fenêtre. Ou, si le format du presse-papiers est **CF \_ OWNERDISPLAY**, envoyez un message [**WM \_ PAINTCLIPBOARD**](wm-paintclipboard.md) au propriétaire du presse-papiers.
3.  Envoyer le message à la fenêtre suivante dans la chaîne du presse-papiers.

Pour obtenir un exemple de traitement du message [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) , consultez l’exemple de la liste dans l’exemple [d’une visionneuse du presse-papiers](#example-of-a-clipboard-viewer).

### <a name="example-of-a-clipboard-viewer"></a>Exemple de visionneuse du presse-papiers

L’exemple suivant montre une application de visionneuse du presse-papiers simple.


```
HINSTANCE hinst; 
UINT uFormat = (UINT)(-1); 
BOOL fAuto = TRUE; 
 
LRESULT APIENTRY MainWndProc(hwnd, uMsg, wParam, lParam) 
HWND hwnd; 
UINT uMsg; 
WPARAM wParam; 
LPARAM lParam; 
{ 
    static HWND hwndNextViewer; 
 
    HDC hdc; 
    HDC hdcMem; 
    PAINTSTRUCT ps; 
    LPPAINTSTRUCT lpps; 
    RECT rc; 
    LPRECT lprc; 
    HGLOBAL hglb; 
    LPSTR lpstr; 
    HBITMAP hbm; 
    HENHMETAFILE hemf; 
    HWND hwndOwner; 
 
    switch (uMsg) 
    { 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
 
            // Branch depending on the clipboard format. 
 
            switch (uFormat) 
            { 
                case CF_OWNERDISPLAY: 
                    hwndOwner = GetClipboardOwner(); 
                    hglb = GlobalAlloc(GMEM_MOVEABLE, 
                        sizeof(PAINTSTRUCT)); 
                    lpps = GlobalLock(hglb);
                    memcpy(lpps, &ps, sizeof(PAINTSTRUCT)); 
                    GlobalUnlock(hglb); 
 
                    SendMessage(hwndOwner, WM_PAINTCLIPBOARD, 
                        (WPARAM) hwnd, (LPARAM) hglb); 
 
                    GlobalFree(hglb); 
                    break; 
 
                case CF_BITMAP: 
                    hdcMem = CreateCompatibleDC(hdc); 
                    if (hdcMem != NULL) 
                    { 
                        if (OpenClipboard(hwnd)) 
                        { 
                            hbm = (HBITMAP) 
                                GetClipboardData(uFormat); 
                            SelectObject(hdcMem, hbm); 
                            GetClientRect(hwnd, &rc); 
 
                            BitBlt(hdc, 0, 0, rc.right, rc.bottom, 
                                hdcMem, 0, 0, SRCCOPY); 
                            CloseClipboard(); 
                        } 
                        DeleteDC(hdcMem); 
                    } 
                    break; 
 
                case CF_TEXT: 
                    if (OpenClipboard(hwnd)) 
                    { 
                        hglb = GetClipboardData(uFormat); 
                        lpstr = GlobalLock(hglb); 
 
                        GetClientRect(hwnd, &rc); 
                        DrawText(hdc, lpstr, -1, &rc, DT_LEFT); 
 
                        GlobalUnlock(hglb); 
                        CloseClipboard(); 
                    } 
                    break; 
 
                case CF_ENHMETAFILE: 
                    if (OpenClipboard(hwnd)) 
                    { 
                        hemf = GetClipboardData(uFormat); 
                        GetClientRect(hwnd, &rc); 
                        PlayEnhMetaFile(hdc, hemf, &rc); 
                        CloseClipboard(); 
                    } 
                    break; 
 
                case 0: 
                    GetClientRect(hwnd, &rc); 
                    DrawText(hdc, "The clipboard is empty.", -1, 
                        &rc, DT_CENTER | DT_SINGLELINE | 
                        DT_VCENTER); 
                    break; 
 
                default: 
                    GetClientRect(hwnd, &rc); 
                    DrawText(hdc, "Unable to display format.", -1, 
                        &rc, DT_CENTER | DT_SINGLELINE | 
                        DT_VCENTER); 
            } 
            EndPaint(hwnd, &ps); 
            break; 
 
        case WM_SIZE: 
            if (uFormat == CF_OWNERDISPLAY) 
            { 
                hwndOwner = GetClipboardOwner(); 
                hglb = GlobalAlloc(GMEM_MOVEABLE, sizeof(RECT)); 
                lprc = GlobalLock(hglb); 
                GetClientRect(hwnd, lprc); 
                GlobalUnlock(hglb); 
 
                SendMessage(hwndOwner, WM_SIZECLIPBOARD, 
                    (WPARAM) hwnd, (LPARAM) hglb); 
 
                GlobalFree(hglb); 
            } 
            break; 
 
        case WM_CREATE: 
 
            // Add the window to the clipboard viewer chain. 
 
            hwndNextViewer = SetClipboardViewer(hwnd); 
            break; 
 
        case WM_CHANGECBCHAIN: 
 
            // If the next window is closing, repair the chain. 
 
            if ((HWND) wParam == hwndNextViewer) 
                hwndNextViewer = (HWND) lParam; 
 
            // Otherwise, pass the message to the next link. 
 
            else if (hwndNextViewer != NULL) 
                SendMessage(hwndNextViewer, uMsg, wParam, lParam); 
 
            break; 
 
        case WM_DESTROY: 
            ChangeClipboardChain(hwnd, hwndNextViewer); 
            PostQuitMessage(0); 
            break; 
 
        case WM_DRAWCLIPBOARD:  // clipboard contents changed. 
 
            // Update the window by using Auto clipboard format. 
 
            SetAutoView(hwnd); 
 
            // Pass the message to the next window in clipboard 
            // viewer chain. 
 
            SendMessage(hwndNextViewer, uMsg, wParam, lParam); 
            break; 
 
        case WM_INITMENUPOPUP: 
            if (!HIWORD(lParam)) 
                InitMenu(hwnd, (HMENU) wParam); 
            break; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDM_EXIT: 
                    DestroyWindow(hwnd); 
                    break; 
 
                case IDM_AUTO: 
                    SetAutoView(hwnd); 
                    break; 
 
                default: 
                    fAuto = FALSE; 
                    uFormat = LOWORD(wParam); 
                    InvalidateRect(hwnd, NULL, TRUE); 
            } 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return (LRESULT) NULL; 
} 
 
void WINAPI SetAutoView(HWND hwnd) 
{ 
    static UINT auPriorityList[] = { 
        CF_OWNERDISPLAY, 
        CF_TEXT, 
        CF_ENHMETAFILE, 
        CF_BITMAP 
    }; 
 
    uFormat = GetPriorityClipboardFormat(auPriorityList, 4); 
    fAuto = TRUE; 
 
    InvalidateRect(hwnd, NULL, TRUE); 
    UpdateWindow(hwnd); 
} 
 
void WINAPI InitMenu(HWND hwnd, HMENU hmenu) 
{ 
    UINT uFormat; 
    char szFormatName[80]; 
    LPCSTR lpFormatName; 
    UINT fuFlags; 
    UINT idMenuItem; 
 
    // If a menu is not the display menu, no initialization is necessary. 
 
    if (GetMenuItemID(hmenu, 0) != IDM_AUTO) 
        return; 
 
    // Delete all menu items except the first. 
 
    while (GetMenuItemCount(hmenu) > 1) 
        DeleteMenu(hmenu, 1, MF_BYPOSITION); 
 
    // Check or uncheck the Auto menu item. 
 
    fuFlags = fAuto ? MF_BYCOMMAND | MF_CHECKED : 
        MF_BYCOMMAND | MF_UNCHECKED; 
    CheckMenuItem(hmenu, IDM_AUTO, fuFlags); 
 
    // If there are no clipboard formats, return. 
 
    if (CountClipboardFormats() == 0) 
        return; 
 
    // Open the clipboard. 
 
    if (!OpenClipboard(hwnd)) 
        return; 
 
    // Add a separator and then a menu item for each format. 
 
    AppendMenu(hmenu, MF_SEPARATOR, 0, NULL); 
    uFormat = EnumClipboardFormats(0); 
 
    while (uFormat) 
    { 
        // Call an application-defined function to get the name 
        // of the clipboard format. 
 
        lpFormatName = GetPredefinedClipboardFormatName(uFormat); 
 
        // For registered formats, get the registered name. 
 
        if (lpFormatName == NULL) 
        {

        // Note that, if the format name is larger than the
        // buffer, it is truncated. 
            if (GetClipboardFormatName(uFormat, szFormatName, 
                    sizeof(szFormatName))) 
                lpFormatName = szFormatName; 
            else 
                lpFormatName = "(unknown)"; 
        } 
 
        // Add a menu item for the format. For displayable 
        // formats, use the format ID for the menu ID. 
 
        if (IsDisplayableFormat(uFormat)) 
        { 
            fuFlags = MF_STRING; 
            idMenuItem = uFormat; 
        } 
        else 
        { 
            fuFlags = MF_STRING | MF_GRAYED; 
            idMenuItem = 0; 
        } 
        AppendMenu(hmenu, fuFlags, idMenuItem, lpFormatName); 
 
        uFormat = EnumClipboardFormats(uFormat); 
    } 
    CloseClipboard(); 
 
} 
 
BOOL WINAPI IsDisplayableFormat(UINT uFormat) 
{ 
    switch (uFormat) 
    { 
        case CF_OWNERDISPLAY: 
        case CF_TEXT: 
        case CF_ENHMETAFILE: 
        case CF_BITMAP: 
            return TRUE; 
    } 
    return FALSE; 
} 
```



 

 