---
title: Comment créer une boîte de dialogue à onglets
description: L’exemple de cette section montre comment créer une boîte de dialogue qui utilise des onglets pour fournir plusieurs pages de contrôles.
ms.assetid: DBF7FBDF-AADC-45CE-833E-F893C1129FC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0b84a8a77d18903ddbdb29687cc2b97b88872b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195740"
---
# <a name="how-to-create-a-tabbed-dialog-box"></a>Comment créer une boîte de dialogue à onglets

L’exemple de cette section montre comment créer une boîte de dialogue qui utilise des onglets pour fournir plusieurs pages de contrôles. La boîte de dialogue principale est une boîte de dialogue modale. Chaque page de contrôles est définie par un modèle de boîte de dialogue qui a le style [**WS \_ Child**](/windows/desktop/winmsg/window-styles) . Lorsqu’un onglet est sélectionné, une boîte de dialogue non modale est créée pour la page entrante et la boîte de dialogue de la page sortante est détruite.

> [!Note]  
> Dans de nombreux cas, vous pouvez implémenter des boîtes de dialogue de plusieurs pages plus facilement en utilisant des feuilles de propriétés. Pour plus d’informations sur les feuilles de propriétés, consultez [à propos des feuilles de propriétés](property-sheets.md).

 

Le modèle de la boîte de dialogue principale définit simplement deux contrôles bouton. Lors du traitement du message [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) , la procédure de la boîte de dialogue crée un contrôle onglet et charge les ressources du modèle de boîte de dialogue pour chacune des boîtes de dialogue enfants.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="create-a-tabbed-dialog-box"></a>Créer une boîte de dialogue à onglets

Les informations sont enregistrées dans une structure définie par l’application appelée DLGHDR. Un pointeur vers cette structure est associé à la fenêtre de boîte de dialogue à l’aide de la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) . La structure est définie dans le fichier d’en-tête de l’application, comme suit.


```C++
#define C_PAGES 3 

typedef struct tag_dlghdr { 
    HWND hwndTab;       // tab control 
    HWND hwndDisplay;   // current child dialog box 
    RECT rcDisplay;     // display rectangle for the tab control 
    DLGTEMPLATEEX *apRes[C_PAGES]; 
} DLGHDR; 
```



La fonction suivante traite le message [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) pour la boîte de dialogue principale. La fonction alloue la `DLGHDR` structure, charge les ressources de modèle de boîte de dialogue pour les boîtes de dialogue enfants et crée le contrôle onglet.

La taille de chaque boîte de dialogue enfant est spécifiée par la structure [**DLGTEMPLATEEX**](/windows/desktop/dlgbox/dlgtemplateex) . La fonction examine la taille de chaque boîte de dialogue et utilise la macro pour le [**message \_ ADJUSTRECT TCM**](tcm-adjustrect.md) pour calculer une taille appropriée pour le contrôle Tab. Elle dimensionne ensuite la boîte de dialogue et positionne les deux boutons en conséquence. Cet exemple envoie **TCM \_ ADJUSTRECT** à l’aide de la macro [**TabCtrl \_ ADJUSTRECT**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) .


