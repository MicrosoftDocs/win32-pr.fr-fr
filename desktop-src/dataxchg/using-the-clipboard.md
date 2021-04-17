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
# <a name="using-the-clipboard"></a><span data-ttu-id="a0f91-110">Utilisation du presse-papiers</span><span class="sxs-lookup"><span data-stu-id="a0f91-110">Using the Clipboard</span></span>

<span data-ttu-id="a0f91-111">Cette section contient des exemples de code pour les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="a0f91-111">This section has code samples for the following tasks:</span></span>

-   [<span data-ttu-id="a0f91-112">Implémentation des commandes Couper, copier et coller</span><span class="sxs-lookup"><span data-stu-id="a0f91-112">Implementing the Cut, Copy, and Paste Commands</span></span>](#implementing-the-cut-copy-and-paste-commands)
    -   [<span data-ttu-id="a0f91-113">Sélection de données</span><span class="sxs-lookup"><span data-stu-id="a0f91-113">Selecting Data</span></span>](#selecting-data)
    -   [<span data-ttu-id="a0f91-114">Création d’un menu Edition</span><span class="sxs-lookup"><span data-stu-id="a0f91-114">Creating an Edit Menu</span></span>](#creating-an-edit-menu)
    -   [<span data-ttu-id="a0f91-115">Traitement du \_ message WM INITMENUPOPUP</span><span class="sxs-lookup"><span data-stu-id="a0f91-115">Processing the WM\_INITMENUPOPUP Message</span></span>](#processing-the-wm_initmenupopup-message)
    -   [<span data-ttu-id="a0f91-116">Traitement du \_ message de commande WM</span><span class="sxs-lookup"><span data-stu-id="a0f91-116">Processing the WM\_COMMAND Message</span></span>](#processing-the-wm_command-message)
    -   [<span data-ttu-id="a0f91-117">Copie d’informations dans le presse-papiers</span><span class="sxs-lookup"><span data-stu-id="a0f91-117">Copying Information to the Clipboard</span></span>](#copying-information-to-the-clipboard)
    -   [<span data-ttu-id="a0f91-118">Collage d’informations à partir du presse-papiers</span><span class="sxs-lookup"><span data-stu-id="a0f91-118">Pasting Information from the Clipboard</span></span>](#pasting-information-from-the-clipboard)
    -   [<span data-ttu-id="a0f91-119">Inscription d’un format de presse-papiers</span><span class="sxs-lookup"><span data-stu-id="a0f91-119">Registering a Clipboard Format</span></span>](#registering-a-clipboard-format)
    -   [<span data-ttu-id="a0f91-120">Traitement des \_ messages WM RENDERFORMAT et WM \_ RENDERALLFORMATS</span><span class="sxs-lookup"><span data-stu-id="a0f91-120">Processing the WM\_RENDERFORMAT and WM\_RENDERALLFORMATS Messages</span></span>](#processing-the-wm_renderformat-and-wm_renderallformats-messages)
    -   [<span data-ttu-id="a0f91-121">Traitement du \_ message WM DESTROYCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="a0f91-121">Processing the WM\_DESTROYCLIPBOARD Message</span></span>](#processing-the-wm_destroyclipboard-message)
    -   [<span data-ttu-id="a0f91-122">Utilisation du format de presse-papiers Owner-Display</span><span class="sxs-lookup"><span data-stu-id="a0f91-122">Using the Owner-Display Clipboard Format</span></span>](#using-the-owner-display-clipboard-format)
-   [<span data-ttu-id="a0f91-123">Surveiller le contenu du presse-papiers</span><span class="sxs-lookup"><span data-stu-id="a0f91-123">Monitoring Clipboard Contents</span></span>](#monitoring-clipboard-contents)
-   [<span data-ttu-id="a0f91-124">Interrogation du numéro de séquence du presse-papiers</span><span class="sxs-lookup"><span data-stu-id="a0f91-124">Querying the Clipboard Sequence Number</span></span>](#querying-the-clipboard-sequence-number)
-   [<span data-ttu-id="a0f91-125">Création d’un écouteur de format de presse-papiers</span><span class="sxs-lookup"><span data-stu-id="a0f91-125">Creating a Clipboard Format Listener</span></span>](#creating-a-clipboard-format-listener)
-   [<span data-ttu-id="a0f91-126">Création d’une fenêtre de la visionneuse du presse-papiers</span><span class="sxs-lookup"><span data-stu-id="a0f91-126">Creating a Clipboard Viewer Window</span></span>](#creating-a-clipboard-viewer-window)
-   [<span data-ttu-id="a0f91-127">Ajout d’une fenêtre à la chaîne de la visionneuse du presse-papiers</span><span class="sxs-lookup"><span data-stu-id="a0f91-127">Adding a Window to the Clipboard Viewer Chain</span></span>](#adding-a-window-to-the-clipboard-viewer-chain)
    -   [<span data-ttu-id="a0f91-128">Traitement du \_ message WM CHANGECBCHAIN</span><span class="sxs-lookup"><span data-stu-id="a0f91-128">Processing the WM\_CHANGECBCHAIN Message</span></span>](#processing-the-wm_changecbchain-message)
    -   [<span data-ttu-id="a0f91-129">Suppression d’une fenêtre de la chaîne de la visionneuse du presse-papiers</span><span class="sxs-lookup"><span data-stu-id="a0f91-129">Removing a Window from the Clipboard Viewer Chain</span></span>](#removing-a-window-from-the-clipboard-viewer-chain)
    -   [<span data-ttu-id="a0f91-130">Traitement du \_ message WM DRAWCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="a0f91-130">Processing the WM\_DRAWCLIPBOARD Message</span></span>](#processing-the-wm_drawclipboard-message)
    -   [<span data-ttu-id="a0f91-131">Exemple de visionneuse du presse-papiers</span><span class="sxs-lookup"><span data-stu-id="a0f91-131">Example of a Clipboard Viewer</span></span>](#example-of-a-clipboard-viewer)

## <a name="implementing-the-cut-copy-and-paste-commands"></a><span data-ttu-id="a0f91-132">Implémentation des commandes Couper, copier et coller</span><span class="sxs-lookup"><span data-stu-id="a0f91-132">Implementing the Cut, Copy, and Paste Commands</span></span>

<span data-ttu-id="a0f91-133">Cette section décrit comment les commandes **couper**, **copier** et **coller** standard sont implémentées dans une application.</span><span class="sxs-lookup"><span data-stu-id="a0f91-133">This section describes how standard **Cut**, **Copy**, and **Paste** commands are implemented in an application.</span></span> <span data-ttu-id="a0f91-134">L’exemple de cette section utilise ces méthodes pour placer des données dans le presse-papiers à l’aide d’un format de presse-papiers enregistré, du format **CF \_ OWNERDISPLAY** et du format de **\_ texte CF** .</span><span class="sxs-lookup"><span data-stu-id="a0f91-134">The example in this section uses these methods to place data on the clipboard using a registered clipboard format, the **CF\_OWNERDISPLAY** format, and the **CF\_TEXT** format.</span></span> <span data-ttu-id="a0f91-135">Le format enregistré est utilisé pour représenter des fenêtres de texte rectangulaires ou elliptiques, appelées étiquettes.</span><span class="sxs-lookup"><span data-stu-id="a0f91-135">The registered format is used to represent rectangular or elliptical text windows, called labels.</span></span>

### <a name="selecting-data"></a><span data-ttu-id="a0f91-136">Sélection de données</span><span class="sxs-lookup"><span data-stu-id="a0f91-136">Selecting Data</span></span>

<span data-ttu-id="a0f91-137">Pour que les informations puissent être copiées dans le presse-papiers, l’utilisateur doit sélectionner des informations spécifiques à copier ou couper.</span><span class="sxs-lookup"><span data-stu-id="a0f91-137">Before information can be copied to the clipboard, the user must select specific information to be copied or cut.</span></span> <span data-ttu-id="a0f91-138">Une application doit fournir à l’utilisateur un moyen de sélectionner des informations dans un document et un certain type de retour visuel pour indiquer les données sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="a0f91-138">An application should provide a means for the user to select information within a document and some kind of visual feedback to indicate selected data.</span></span>

### <a name="creating-an-edit-menu"></a><span data-ttu-id="a0f91-139">Création d’un menu Edition</span><span class="sxs-lookup"><span data-stu-id="a0f91-139">Creating an Edit Menu</span></span>

<span data-ttu-id="a0f91-140">Une application doit charger une table d’accélérateurs contenant les accélérateurs de clavier standard pour les commandes du menu **Edition** .</span><span class="sxs-lookup"><span data-stu-id="a0f91-140">An application should load an accelerator table containing the standard keyboard accelerators for the **Edit** menu commands.</span></span> <span data-ttu-id="a0f91-141">La fonction [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) doit être ajoutée à la boucle de messages de l’application pour que les accélérateurs prennent effet.</span><span class="sxs-lookup"><span data-stu-id="a0f91-141">The [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function must be added to the application's message loop for the accelerators to take effect.</span></span> <span data-ttu-id="a0f91-142">Pour plus d’informations sur les accélérateurs de clavier, consultez [accélérateurs clavier](/windows/desktop/menurc/keyboard-accelerators).</span><span class="sxs-lookup"><span data-stu-id="a0f91-142">For more information about keyboard accelerators, see [Keyboard Accelerators](/windows/desktop/menurc/keyboard-accelerators).</span></span>

### <a name="processing-the-wm_initmenupopup-message"></a><span data-ttu-id="a0f91-143">Traitement du \_ message WM INITMENUPOPUP</span><span class="sxs-lookup"><span data-stu-id="a0f91-143">Processing the WM\_INITMENUPOPUP Message</span></span>

<span data-ttu-id="a0f91-144">Toutes les commandes du presse-papiers ne sont pas accessibles à l’utilisateur à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="a0f91-144">Not all clipboard commands are available to the user at any given time.</span></span> <span data-ttu-id="a0f91-145">Une application doit traiter le message [**WM \_ INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) pour activer les éléments de menu des commandes disponibles et désactiver les commandes non disponibles.</span><span class="sxs-lookup"><span data-stu-id="a0f91-145">An application should process the [**WM\_INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) message to enable the menu items for available commands and disable unavailable commands.</span></span>

<span data-ttu-id="a0f91-146">Voici le cas [**WM \_ INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) pour une application nommée label.</span><span class="sxs-lookup"><span data-stu-id="a0f91-146">Following is the [**WM\_INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) case for an application named Label.</span></span>


```
case WM_INITMENUPOPUP:
    InitMenu((HMENU) wParam);
    break;
```



<span data-ttu-id="a0f91-147">La fonction InitMenu est définie comme suit.</span><span class="sxs-lookup"><span data-stu-id="a0f91-147">The InitMenu function is defined as follows.</span></span>


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



### <a name="processing-the-wm_command-message"></a><span data-ttu-id="a0f91-148">Traitement du \_ message de commande WM</span><span class="sxs-lookup"><span data-stu-id="a0f91-148">Processing the WM\_COMMAND Message</span></span>

<span data-ttu-id="a0f91-149">Pour traiter les commandes de menu, ajoutez le cas de [**\_ commande WM**](/windows/desktop/menurc/wm-command) à la procédure de fenêtre principale de votre application.</span><span class="sxs-lookup"><span data-stu-id="a0f91-149">To process menu commands, add the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) case to your application's main window procedure.</span></span> <span data-ttu-id="a0f91-150">Voici le cas **de \_ commande WM** pour la procédure de fenêtre de l’application label.</span><span class="sxs-lookup"><span data-stu-id="a0f91-150">Following is the **WM\_COMMAND** case for the Label application's window procedure.</span></span>


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



<span data-ttu-id="a0f91-151">Pour exécuter les commandes **Copy** et **Cut** , la procédure de fenêtre appelle la fonction EditCopy définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="a0f91-151">To carry out the **Copy** and **Cut** commands, the window procedure calls the application-defined EditCopy function.</span></span> <span data-ttu-id="a0f91-152">Pour plus d’informations, consultez [copie d’informations dans le presse-papiers](#copying-information-to-the-clipboard).</span><span class="sxs-lookup"><span data-stu-id="a0f91-152">For more information, see [Copying Information to the Clipboard](#copying-information-to-the-clipboard).</span></span> <span data-ttu-id="a0f91-153">Pour exécuter la commande de **Collage** , la procédure de fenêtre appelle la fonction EditPaste définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="a0f91-153">To carry out the **Paste** command, the window procedure calls the application-defined EditPaste function.</span></span> <span data-ttu-id="a0f91-154">Pour plus d’informations sur la fonction EditPaste, consultez [collage d’informations à partir du presse-papiers](#pasting-information-from-the-clipboard).</span><span class="sxs-lookup"><span data-stu-id="a0f91-154">For more information about the EditPaste function, see [Pasting Information from the Clipboard](#pasting-information-from-the-clipboard).</span></span>

### <a name="copying-information-to-the-clipboard"></a><span data-ttu-id="a0f91-155">Copie d’informations dans le presse-papiers</span><span class="sxs-lookup"><span data-stu-id="a0f91-155">Copying Information to the Clipboard</span></span>

<span data-ttu-id="a0f91-156">Dans l’application label, la fonction EditCopy définie par l’application copie la sélection actuelle dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="a0f91-156">In the Label application, the application-defined EditCopy function copies the current selection to the clipboard.</span></span> <span data-ttu-id="a0f91-157">Cette fonction effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="a0f91-157">This function does the following:</span></span>

1.  <span data-ttu-id="a0f91-158">Ouvre le presse-papiers en appelant la fonction [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) .</span><span class="sxs-lookup"><span data-stu-id="a0f91-158">Opens the clipboard by calling the [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) function.</span></span>
2.  <span data-ttu-id="a0f91-159">Vide le presse-papiers en appelant la fonction [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) .</span><span class="sxs-lookup"><span data-stu-id="a0f91-159">Empties the clipboard by calling the [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) function.</span></span>
3.  <span data-ttu-id="a0f91-160">Appelle la fonction [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) une fois pour chaque format de presse-papiers fourni par l’application.</span><span class="sxs-lookup"><span data-stu-id="a0f91-160">Calls the [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) function once for each clipboard format the application provides.</span></span>
4.  <span data-ttu-id="a0f91-161">Ferme le presse-papiers en appelant la fonction [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) .</span><span class="sxs-lookup"><span data-stu-id="a0f91-161">Closes the clipboard by calling the [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) function.</span></span>

<span data-ttu-id="a0f91-162">Selon la sélection actuelle, la fonction EditCopy copie une plage de texte ou copie une structure définie par l’application représentant une étiquette entière.</span><span class="sxs-lookup"><span data-stu-id="a0f91-162">Depending on the current selection, the EditCopy function either copies a range of text or copies an application-defined structure representing an entire label.</span></span> <span data-ttu-id="a0f91-163">La structure, appelée LABELBOX, est définie comme suit.</span><span class="sxs-lookup"><span data-stu-id="a0f91-163">The structure, called LABELBOX, is defined as follows.</span></span>


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



<span data-ttu-id="a0f91-164">Voici la fonction EditCopy.</span><span class="sxs-lookup"><span data-stu-id="a0f91-164">Following is the EditCopy function.</span></span>


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



### <a name="pasting-information-from-the-clipboard"></a><span data-ttu-id="a0f91-165">Collage d’informations à partir du presse-papiers</span><span class="sxs-lookup"><span data-stu-id="a0f91-165">Pasting Information from the Clipboard</span></span>

<span data-ttu-id="a0f91-166">Dans l’application label, la fonction EditPaste définie par l’application colle le contenu du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="a0f91-166">In the Label application, the application-defined EditPaste function pastes the content of the clipboard.</span></span> <span data-ttu-id="a0f91-167">Cette fonction effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="a0f91-167">This function does the following:</span></span>

1.  <span data-ttu-id="a0f91-168">Ouvre le presse-papiers en appelant la fonction [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) .</span><span class="sxs-lookup"><span data-stu-id="a0f91-168">Opens the clipboard by calling the [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) function.</span></span>
2.  <span data-ttu-id="a0f91-169">Détermine les formats de presse-papiers disponibles à récupérer.</span><span class="sxs-lookup"><span data-stu-id="a0f91-169">Determines which of the available clipboard formats to retrieve.</span></span>
3.  <span data-ttu-id="a0f91-170">Récupère le handle des données dans le format sélectionné en appelant la fonction [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) .</span><span class="sxs-lookup"><span data-stu-id="a0f91-170">Retrieves the handle to the data in the selected format by calling the [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) function.</span></span>
4.  <span data-ttu-id="a0f91-171">Insère une copie des données dans le document.</span><span class="sxs-lookup"><span data-stu-id="a0f91-171">Inserts a copy of the data into the document.</span></span>

    <span data-ttu-id="a0f91-172">Le handle retourné par [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) est toujours détenu par le presse-papiers, de sorte qu’une application ne doit pas la libérer ou la conserver verrouillée.</span><span class="sxs-lookup"><span data-stu-id="a0f91-172">The handle returned by [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) is still owned by the clipboard, so an application must not free it or leave it locked.</span></span>

5.  <span data-ttu-id="a0f91-173">Ferme le presse-papiers en appelant la fonction [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) .</span><span class="sxs-lookup"><span data-stu-id="a0f91-173">Closes the clipboard by calling the [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) function.</span></span>

<span data-ttu-id="a0f91-174">Si une étiquette est sélectionnée et contient un point d’insertion, la fonction EditPaste insère le texte à partir du presse-papiers au point d’insertion.</span><span class="sxs-lookup"><span data-stu-id="a0f91-174">If a label is selected and contains an insertion point, the EditPaste function inserts the text from the clipboard at the insertion point.</span></span> <span data-ttu-id="a0f91-175">S’il n’y a aucune sélection ou si une étiquette est sélectionnée, la fonction crée une nouvelle étiquette à l’aide de la structure LABELBOX définie par l’application sur le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="a0f91-175">If there is no selection or if a label is selected, the function creates a new label, using the application-defined LABELBOX structure on the clipboard.</span></span> <span data-ttu-id="a0f91-176">La structure LABELBOX est placée dans le presse-papiers à l’aide d’un format de presse-papiers inscrit.</span><span class="sxs-lookup"><span data-stu-id="a0f91-176">The LABELBOX structure is placed on the clipboard by using a registered clipboard format.</span></span>

<span data-ttu-id="a0f91-177">La structure, appelée LABELBOX, est définie comme suit.</span><span class="sxs-lookup"><span data-stu-id="a0f91-177">The structure, called LABELBOX, is defined as follows.</span></span>


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



<span data-ttu-id="a0f91-178">Voici la fonction EditPaste.</span><span class="sxs-lookup"><span data-stu-id="a0f91-178">Following is the EditPaste function.</span></span>


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



### <a name="registering-a-clipboard-format"></a><span data-ttu-id="a0f91-179">Inscription d’un format de presse-papiers</span><span class="sxs-lookup"><span data-stu-id="a0f91-179">Registering a Clipboard Format</span></span>

<span data-ttu-id="a0f91-180">Pour inscrire un format de presse-papiers, ajoutez un appel à la fonction [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) à la fonction d’initialisation d’instance de votre application, comme suit.</span><span class="sxs-lookup"><span data-stu-id="a0f91-180">To register a clipboard format, add a call to the [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) function to your application's instance initialization function, as follows.</span></span>


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



### <a name="processing-the-wm_renderformat-and-wm_renderallformats-messages"></a><span data-ttu-id="a0f91-181">Traitement des \_ messages WM RENDERFORMAT et WM \_ RENDERALLFORMATS</span><span class="sxs-lookup"><span data-stu-id="a0f91-181">Processing the WM\_RENDERFORMAT and WM\_RENDERALLFORMATS Messages</span></span>

<span data-ttu-id="a0f91-182">Si une fenêtre passe un handle **null** à la fonction [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) , elle doit traiter les messages [**WM \_ RENDERFORMAT**](wm-renderformat.md) et [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) pour restituer les données à la demande.</span><span class="sxs-lookup"><span data-stu-id="a0f91-182">If a window passes a **NULL** handle to the [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) function, it must process the [**WM\_RENDERFORMAT**](wm-renderformat.md) and [**WM\_RENDERALLFORMATS**](wm-renderallformats.md) messages to render data upon request.</span></span>

<span data-ttu-id="a0f91-183">Si une fenêtre retarde le rendu d’un format spécifique, puis qu’une autre application demande des données dans ce format, un message [**WM \_ RENDERFORMAT**](wm-renderformat.md) est envoyé à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a0f91-183">If a window delays rendering a specific format and then another application requests data in that format, then a [**WM\_RENDERFORMAT**](wm-renderformat.md) message is sent to the window.</span></span> <span data-ttu-id="a0f91-184">En outre, si une fenêtre retarde le rendu d’un ou de plusieurs formats, et si certains de ces formats restent non rendus lorsque la fenêtre est sur le lieu d’être détruite, un message [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) est envoyé à la fenêtre avant sa destruction.</span><span class="sxs-lookup"><span data-stu-id="a0f91-184">In addition, if a window delays rendering one or more formats, and if some of those formats remain unrendered when the window is about to be destroyed, then a [**WM\_RENDERALLFORMATS**](wm-renderallformats.md) message is sent to the window before its destruction.</span></span>

<span data-ttu-id="a0f91-185">Pour afficher un format de presse-papiers, la procédure de fenêtre doit placer un handle de données non **null** dans le presse-papiers à l’aide de la fonction [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) .</span><span class="sxs-lookup"><span data-stu-id="a0f91-185">To render a clipboard format, the window procedure should place a non-**NULL** data handle on the clipboard using the [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) function.</span></span> <span data-ttu-id="a0f91-186">Si la procédure de fenêtre restitue un format en réponse au message [**WM \_ RENDERFORMAT**](wm-renderformat.md) , il ne doit pas ouvrir le presse-papiers avant d’appeler **SetClipboardData**.</span><span class="sxs-lookup"><span data-stu-id="a0f91-186">If the window procedure is rendering a format in response to the [**WM\_RENDERFORMAT**](wm-renderformat.md) message, it must not open the clipboard before calling **SetClipboardData**.</span></span> <span data-ttu-id="a0f91-187">Mais s’il affiche un ou plusieurs formats en réponse au message [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) , il doit ouvrir le presse-papiers et vérifier que la fenêtre possède toujours le presse-papiers avant d’appeler **SetClipboardData**, et il doit fermer le presse-papiers avant de retourner.</span><span class="sxs-lookup"><span data-stu-id="a0f91-187">But if it is rendering one or more formats in response to the [**WM\_RENDERALLFORMATS**](wm-renderallformats.md) message, it must open the clipboard and check that the window still owns the clipboard before calling **SetClipboardData**, and it must close the clipboard before returning.</span></span>

<span data-ttu-id="a0f91-188">L’application label traite les messages [**WM \_ RENDERFORMAT**](wm-renderformat.md) et [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) comme suit.</span><span class="sxs-lookup"><span data-stu-id="a0f91-188">The Label application processes the [**WM\_RENDERFORMAT**](wm-renderformat.md) and [**WM\_RENDERALLFORMATS**](wm-renderallformats.md) messages as follows.</span></span>


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



<span data-ttu-id="a0f91-189">Dans les deux cas, la procédure de fenêtre appelle la fonction RenderFormat définie par l’application, définie comme suit.</span><span class="sxs-lookup"><span data-stu-id="a0f91-189">In both cases, the window procedure calls the application-defined RenderFormat function, defined as follows.</span></span>

<span data-ttu-id="a0f91-190">La structure, appelée LABELBOX, est définie comme suit.</span><span class="sxs-lookup"><span data-stu-id="a0f91-190">The structure, called LABELBOX, is defined as follows.</span></span>


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



### <a name="processing-the-wm_destroyclipboard-message"></a><span data-ttu-id="a0f91-191">Traitement du \_ message WM DESTROYCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="a0f91-191">Processing the WM\_DESTROYCLIPBOARD Message</span></span>

<span data-ttu-id="a0f91-192">Une fenêtre peut traiter le message [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) afin de libérer toutes les ressources qu’il a réservées pour prendre en charge le rendu retardé.</span><span class="sxs-lookup"><span data-stu-id="a0f91-192">A window can process the [**WM\_DESTROYCLIPBOARD**](wm-destroyclipboard.md) message in order to free any resources that it set aside to support delayed rendering.</span></span> <span data-ttu-id="a0f91-193">Par exemple, l’application de l’étiquette, lors de la copie d’une étiquette dans le presse-papiers, alloue un objet mémoire local.</span><span class="sxs-lookup"><span data-stu-id="a0f91-193">For example the Label application, when copying a label to the clipboard, allocates a local memory object.</span></span> <span data-ttu-id="a0f91-194">Il libère ensuite cet objet en réponse au message **WM \_ DESTROYCLIPBOARD** , comme suit.</span><span class="sxs-lookup"><span data-stu-id="a0f91-194">It then frees this object in response to the **WM\_DESTROYCLIPBOARD** message, as follows.</span></span>


```
case WM_DESTROYCLIPBOARD: 
    if (pboxLocalClip != NULL) 
    { 
        LocalFree(pboxLocalClip); 
        pboxLocalClip = NULL; 
    } 
    break;
```



### <a name="using-the-owner-display-clipboard-format"></a><span data-ttu-id="a0f91-195">Utilisation du format de presse-papiers Owner-Display</span><span class="sxs-lookup"><span data-stu-id="a0f91-195">Using the Owner-Display Clipboard Format</span></span>

<span data-ttu-id="a0f91-196">Si une fenêtre place des informations dans le presse-papiers en utilisant le format de presse-papiers **CF \_ OWNERDISPLAY** , elle doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="a0f91-196">If a window places information on the clipboard by using the **CF\_OWNERDISPLAY** clipboard format, it must do the following:</span></span>

-   <span data-ttu-id="a0f91-197">Traitez le message [**WM \_ PAINTCLIPBOARD**](wm-paintclipboard.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f91-197">Process the [**WM\_PAINTCLIPBOARD**](wm-paintclipboard.md) message.</span></span> <span data-ttu-id="a0f91-198">Ce message est envoyé au propriétaire du presse-papiers lorsqu’une partie de la fenêtre de la visionneuse du presse-papiers doit être repeinte.</span><span class="sxs-lookup"><span data-stu-id="a0f91-198">This message is sent to the clipboard owner when a portion of the clipboard viewer window must be repainted.</span></span>

-   <span data-ttu-id="a0f91-199">Traitez le message [**WM \_ SIZECLIPBOARD**](wm-sizeclipboard.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f91-199">Process the [**WM\_SIZECLIPBOARD**](wm-sizeclipboard.md) message.</span></span> <span data-ttu-id="a0f91-200">Ce message est envoyé au propriétaire du presse-papiers lorsque la fenêtre de la visionneuse du presse-papiers a été redimensionnée ou que son contenu a changé.</span><span class="sxs-lookup"><span data-stu-id="a0f91-200">This message is sent to the clipboard owner when the clipboard viewer window has been resized or its content has changed.</span></span>

    <span data-ttu-id="a0f91-201">En règle générale, une fenêtre répond à ce message en définissant les positions et les plages de défilement pour la fenêtre de la visionneuse du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="a0f91-201">Typically, a window responds to this message by setting the scroll positions and ranges for the clipboard viewer window.</span></span> <span data-ttu-id="a0f91-202">En réponse à ce message, l’application étiquette met également à jour une structure de [**taille**](/previous-versions//dd145106(v=vs.85)) pour la fenêtre de la visionneuse du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="a0f91-202">In response to this message, the Label application also updates a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure for the clipboard viewer window.</span></span>

-   <span data-ttu-id="a0f91-203">Traitez les messages [**WM \_ HSCROLLCLIPBOARD**](wm-hscrollclipboard.md) et [**WM \_ VSCROLLCLIPBOARD**](wm-vscrollclipboard.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f91-203">Process the [**WM\_HSCROLLCLIPBOARD**](wm-hscrollclipboard.md) and [**WM\_VSCROLLCLIPBOARD**](wm-vscrollclipboard.md) messages.</span></span> <span data-ttu-id="a0f91-204">Ces messages sont envoyés au propriétaire du presse-papiers lorsqu’un événement de barre de défilement se produit dans la fenêtre de la visionneuse du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="a0f91-204">These messages are sent to the clipboard owner when a scroll bar event occurs in the clipboard viewer window.</span></span>

-   <span data-ttu-id="a0f91-205">Traitez le message [**WM \_ ASKCBFORMATNAME**](wm-askcbformatname.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f91-205">Process the [**WM\_ASKCBFORMATNAME**](wm-askcbformatname.md) message.</span></span> <span data-ttu-id="a0f91-206">La fenêtre de la visionneuse du presse-papiers envoie ce message à une application pour récupérer le nom du format d’affichage propriétaire.</span><span class="sxs-lookup"><span data-stu-id="a0f91-206">The clipboard viewer window sends this message to an application to retrieve the name of the owner-display format.</span></span>

<span data-ttu-id="a0f91-207">La procédure de fenêtre pour l’application de l’étiquette traite ces messages, comme suit.</span><span class="sxs-lookup"><span data-stu-id="a0f91-207">The window procedure for the Label application processes these messages, as follows.</span></span>


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



## <a name="monitoring-clipboard-contents"></a><span data-ttu-id="a0f91-208">Surveiller le contenu du presse-papiers</span><span class="sxs-lookup"><span data-stu-id="a0f91-208">Monitoring Clipboard Contents</span></span>

<span data-ttu-id="a0f91-209">Il existe trois façons de surveiller les modifications apportées au Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="a0f91-209">There are three ways of monitoring changes to the clipboard.</span></span> <span data-ttu-id="a0f91-210">La méthode la plus ancienne consiste à créer une fenêtre de la visionneuse du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="a0f91-210">The oldest method is to create a clipboard viewer window.</span></span> <span data-ttu-id="a0f91-211">Windows 2000 a ajouté la possibilité d’interroger le numéro de séquence du presse-papiers, et Windows Vista a ajouté la prise en charge des écouteurs de format du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="a0f91-211">Windows 2000 added the ability to query the clipboard sequence number, and Windows Vista added support for clipboard format listeners.</span></span> <span data-ttu-id="a0f91-212">La visionneuse du presse-papiers Windows est prise en charge pour la compatibilité descendante avec les versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="a0f91-212">Clipboard viewer windows are supported for backward compatibility with earlier versions of Windows.</span></span> <span data-ttu-id="a0f91-213">Les nouveaux programmes doivent utiliser les écouteurs de format du presse-papiers ou le numéro de séquence du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="a0f91-213">New programs should use clipboard format listeners or the clipboard sequence number.</span></span>

## <a name="querying-the-clipboard-sequence-number"></a><span data-ttu-id="a0f91-214">Interrogation du numéro de séquence du presse-papiers</span><span class="sxs-lookup"><span data-stu-id="a0f91-214">Querying the Clipboard Sequence Number</span></span>

<span data-ttu-id="a0f91-215">Chaque fois que le contenu du presse-papiers change, une valeur 32 bits connue comme le numéro de séquence du presse-papiers est incrémentée.</span><span class="sxs-lookup"><span data-stu-id="a0f91-215">Each time the contents of the clipboard change, a 32-bit value known as the clipboard sequence number is incremented.</span></span> <span data-ttu-id="a0f91-216">Un programme peut récupérer le numéro de séquence du presse-papiers actuel en appelant la fonction [**GetClipboardSequenceNumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) .</span><span class="sxs-lookup"><span data-stu-id="a0f91-216">A program can retrieve the current clipboard sequence number by calling the [**GetClipboardSequenceNumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) function.</span></span> <span data-ttu-id="a0f91-217">En comparant la valeur retournée par rapport à une valeur retournée par un appel précédent à **GetClipboardSequenceNumber**, un programme peut déterminer si le contenu du presse-papiers a changé.</span><span class="sxs-lookup"><span data-stu-id="a0f91-217">By comparing the value returned against a value returned by a previous call to **GetClipboardSequenceNumber**, a program can determine whether the clipboard contents have changed.</span></span> <span data-ttu-id="a0f91-218">Cette méthode est plus adaptée aux programmes qui cachent les résultats en fonction du contenu actuel du presse-papiers et doivent savoir si les calculs sont toujours valides avant d’utiliser les résultats de ce cache.</span><span class="sxs-lookup"><span data-stu-id="a0f91-218">This method is more suitable to programs which cache results based on the current clipboard contents and need to know whether the calculations are still valid before using the results from that cache.</span></span> <span data-ttu-id="a0f91-219">Notez qu’il ne s’agit pas d’une méthode de notification et qu’elle ne doit pas être utilisée dans une boucle d’interrogation.</span><span class="sxs-lookup"><span data-stu-id="a0f91-219">Note that this is a not a notification method and should not be used in a polling loop.</span></span> <span data-ttu-id="a0f91-220">Pour être averti lorsque le contenu du presse-papiers change, utilisez un écouteur de format du presse-papiers ou une visionneuse du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="a0f91-220">To be notified when clipboard contents change, use a clipboard format listener or a clipboard viewer.</span></span>

## <a name="creating-a-clipboard-format-listener"></a><span data-ttu-id="a0f91-221">Création d’un écouteur de format de presse-papiers</span><span class="sxs-lookup"><span data-stu-id="a0f91-221">Creating a Clipboard Format Listener</span></span>

<span data-ttu-id="a0f91-222">Un écouteur de format de presse-papiers est une fenêtre qui s’est inscrite pour être averti lorsque le contenu du presse-papiers a changé.</span><span class="sxs-lookup"><span data-stu-id="a0f91-222">A clipboard format listener is a window which has registered to be notified when the contents of the clipboard has changed.</span></span> <span data-ttu-id="a0f91-223">Cette méthode est recommandée par rapport à la création d’une fenêtre du presse-papiers, car elle est plus simple à implémenter et évite les problèmes si les programmes ne parviennent pas à gérer correctement la chaîne du presse-papiers ou si une fenêtre de la chaîne de la visionneuse du presse-papiers ne répond plus aux messages.</span><span class="sxs-lookup"><span data-stu-id="a0f91-223">This method is recommended over creating a clipboard viewer window because it is simpler to implement and avoids problems if programs fail to maintain the clipboard viewer chain properly or if a window in the clipboard viewer chain stops responding to messages.</span></span>

<span data-ttu-id="a0f91-224">Une fenêtre s’inscrit comme un écouteur de format de presse-papiers en appelant la fonction [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) .</span><span class="sxs-lookup"><span data-stu-id="a0f91-224">A window registers as a clipboard format listener by calling the [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) function.</span></span> <span data-ttu-id="a0f91-225">Lorsque le contenu du presse-papiers change, la fenêtre est publiée dans un message [**WM \_ CLIPBOARDUPDATE**](wm-clipboardupdate.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f91-225">When the contents of the clipboard change, the window is posted a [**WM\_CLIPBOARDUPDATE**](wm-clipboardupdate.md) message.</span></span> <span data-ttu-id="a0f91-226">L’inscription reste valide jusqu’à ce que la fenêtre annule son inscription en appelant la fonction [**RemoveClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener) .</span><span class="sxs-lookup"><span data-stu-id="a0f91-226">The registration remains valid until the window unregister itself by calling the [**RemoveClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener) function.</span></span>

## <a name="creating-a-clipboard-viewer-window"></a><span data-ttu-id="a0f91-227">Création d’une fenêtre de la visionneuse du presse-papiers</span><span class="sxs-lookup"><span data-stu-id="a0f91-227">Creating a Clipboard Viewer Window</span></span>

<span data-ttu-id="a0f91-228">Une fenêtre de la visionneuse du presse-papiers affiche le contenu actuel du presse-papiers et reçoit des messages lorsque le contenu du presse-papiers change.</span><span class="sxs-lookup"><span data-stu-id="a0f91-228">A clipboard viewer window displays the current content of the clipboard, and receives messages when the clipboard content changes.</span></span> <span data-ttu-id="a0f91-229">Pour créer une fenêtre de la visionneuse du presse-papiers, votre application doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="a0f91-229">To create a clipboard viewer window, your application must do the following:</span></span>

-   <span data-ttu-id="a0f91-230">Ajoutez la fenêtre à la chaîne de la visionneuse du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="a0f91-230">Add the window to the clipboard viewer chain.</span></span>
-   <span data-ttu-id="a0f91-231">Traitez le message [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f91-231">Process the [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message.</span></span>
-   <span data-ttu-id="a0f91-232">Traitez le message [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f91-232">Process the [**WM\_DRAWCLIPBOARD**](wm-drawclipboard.md) message.</span></span>
-   <span data-ttu-id="a0f91-233">Supprime la fenêtre de la chaîne de la visionneuse du presse-papiers avant sa destruction.</span><span class="sxs-lookup"><span data-stu-id="a0f91-233">Remove the window from the clipboard viewer chain before it is destroyed.</span></span>

## <a name="adding-a-window-to-the-clipboard-viewer-chain"></a><span data-ttu-id="a0f91-234">Ajout d’une fenêtre à la chaîne de la visionneuse du presse-papiers</span><span class="sxs-lookup"><span data-stu-id="a0f91-234">Adding a Window to the Clipboard Viewer Chain</span></span>

<span data-ttu-id="a0f91-235">Une fenêtre s’ajoute à la chaîne de la visionneuse du presse-papiers en appelant la fonction [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .</span><span class="sxs-lookup"><span data-stu-id="a0f91-235">A window adds itself to the clipboard viewer chain by calling the [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) function.</span></span> <span data-ttu-id="a0f91-236">La valeur de retour est le handle de la fenêtre suivante dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="a0f91-236">The return value is the handle to the next window in the chain.</span></span> <span data-ttu-id="a0f91-237">Une fenêtre doit assurer le suivi de cette valeur, par exemple, en l’enregistrant dans une variable statique nommée *hwndNextViewer*.</span><span class="sxs-lookup"><span data-stu-id="a0f91-237">A window must keep track of this value — for example, by saving it in a static variable named *hwndNextViewer*.</span></span>

<span data-ttu-id="a0f91-238">L’exemple suivant ajoute une fenêtre à la chaîne de la visionneuse du presse-papiers en réponse au message [**WM \_ Create**](/windows/desktop/winmsg/wm-create) .</span><span class="sxs-lookup"><span data-stu-id="a0f91-238">The following example adds a window to the clipboard viewer chain in response to the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message.</span></span>


```
case WM_CREATE: 
 
    // Add the window to the clipboard viewer chain. 
 
    hwndNextViewer = SetClipboardViewer(hwnd); 
    break;
```



<span data-ttu-id="a0f91-239">Les extraits de code sont affichés pour les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="a0f91-239">Code snippets are shown for the following tasks:</span></span>

-   [<span data-ttu-id="a0f91-240">Traitement du \_ message WM CHANGECBCHAIN</span><span class="sxs-lookup"><span data-stu-id="a0f91-240">Processing the WM\_CHANGECBCHAIN Message</span></span>](/windows)
-   [<span data-ttu-id="a0f91-241">Suppression d’une fenêtre de la chaîne de la visionneuse du presse-papiers</span><span class="sxs-lookup"><span data-stu-id="a0f91-241">Removing a Window from the Clipboard Viewer Chain</span></span>](#removing-a-window-from-the-clipboard-viewer-chain)
-   [<span data-ttu-id="a0f91-242">Traitement du \_ message WM DRAWCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="a0f91-242">Processing the WM\_DRAWCLIPBOARD Message</span></span>](/windows)
-   [<span data-ttu-id="a0f91-243">Exemple de visionneuse du presse-papiers</span><span class="sxs-lookup"><span data-stu-id="a0f91-243">Example of a Clipboard Viewer</span></span>](#example-of-a-clipboard-viewer)

### <a name="processing-the-wm_changecbchain-message"></a><span data-ttu-id="a0f91-244">Traitement du \_ message WM CHANGECBCHAIN</span><span class="sxs-lookup"><span data-stu-id="a0f91-244">Processing the WM\_CHANGECBCHAIN Message</span></span>

<span data-ttu-id="a0f91-245">Une fenêtre de la visionneuse du presse-papiers reçoit le message [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) lorsqu’une autre fenêtre se supprime lui-même de la chaîne du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="a0f91-245">A clipboard viewer window receives the [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message when another window is removing itself from the clipboard viewer chain.</span></span> <span data-ttu-id="a0f91-246">Si la fenêtre en cours de suppression est la fenêtre suivante dans la chaîne, la fenêtre recevant le message doit dissocier la fenêtre suivante de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="a0f91-246">If the window being removed is the next window in the chain, the window receiving the message must unlink the next window from the chain.</span></span> <span data-ttu-id="a0f91-247">Dans le cas contraire, ce message doit être passé à la fenêtre suivante dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="a0f91-247">Otherwise, this message should be passed to the next window in the chain.</span></span>

<span data-ttu-id="a0f91-248">L’exemple suivant illustre le traitement du message [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f91-248">The following example shows the processing of the [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message.</span></span>


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



### <a name="removing-a-window-from-the-clipboard-viewer-chain"></a><span data-ttu-id="a0f91-249">Suppression d’une fenêtre de la chaîne de la visionneuse du presse-papiers</span><span class="sxs-lookup"><span data-stu-id="a0f91-249">Removing a Window from the Clipboard Viewer Chain</span></span>

<span data-ttu-id="a0f91-250">Pour se supprimer de la chaîne de la visionneuse du presse-papiers, une fenêtre appelle la fonction [**ChangeClipboardChain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) .</span><span class="sxs-lookup"><span data-stu-id="a0f91-250">To remove itself from the clipboard viewer chain, a window calls the [**ChangeClipboardChain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) function.</span></span> <span data-ttu-id="a0f91-251">L’exemple suivant supprime une fenêtre de la chaîne de la visionneuse du presse-papiers en réponse au message [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) .</span><span class="sxs-lookup"><span data-stu-id="a0f91-251">The following example removes a window from the clipboard viewer chain in response to the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span>


```
case WM_DESTROY: 
    ChangeClipboardChain(hwnd, hwndNextViewer); 
    PostQuitMessage(0); 
    break;
```



### <a name="processing-the-wm_drawclipboard-message"></a><span data-ttu-id="a0f91-252">Traitement du \_ message WM DRAWCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="a0f91-252">Processing the WM\_DRAWCLIPBOARD Message</span></span>

<span data-ttu-id="a0f91-253">Le message [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) avertit une fenêtre de la visionneuse du presse-papiers que le contenu du presse-papiers a changé.</span><span class="sxs-lookup"><span data-stu-id="a0f91-253">The [**WM\_DRAWCLIPBOARD**](wm-drawclipboard.md) message notifies a clipboard viewer window that the content of the clipboard has changed.</span></span> <span data-ttu-id="a0f91-254">Une fenêtre doit effectuer les opérations suivantes lors du traitement du message **WM \_ DRAWCLIPBOARD** :</span><span class="sxs-lookup"><span data-stu-id="a0f91-254">A window should do the following when processing the **WM\_DRAWCLIPBOARD** message:</span></span>

1.  <span data-ttu-id="a0f91-255">Déterminez les formats de presse-papiers disponibles à afficher.</span><span class="sxs-lookup"><span data-stu-id="a0f91-255">Determine which of the available clipboard formats to display.</span></span>
2.  <span data-ttu-id="a0f91-256">Récupérer les données du presse-papiers et les afficher dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a0f91-256">Retrieve the clipboard data and display it in the window.</span></span> <span data-ttu-id="a0f91-257">Ou, si le format du presse-papiers est **CF \_ OWNERDISPLAY**, envoyez un message [**WM \_ PAINTCLIPBOARD**](wm-paintclipboard.md) au propriétaire du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="a0f91-257">Or if the clipboard format is **CF\_OWNERDISPLAY**, send a [**WM\_PAINTCLIPBOARD**](wm-paintclipboard.md) message to the clipboard owner.</span></span>
3.  <span data-ttu-id="a0f91-258">Envoyer le message à la fenêtre suivante dans la chaîne du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="a0f91-258">Send the message to the next window in the clipboard viewer chain.</span></span>

<span data-ttu-id="a0f91-259">Pour obtenir un exemple de traitement du message [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) , consultez l’exemple de la liste dans l’exemple [d’une visionneuse du presse-papiers](#example-of-a-clipboard-viewer).</span><span class="sxs-lookup"><span data-stu-id="a0f91-259">For an example of processing the [**WM\_DRAWCLIPBOARD**](wm-drawclipboard.md) message, see the example listing in [Example of a Clipboard Viewer](#example-of-a-clipboard-viewer).</span></span>

### <a name="example-of-a-clipboard-viewer"></a><span data-ttu-id="a0f91-260">Exemple de visionneuse du presse-papiers</span><span class="sxs-lookup"><span data-stu-id="a0f91-260">Example of a Clipboard Viewer</span></span>

<span data-ttu-id="a0f91-261">L’exemple suivant montre une application de visionneuse du presse-papiers simple.</span><span class="sxs-lookup"><span data-stu-id="a0f91-261">The following example shows a simple clipboard viewer application.</span></span>


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



 

 