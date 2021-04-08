---
title: Comment créer une interface clavier pour les barres de défilement standard
description: Bien qu’un contrôle de barre de défilement fournisse une interface clavier intégrée, aucune barre de défilement standard ne le fait.
ms.assetid: 249D0077-6E61-479A-91D5-A4BD9752B82E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b739638d95d9f3e530718f8e9b9e6168069420
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842777"
---
# <a name="how-to-create-a-keyboard-interface-for-standard-scroll-bars"></a><span data-ttu-id="2c321-103">Comment créer une interface clavier pour les barres de défilement standard</span><span class="sxs-lookup"><span data-stu-id="2c321-103">How to Create a Keyboard Interface for Standard Scroll Bars</span></span>

<span data-ttu-id="2c321-104">Bien qu’un contrôle de barre de défilement fournisse une interface clavier intégrée, aucune barre de défilement standard ne le fait.</span><span class="sxs-lookup"><span data-stu-id="2c321-104">Although a scroll bar control provides a built-in keyboard interface, a standard scroll bar does not.</span></span> <span data-ttu-id="2c321-105">Pour implémenter une interface clavier pour une barre de défilement standard, une procédure de fenêtre doit traiter le message KeyOut [**WM \_**](/windows/desktop/inputdev/wm-keydown) et examiner le code de la touche virtuelle spécifié par le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="2c321-105">To implement a keyboard interface for a standard scroll bar, a window procedure must process the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message and examine the virtual-key code specified by the *wParam* parameter.</span></span> <span data-ttu-id="2c321-106">Si le code de la touche virtuelle correspond à une touche de direction, la procédure de fenêtre s’envoie un message [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) avec le mot de poids faible du paramètre *wParam* défini sur le code de requête de la barre de défilement appropriée.</span><span class="sxs-lookup"><span data-stu-id="2c321-106">If the virtual-key code corresponds to an arrow key, the window procedure sends itself a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the low-order word of the *wParam* parameter set to the appropriate scroll bar request code.</span></span>

<span data-ttu-id="2c321-107">Par exemple, quand l’utilisateur appuie sur la touche haut, la procédure de fenêtre reçoit un [**message \_ WM**](/windows/desktop/inputdev/wm-keydown) KeyOut avec *wParam* égal à VK \_ up.</span><span class="sxs-lookup"><span data-stu-id="2c321-107">For example, when the user presses the UP arrow key, the window procedure receives a [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message with *wParam* equal to VK\_UP.</span></span> <span data-ttu-id="2c321-108">En réponse, la procédure de fenêtre s’envoie lui-même un message [**WM \_ VSCROLL**](wm-vscroll.md) avec le mot de poids faible de *wParam* défini sur le code de demande de la \_ programmation SB.</span><span class="sxs-lookup"><span data-stu-id="2c321-108">In response, the window procedure sends itself a [**WM\_VSCROLL**](wm-vscroll.md) message with the low-order word of *wParam* set to the SB\_LINEUP request code.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="2c321-109">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="2c321-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="2c321-110">Technologies</span><span class="sxs-lookup"><span data-stu-id="2c321-110">Technologies</span></span>

-   [<span data-ttu-id="2c321-111">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="2c321-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="2c321-112">Prérequis</span><span class="sxs-lookup"><span data-stu-id="2c321-112">Prerequisites</span></span>

-   <span data-ttu-id="2c321-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="2c321-113">C/C++</span></span>
-   <span data-ttu-id="2c321-114">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="2c321-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="2c321-115">Instructions</span><span class="sxs-lookup"><span data-stu-id="2c321-115">Instructions</span></span>

### <a name="create-a-keyboard-interface-for-a-standard-scroll-bar"></a><span data-ttu-id="2c321-116">Créer une interface clavier pour une barre de défilement standard</span><span class="sxs-lookup"><span data-stu-id="2c321-116">Create a Keyboard Interface for a Standard Scroll Bar</span></span>

<span data-ttu-id="2c321-117">L’exemple de code suivant montre comment inclure une interface clavier pour une barre de défilement standard.</span><span class="sxs-lookup"><span data-stu-id="2c321-117">The following code example demonstrates how to include a keyboard interface for a standard scroll bar.</span></span>


```C++
    case WM_KEYDOWN: 
    {
        WORD wScrollNotify = 0xFFFF;

        switch (wParam) 
        { 
            case VK_UP: 
                wScrollNotify = SB_LINEUP; 
                break; 
 
            case VK_PRIOR: 
                wScrollNotify = SB_PAGEUP; 
                break; 
 
            case VK_NEXT: 
                wScrollNotify = SB_PAGEDOWN; 
                break; 
 
            case VK_DOWN: 
                wScrollNotify = SB_LINEDOWN; 
                break; 
 
            case VK_HOME: 
                wScrollNotify = SB_TOP; 
                break; 
 
            case VK_END: 
                wScrollNotify = SB_BOTTOM; 
                break; 
        } 
 
        if (wScrollNotify != -1) 
            SendMessage(hwnd, WM_VSCROLL, MAKELONG(wScrollNotify, 0), 0L); 
 
        break; 
    }
```



## <a name="related-topics"></a><span data-ttu-id="2c321-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2c321-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c321-119">Utilisation des barres de défilement</span><span class="sxs-lookup"><span data-stu-id="2c321-119">Using Scroll Bars</span></span>](using-scroll-bars.md)
</dt> <dt>

<span data-ttu-id="2c321-120">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="2c321-120">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 