```C++
// Handles the WM_INITDIALOG message for a dialog box that contains 
//   a tab control used to select among three child dialog boxes.
// Returns a result code.
// hwndDlg - handle of the dialog box.
// 
HRESULT OnTabbedDialogInit(HWND hwndDlg) 
{ 
    INITCOMMONCONTROLSEX iccex;
    DWORD dwDlgBase = GetDialogBaseUnits();
    int cxMargin = LOWORD(dwDlgBase) / 4; 
    int cyMargin = HIWORD(dwDlgBase) / 8; 

    TCITEM tie; 
    RECT rcTab; 
    HWND hwndButton; 
    RECT rcButton; 
    int i; 

    // Initialize common controls.
    iccex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    iccex.dwICC = ICC_TAB_CLASSES;
    InitCommonControlsEx(&iccex); 

    // Allocate memory for the DLGHDR structure. Remember to 
    // free this memory before the dialog box is destroyed.
    DLGHDR *pHdr = (DLGHDR *) LocalAlloc(LPTR, sizeof(DLGHDR)); 

    // Save a pointer to the DLGHDR structure in the window
    // data of the dialog box. 
    SetWindowLongPtr(hwndDlg, GWLP_USERDATA, (LONG_PTR) pHdr); 
 
    // Create the tab control. Note that g_hInst is a global 
    // instance handle. 
    pHdr->hwndTab = CreateWindow( 
        WC_TABCONTROL, L"", 
        WS_CHILD | WS_CLIPSIBLINGS | WS_VISIBLE, 
        0, 0, 100, 100, 
        hwndDlg, NULL, g_hInst, NULL 
        ); 
    if (pHdr->hwndTab == NULL) 
    {
        return HRESULT_FROM_WIN32(GetLastError());
    }
 
    // Add a tab for each of the three child dialog boxes. 
    tie.mask = TCIF_TEXT | TCIF_IMAGE; 
    tie.iImage = -1; 
    tie.pszText = L"First"; 
    TabCtrl_InsertItem(pHdr->hwndTab, 0, &tie); 
    tie.pszText = L"Second"; 
    TabCtrl_InsertItem(pHdr->hwndTab, 1, &tie); 
    tie.pszText = L"Third"; 
    TabCtrl_InsertItem(pHdr->hwndTab, 2, &tie); 

    // Lock the resources for the three child dialog boxes. 
    pHdr->apRes[0] = DoLockDlgRes(MAKEINTRESOURCE(IDD_FIRSTDLG)); 
    pHdr->apRes[1] = DoLockDlgRes(MAKEINTRESOURCE(IDD_SECONDDLG)); 
    pHdr->apRes[2] = DoLockDlgRes(MAKEINTRESOURCE(IDD_THIRDDLG)); 

    // Determine a bounding rectangle that is large enough to 
    // contain the largest child dialog box. 
    SetRectEmpty(&rcTab); 
    for (i = 0; i < C_PAGES; i++) 
    { 
        if (pHdr->apRes[i]->cx > rcTab.right) 
            rcTab.right = pHdr->apRes[i]->cx; 
        if (pHdr->apRes[i]->cy > rcTab.bottom) 
            rcTab.bottom = pHdr->apRes[i]->cy; 
    }

    // Map the rectangle from dialog box units to pixels.
    MapDialogRect(hwndDlg, &rcTab);
    
    // Calculate how large to make the tab control, so 
    // the display area can accommodate all the child dialog boxes. 
    TabCtrl_AdjustRect(pHdr->hwndTab, TRUE, &rcTab); 
    OffsetRect(&rcTab, cxMargin - rcTab.left, cyMargin - rcTab.top); 
 
    // Calculate the display rectangle. 
    CopyRect(&pHdr->rcDisplay, &rcTab); 
    TabCtrl_AdjustRect(pHdr->hwndTab, FALSE, &pHdr->rcDisplay); 
 
    // Set the size and position of the tab control, buttons, 
    // and dialog box. 
    SetWindowPos(pHdr->hwndTab, NULL, rcTab.left, rcTab.top, 
            rcTab.right - rcTab.left, rcTab.bottom - rcTab.top, 
            SWP_NOZORDER); 
 
    // Move the first button below the tab control. 
    hwndButton = GetDlgItem(hwndDlg, IDB_CLOSE); 
    SetWindowPos(hwndButton, NULL, 
            rcTab.left, rcTab.bottom + cyMargin, 0, 0, 
            SWP_NOSIZE | SWP_NOZORDER); 
 
    // Determine the size of the button. 
    GetWindowRect(hwndButton, &rcButton); 
    rcButton.right -= rcButton.left; 
    rcButton.bottom -= rcButton.top; 
 
    // Move the second button to the right of the first. 
    hwndButton = GetDlgItem(hwndDlg, IDB_TEST); 
    SetWindowPos(hwndButton, NULL, 
        rcTab.left + rcButton.right + cxMargin, 
        rcTab.bottom + cyMargin, 0, 0, 
        SWP_NOSIZE | SWP_NOZORDER); 
 
    // Size the dialog box. 
    SetWindowPos(hwndDlg, NULL, 0, 0, 
        rcTab.right + cyMargin + (2 * GetSystemMetrics(SM_CXDLGFRAME)), 
        rcTab.bottom + rcButton.bottom + (2 * cyMargin)
        + (2 * GetSystemMetrics(SM_CYDLGFRAME)) 
        + GetSystemMetrics(SM_CYCAPTION), 
        SWP_NOMOVE | SWP_NOZORDER); 
 
    // Simulate selection of the first item. 
    OnSelChanged(hwndDlg); 

    return S_OK;
} 

// Loads and locks a dialog box template resource. 
// Returns the address of the locked dialog box template resource. 
// lpszResName - name of the resource. 
//
DLGTEMPLATEEX* DoLockDlgRes(LPCTSTR lpszResName) 
{ 
    HRSRC hrsrc = FindResource(NULL, lpszResName, RT_DIALOG); 

    // Note that g_hInst is the global instance handle
    HGLOBAL hglb = LoadResource(g_hInst, hrsrc);  
    return (DLGTEMPLATEEX *) LockResource(hglb); 
} 
```



