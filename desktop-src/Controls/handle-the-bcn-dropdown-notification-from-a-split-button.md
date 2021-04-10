---
title: Gérer les notifications de BCN_DROPDOWN à partir de SplitButtons
description: Cette rubrique décrit une manière possible de répondre à la \_ notification de liste déroulante BCN dans une procédure de dialogue.
ms.assetid: 847DD645-AE29-4F62-BC32-F235BA409E1E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a368dd28c5347f438feff75fbddb129a420caae7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102444"
---
# <a name="how-to-handle-the-bcn_dropdown-notification-from-a-split-button"></a><span data-ttu-id="ca0b8-103">Gestion \_ de la notification de liste déroulante BCN à partir d’un bouton partagé</span><span class="sxs-lookup"><span data-stu-id="ca0b8-103">How to Handle the BCN\_DROPDOWN Notification from a Split Button</span></span>

<span data-ttu-id="ca0b8-104">Cette rubrique décrit une manière possible de répondre à la notification de [ \_ liste déroulante BCN](bcn-dropdown.md) dans une procédure de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ca0b8-104">This topic describes one possible way of responding to the [BCN\_DROPDOWN](bcn-dropdown.md) notification in a dialog procedure.</span></span>

<span data-ttu-id="ca0b8-105">L’application C++ récupère les coordonnées clientes du bouton à partir de l’en-tête de notification et les convertit en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="ca0b8-105">The C++ application retrieves the client coordinates of the button from the notification header and converts them to screen coordinates.</span></span> <span data-ttu-id="ca0b8-106">Il crée ensuite un menu contextuel et l’affiche en bas du bouton.</span><span class="sxs-lookup"><span data-stu-id="ca0b8-106">It then creates a popup menu and displays it at the bottom of the button.</span></span> <span data-ttu-id="ca0b8-107">Pour que l’exemple reste simple, les raccourcis clavier ne sont pas implémentés pour le menu.</span><span class="sxs-lookup"><span data-stu-id="ca0b8-107">To keep the example simple, keyboard shortcuts are not implemented for the menu.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ca0b8-108">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="ca0b8-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ca0b8-109">Technologies</span><span class="sxs-lookup"><span data-stu-id="ca0b8-109">Technologies</span></span>

