---
title: Comment créer une zone de liste déroulante Owner-Drawn
description: Cette rubrique montre comment utiliser une zone de liste déroulante owner-drawn.
ms.assetid: D866DE82-9734-4E8A-A366-5870C25B7C7B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5355dd33fe0067165308e9e6e5885b76edbe7ceb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006510"
---
# <a name="how-to-create-an-owner-drawn-combo-box"></a>Comment créer une zone de liste déroulante Owner-Drawn

Cette rubrique montre comment utiliser une zone de liste déroulante owner-drawn. L’exemple de code C++ utilise une zone de liste déroulante owner-drawn pour afficher les quatre groupes d’aliments, chacun représenté par une image bitmap et un nom. Si vous sélectionnez un groupe de nourriture, les aliments de ce groupe s’affichent dans une liste.

![capture d’écran montrant une boîte de dialogue avec une zone de liste et une zone de liste déroulante développée montrant une icône et une étiquette pour chaque élément](images/cscbx-01.png)

La boîte de dialogue contient également une zone de liste (IDLIST) et deux boutons : **OK** (IDOK) et **Annuler** (IDCANCEL). Les constantes IDOK et IDCANCEL sont définies par les fichiers d’en-tête du kit de développement logiciel (SDK). La constante IDLIST est définie dans le fichier d’en-tête de l’application, comme l’identificateur de contrôle, IDCOMBO. Pour plus d’informations sur les boîtes de dialogue, consultez [boîtes de dialogue](/windows/desktop/dlgbox/dialog-boxes).

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="step-1-create-the-owner-drawn-dialog-box"></a>Étape 1 : créer la boîte de dialogue Owner-Drawn

L’exemple de code utilise la fonction [**DialogBox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa) pour créer une boîte de dialogue modale. Le modèle de boîte de dialogue, IDD \_ SQMEAL, définit les styles de fenêtre, les boutons et les identificateurs de contrôle pour la zone de liste déroulante. Dans cet exemple, la zone de liste déroulante utilise les styles [**CBS \_**](combo-box-styles.md), CBS [**\_ OWNERDRAWFIXED**](combo-box-styles.md), CBS [**\_ sort**](combo-box-styles.md), [**CBS \_ HASSTRINGS**](combo-box-styles.md), [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles)et [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) .


```C++
DialogBox(hInst, MAKEINTRESOURCE(IDD_SQMEAL), 
    hWnd, FoodDlgProc);
```



### <a name="step-2-process-the-wm_initdialog-and-wm_destroy-messages-in-a-dialog-box"></a>Étape 2 : traiter les \_ messages WM INITDIALOG et WM \_ Destroy dans une boîte de dialogue.

Lorsque vous utilisez une zone de liste déroulante dans une boîte de dialogue, vous répondez généralement à un message [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) en initialisant la zone de liste déroulante. L’application charge les bitmaps utilisées pour la zone de liste déroulante owner-drawn, puis appelle la fonction définie par l’application `InitGroupList` pour initialiser la zone de liste déroulante. Il sélectionne également le premier élément de liste dans la zone de liste déroulante, puis appelle la fonction définie par l’application `InitFoodList` pour initialiser la zone de liste.

Dans l’exemple, la zone de liste déroulante owner-drawn est une zone de liste déroulante qui contient les noms de chacun des quatre groupes de nourriture. `InitGroupList` Ajoute le nom de chaque groupe de nourriture et utilise le message [**CB \_ SETITEMDATA**](cb-setitemdata.md) pour associer un handle de bitmap à chaque élément de liste identifiant un groupe alimentaire.

La zone de liste de l’exemple contient les noms des aliments dans le groupe de nourriture sélectionné. **InitFoodList** réinitialise le contenu de la zone de liste, puis ajoute les noms de la sélection de nourriture actuelle dans la zone de liste déroulante groupe de nourriture actuel.


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



Lorsqu’il reçoit le message [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) , l’application supprime les bitmaps de la zone de liste déroulante owner-drawn.


```C++
case WM_DESTROY:

    // Call the application-defined function to free the bitmap resources.
    DeleteIconBitmaps();
    break;
```



### <a name="step-3-process-the-wm_measureitem-message"></a>Étape 3 : traiter le \_ message WM MEASUREITEM.

Une zone de liste déroulante owner-drawn envoie le message [**WM \_ MEASUREITEM**](wm-measureitem.md) à sa procédure de boîte de dialogue ou de fenêtre parente afin que l’application puisse définir les dimensions de chaque élément de liste. Étant donné que la zone de liste déroulante exemple a le style [**CBS \_ OWNERDRAWFIXED**](combo-box-styles.md) , le système envoie le message **WM \_ MEASUREITEM** une seule fois. Les zones de liste déroulante avec le style [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) envoient un message **WM \_ MEASUREITEM** pour chaque élément de liste.

