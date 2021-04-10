---
title: Comment créer un bouton
description: Pour créer des boutons de manière dynamique, vous utilisez la fonction CreateWindow ou CreateWindowEx. Cette rubrique montre comment utiliser la fonction CreateWindow pour créer un bouton de commande par défaut.
ms.assetid: A8C56D09-90A3-4C70-9907-61390521D1DA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dadc53f91f773e5fce9e29bdf1ae50cc59bfdfd
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104032120"
---
# <a name="how-to-create-a-button"></a><span data-ttu-id="67618-104">Comment créer un bouton</span><span class="sxs-lookup"><span data-stu-id="67618-104">How to Create a Button</span></span>

<span data-ttu-id="67618-105">Pour créer des boutons de manière dynamique, vous utilisez la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="67618-105">To create buttons dynamically, you use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="67618-106">Cette rubrique montre comment utiliser la fonction **CreateWindow** pour créer un bouton de commande par défaut.</span><span class="sxs-lookup"><span data-stu-id="67618-106">This topic demonstrates how to use the **CreateWindow** function to create a default push button.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="67618-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="67618-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="67618-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="67618-108">Technologies</span></span>

-   [<span data-ttu-id="67618-109">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="67618-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="67618-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="67618-110">Prerequisites</span></span>

-   <span data-ttu-id="67618-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="67618-111">C/C++</span></span>
-   <span data-ttu-id="67618-112">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="67618-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="67618-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="67618-113">Instructions</span></span>


<span data-ttu-id="67618-114">Utilisez la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) pour créer un contrôle bouton.</span><span class="sxs-lookup"><span data-stu-id="67618-114">Use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function to create a button control.</span></span>

<span data-ttu-id="67618-115">Dans l’exemple C++ suivant, le paramètre *m \_ HWND* est le handle de la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="67618-115">In the following C++ example, the *m\_hwnd* parameter is the handle to the parent window.</span></span> <span data-ttu-id="67618-116">Le style [**BS \_ DEFPUSHBUTTON**](button-styles.md) spécifie qu’un bouton de commande par défaut doit être créé.</span><span class="sxs-lookup"><span data-stu-id="67618-116">The [**BS\_DEFPUSHBUTTON**](button-styles.md) style specifies that a default push button should be created.</span></span> <span data-ttu-id="67618-117">Notez que les valeurs de taille et de position doivent être spécifiées car l’utilisation de **\_ usedefault en PV** pour un bouton définit les valeurs sur zéro.</span><span class="sxs-lookup"><span data-stu-id="67618-117">Note that the size and position values must be specified because using **CW\_USEDEFAULT** for a button sets the values to zero.</span></span>


```C++
HWND hwndButton = CreateWindow( 
    L"BUTTON",  // Predefined class; Unicode assumed 
    L"OK",      // Button text 
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_DEFPUSHBUTTON,  // Styles 
    10,         // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu.
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed.
```



## <a name="related-topics"></a><span data-ttu-id="67618-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="67618-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67618-119">À propos des boutons</span><span class="sxs-lookup"><span data-stu-id="67618-119">About Buttons</span></span>](about-buttons.md)
</dt> <dt>

[<span data-ttu-id="67618-120">Référence du contrôle Button</span><span class="sxs-lookup"><span data-stu-id="67618-120">Button Control Reference</span></span>](bumper-button-button-control-reference.md)
</dt> <dt>

[<span data-ttu-id="67618-121">Utilisation des boutons</span><span class="sxs-lookup"><span data-stu-id="67618-121">Using Buttons</span></span>](using-buttons.md)
</dt> <dt>

[<span data-ttu-id="67618-122">Button</span><span class="sxs-lookup"><span data-stu-id="67618-122">Button</span></span>](buttons.md)
</dt> </dl>

 

 