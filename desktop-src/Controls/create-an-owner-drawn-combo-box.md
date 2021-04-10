---
title: Comment créer une zone de liste déroulante Owner-Drawn
description: Cette rubrique montre comment utiliser une zone de liste déroulante owner-drawn.
ms.assetid: D866DE82-9734-4E8A-A366-5870C25B7C7B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5355dd33fe0067165308e9e6e5885b76edbe7ceb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031891"
---
# <a name="how-to-create-an-owner-drawn-combo-box"></a><span data-ttu-id="d88fa-103">Comment créer une zone de liste déroulante Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="d88fa-103">How to Create an Owner-Drawn Combo Box</span></span>

<span data-ttu-id="d88fa-104">Cette rubrique montre comment utiliser une zone de liste déroulante owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="d88fa-104">This topic demonstrates how to use an owner-drawn combo box.</span></span> <span data-ttu-id="d88fa-105">L’exemple de code C++ utilise une zone de liste déroulante owner-drawn pour afficher les quatre groupes d’aliments, chacun représenté par une image bitmap et un nom.</span><span class="sxs-lookup"><span data-stu-id="d88fa-105">The C++ code example uses an owner-drawn drop-down list box to display the four food groups, each represented by a bitmap and a name.</span></span> <span data-ttu-id="d88fa-106">Si vous sélectionnez un groupe de nourriture, les aliments de ce groupe s’affichent dans une liste.</span><span class="sxs-lookup"><span data-stu-id="d88fa-106">Selecting a food group causes the foods in that group to appear in a list.</span></span>

![capture d’écran montrant une boîte de dialogue avec une zone de liste et une zone de liste déroulante développée montrant une icône et une étiquette pour chaque élément](images/cscbx-01.png)

<span data-ttu-id="d88fa-108">La boîte de dialogue contient également une zone de liste (IDLIST) et deux boutons : **OK** (IDOK) et **Annuler** (IDCANCEL).</span><span class="sxs-lookup"><span data-stu-id="d88fa-108">The dialog box also contains a list box (IDLIST) and two buttons: **OK** (IDOK) and **Cancel** (IDCANCEL).</span></span> <span data-ttu-id="d88fa-109">Les constantes IDOK et IDCANCEL sont définies par les fichiers d’en-tête du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="d88fa-109">The IDOK and IDCANCEL constants are defined by the SDK header files.</span></span> <span data-ttu-id="d88fa-110">La constante IDLIST est définie dans le fichier d’en-tête de l’application, comme l’identificateur de contrôle, IDCOMBO.</span><span class="sxs-lookup"><span data-stu-id="d88fa-110">The constant IDLIST is defined in the application's header file, as is the control identifier, IDCOMBO.</span></span> <span data-ttu-id="d88fa-111">Pour plus d’informations sur les boîtes de dialogue, consultez [boîtes de dialogue](/windows/desktop/dlgbox/dialog-boxes).</span><span class="sxs-lookup"><span data-stu-id="d88fa-111">For more information about dialog boxes, see [Dialog Boxes](/windows/desktop/dlgbox/dialog-boxes).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="d88fa-112">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="d88fa-112">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d88fa-113">Technologies</span><span class="sxs-lookup"><span data-stu-id="d88fa-113">Technologies</span></span>

