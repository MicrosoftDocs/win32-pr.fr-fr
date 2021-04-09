---
title: Comment créer un contrôle de touche d’accès rapide
description: Cette rubrique montre comment créer un contrôle de touche d’accès rapide. Vous créez un contrôle de touche d’accès rapide à l’aide de la fonction CreateWindowEx, en spécifiant la classe de fenêtre de raccourci de \_ classe.
ms.assetid: A6723D4E-B8F6-4365-8FCD-99B73D2C0470
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 498005efcdfbbf001283551bbeea4906ebc854cf
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103842913"
---
# <a name="how-to-create-a-hot-key-control"></a><span data-ttu-id="81ab7-104">Comment créer un contrôle de touche d’accès rapide</span><span class="sxs-lookup"><span data-stu-id="81ab7-104">How to Create a Hot Key Control</span></span>

<span data-ttu-id="81ab7-105">Cette rubrique montre comment créer un contrôle de touche d’accès rapide.</span><span class="sxs-lookup"><span data-stu-id="81ab7-105">This topic demonstrates how to create a hot key control.</span></span> <span data-ttu-id="81ab7-106">Vous créez un contrôle de touche d’accès rapide à l’aide de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , en spécifiant la classe de fenêtre de raccourci de \_ classe.</span><span class="sxs-lookup"><span data-stu-id="81ab7-106">You create a hot key control by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the HOTKEY\_CLASS window class.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="81ab7-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="81ab7-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="81ab7-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="81ab7-108">Technologies</span></span>

-   [<span data-ttu-id="81ab7-109">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="81ab7-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="81ab7-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="81ab7-110">Prerequisites</span></span>

-   <span data-ttu-id="81ab7-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="81ab7-111">C/C++</span></span>
-   <span data-ttu-id="81ab7-112">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="81ab7-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="81ab7-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="81ab7-113">Instructions</span></span>


<span data-ttu-id="81ab7-114">Avant de créer le contrôle de touche d’accès rapide, assurez-vous que la DLL de contrôles communs est chargée.</span><span class="sxs-lookup"><span data-stu-id="81ab7-114">Before you create the hot key control, ensure that the common controls DLL is loaded.</span></span>

<span data-ttu-id="81ab7-115">Dans l’exemple de code C++ suivant, la fonction définie par l’application appelle la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) pour charger la dll de contrôle commune.</span><span class="sxs-lookup"><span data-stu-id="81ab7-115">In the following C++ code example, the application-defined function calls the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function to load the common control DLL.</span></span> <span data-ttu-id="81ab7-116">Elle appelle ensuite la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , en spécifiant la classe de fenêtre de raccourcis de la **\_ classe** , pour créer un contrôle de touche d’accès rapide.</span><span class="sxs-lookup"><span data-stu-id="81ab7-116">Then it calls the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the **HOTKEY\_CLASS** window class, to create a hot key control.</span></span> <span data-ttu-id="81ab7-117">Elle utilise les messages [**hkm \_ SETRULES**](hkm-setrules.md) et [**hkm \_ SETHOTKEY**](hkm-sethotkey.md) pour initialiser le contrôle et retourne un handle pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="81ab7-117">It uses the [**HKM\_SETRULES**](hkm-setrules.md) and [**HKM\_SETHOTKEY**](hkm-sethotkey.md) messages to initialize the control and returns a handle to the control.</span></span>

<span data-ttu-id="81ab7-118">Ce contrôle de touche d’accès rapide ne permet pas à l’utilisateur de choisir une touche d’accès rapide qui est une seule clé non modifiée, pas plus qu’il ne permet à l’utilisateur de choisir uniquement Maj et une clé.</span><span class="sxs-lookup"><span data-stu-id="81ab7-118">This hot key control does not allow the user to choose a hot key that is a single unmodified key, nor does it permit the user to choose only SHIFT and a key.</span></span> <span data-ttu-id="81ab7-119">Ces règles empêchent l’utilisateur de choisir une touche d’accès rapide qui peut être entrée accidentellement lors de la saisie de texte.</span><span class="sxs-lookup"><span data-stu-id="81ab7-119">These rules effectively prevent the user from choosing a hot key that might be entered accidentally while typing text.</span></span>



```C++
// Creates a hot key control and sets rules and default settings for it.
// 
// Returns the handle of the hot key control. 
//
// Parameter
//     hwndDlg - Handle of the parent window (dialog box). 
// 
// Global variable 
//     g_hinst - Handle of the application instance. 

extern HINSTANCE g_hinst; 

HWND WINAPI InitializeHotkey(HWND hwndDlg) 
{ 
    HWND hwndHot = NULL;
    
    // Ensure that the common control DLL is loaded. 
    INITCOMMONCONTROLSEX icex;  //declare an INITCOMMONCONTROLSEX Structure
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_HOTKEY_CLASS;   //set dwICC member to ICC_HOTKEY_CLASS    
                                     // this loads the Hot Key control class.
    InitCommonControlsEx(&icex);  
 
    hwndHot = CreateWindowEx(0,                        // no extended styles 
                             HOTKEY_CLASS,             // class name 
                             TEXT(""),                 // no title (caption) 
                             WS_CHILD | WS_VISIBLE,    // style 
                             15, 10,                   // position 
                             200, 20,                  // size 
                             hwndDlg,                  // parent window 
                             NULL,                     // uses class menu 
                             g_hinst,                  // instance 
                             NULL);                    // no WM_CREATE parameter 
 
    SetFocus(hwndHot); 
 
    // Set rules for invalid key combinations. If the user does not supply a
    // modifier key, use ALT as a modifier. If the user supplies SHIFT as a 
    // modifier key, use SHIFT + ALT instead.
    SendMessage(hwndHot, 
                HKM_SETRULES, 
                (WPARAM) HKCOMB_NONE | HKCOMB_S,   // invalid key combinations 
                MAKELPARAM(HOTKEYF_ALT, 0));       // add ALT to invalid entries 
 
    // Set CTRL + ALT + A as the default hot key for this window. 
    // 0x41 is the virtual key code for 'A'. 
    SendMessage(hwndHot, 
                HKM_SETHOTKEY, 
                MAKEWORD(0x41, HOTKEYF_CONTROL | HOTKEYF_ALT), 
                0); 
 
    return hwndHot; 
}
```



## <a name="related-topics"></a><span data-ttu-id="81ab7-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="81ab7-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81ab7-121">Référence de contrôle de touche d’accès rapide</span><span class="sxs-lookup"><span data-stu-id="81ab7-121">Hot Key Control Reference</span></span>](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[<span data-ttu-id="81ab7-122">À propos des contrôles de touche d’accès rapide</span><span class="sxs-lookup"><span data-stu-id="81ab7-122">About Hot Key Controls</span></span>](hot-key-controls.md)
</dt> <dt>

[<span data-ttu-id="81ab7-123">Utilisation des contrôles de touche d’accès rapide</span><span class="sxs-lookup"><span data-stu-id="81ab7-123">Using Hot Key Controls</span></span>](using-hot-key-controls.md)
</dt> </dl>

 

 