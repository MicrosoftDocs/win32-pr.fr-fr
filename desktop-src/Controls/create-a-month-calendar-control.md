---
title: Comment créer un contrôle Month Calendar
description: Cette rubrique montre comment créer dynamiquement un contrôle Month Calendar à l’aide de la fonction CreateWindowEx.
ms.assetid: 35ADDA85-5D7D-46F4-A637-99FEE4592B3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f3824618e9801b68eb67b13c64c638a5057481
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999384"
---
# <a name="how-to-create-a-month-calendar-control"></a>Comment créer un contrôle Month Calendar

Cette rubrique montre comment créer dynamiquement un contrôle Month Calendar à l’aide de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions


Pour créer un contrôle Month Calendar, utilisez la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , en spécifiant la [**\_ classe calendrier monthcal**](common-control-window-classes.md) comme classe de fenêtre. Vous devez d’abord inscrire la classe de fenêtre en appelant la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , en spécifiant le bit des **\_ \_ classes de date ICC** dans la structure [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) qui l’accompagne.

L’exemple suivant montre comment créer un contrôle Month Calendar dans une boîte de dialogue non modale existante. Notez que les valeurs de taille transmises à [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ne sont que des zéros. Étant donné que la taille minimale requise dépend de la police utilisée par le contrôle, l’exemple utilise la macro [**calendrier monthcal \_ GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) pour demander des informations sur la taille, puis redimensionne le contrôle en appelant [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos). Si vous modifiez par la suite la police avec [**WM \_ SetFont**](/windows/desktop/winmsg/wm-setfont), les dimensions du contrôle ne changeront pas. Vous devez rappeler **calendrier monthcal \_ GetMinReqRect** et redimensionner le contrôle pour l’adapter à la nouvelle police.



```C++
// Child window identifier of the month calendar.
#define IDC_MONTHCAL 101

// Symbols used by SetWindowPos function (arbitrary values).
#define LEFT 35
#define TOP  40

// Description:
//   Creates a month calendar control in a dialog box.  
// Parameters:
//   hwndOwner - handle of the owner window.
// Nonlocal variables:
//   MonthCalDlgProc - window procedure of the dialog box that 
//     contains the month calendar.
//   g_hInst - global instance handle.
//
HRESULT CreateMonthCalDialog(HWND hwndOwner)
{
    RECT rc;
    INITCOMMONCONTROLSEX icex;
    HWND hwndDlg = NULL;
    HWND hwndMonthCal = NULL;

    // Return an error code if the owner handle is invalid.
    if (hwndOwner == NULL)
        return E_INVALIDARG;

    // Load the window class.
    icex.dwSize = sizeof(icex);
    icex.dwICC  = ICC_DATE_CLASSES;
    InitCommonControlsEx(&icex);

    // Create a modeless dialog box to hold the control.
    hwndDlg = CreateDialog(g_hInst,
                    MAKEINTRESOURCE(IDD_DATE_PICKER),
                    hwndOwner,
                    MonthCalDlgProc);
   
    // Return if creating the dialog box failed. 
    if (hwndDlg == NULL)
        return HRESULT_FROM_WIN32(GetLastError()); 
                        
    // Create the month calendar.
    hwndMonthCal  = CreateWindowEx(0,
                    MONTHCAL_CLASS,
                    L"",
                    WS_BORDER | WS_CHILD | WS_VISIBLE | MCS_DAYSTATE,
                    0,0,0,0, // resize it later
                    hwndDlg,
                    (HMENU) IDC_MONTHCAL,
                    g_hInst,
                    NULL);

    // Return if creating the month calendar failed. 
    if (hwndMonthCal == NULL)
        return HRESULT_FROM_WIN32(GetLastError()); 
                     
    // Get the size required to show an entire month.
    MonthCal_GetMinReqRect(hwndMonthCal, &rc);

    // Resize the control now that the size values have been obtained.
    SetWindowPos(hwndMonthCal, NULL, LEFT, TOP, 
        rc.right, rc.bottom, SWP_NOZORDER);

    // Set the calendar to the annual view.
    MonthCal_SetCurrentView(hwndMonthCal, MCMV_YEAR);

    // Make the window visible.
    ShowWindow(hwndDlg, SW_SHOW);

    return S_OK;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence du contrôle Month Calendar](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[À propos des contrôles Month Calendar](month-calendar-controls.md)
</dt> <dt>

[Utilisation des contrôles Month Calendar](using-month-calendar-controls.md)
</dt> </dl>

 

 