-   [<span data-ttu-id="d88fa-114">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="d88fa-114">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d88fa-115">Prérequis</span><span class="sxs-lookup"><span data-stu-id="d88fa-115">Prerequisites</span></span>

-   <span data-ttu-id="d88fa-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="d88fa-116">C/C++</span></span>
-   <span data-ttu-id="d88fa-117">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="d88fa-117">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d88fa-118">Instructions</span><span class="sxs-lookup"><span data-stu-id="d88fa-118">Instructions</span></span>

### <a name="step-1-create-the-owner-drawn-dialog-box"></a><span data-ttu-id="d88fa-119">Étape 1 : créer la boîte de dialogue Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="d88fa-119">Step 1: Create the Owner-Drawn Dialog Box</span></span>

<span data-ttu-id="d88fa-120">L’exemple de code utilise la fonction [**DialogBox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa) pour créer une boîte de dialogue modale.</span><span class="sxs-lookup"><span data-stu-id="d88fa-120">The code example uses the [**DialogBox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa) function to create a modal dialog box.</span></span> <span data-ttu-id="d88fa-121">Le modèle de boîte de dialogue, IDD \_ SQMEAL, définit les styles de fenêtre, les boutons et les identificateurs de contrôle pour la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="d88fa-121">The dialog box template, IDD\_SQMEAL, defines the window styles, buttons, and control identifiers for the combo box.</span></span> <span data-ttu-id="d88fa-122">Dans cet exemple, la zone de liste déroulante utilise les styles [**CBS \_**](combo-box-styles.md), CBS [**\_ OWNERDRAWFIXED**](combo-box-styles.md), CBS [**\_ sort**](combo-box-styles.md), [**CBS \_ HASSTRINGS**](combo-box-styles.md), [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles)et [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="d88fa-122">The combo box in this example uses the [**CBS\_DROPDOWNLIST**](combo-box-styles.md), [**CBS\_OWNERDRAWFIXED**](combo-box-styles.md), [**CBS\_SORT**](combo-box-styles.md), [**CBS\_HASSTRINGS**](combo-box-styles.md), [**WS\_VSCROLL**](/windows/desktop/winmsg/window-styles), and [**WS\_TABSTOP**](/windows/desktop/winmsg/window-styles) styles.</span></span>


```C++
DialogBox(hInst, MAKEINTRESOURCE(IDD_SQMEAL), 
    hWnd, FoodDlgProc);
```



### <a name="step-2-process-the-wm_initdialog-and-wm_destroy-messages-in-a-dialog-box"></a><span data-ttu-id="d88fa-123">Étape 2 : traiter les \_ messages WM INITDIALOG et WM \_ Destroy dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d88fa-123">Step 2: Process the WM\_INITDIALOG and WM\_DESTROY messages in a dialog box.</span></span>

<span data-ttu-id="d88fa-124">Lorsque vous utilisez une zone de liste déroulante dans une boîte de dialogue, vous répondez généralement à un message [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) en initialisant la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="d88fa-124">When you use a combo box in a dialog box, you usually respond to a [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message by initializing the combo box.</span></span> <span data-ttu-id="d88fa-125">L’application charge les bitmaps utilisées pour la zone de liste déroulante owner-drawn, puis appelle la fonction définie par l’application `InitGroupList` pour initialiser la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="d88fa-125">The application loads the bitmaps used for the owner-drawn combo box and then calls the application-defined `InitGroupList` function to initialize the combo box.</span></span> <span data-ttu-id="d88fa-126">Il sélectionne également le premier élément de liste dans la zone de liste déroulante, puis appelle la fonction définie par l’application `InitFoodList` pour initialiser la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="d88fa-126">It also selects the first list item in the combo box and then calls the application-defined `InitFoodList` function to initialize the list box.</span></span>

<span data-ttu-id="d88fa-127">Dans l’exemple, la zone de liste déroulante owner-drawn est une zone de liste déroulante qui contient les noms de chacun des quatre groupes de nourriture.</span><span class="sxs-lookup"><span data-stu-id="d88fa-127">In the example, the owner-drawn combo box is a drop-down list box that contains the names of each of the four food groups.</span></span> <span data-ttu-id="d88fa-128">`InitGroupList` Ajoute le nom de chaque groupe de nourriture et utilise le message [**CB \_ SETITEMDATA**](cb-setitemdata.md) pour associer un handle de bitmap à chaque élément de liste identifiant un groupe alimentaire.</span><span class="sxs-lookup"><span data-stu-id="d88fa-128">`InitGroupList` adds the name of each food group , and uses the [**CB\_SETITEMDATA**](cb-setitemdata.md) message to associate a bitmap handle with each list item that identifies a food group.</span></span>

<span data-ttu-id="d88fa-129">La zone de liste de l’exemple contient les noms des aliments dans le groupe de nourriture sélectionné.</span><span class="sxs-lookup"><span data-stu-id="d88fa-129">The list box in the example contains the names of foods in the selected food group.</span></span> <span data-ttu-id="d88fa-130">**InitFoodList** réinitialise le contenu de la zone de liste, puis ajoute les noms de la sélection de nourriture actuelle dans la zone de liste déroulante groupe de nourriture actuel.</span><span class="sxs-lookup"><span data-stu-id="d88fa-130">**InitFoodList** resets the contents of the list box, then adds the names of the current food selection in the current food group drop-down list box.</span></span>


```C++
case WM_INITDIALOG:

    // Call an application-defined function to load bitmap resources.
    if (!LoadIconBitmaps())
    {
        EndDialog(hDlg, -1);
        break;
    }

    // Initialize the food groups combo box and select the first item.
    InitGroupList(hDlg);
    SendDlgItemMessage(hDlg, IDCOMBO, CB_SETCURSEL, 0, 0); 

    // Initialize the food list box and select the first item.
    InitFoodList(hDlg);
    SendDlgItemMessage(hDlg, IDLIST, LB_SETCURSEL, 0, 0); 

     return (INT_PTR)TRUE;
```



<span data-ttu-id="d88fa-131">Lorsqu’il reçoit le message [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) , l’application supprime les bitmaps de la zone de liste déroulante owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="d88fa-131">When it receives the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message, the application deletes the bitmaps in the owner-drawn combo box.</span></span>


```C++
case WM_DESTROY:

    // Call the application-defined function to free the bitmap resources.
    DeleteIconBitmaps();
    break;
```



### <a name="step-3-process-the-wm_measureitem-message"></a><span data-ttu-id="d88fa-132">Étape 3 : traiter le \_ message WM MEASUREITEM.</span><span class="sxs-lookup"><span data-stu-id="d88fa-132">Step 3: Process the WM\_MEASUREITEM message.</span></span>

<span data-ttu-id="d88fa-133">Une zone de liste déroulante owner-drawn envoie le message [**WM \_ MEASUREITEM**](wm-measureitem.md) à sa procédure de boîte de dialogue ou de fenêtre parente afin que l’application puisse définir les dimensions de chaque élément de liste.</span><span class="sxs-lookup"><span data-stu-id="d88fa-133">An owner-drawn combo box sends the [**WM\_MEASUREITEM**](wm-measureitem.md) message to its parent window or dialog box procedure so that the application can set the dimensions of each list item.</span></span> <span data-ttu-id="d88fa-134">Étant donné que la zone de liste déroulante exemple a le style [**CBS \_ OWNERDRAWFIXED**](combo-box-styles.md) , le système envoie le message **WM \_ MEASUREITEM** une seule fois.</span><span class="sxs-lookup"><span data-stu-id="d88fa-134">Because the example combo box has the [**CBS\_OWNERDRAWFIXED**](combo-box-styles.md) style, the system sends the **WM\_MEASUREITEM** message only once.</span></span> <span data-ttu-id="d88fa-135">Les zones de liste déroulante avec le style [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) envoient un message **WM \_ MEASUREITEM** pour chaque élément de liste.</span><span class="sxs-lookup"><span data-stu-id="d88fa-135">Combo boxes with the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style send a **WM\_MEASUREITEM** message for each list item.</span></span>

<span data-ttu-id="d88fa-136">Le paramètre *lParam* est un pointeur vers une structure [**measureitemstruct,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) qui identifie l’élément de contrôle et de liste.</span><span class="sxs-lookup"><span data-stu-id="d88fa-136">The *lParam* parameter is a pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that identifies the control and list item.</span></span> <span data-ttu-id="d88fa-137">Elle contient également les dimensions par défaut de l’élément de liste.</span><span class="sxs-lookup"><span data-stu-id="d88fa-137">It also contains the default dimensions of the list item.</span></span> <span data-ttu-id="d88fa-138">L’exemple modifie le membre de la structure **ItemHeight** pour garantir que les éléments de liste sont suffisamment hauts pour accueillir les bitmaps de groupe de nourriture.</span><span class="sxs-lookup"><span data-stu-id="d88fa-138">The example modifies the **itemHeight** structure member to ensure that the list items are high enough to accommodate the food-group bitmaps.</span></span>


```C++
case WM_MEASUREITEM:
    {
    // Set the height of the items in the food groups combo box.
    LPMEASUREITEMSTRUCT lpmis = (LPMEASUREITEMSTRUCT) lParam;

    if (lpmis->itemHeight < CY_BITMAP + 2)
        lpmis->itemHeight = CY_BITMAP + 2;

    break;
    }
```



### <a name="step-4-process-the-wm_drawitem-message"></a><span data-ttu-id="d88fa-139">Étape 4 : traiter le \_ message WM DRAWITEM.</span><span class="sxs-lookup"><span data-stu-id="d88fa-139">Step 4: Process the WM\_DRAWITEM message.</span></span>

<span data-ttu-id="d88fa-140">Une zone de liste déroulante owner-drawn envoie le message [**WM \_ DRAWITEM**](wm-drawitem.md) à la procédure de la fenêtre ou de la boîte de dialogue parente chaque fois que l’application doit repeindre un élément de liste.</span><span class="sxs-lookup"><span data-stu-id="d88fa-140">An owner-drawn combo box sends the [**WM\_DRAWITEM**](wm-drawitem.md) message to its parent window or dialog box procedure each time the application must repaint a list item.</span></span> <span data-ttu-id="d88fa-141">Le paramètre *lParam* est un pointeur vers une structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) qui identifie l’élément de contrôle et de liste.</span><span class="sxs-lookup"><span data-stu-id="d88fa-141">The *lParam* parameter is a pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure that identifies the control and list item.</span></span> <span data-ttu-id="d88fa-142">Elle contient également les informations nécessaires pour peindre l’élément.</span><span class="sxs-lookup"><span data-stu-id="d88fa-142">It also contains information needed to paint the item.</span></span>

<span data-ttu-id="d88fa-143">L’exemple d’application affiche le texte de l’élément de liste et le bitmap associé au groupe Food.</span><span class="sxs-lookup"><span data-stu-id="d88fa-143">The example application displays the list-item text and the bitmap associated with the food group.</span></span> <span data-ttu-id="d88fa-144">Si l’élément a le focus, il dessine également un rectangle de focus.</span><span class="sxs-lookup"><span data-stu-id="d88fa-144">If the item has the focus, it also draws a focus rectangle.</span></span> <span data-ttu-id="d88fa-145">Avant d’afficher le texte, l’exemple définit les couleurs de premier plan et d’arrière-plan, en fonction de l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="d88fa-145">Before displaying the text, the example sets the foreground and background colors, based on the item selected.</span></span> <span data-ttu-id="d88fa-146">Étant donné que la zone de liste déroulante a le style [**CBS \_ HASSTRINGS**](combo-box-styles.md) , la zone de liste déroulante conserve le texte de chaque élément de liste qui peut être extrait à l’aide du message [**CB \_ GETLBTEXT**](cb-getlbtext.md) .</span><span class="sxs-lookup"><span data-stu-id="d88fa-146">Because the combo box has the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the combo box maintains the text for each list item that can be retrieved using the [**CB\_GETLBTEXT**](cb-getlbtext.md) message.</span></span>

<span data-ttu-id="d88fa-147">Les bitmaps utilisées pour l’élément de liste dépendent du groupe Food.</span><span class="sxs-lookup"><span data-stu-id="d88fa-147">The bitmaps used for the list item depend on the food group.</span></span> <span data-ttu-id="d88fa-148">`InitGroupList` utilise le message [**CB \_ SETITEMDATA**](cb-setitemdata.md) pour associer un handle de bitmap à chaque élément de liste.</span><span class="sxs-lookup"><span data-stu-id="d88fa-148">`InitGroupList` uses the [**CB\_SETITEMDATA**](cb-setitemdata.md) message to associate a bitmap handle with each list item.</span></span> <span data-ttu-id="d88fa-149">La procédure de fenêtre récupère le handle de bitmap à partir du membre **ItemData** de la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="d88fa-149">The window procedure retrieves the bitmap handle from the **itemData** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure.</span></span> <span data-ttu-id="d88fa-150">Le système utilise deux bitmaps pour chaque symbole de groupe alimentaire : un bitmap monochrome avec l’opération SRCAND raster pour effacer la zone irrégulière derrière l’image, et une image bitmap de couleur avec l’opération Raster SRCPAINT pour peindre l’image.</span><span class="sxs-lookup"><span data-stu-id="d88fa-150">The system uses two bitmaps for each food group symbol: a monochrome bitmap with the SRCAND raster operation to erase the irregular region behind the image, and a color bitmap with the SRCPAINT raster operation to paint the image.</span></span>


```C++
case WM_DRAWITEM:
    {
    COLORREF clrBackground;
    COLORREF clrForeground;
    TEXTMETRIC tm;
    int x;
    int y;
    HRESULT hr;
    size_t cch;

    LPDRAWITEMSTRUCT lpdis = (LPDRAWITEMSTRUCT) lParam;
       
    if (lpdis->itemID == -1) // Empty item)
        break;

    // Get the food icon from the item data.
    hbmIcon = (HBITMAP) lpdis->itemData;

    // The colors depend on whether the item is selected.
    clrForeground = SetTextColor(lpdis->hDC, 
        GetSysColor(lpdis->itemState & ODS_SELECTED ?
        COLOR_HIGHLIGHTTEXT : COLOR_WINDOWTEXT));

    clrBackground = SetBkColor(lpdis->hDC, 
        GetSysColor(lpdis->itemState & ODS_SELECTED ?
        COLOR_HIGHLIGHT : COLOR_WINDOW));

    // Calculate the vertical and horizontal position.
    GetTextMetrics(lpdis->hDC, &tm);
    y = (lpdis->rcItem.bottom + lpdis->rcItem.top - tm.tmHeight) / 2;
    x = LOWORD(GetDialogBaseUnits()) / 4;

    // Get and display the text for the list item.
    SendMessage(lpdis->hwndItem, CB_GETLBTEXT,
        lpdis->itemID, (LPARAM) achTemp);

    hr = StringCchLength(achTemp, 256, &cch);
    if (FAILED(hr))
    {
        // TODO: Write error handler.
    }

    ExtTextOut(lpdis->hDC, CX_BITMAP + 2 * x, y,
        ETO_CLIPPED | ETO_OPAQUE, &lpdis->rcItem,
        achTemp, (UINT)cch, NULL);

    // Restore the previous colors.
    SetTextColor(lpdis->hDC, clrForeground);
    SetBkColor(lpdis->hDC, clrBackground);
    
    //  Draw the food icon for the item. 
    HDC hdc = CreateCompatibleDC(lpdis->hDC); 
    if (hdc == NULL) 
        break; 
 
    SelectObject(hdc, hbmMask); 
    BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
        CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCAND); 
 
    SelectObject(hdc, hbmIcon); 
    BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
        CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCPAINT); 
 
    DeleteDC(hdc); 
  
    // If the item has the focus, draw the focus rectangle.
    if (lpdis->itemState & ODS_FOCUS)
        DrawFocusRect(lpdis->hDC, &lpdis->rcItem);

    break;
    }
```



### <a name="step-5-process-the-wm_command-message"></a><span data-ttu-id="d88fa-151">Étape 5 : traiter le \_ message de commande WM.</span><span class="sxs-lookup"><span data-stu-id="d88fa-151">Step 5: Process the WM\_COMMAND message.</span></span>

<span data-ttu-id="d88fa-152">Lorsqu’un événement se produit dans un contrôle de boîte de dialogue, le contrôle notifie la procédure de boîte de dialogue au moyen d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="d88fa-152">When an event occurs in a dialog box control, the control notifies the dialog box procedure by means of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="d88fa-153">L’exemple traite les messages de notification de la zone de liste déroulante, la zone de liste et le bouton **OK** .</span><span class="sxs-lookup"><span data-stu-id="d88fa-153">The example processes notification messages from the combo box, the list box, and the **OK** button.</span></span> <span data-ttu-id="d88fa-154">L’identificateur de contrôle se trouve dans le mot de poids faible de *wParam* et le code de notification se trouve dans le mot de poids fort de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="d88fa-154">The control identifier is in the low-order word of *wParam*, and the notification code is in the high-order word of *wParam*.</span></span>

<span data-ttu-id="d88fa-155">Si l’identificateur de contrôle est IDCOMBO, un événement s’est produit dans la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="d88fa-155">If the control identifier is IDCOMBO, an event has occurred in the combo box.</span></span> <span data-ttu-id="d88fa-156">En réponse, la procédure de boîte de dialogue ignore tous les autres événements de zone de liste modifiable, à l’exception de [**CBN \_ SELENDOK**](cbn-selendok.md), qui indique qu’une sélection a été effectuée, la zone de liste déroulante a été fermée et les modifications apportées doivent être acceptées.</span><span class="sxs-lookup"><span data-stu-id="d88fa-156">In response, the dialog box procedure ignores all other combo box events except [**CBN\_SELENDOK**](cbn-selendok.md), which indicates that a selection was made, the drop down list box was closed, and the changes made should be accepted.</span></span> <span data-ttu-id="d88fa-157">La procédure de boîte de dialogue appelle `InitFoodList` pour réinitialiser le contenu de la zone de liste et ajouter les noms des sélections actuelles dans la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="d88fa-157">The dialog box procedure calls `InitFoodList` to reset the contents of the list box and to add the names of the current selections in the drop-down list box.</span></span>

<span data-ttu-id="d88fa-158">Si l’identificateur de contrôle est IDLIST, un événement s’est produit dans la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="d88fa-158">If the control identifier is IDLIST, an event has occurred in the list box.</span></span> <span data-ttu-id="d88fa-159">La procédure de la boîte de dialogue ignore tous les événements de zone de liste, à l’exception de [**LBN \_ DBLCLK**](lbn-dblclk.md), qui indique que l’utilisateur a double-cliqué sur un élément de liste.</span><span class="sxs-lookup"><span data-stu-id="d88fa-159">This causes the dialog box procedure to ignore all list box events except [**LBN\_DBLCLK**](lbn-dblclk.md), which indicates that the user has double-clicked a list item.</span></span> <span data-ttu-id="d88fa-160">Cet événement est traité de la même façon que si un bouton **OK** avait été choisi.</span><span class="sxs-lookup"><span data-stu-id="d88fa-160">This event is processed in the same way as if an **OK** button had been chosen.</span></span>

<span data-ttu-id="d88fa-161">Si l’identificateur de contrôle est IDOK, l’utilisateur a choisi le bouton **OK** .</span><span class="sxs-lookup"><span data-stu-id="d88fa-161">If the control identifier is IDOK, the user has chosen the **OK** button.</span></span> <span data-ttu-id="d88fa-162">En réponse, la procédure de boîte de dialogue insère le nom des aliments sélectionnés dans le contrôle d’édition multiligne de l’application, puis appelle la fonction [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) pour fermer la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d88fa-162">In response, the dialog box procedure inserts the name of the selected food into the application's multi-line edit control, then calls the [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) function to close the dialog box.</span></span>

<span data-ttu-id="d88fa-163">Si l’identificateur de contrôle est IDCANCEL, l’utilisateur a cliqué sur le bouton **Annuler** .</span><span class="sxs-lookup"><span data-stu-id="d88fa-163">If the control identifier is IDCANCEL, the user has clicked the **Cancel** button.</span></span> <span data-ttu-id="d88fa-164">En réponse, la procédure de boîte de dialogue appelle [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) pour fermer la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d88fa-164">In response, the dialog box procedure calls [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) to close the dialog box.</span></span>


```C++
case WM_COMMAND:
        switch (LOWORD(wParam)) 
        { 
            case IDCOMBO: 
                if (HIWORD(wParam) == CBN_SELENDOK) 
                { 
                    InitFoodList(hDlg); 
                    SendDlgItemMessage(hDlg, IDLIST, 
                        LB_SETCURSEL, 0, 0); 
                } 
                break; 
 
            case IDLIST: 
                if (HIWORD(wParam) != LBN_DBLCLK) 
                    break; 
 
            // For a double-click, process the OK case. 
            case IDOK: 
 
                // Get the text for the selected list item. 
                hwnd = GetDlgItem(hDlg, IDLIST); 

                // Here it is assumed the text can fit into achTemp.
                // If there is doubt, call LB_GETTEXTLENGTH first.
                SendMessage(hwnd, LB_GETTEXT, 
                    SendMessage(hwnd, LB_GETCURSEL, 0, 0), 
                    (LPARAM) achTemp); 
 
                // TODO: Do something with the selected text.
 
                EndDialog(hDlg, 0); 
                break; 
 
            case IDCANCEL: 
                hwnd = GetDlgItem(hDlg, IDCOMBO); 
                if (SendMessage(hwnd, CB_GETDROPPEDSTATE, 0, 0)) 
                    SendMessage(hwnd, CB_SHOWDROPDOWN, FALSE, 0); 
                else EndDialog(hDlg, 0); 
        } 
        break; 
```



## <a name="complete-example"></a><span data-ttu-id="d88fa-165">Exemple complet</span><span class="sxs-lookup"><span data-stu-id="d88fa-165">Complete example</span></span>

<span data-ttu-id="d88fa-166">Voici la procédure de la boîte de dialogue et les fonctions de prise en charge pour la boîte de dialogue **repas carrés** .</span><span class="sxs-lookup"><span data-stu-id="d88fa-166">Following is the dialog box procedure and the supporting functions for the **Square Meal** dialog box.</span></span>


```C++
#define ID_BREAD 0
#define ID_DAIRY 1
#define ID_FRUIT 2
#define ID_MEAT  3

#define CX_BITMAP 24
#define CY_BITMAP 24

HBITMAP hbmBread;
HBITMAP hbmDairy;
HBITMAP hbmMeat;
HBITMAP hbmFruit;
HBITMAP hbmMask;

HBITMAP hbmIcon;
```

```C++
// Message handler for Square Meal dialog box.
INT_PTR CALLBACK FoodDlgProc(HWND hDlg, UINT message, WPARAM wParam, 
    LPARAM lParam)
{
    UNREFERENCED_PARAMETER(lParam);
    TCHAR achTemp[256];
    HWND hwnd;

    switch (message)
    {
    case WM_INITDIALOG:

        // Call an application-defined function to load bitmap resources.
        if (!LoadIconBitmaps())
        {
            EndDialog(hDlg, -1);
            break;
        }

        // Initialize the food groups combo box and select the first item.
        InitGroupList(hDlg);
        SendDlgItemMessage(hDlg, IDCOMBO, CB_SETCURSEL, 0, 0); 

        // Initialize the food list box and select the first item.
        InitFoodList(hDlg);
        SendDlgItemMessage(hDlg, IDLIST, LB_SETCURSEL, 0, 0); 

         return (INT_PTR)TRUE;
   
    case WM_MEASUREITEM:
        {
        // Set the height of the items in the food groups combo box.
        LPMEASUREITEMSTRUCT lpmis = (LPMEASUREITEMSTRUCT) lParam;

        if (lpmis->itemHeight < CY_BITMAP + 2)
            lpmis->itemHeight = CY_BITMAP + 2;

        break;
        }

    case WM_DRAWITEM:
        {
        COLORREF clrBackground;
        COLORREF clrForeground;
        TEXTMETRIC tm;
        int x;
        int y;
        HRESULT hr;
        size_t cch;

        LPDRAWITEMSTRUCT lpdis = (LPDRAWITEMSTRUCT) lParam;
           
        if (lpdis->itemID == -1) // Empty item)
            break;

        // Get the food icon from the item data.
        hbmIcon = (HBITMAP) lpdis->itemData;

        // The colors depend on whether the item is selected.
        clrForeground = SetTextColor(lpdis->hDC, 
            GetSysColor(lpdis->itemState & ODS_SELECTED ?
            COLOR_HIGHLIGHTTEXT : COLOR_WINDOWTEXT));

        clrBackground = SetBkColor(lpdis->hDC, 
            GetSysColor(lpdis->itemState & ODS_SELECTED ?
            COLOR_HIGHLIGHT : COLOR_WINDOW));

        // Calculate the vertical and horizontal position.
        GetTextMetrics(lpdis->hDC, &tm);
        y = (lpdis->rcItem.bottom + lpdis->rcItem.top - tm.tmHeight) / 2;
        x = LOWORD(GetDialogBaseUnits()) / 4;

        // Get and display the text for the list item.
        SendMessage(lpdis->hwndItem, CB_GETLBTEXT,
            lpdis->itemID, (LPARAM) achTemp);

        hr = StringCchLength(achTemp, 256, &cch);
        if (FAILED(hr))
        {
            // TODO: Write error handler.
        }

        ExtTextOut(lpdis->hDC, CX_BITMAP + 2 * x, y,
            ETO_CLIPPED | ETO_OPAQUE, &lpdis->rcItem,
            achTemp, (UINT)cch, NULL);

        // Restore the previous colors.
        SetTextColor(lpdis->hDC, clrForeground);
        SetBkColor(lpdis->hDC, clrBackground);
        
        //  Draw the food icon for the item. 
        HDC hdc = CreateCompatibleDC(lpdis->hDC); 
        if (hdc == NULL) 
            break; 
 
        SelectObject(hdc, hbmMask); 
        BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
            CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCAND); 
 
        SelectObject(hdc, hbmIcon); 
        BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
            CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCPAINT); 
 
        DeleteDC(hdc); 
      
        // If the item has the focus, draw the focus rectangle.
        if (lpdis->itemState & ODS_FOCUS)
            DrawFocusRect(lpdis->hDC, &lpdis->rcItem);

        break;
        }

    case WM_COMMAND:
            switch (LOWORD(wParam)) 
            { 
                case IDCOMBO: 
                    if (HIWORD(wParam) == CBN_SELENDOK) 
                    { 
                        InitFoodList(hDlg); 
                        SendDlgItemMessage(hDlg, IDLIST, 
                            LB_SETCURSEL, 0, 0); 
                    } 
                    break; 
 
                case IDLIST: 
                    if (HIWORD(wParam) != LBN_DBLCLK) 
                        break; 
 
                // For a double-click, process the OK case. 
                case IDOK: 
 
                    // Get the text for the selected list item. 
                    hwnd = GetDlgItem(hDlg, IDLIST); 

                    // Here it is assumed the text can fit into achTemp.
                    // If there is doubt, call LB_GETTEXTLENGTH first.
                    SendMessage(hwnd, LB_GETTEXT, 
                        SendMessage(hwnd, LB_GETCURSEL, 0, 0), 
                        (LPARAM) achTemp); 
 
                    // TODO: Do something with the selected text.
 
                    EndDialog(hDlg, 0); 
                    break; 
 
                case IDCANCEL: 
                    hwnd = GetDlgItem(hDlg, IDCOMBO); 
                    if (SendMessage(hwnd, CB_GETDROPPEDSTATE, 0, 0)) 
                        SendMessage(hwnd, CB_SHOWDROPDOWN, FALSE, 0); 
                    else EndDialog(hDlg, 0); 
            } 
            break; 

    case WM_DESTROY:

        // Call the application-defined function to free the bitmap resources.
        DeleteIconBitmaps();
        break;
    }
    return (INT_PTR)FALSE;
}

// Loads string resources and adds them as items to the drop-down list of
//   the food groups combo box. The bitmap handle of each item&#39;s icon is
//   stored as item data for easy access when the item needs to be drawn.
// 
void InitGroupList(HWND hDlg)
{
    TCHAR achTemp[256];
    DWORD dwIndex;

    // Get the handle of the food groups combo box.
    HWND hwndGroupsBox = GetDlgItem(hDlg, IDCOMBO);

    LoadString(hInst, IDS_BREAD, achTemp, sizeof(achTemp)/sizeof(TCHAR));
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmBread);
    
    LoadString(hInst, IDS_DAIRY, achTemp, sizeof(achTemp)/sizeof(TCHAR)); 
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmDairy);

    LoadString(hInst, IDS_FRUIT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmFruit); 

    LoadString(hInst, IDS_MEAT, achTemp, sizeof(achTemp)/sizeof(TCHAR)); 
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmMeat);

    return;
}

// Fills the food list based on the selected item in the food groups
//   combo box.
void InitFoodList(HWND hDlg)
{
    TCHAR achTemp[256];

    HWND hwndGroupsBox = GetDlgItem(hDlg, IDCOMBO);
    HWND hwndFoodList = GetDlgItem(hDlg, IDLIST);

    // Clear the list contents.
    SendMessage(hwndFoodList, LB_RESETCONTENT, 0, 0);

    // Find out which food group is selected.
    int idFoodGroup = SendMessage(hwndGroupsBox, CB_GETCURSEL, 0, 0);

    switch (idFoodGroup)
    {
    case ID_BREAD:
        LoadString(hInst, IDS_OAT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_WHEAT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_RYE, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);
        break;

    case ID_DAIRY:
        LoadString(hInst, IDS_CHEDDAR, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_MILK, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_PROCESSED, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_SWISS, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);
        
        break;

    case ID_FRUIT:
        LoadString(hInst, IDS_APPLES, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_BANANAS, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_ORANGES, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        break;

    case ID_MEAT:
        LoadString(hInst, IDS_BEEF, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_CHICKEN, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_PORK, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        break;

    default:
        break;
    }

    return;
}

// Loads the food icon bitmaps from the application resources.
//
BOOL LoadIconBitmaps(void)
{
    hbmBread = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_BREAD));

    if (hbmBread != NULL)
         hbmDairy = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_DAIRY));

    if (hbmDairy != NULL)
         hbmMeat = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_MEAT));

    if (hbmMeat != NULL)
        hbmFruit = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_FRUIT));
    
    if (hbmFruit != NULL)
        hbmMask = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_MASK));

    if (hbmMask != NULL)
        return TRUE;
        
    return FALSE;
}

// Frees the icon bitmps.
//
void DeleteIconBitmaps(void)
{
    FreeResource(reinterpret_cast<HGLOBAL>(hbmBread));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmDairy));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmMeat));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmFruit));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmMask));
}
```


## <a name="related-topics"></a><span data-ttu-id="d88fa-167">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d88fa-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d88fa-168">Utilisation de zones de liste déroulante</span><span class="sxs-lookup"><span data-stu-id="d88fa-168">Using Combo Boxes</span></span>](using-combo-boxes.md)
</dt> </dl>

 

 