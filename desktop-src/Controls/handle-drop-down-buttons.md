---
title: Comment gérer les boutons déroulants
description: Un bouton déroulant peut présenter aux utilisateurs une liste d’options.
ms.assetid: 2D908D4B-AA8B-4DEF-B656-C37B673ABB4D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d6f59bfa888d346e196e13ce030d1473a07f0f
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103724271"
---
# <a name="how-to-handle-drop-down-buttons"></a><span data-ttu-id="a8d9f-103">Comment gérer les boutons déroulants</span><span class="sxs-lookup"><span data-stu-id="a8d9f-103">How to Handle Drop-down Buttons</span></span>

<span data-ttu-id="a8d9f-104">Un bouton déroulant peut présenter aux utilisateurs une liste d’options.</span><span class="sxs-lookup"><span data-stu-id="a8d9f-104">A drop-down button can present users with a list of options.</span></span> <span data-ttu-id="a8d9f-105">Pour créer ce style de bouton, spécifiez le style de [**\_ liste déroulante BTNS**](toolbar-control-and-button-styles.md) (également appelé [**\_ liste**](toolbar-control-and-button-styles.md) déroulante TBSTYLE pour la compatibilité avec les versions précédentes des contrôles communs).</span><span class="sxs-lookup"><span data-stu-id="a8d9f-105">To create this style of button, specify the [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style (also called [**TBSTYLE\_DROPDOWN**](toolbar-control-and-button-styles.md) for compatibility with previous versions of the common controls).</span></span> <span data-ttu-id="a8d9f-106">Pour afficher un bouton déroulant avec une flèche, vous devez également définir le style de barre d’outils [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) en envoyant un message [**to \_ SETEXTENDEDSTYLE**](tb-setextendedstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="a8d9f-106">To show a drop-down button with an arrow, you must also set the [**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) toolbar style by sending a [**TB\_SETEXTENDEDSTYLE**](tb-setextendedstyle.md) message.</span></span>

<span data-ttu-id="a8d9f-107">L’illustration suivante montre un bouton déroulant « ouvrir » avec le menu contextuel ouvert et affichant une liste de fichiers.</span><span class="sxs-lookup"><span data-stu-id="a8d9f-107">The following illustration shows a drop-down "Open" button with the context menu open and showing a list of files.</span></span> <span data-ttu-id="a8d9f-108">Dans cet exemple, la barre d’outils a le style [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a8d9f-108">In this example, the toolbar has the [**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) style.</span></span>

![capture d’écran d’une boîte de dialogue avec trois éléments de barre d’outils représentés par des icônes ; l’un contient une flèche de déroulement développée et un menu contextuel à trois éléments.](images/tb-dropdown.png)

<span data-ttu-id="a8d9f-110">L’illustration suivante montre la même barre d’outils, cette fois sans le style [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a8d9f-110">The following illustration shows the same toolbar, this time without the [**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) style.</span></span>

![capture d’écran d’une boîte de dialogue précédente, mais l’icône avec le menu contextuel n’a pas de flèche déroulante](images/tb-dropdown2.png)

<span data-ttu-id="a8d9f-112">Quand les utilisateurs cliquent sur un bouton de barre d’outils qui utilise le style de [**\_ liste déroulante BTNS**](toolbar-control-and-button-styles.md) , le contrôle ToolBar envoie à la fenêtre parente un code de notification de [ \_ liste déroulante TBN](tbn-dropdown.md) .</span><span class="sxs-lookup"><span data-stu-id="a8d9f-112">When users click a toolbar button that uses the [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style, the toolbar control sends its parent window a [TBN\_DROPDOWN](tbn-dropdown.md) notification code.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a8d9f-113">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="a8d9f-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a8d9f-114">Technologies</span><span class="sxs-lookup"><span data-stu-id="a8d9f-114">Technologies</span></span>

-   [<span data-ttu-id="a8d9f-115">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="a8d9f-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a8d9f-116">Prérequis</span><span class="sxs-lookup"><span data-stu-id="a8d9f-116">Prerequisites</span></span>

-   <span data-ttu-id="a8d9f-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="a8d9f-117">C/C++</span></span>
-   <span data-ttu-id="a8d9f-118">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="a8d9f-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a8d9f-119">Instructions</span><span class="sxs-lookup"><span data-stu-id="a8d9f-119">Instructions</span></span>

### <a name="handle-a-drop-down-button"></a><span data-ttu-id="a8d9f-120">Gérer un bouton déroulant</span><span class="sxs-lookup"><span data-stu-id="a8d9f-120">Handle a Drop-down Button</span></span>

<span data-ttu-id="a8d9f-121">L’exemple de code suivant montre comment une application peut prendre en charge un bouton déroulant dans un contrôle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="a8d9f-121">The following code example demonstrates how an application can support a drop-down button in a toolbar control.</span></span>


```C++
BOOL DoNotify(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam)
{

    #define lpnm   ((LPNMHDR)lParam)
    #define lpnmTB ((LPNMTOOLBAR)lParam)

    switch(lpnm->code)
    {
        case TBN_DROPDOWN:
        {
            // Get the coordinates of the button.
            RECT rc;
            SendMessage(lpnmTB->hdr.hwndFrom, TB_GETRECT, (WPARAM)lpnmTB->iItem, (LPARAM)&rc);

            // Convert to screen coordinates.            
            MapWindowPoints(lpnmTB->hdr.hwndFrom, HWND_DESKTOP, (LPPOINT)&rc, 2);                         
        
            // Get the menu.
            HMENU hMenuLoaded = LoadMenu(g_hinst, MAKEINTRESOURCE(IDR_POPUP)); 
         
            // Get the submenu for the first menu item.
            HMENU hPopupMenu = GetSubMenu(hMenuLoaded, 0);

            // Set up the pop-up menu.
            // In case the toolbar is too close to the bottom of the screen, 
            // set rcExclude equal to the button rectangle and the menu will appear above 
            // the button, and not below it.
         
            TPMPARAMS tpm;
         
            tpm.cbSize    = sizeof(TPMPARAMS);
            tpm.rcExclude = rc;
         
            // Show the menu and wait for input. 
            // If the user selects an item, its WM_COMMAND is sent.
         
            TrackPopupMenuEx(hPopupMenu, 
                             TPM_LEFTALIGN | TPM_LEFTBUTTON | TPM_VERTICAL, 
                             rc.left, rc.bottom, g_hwndMain, &tpm);

            DestroyMenu(hMenuLoaded);
         
        return (FALSE);
      
        }
    }
   
    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="a8d9f-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a8d9f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8d9f-123">Utilisation des contrôles ToolBar</span><span class="sxs-lookup"><span data-stu-id="a8d9f-123">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="a8d9f-124">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="a8d9f-124">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