La fonction suivante traite le code de notification [TCN \_ selChange](tcn-selchange.md) pour la boîte de dialogue principale. La fonction détruit la boîte de dialogue de la page sortante, le cas échéant. Elle utilise ensuite la fonction [**CreateDialogIndirect**](/windows/desktop/api/winuser/nf-winuser-createdialogindirecta) pour créer une boîte de dialogue non modale pour la page entrante.


```C++
// Processes the TCN_SELCHANGE notification. 
// hwndDlg - handle to the parent dialog box. 
//
VOID OnSelChanged(HWND hwndDlg) 
{ 
    // Get the dialog header data.
    DLGHDR *pHdr = (DLGHDR *) GetWindowLongPtr( 
        hwndDlg, GWLP_USERDATA); 

    // Get the index of the selected tab.
    int iSel = TabCtrl_GetCurSel(pHdr->hwndTab); 
 
    // Destroy the current child dialog box, if any. 
    if (pHdr->hwndDisplay != NULL) 
        DestroyWindow(pHdr->hwndDisplay); 
 
    // Create the new child dialog box. Note that g_hInst is the
    // global instance handle.
    pHdr->hwndDisplay = CreateDialogIndirect(g_hInst, 
        (DLGTEMPLATE *)pHdr->apRes[iSel], hwndDlg, ChildDialogProc); 

    return;
} 
```



La fonction suivante traite le message [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) pour chacune des boîtes de dialogue enfants. Vous ne pouvez pas spécifier la position d’une boîte de dialogue créée à l’aide de la fonction [**CreateDialogIndirect**](/windows/desktop/api/winuser/nf-winuser-createdialogindirecta) . Cette fonction utilise la fonction [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) pour positionner la boîte de dialogue enfant dans la zone d’affichage du contrôle onglet.


```C++
// Positions the child dialog box to occupy the display area of the 
//   tab control. 
// hwndDlg - handle of the dialog box.
//
VOID WINAPI OnChildDialogInit(HWND hwndDlg) 
{ 
    HWND hwndParent = GetParent(hwndDlg);
    DLGHDR *pHdr = (DLGHDR *) GetWindowLongPtr( 
        hwndParent, GWLP_USERDATA); 
    SetWindowPos(hwndDlg, NULL, pHdr->rcDisplay.left,
        pHdr->rcDisplay.top,//-2,
        (pHdr->rcDisplay.right - pHdr->rcDisplay.left),
        (pHdr->rcDisplay.bottom - pHdr->rcDisplay.top),
        SWP_SHOWWINDOW);
        
    return;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles Tab](using-tab-controls.md)
</dt> <dt>

[Windows démonstration des contrôles communs (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 