Le paramètre *lParam* est un pointeur vers une structure [**measureitemstruct,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) qui identifie l’élément de contrôle et de liste. Elle contient également les dimensions par défaut de l’élément de liste. L’exemple modifie le membre de la structure **ItemHeight** pour garantir que les éléments de liste sont suffisamment hauts pour accueillir les bitmaps de groupe de nourriture.


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



### <a name="step-4-process-the-wm_drawitem-message"></a>Étape 4 : traiter le \_ message WM DRAWITEM.

Une zone de liste déroulante owner-drawn envoie le message [**WM \_ DRAWITEM**](wm-drawitem.md) à la procédure de la fenêtre ou de la boîte de dialogue parente chaque fois que l’application doit repeindre un élément de liste. Le paramètre *lParam* est un pointeur vers une structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) qui identifie l’élément de contrôle et de liste. Elle contient également les informations nécessaires pour peindre l’élément.

L’exemple d’application affiche le texte de l’élément de liste et le bitmap associé au groupe Food. Si l’élément a le focus, il dessine également un rectangle de focus. Avant d’afficher le texte, l’exemple définit les couleurs de premier plan et d’arrière-plan, en fonction de l’élément sélectionné. Étant donné que la zone de liste déroulante a le style [**CBS \_ HASSTRINGS**](combo-box-styles.md) , la zone de liste déroulante conserve le texte de chaque élément de liste qui peut être extrait à l’aide du message [**CB \_ GETLBTEXT**](cb-getlbtext.md) .

Les bitmaps utilisées pour l’élément de liste dépendent du groupe Food. `InitGroupList` utilise le message [**CB \_ SETITEMDATA**](cb-setitemdata.md) pour associer un handle de bitmap à chaque élément de liste. La procédure de fenêtre récupère le handle de bitmap à partir du membre **ItemData** de la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) . Le système utilise deux bitmaps pour chaque symbole de groupe alimentaire : un bitmap monochrome avec l’opération SRCAND raster pour effacer la zone irrégulière derrière l’image, et une image bitmap de couleur avec l’opération Raster SRCPAINT pour peindre l’image.


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



### <a name="step-5-process-the-wm_command-message"></a>Étape 5 : traiter le \_ message de commande WM.

Lorsqu’un événement se produit dans un contrôle de boîte de dialogue, le contrôle notifie la procédure de boîte de dialogue au moyen d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) . L’exemple traite les messages de notification de la zone de liste déroulante, la zone de liste et le bouton **OK** . L’identificateur de contrôle se trouve dans le mot de poids faible de *wParam* et le code de notification se trouve dans le mot de poids fort de *wParam*.

Si l’identificateur de contrôle est IDCOMBO, un événement s’est produit dans la zone de liste déroulante. En réponse, la procédure de boîte de dialogue ignore tous les autres événements de zone de liste modifiable, à l’exception de [**CBN \_ SELENDOK**](cbn-selendok.md), qui indique qu’une sélection a été effectuée, la zone de liste déroulante a été fermée et les modifications apportées doivent être acceptées. La procédure de boîte de dialogue appelle `InitFoodList` pour réinitialiser le contenu de la zone de liste et ajouter les noms des sélections actuelles dans la zone de liste déroulante.

Si l’identificateur de contrôle est IDLIST, un événement s’est produit dans la zone de liste. La procédure de la boîte de dialogue ignore tous les événements de zone de liste, à l’exception de [**LBN \_ DBLCLK**](lbn-dblclk.md), qui indique que l’utilisateur a double-cliqué sur un élément de liste. Cet événement est traité de la même façon que si un bouton **OK** avait été choisi.

Si l’identificateur de contrôle est IDOK, l’utilisateur a choisi le bouton **OK** . En réponse, la procédure de boîte de dialogue insère le nom des aliments sélectionnés dans le contrôle d’édition multiligne de l’application, puis appelle la fonction [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) pour fermer la boîte de dialogue.

Si l’identificateur de contrôle est IDCANCEL, l’utilisateur a cliqué sur le bouton **Annuler** . En réponse, la procédure de boîte de dialogue appelle [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) pour fermer la boîte de dialogue.


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



## <a name="complete-example"></a>Exemple complet

Voici la procédure de la boîte de dialogue et les fonctions de prise en charge pour la boîte de dialogue **repas carrés** .


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


## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de zones de liste déroulante](using-combo-boxes.md)
</dt> </dl>

 

 