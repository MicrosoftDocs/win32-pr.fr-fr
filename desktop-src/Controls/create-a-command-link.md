---
title: Comment créer un lien de commande
description: Cette rubrique décrit une façon de créer un lien de commande.
ms.assetid: F342075B-2D3B-40E0-B657-E1C57EDC2E3A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8024a7f060a7bae3779b9ec9ebec40bd81c74bb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463818"
---
# <a name="how-to-create-a-command-link"></a><span data-ttu-id="b78c8-103">Comment créer un lien de commande</span><span class="sxs-lookup"><span data-stu-id="b78c8-103">How to Create a Command Link</span></span>

<span data-ttu-id="b78c8-104">Cette rubrique décrit une façon de créer un lien de commande.</span><span class="sxs-lookup"><span data-stu-id="b78c8-104">This topic describes one way to create a command link.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="b78c8-105">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="b78c8-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="b78c8-106">Technologies</span><span class="sxs-lookup"><span data-stu-id="b78c8-106">Technologies</span></span>

-   [<span data-ttu-id="b78c8-107">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="b78c8-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="b78c8-108">Prérequis</span><span class="sxs-lookup"><span data-stu-id="b78c8-108">Prerequisites</span></span>

-   <span data-ttu-id="b78c8-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="b78c8-109">C/C++</span></span>
-   <span data-ttu-id="b78c8-110">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="b78c8-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="b78c8-111">Instructions</span><span class="sxs-lookup"><span data-stu-id="b78c8-111">Instructions</span></span>

### <a name="step-1-create-an-instance-of-the-command-link-button"></a><span data-ttu-id="b78c8-112">Étape 1 : créer une instance du bouton lien de commande.</span><span class="sxs-lookup"><span data-stu-id="b78c8-112">Step 1: Create an instance of the command link button.</span></span>

<span data-ttu-id="b78c8-113">Dans l’exemple de code C++ suivant, le style constant [**BS \_ COMMANDLINK**](button-styles.md) spécifie le bouton sous la forme d’un bouton de lien de commande.</span><span class="sxs-lookup"><span data-stu-id="b78c8-113">In the following C++ code example, the style constant [**BS\_COMMANDLINK**](button-styles.md) specifies the button as a command link button.</span></span>


```C++
HWND hwndCommandLink = CreateWindow(
    L"BUTTON",  // Predefined class; Unicode assumed
    L"",        // Text will be defined later
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_COMMANDLINK,  // Styles
    200,        // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed
```



### <a name="step-2-set-the-command-link-label-and-explanation-text"></a><span data-ttu-id="b78c8-114">Étape 2 : définir l’étiquette du lien de commande et le texte d’explication</span><span class="sxs-lookup"><span data-stu-id="b78c8-114">Step 2: Set the command link label and explanation text</span></span>

<span data-ttu-id="b78c8-115">Utilisez la fonction [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) pour définir l’étiquette de lien de commande et le texte supplémentaire via le message [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) et le message [**\_ SETNOTE BCM**](bcm-setnote.md) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="b78c8-115">Use the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to set the command link label and supplementary text via the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message and the [**BCM\_SETNOTE**](bcm-setnote.md) message, respectively.</span></span>


```C++
SendMessage(hwndCommandLink, WM_SETTEXT, 0, (LPARAM)L"Command link");
SendMessage(hwndCommandLink, BCM_SETNOTE, 0, (LPARAM)L"with note");
```



## <a name="related-topics"></a><span data-ttu-id="b78c8-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b78c8-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b78c8-117">À propos des boutons</span><span class="sxs-lookup"><span data-stu-id="b78c8-117">About Buttons</span></span>](about-buttons.md)
</dt> <dt>

[<span data-ttu-id="b78c8-118">Référence du contrôle Button</span><span class="sxs-lookup"><span data-stu-id="b78c8-118">Button Control Reference</span></span>](bumper-button-button-control-reference.md)
</dt> <dt>

[<span data-ttu-id="b78c8-119">Utilisation des boutons</span><span class="sxs-lookup"><span data-stu-id="b78c8-119">Using Buttons</span></span>](using-buttons.md)
</dt> <dt>

[<span data-ttu-id="b78c8-120">Button</span><span class="sxs-lookup"><span data-stu-id="b78c8-120">Button</span></span>](buttons.md)
</dt> </dl>

 

 