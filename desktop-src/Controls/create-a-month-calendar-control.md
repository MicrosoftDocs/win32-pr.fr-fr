---
title: Comment créer un contrôle Month Calendar
description: Cette rubrique montre comment créer dynamiquement un contrôle Month Calendar à l’aide de la fonction CreateWindowEx.
ms.assetid: 35ADDA85-5D7D-46F4-A637-99FEE4592B3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f3824618e9801b68eb67b13c64c638a5057481
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734916"
---
# <a name="how-to-create-a-month-calendar-control"></a><span data-ttu-id="e3f9f-103">Comment créer un contrôle Month Calendar</span><span class="sxs-lookup"><span data-stu-id="e3f9f-103">How to Create a Month Calendar Control</span></span>

<span data-ttu-id="e3f9f-104">Cette rubrique montre comment créer dynamiquement un contrôle Month Calendar à l’aide de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="e3f9f-104">This topic demonstrates how to dynamically create a month calendar control by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="e3f9f-105">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="e3f9f-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="e3f9f-106">Technologies</span><span class="sxs-lookup"><span data-stu-id="e3f9f-106">Technologies</span></span>

-   [<span data-ttu-id="e3f9f-107">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="e3f9f-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="e3f9f-108">Prérequis</span><span class="sxs-lookup"><span data-stu-id="e3f9f-108">Prerequisites</span></span>

-   <span data-ttu-id="e3f9f-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="e3f9f-109">C/C++</span></span>
-   <span data-ttu-id="e3f9f-110">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="e3f9f-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="e3f9f-111">Instructions</span><span class="sxs-lookup"><span data-stu-id="e3f9f-111">Instructions</span></span>


<span data-ttu-id="e3f9f-112">Pour créer un contrôle Month Calendar, utilisez la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , en spécifiant la [**\_ classe calendrier monthcal**](common-control-window-classes.md) comme classe de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e3f9f-112">To create a month calendar control, use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying [**MONTHCAL\_CLASS**](common-control-window-classes.md) as the window class.</span></span> <span data-ttu-id="e3f9f-113">Vous devez d’abord inscrire la classe de fenêtre en appelant la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , en spécifiant le bit des **\_ \_ classes de date ICC** dans la structure [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) qui l’accompagne.</span><span class="sxs-lookup"><span data-stu-id="e3f9f-113">You must first register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, specifying the **ICC\_DATE\_CLASSES** bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

<span data-ttu-id="e3f9f-114">L’exemple suivant montre comment créer un contrôle Month Calendar dans une boîte de dialogue non modale existante.</span><span class="sxs-lookup"><span data-stu-id="e3f9f-114">The following example demonstrates how to create a month calendar control in an existing modeless dialog box.</span></span> <span data-ttu-id="e3f9f-115">Notez que les valeurs de taille transmises à [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ne sont que des zéros.</span><span class="sxs-lookup"><span data-stu-id="e3f9f-115">Note that the size values passed to [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) are all zeros.</span></span> <span data-ttu-id="e3f9f-116">Étant donné que la taille minimale requise dépend de la police utilisée par le contrôle, l’exemple utilise la macro [**calendrier monthcal \_ GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) pour demander des informations sur la taille, puis redimensionne le contrôle en appelant [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span><span class="sxs-lookup"><span data-stu-id="e3f9f-116">Because the minimum required size depends on the font that the control uses, the example uses the [**MonthCal\_GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) macro to request size information and then resizes the control by calling [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="e3f9f-117">Si vous modifiez par la suite la police avec [**WM \_ SetFont**](/windows/desktop/winmsg/wm-setfont), les dimensions du contrôle ne changeront pas.</span><span class="sxs-lookup"><span data-stu-id="e3f9f-117">If you subsequently change the font with [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont), the dimensions of the control will not change.</span></span> <span data-ttu-id="e3f9f-118">Vous devez rappeler **calendrier monthcal \_ GetMinReqRect** et redimensionner le contrôle pour l’adapter à la nouvelle police.</span><span class="sxs-lookup"><span data-stu-id="e3f9f-118">You must call **MonthCal\_GetMinReqRect** again and resize the control to fit the new font.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="e3f9f-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e3f9f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3f9f-120">Référence du contrôle Month Calendar</span><span class="sxs-lookup"><span data-stu-id="e3f9f-120">Month Calendar Control Reference</span></span>](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[<span data-ttu-id="e3f9f-121">À propos des contrôles Month Calendar</span><span class="sxs-lookup"><span data-stu-id="e3f9f-121">About Month Calendar Controls</span></span>](month-calendar-controls.md)
</dt> <dt>

[<span data-ttu-id="e3f9f-122">Utilisation des contrôles Month Calendar</span><span class="sxs-lookup"><span data-stu-id="e3f9f-122">Using Month Calendar Controls</span></span>](using-month-calendar-controls.md)
</dt> </dl>

 

 