---
title: Comment récupérer et définir une touche d’accès rapide
description: Cette rubrique montre comment récupérer ou définir la combinaison de touches pour un contrôle de touche d’accès rapide.
ms.assetid: F3643196-F847-4EE4-97ED-75AF52D4FF8D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d453433917c211bc787f70a5d9344f1a477858e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "106509890"
---
# <a name="how-to-retrieve-and-set-a-hot-key"></a><span data-ttu-id="bc48c-103">Comment récupérer et définir une touche d’accès rapide</span><span class="sxs-lookup"><span data-stu-id="bc48c-103">How to Retrieve and Set a Hot Key</span></span>

<span data-ttu-id="bc48c-104">Cette rubrique montre comment récupérer ou définir la combinaison de touches pour un contrôle de touche d’accès rapide.</span><span class="sxs-lookup"><span data-stu-id="bc48c-104">This topic demonstrates how to retrieve or set the key combination for a hot key control.</span></span> <span data-ttu-id="bc48c-105">Le message [**hkm \_ SETHOTKEY**](hkm-sethotkey.md) permet à une application de définir la combinaison de touches d’accès rapide pour un contrôle de touche d’accès rapide.</span><span class="sxs-lookup"><span data-stu-id="bc48c-105">The [**HKM\_SETHOTKEY**](hkm-sethotkey.md) message allows an application to set the hot key combination for a hot key control.</span></span> <span data-ttu-id="bc48c-106">Les applications utilisent le message [**hkm \_ GETHOTKEY**](hkm-gethotkey.md) pour récupérer le code de touche virtuel et les indicateurs de modificateur de la touche d’accès rapide choisie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bc48c-106">Applications use the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message to retrieve the virtual key code and modifier flags of the hot key that is chosen by the user.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="bc48c-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="bc48c-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="bc48c-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="bc48c-108">Technologies</span></span>

-   [<span data-ttu-id="bc48c-109">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="bc48c-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="bc48c-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="bc48c-110">Prerequisites</span></span>

-   <span data-ttu-id="bc48c-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="bc48c-111">C/C++</span></span>
-   <span data-ttu-id="bc48c-112">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="bc48c-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="bc48c-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="bc48c-113">Instructions</span></span>


<span data-ttu-id="bc48c-114">Utilisez le message [**hkm \_ GETHOTKEY**](hkm-gethotkey.md) pour récupérer le code de touche virtuelle et les touches de modification qui décrivent une touche d’accès rapide choisie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bc48c-114">Use the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message to retrieve the virtual key code and modifier keys that describe a hot key chosen by the user.</span></span> <span data-ttu-id="bc48c-115">Utilisez le message [**hkm \_ SETHOTKEY**](hkm-sethotkey.md) pour définir ces valeurs pour une touche d’accès rapide.</span><span class="sxs-lookup"><span data-stu-id="bc48c-115">Use the [**HKM\_SETHOTKEY**](hkm-sethotkey.md) message to set those values for a hot key.</span></span>

<span data-ttu-id="bc48c-116">Dans l’exemple de code C++ suivant, la fonction définie par l’application utilise le message [**hkm \_ GETHOTKEY**](hkm-gethotkey.md) pour récupérer une combinaison de touches à partir d’un contrôle de touche d’accès rapide, puis utilise le message [**WM \_ SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey) pour définir une touche d’accès rapide globale.</span><span class="sxs-lookup"><span data-stu-id="bc48c-116">In the following C++ code example, the application-defined function uses the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message to retrieve a key combination from a hot key control and then uses the [**WM\_SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey) message to set a global hot key.</span></span> <span data-ttu-id="bc48c-117">Notez que vous ne pouvez pas définir une touche d’accès rapide globale pour une fenêtre qui a le style de fenêtre [**\_ enfant WS**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="bc48c-117">Note that you cannot set a global hot key for a window that has the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) window style.</span></span>



```C++
// Retrieves the hot key from the hot key control and sets it as
// the hot key for the application's main window. 
//
// Parameters 
//     hwndHot  - Handle of the hot key control. 
//     hwndMain - Handle of the main window. 

BOOL WINAPI ProcessHotkey(HWND hwndHot, HWND hwndMain) 
{ 
    WORD wHotkey;  

    // Retrieve the hot key (virtual key code and modifiers). 
    wHotkey = (WORD) SendMessage(hwndHot, HKM_GETHOTKEY, 0, 0); 
    
    // Use the result as wParam for WM_SETHOTKEY. 
    SendMessage(hwndMain, WM_SETHOTKEY, wHotkey, 0); 
    return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="bc48c-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc48c-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc48c-119">Référence de contrôle de touche d’accès rapide</span><span class="sxs-lookup"><span data-stu-id="bc48c-119">Hot Key Control Reference</span></span>](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[<span data-ttu-id="bc48c-120">À propos des contrôles de touche d’accès rapide</span><span class="sxs-lookup"><span data-stu-id="bc48c-120">About Hot Key Controls</span></span>](hot-key-controls.md)
</dt> <dt>

[<span data-ttu-id="bc48c-121">Utilisation des contrôles de touche d’accès rapide</span><span class="sxs-lookup"><span data-stu-id="bc48c-121">Using Hot Key Controls</span></span>](using-hot-key-controls.md)
</dt> </dl>

 

 