---
title: Comment créer un contrôle onglet dans la fenêtre principale
description: L’exemple de cette section montre comment créer un contrôle onglet et l’afficher dans la zone cliente de la fenêtre principale de l’application.
ms.assetid: 24157B8B-177B-471C-9DA0-548D09EA5F89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b7d945b01c1e6409cf795d7f42f29999830ed1272bb661a9bb13e52cd1e293
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320009"
---
# <a name="how-to-create-a-tab-control-in-the-main-window"></a>Comment créer un contrôle onglet dans la fenêtre principale

L’exemple de cette section montre comment créer un contrôle onglet et l’afficher dans la zone cliente de la fenêtre principale de l’application. L’application affiche une troisième fenêtre (un contrôle statique) dans la zone d’affichage du contrôle onglet. La fenêtre parente positionne et dimensionne le contrôle onglet et le contrôle statique lors du traitement du message de [**\_ taille WM**](/windows/desktop/winmsg/wm-size) .

Cet exemple comporte sept onglets, un pour chaque jour de la semaine. Lorsque l’utilisateur sélectionne un onglet, l’application affiche le nom du jour correspondant dans le contrôle statique.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="create-a-tab-control-in-the-main-window"></a>Créer un contrôle onglet dans la fenêtre principale

La fonction suivante crée le contrôle onglet et ajoute un onglet pour chaque jour de la semaine. Les noms des jours sont définis en tant que ressources de type chaîne, numérotés de manière consécutive à partir de \_ l’ID dimanche (défini dans le fichier d’en-tête de ressource de l’application). La fenêtre parente et le contrôle onglet doivent avoir le style de fenêtre [**WS \_ CLIPSIBLINGS**](/windows/desktop/winmsg/window-styles) . La fonction d’initialisation de l’application appelle cette fonction après la création de la fenêtre principale.


```C++
#define DAYS_IN_WEEK 7

// Creates a tab control, sized to fit the specified parent window's client
//   area, and adds some tabs. 
// Returns the handle to the tab control. 
// hwndParent - parent window (the application's main window). 
// 
HWND DoCreateTabControl(HWND hwndParent) 
{ 
    RECT rcClient; 
    INITCOMMONCONTROLSEX icex;
    HWND hwndTab; 
    TCITEM tie; 
    int i; 
    TCHAR achTemp[256];  // Temporary buffer for strings.
 
    // Initialize common controls.
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_TAB_CLASSES;
    InitCommonControlsEx(&icex);
    
    // Get the dimensions of the parent window's client area, and 
    // create a tab control child window of that size. Note that g_hInst
    // is the global instance handle.
    GetClientRect(hwndParent, &rcClient); 
    hwndTab = CreateWindow(WC_TABCONTROL, L"", 
        WS_CHILD | WS_CLIPSIBLINGS | WS_VISIBLE, 
        0, 0, rcClient.right, rcClient.bottom, 
        hwndParent, NULL, g_hInst, NULL); 
    if (hwndTab == NULL)
    { 
        return NULL; 
    }
 
    // Add tabs for each day of the week. 
    tie.mask = TCIF_TEXT | TCIF_IMAGE; 
    tie.iImage = -1; 
    tie.pszText = achTemp; 
 
    for (i = 0; i < DAYS_IN_WEEK; i++) 
    { 
        // Load the day string from the string resources. Note that
        // g_hInst is the global instance handle.
        LoadString(g_hInst, IDS_SUNDAY + i, 
                achTemp, sizeof(achTemp) / sizeof(achTemp[0])); 
        if (TabCtrl_InsertItem(hwndTab, i, &tie) == -1) 
        { 
            DestroyWindow(hwndTab); 
            return NULL; 
        } 
    } 
    return hwndTab; 
} 
```



La fonction suivante crée le contrôle statique qui réside dans la zone d’affichage du contrôle onglet. La fonction d’initialisation de l’application appelle cette fonction après la création de la fenêtre principale et du contrôle onglet.


```C++
// Creates a child window (a static control) to occupy the tab control's 
//   display area. 
// Returns the handle to the static control. 
// hwndTab - handle of the tab control. 
// 
HWND DoCreateDisplayWindow(HWND hwndTab) 
{ 
    HWND hwndStatic = CreateWindow(WC_STATIC, L"", 
        WS_CHILD | WS_VISIBLE | WS_BORDER, 
        100, 100, 100, 100,        // Position and dimensions; example only.
        hwndTab, NULL, g_hInst,    // g_hInst is the global instance handle
        NULL); 
    return hwndStatic; 
}
```



Les exemples de fonctions suivants sont appelés à partir de la procédure de fenêtre de l’application. L’application appelle la `OnSize` fonction lors du traitement du message de [**\_ taille WM**](/windows/desktop/winmsg/wm-size) pour positionner et dimensionner le contrôle onglet pour l’adapter à la zone cliente de la fenêtre principale.

Lorsqu’un onglet est sélectionné, le contrôle onglet envoie un message [**WM \_ Notify**](wm-notify.md) , en spécifiant le code de notification [TCN \_ selChange](tcn-selchange.md) . La fonction de l’application `OnNotify` traite ce code de notification en définissant le texte du contrôle statique.


```C++
// Handles the WM_SIZE message for the main window by resizing the 
//   tab control. 
// hwndTab - handle of the tab control.
// lParam - the lParam parameter of the WM_SIZE message.
//
HRESULT OnSize(HWND hwndTab, LPARAM lParam)
{
    RECT rc; 

    if (hwndTab == NULL)
        return E_INVALIDARG;

    // Resize the tab control to fit the client are of main window.
     if (!SetWindowPos(hwndTab, HWND_TOP, 0, 0, GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), SWP_SHOWWINDOW))
        return E_FAIL;

    return S_OK;
}

// Handles notifications from the tab control, as follows: 
//   TCN_SELCHANGING - always returns FALSE to allow the user to select a 
//     different tab.  
//   TCN_SELCHANGE - loads a string resource and displays it in a static 
//     control on the selected tab.
// hwndTab - handle of the tab control.
// hwndDisplay - handle of the static control. 
// lParam - the lParam parameter of the WM_NOTIFY message.
//
BOOL OnNotify(HWND hwndTab, HWND hwndDisplay, LPARAM lParam)
{
    TCHAR achTemp[256]; // temporary buffer for strings

    switch (((LPNMHDR)lParam)->code)
        {
            case TCN_SELCHANGING:
                {
                    // Return FALSE to allow the selection to change.
                    return FALSE;
                }

            case TCN_SELCHANGE:
                { 
                    int iPage = TabCtrl_GetCurSel(hwndTab); 

                    // Note that g_hInst is the global instance handle.
                    LoadString(g_hInst, IDS_SUNDAY + iPage, achTemp,
                        sizeof(achTemp) / sizeof(achTemp[0])); 
                    LRESULT result = SendMessage(hwndDisplay, WM_SETTEXT, 0,
                        (LPARAM) achTemp); 
                    break;
                } 
        }
        return TRUE;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles Tab](using-tab-controls.md)
</dt> <dt>

[Windows démonstration des contrôles communs (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 