-   [<span data-ttu-id="ca0b8-110">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="ca0b8-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ca0b8-111">Prérequis</span><span class="sxs-lookup"><span data-stu-id="ca0b8-111">Prerequisites</span></span>

-   <span data-ttu-id="ca0b8-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="ca0b8-112">C/C++</span></span>
-   <span data-ttu-id="ca0b8-113">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="ca0b8-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ca0b8-114">Instructions</span><span class="sxs-lookup"><span data-stu-id="ca0b8-114">Instructions</span></span>

### <a name="step-1-wait-for-the-bcn_dropdown-notification"></a><span data-ttu-id="ca0b8-115">Étape 1 : attendez la notification de la *\_ liste déroulante BCN* .</span><span class="sxs-lookup"><span data-stu-id="ca0b8-115">Step 1: Wait for the *BCN\_DROPDOWN* notification.</span></span>


```C++
case BCN_DROPDOWN:
{
    NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
    if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
    {
```



### <a name="step-2-get-the-screen-coordinates-of-the-button"></a><span data-ttu-id="ca0b8-116">Étape 2 : obtenir les coordonnées d’écran du bouton.</span><span class="sxs-lookup"><span data-stu-id="ca0b8-116">Step 2: Get the screen coordinates of the button.</span></span>

<span data-ttu-id="ca0b8-117">Utilisez la fonction [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) pour convertir les coordonnées de la fenêtre du bord inférieur gauche du bouton en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="ca0b8-117">Use the [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) function to convert the window coordinates of the button's lower left edge to screen coordinates.</span></span>


```C++
POINT pt;
pt.x = pDropDown->rcButton.left;
pt.y = pDropDown->rcButton.bottom;
ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
```



### <a name="step-3-create-a-menu-and-add-items"></a><span data-ttu-id="ca0b8-118">Étape 3 : créer un menu et ajouter des éléments.</span><span class="sxs-lookup"><span data-stu-id="ca0b8-118">Step 3: Create a menu and add items.</span></span>

<span data-ttu-id="ca0b8-119">Utilisez la fonction [**CreatePopupMenu**](/windows/desktop/api/winuser/nf-winuser-createpopupmenu) pour créer un menu.</span><span class="sxs-lookup"><span data-stu-id="ca0b8-119">Use the [**CreatePopupMenu**](/windows/desktop/api/winuser/nf-winuser-createpopupmenu) function to create a menu.</span></span> <span data-ttu-id="ca0b8-120">Utilisez la fonction [**AppendMenu**](/windows/desktop/menurc/u) pour ajouter des éléments au menu.</span><span class="sxs-lookup"><span data-stu-id="ca0b8-120">Use the [**AppendMenu**](/windows/desktop/menurc/u) function to add items to the menu.</span></span> <span data-ttu-id="ca0b8-121">IDC \_ MENUCOMMAND1 et IDC \_ MENUCOMMAND2 sont des constantes définies par l’application pour les commandes de menu.</span><span class="sxs-lookup"><span data-stu-id="ca0b8-121">IDC\_MENUCOMMAND1 and IDC\_MENUCOMMAND2 are application-defined constants for menu commands.</span></span>


```C++
HMENU hSplitMenu = CreatePopupMenu();
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
```



### <a name="step-4-display-the-menu"></a><span data-ttu-id="ca0b8-122">Étape 4 : afficher le menu.</span><span class="sxs-lookup"><span data-stu-id="ca0b8-122">Step 4: Display the menu.</span></span>

<span data-ttu-id="ca0b8-123">La fonction [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) affiche un menu contextuel à l’emplacement spécifié et effectue le suivi de la sélection des éléments dans le menu.</span><span class="sxs-lookup"><span data-stu-id="ca0b8-123">The [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) function displays a shortcut menu at the specified location and tracks the selection of items on the menu.</span></span>


```C++
TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
```



## <a name="complete-example"></a><span data-ttu-id="ca0b8-124">Exemple complet</span><span class="sxs-lookup"><span data-stu-id="ca0b8-124">Complete example</span></span>


```C++
case WM_NOTIFY:
    switch (((LPNMHDR)lParam)->code)
    {
        case BCN_DROPDOWN:
        {
            NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
            if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
            {

                // Get screen coordinates of the button.
                POINT pt;
                pt.x = pDropDown->rcButton.left;
                pt.y = pDropDown->rcButton.bottom;
                ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
        
                // Create a menu and add items.
                HMENU hSplitMenu = CreatePopupMenu();
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
        
                // Display the menu.
                TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
                return TRUE;
            }
            break;
        }
    }
    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="ca0b8-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ca0b8-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca0b8-126">\_Code de notification de liste déroulante BCN</span><span class="sxs-lookup"><span data-stu-id="ca0b8-126">BCN\_DROPDOWN Notification Code</span></span>](bcn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="ca0b8-127">À propos des boutons</span><span class="sxs-lookup"><span data-stu-id="ca0b8-127">About Buttons</span></span>](about-buttons.md)
</dt> <dt>

[<span data-ttu-id="ca0b8-128">Référence du contrôle Button</span><span class="sxs-lookup"><span data-stu-id="ca0b8-128">Button Control Reference</span></span>](bumper-button-button-control-reference.md)
</dt> <dt>

[<span data-ttu-id="ca0b8-129">Utilisation des boutons</span><span class="sxs-lookup"><span data-stu-id="ca0b8-129">Using Buttons</span></span>](using-buttons.md)
</dt> <dt>

[<span data-ttu-id="ca0b8-130">Button</span><span class="sxs-lookup"><span data-stu-id="ca0b8-130">Button</span></span>](buttons.md)
</dt> </dl>

 

 