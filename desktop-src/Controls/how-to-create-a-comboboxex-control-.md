---
title: Comment créer un contrôle ComboBoxEx
description: Cette rubrique montre comment créer un contrôle ComboBoxEx.
ms.assetid: E3D577AF-3290-431E-AA6C-1E9A9ED6448C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73989124982cb563fc008d7f3c543388cca685a5
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103941508"
---
# <a name="how-to-create-a-comboboxex-control"></a><span data-ttu-id="2c2d7-103">Comment créer un contrôle ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="2c2d7-103">How to Create a ComboBoxEx Control</span></span>

<span data-ttu-id="2c2d7-104">Cette rubrique montre comment créer un contrôle ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="2c2d7-104">This topic demonstrates how to create a ComboBoxEx control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="2c2d7-105">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="2c2d7-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="2c2d7-106">Technologies</span><span class="sxs-lookup"><span data-stu-id="2c2d7-106">Technologies</span></span>

-   [<span data-ttu-id="2c2d7-107">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="2c2d7-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="2c2d7-108">Prérequis</span><span class="sxs-lookup"><span data-stu-id="2c2d7-108">Prerequisites</span></span>

-   <span data-ttu-id="2c2d7-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="2c2d7-109">C/C++</span></span>
-   <span data-ttu-id="2c2d7-110">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="2c2d7-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="2c2d7-111">Instructions</span><span class="sxs-lookup"><span data-stu-id="2c2d7-111">Instructions</span></span>


<span data-ttu-id="2c2d7-112">Pour créer un contrôle ComboBoxEx, appelez la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , en utilisant [**WC \_ ComboBoxEx**](common-control-window-classes.md) comme classe de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="2c2d7-112">To create a ComboBoxEx control, call the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, using [**WC\_COMBOBOXEX**](common-control-window-classes.md) as the window class.</span></span> <span data-ttu-id="2c2d7-113">Vous devez d’abord inscrire la classe de fenêtre en appelant la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , tout en spécifiant le \_ bit des classes ICC USEREX \_ dans la structure [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) qui l’accompagne.</span><span class="sxs-lookup"><span data-stu-id="2c2d7-113">You must first register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, while specifying the ICC\_USEREX\_CLASSES bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

## <a name="complete-example"></a><span data-ttu-id="2c2d7-114">Exemple complet</span><span class="sxs-lookup"><span data-stu-id="2c2d7-114">Complete example</span></span>

<span data-ttu-id="2c2d7-115">La fonction définie par l’application suivante crée un contrôle ComboBoxEx avec le style de [**\_ liste déroulante CBS**](combo-box-styles.md) dans la fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="2c2d7-115">The following application-defined function creates a ComboBoxEx control with the [**CBS\_DROPDOWN**](combo-box-styles.md) style in the main window.</span></span>


```C++
// CreateComboEx - Registers the ComboBoxEx window class and creates
// a ComboBoxEx control in the client area of the main window.
//
// g_hwndMain - A handle to the main window.
// g_hinst    - A handle to the program instance.
HWND WINAPI CreateComboEx(void)
{
    HWND hwnd;
    INITCOMMONCONTROLSEX icex;

    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_USEREX_CLASSES;

    InitCommonControlsEx(&icex);

    hwnd = CreateWindowEx(0, WC_COMBOBOXEX, NULL,
                    WS_BORDER | WS_VISIBLE |
                    WS_CHILD | CBS_DROPDOWN,
                    // No size yet--resize after setting image list.
                    0,      // Vertical position of Combobox
                    0,      // Horizontal position of Combobox
                    0,      // Sets the width of Combobox
                    100,    // Sets the height of Combobox
                    g_hwndMain,
                    NULL,
                    g_hinst,
                    NULL);

    return (hwnd);
}
```



## <a name="related-topics"></a><span data-ttu-id="2c2d7-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2c2d7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c2d7-117">À propos des contrôles ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="2c2d7-117">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> <dt>

[<span data-ttu-id="2c2d7-118">Référence du contrôle ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="2c2d7-118">ComboBoxEx Control Reference</span></span>](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[<span data-ttu-id="2c2d7-119">Utilisation des contrôles ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="2c2d7-119">Using ComboBoxEx Controls</span></span>](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[<span data-ttu-id="2c2d7-120">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="2c2d7-120">ComboBoxEx</span></span>](comboboxex-control-reference.md)
</dt> </dl>

 

 