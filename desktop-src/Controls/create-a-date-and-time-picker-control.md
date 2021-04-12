---
title: Comment créer un contrôle de sélecteur de date et d’heure
description: Cette rubrique montre comment créer dynamiquement un contrôle de sélecteur de date et d’heure (PAO).
ms.assetid: D4ACA939-3004-48D3-ADD9-FC5E53128BA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1253a2972b8d858a7440b3e472d5b3aa347b8175
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104199372"
---
# <a name="how-to-create-a-date-and-time-picker-control"></a><span data-ttu-id="a8cd2-103">Comment créer un contrôle de sélecteur de date et d’heure</span><span class="sxs-lookup"><span data-stu-id="a8cd2-103">How to Create a Date and Time Picker Control</span></span>

<span data-ttu-id="a8cd2-104">Cette rubrique montre comment créer dynamiquement un contrôle de sélecteur de date et d’heure (PAO).</span><span class="sxs-lookup"><span data-stu-id="a8cd2-104">This topic demonstrates how to dynamically create a date and time picker (DTP) control.</span></span> <span data-ttu-id="a8cd2-105">L’exemple de code C++ qui l’accompagne crée un contrôle PAO dans une boîte de dialogue non modale.</span><span class="sxs-lookup"><span data-stu-id="a8cd2-105">The accompanying C++ code example creates a DTP control in a modeless dialog box.</span></span> <span data-ttu-id="a8cd2-106">Elle utilise le style [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) pour permettre à l’utilisateur de simuler la désactivation de la date dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="a8cd2-106">It uses the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style to enable the user to simulate deactivation of the date within the control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a8cd2-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="a8cd2-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a8cd2-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="a8cd2-108">Technologies</span></span>

-   [<span data-ttu-id="a8cd2-109">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="a8cd2-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a8cd2-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="a8cd2-110">Prerequisites</span></span>

-   <span data-ttu-id="a8cd2-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="a8cd2-111">C/C++</span></span>
-   <span data-ttu-id="a8cd2-112">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="a8cd2-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a8cd2-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="a8cd2-113">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="a8cd2-114">Étape 1 :</span><span class="sxs-lookup"><span data-stu-id="a8cd2-114">Step 1:</span></span>

<span data-ttu-id="a8cd2-115">Inscrivez la classe de fenêtre en appelant la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) et en spécifiant le \_ bit des \_ classes de date ICC dans la structure [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) qui l’accompagne.</span><span class="sxs-lookup"><span data-stu-id="a8cd2-115">Register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function and specifying the ICC\_DATE\_CLASSES bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>


```C++
 INITCOMMONCONTROLSEX icex;

 icex.dwSize = sizeof(icex);
 icex.dwICC = ICC_DATE_CLASSES;

 InitCommonControlsEx(&icex);
```



### <a name="step-2"></a><span data-ttu-id="a8cd2-116">Étape 2 :</span><span class="sxs-lookup"><span data-stu-id="a8cd2-116">Step 2:</span></span>

<span data-ttu-id="a8cd2-117">Pour créer le contrôle PAO, utilisez la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="a8cd2-117">To create the DTP control, use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="a8cd2-118">Spécifiez la [**\_ classe DATETIMEPICK**](common-control-window-classes.md) comme classe de fenêtre et transmettez le descripteur à la boîte de dialogue parent.</span><span class="sxs-lookup"><span data-stu-id="a8cd2-118">Specify [**DATETIMEPICK\_CLASS**](common-control-window-classes.md) as the window class, and pass the handle to the parent dialog box.</span></span>

<span data-ttu-id="a8cd2-119">L’exemple de code C++ suivant utilise la fonction [**createDialog**](/windows/desktop/api/winuser/nf-winuser-createdialoga) pour créer une boîte de dialogue non modale.</span><span class="sxs-lookup"><span data-stu-id="a8cd2-119">The following C++ code example uses the [**CreateDialog**](/windows/desktop/api/winuser/nf-winuser-createdialoga) function to create a modeless dialog box.</span></span> <span data-ttu-id="a8cd2-120">Il appelle ensuite **CreateWindowEx** pour créer le contrôle de PAO.</span><span class="sxs-lookup"><span data-stu-id="a8cd2-120">It then calls **CreateWindowEx** to create the DTP control.</span></span>


```C++
  hwndDlg = CreateDialog  (g_hinst,
                           MAKEINTRESOURCE(IDD_DIALOG1),
                           hwndMain,
                           DlgProc);

  if(hwndDlg)
      hwndDP = CreateWindowEx(0,
                           DATETIMEPICK_CLASS,
                           TEXT("DateTime"),
                           WS_BORDER|WS_CHILD|WS_VISIBLE|DTS_SHOWNONE,
                           20,50,220,20,
                           hwndDlg,
                           NULL,
                           g_hinst,
                           NULL);
```



## <a name="complete-example"></a><span data-ttu-id="a8cd2-121">Exemple complet</span><span class="sxs-lookup"><span data-stu-id="a8cd2-121">Complete example</span></span>


```C++
//  CreateDatePick creates a DTP control within a dialog box.
//  Returns the handle to the new DTP control if successful, or NULL 
//  otherwise.
// 
//    hwndMain - The handle to the main window.
//    g_hinst  - global handle to the program instance.

HWND WINAPI CreateDatePick(HWND hwndMain)
{
    HWND hwndDP = NULL;
    HWND hwndDlg = NULL;

    INITCOMMONCONTROLSEX icex;

    icex.dwSize = sizeof(icex);
    icex.dwICC = ICC_DATE_CLASSES;

    InitCommonControlsEx(&icex);

    hwndDlg = CreateDialog  (g_hinst,
                             MAKEINTRESOURCE(IDD_DIALOG1),
                             hwndMain,
                             DlgProc);

    if(hwndDlg)
        hwndDP = CreateWindowEx(0,
                             DATETIMEPICK_CLASS,
                             TEXT("DateTime"),
                             WS_BORDER|WS_CHILD|WS_VISIBLE|DTS_SHOWNONE,
                             20,50,220,20,
                             hwndDlg,
                             NULL,
                             g_hinst,
                             NULL);

    return (hwndDP);
}

```



## <a name="related-topics"></a><span data-ttu-id="a8cd2-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a8cd2-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8cd2-123">Utilisation des contrôles de sélecteur de date et heure</span><span class="sxs-lookup"><span data-stu-id="a8cd2-123">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="a8cd2-124">Référence de contrôle de sélecteur de date et heure</span><span class="sxs-lookup"><span data-stu-id="a8cd2-124">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="a8cd2-125">Sélecteur de date et heure</span><span class="sxs-lookup"><span data-stu-id="a8cd2-125">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 