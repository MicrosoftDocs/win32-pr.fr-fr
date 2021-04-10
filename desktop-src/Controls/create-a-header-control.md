---
title: Comment créer un contrôle header
description: Cette rubrique montre comment créer un contrôle header et le positionner dans la zone cliente de la fenêtre parente.
ms.assetid: 094AF70C-2761-439E-A1E3-0FD04212FE87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bce9bf9d7b117f5f61766ca326b91b0d19a2c903
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104032119"
---
# <a name="how-to-create-a-header-control"></a><span data-ttu-id="05ce6-103">Comment créer un contrôle header</span><span class="sxs-lookup"><span data-stu-id="05ce6-103">How to Create a Header Control</span></span>

<span data-ttu-id="05ce6-104">Cette rubrique montre comment créer un contrôle header et le positionner dans la zone cliente de la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="05ce6-104">This topic demonstrates how to create a header control and position it within the parent window's client area.</span></span> <span data-ttu-id="05ce6-105">Vous pouvez créer un contrôle header à l’aide de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) et en spécifiant la classe de fenêtre d' [**\_ en-tête WC**](common-control-window-classes.md) et les [styles de contrôle d’en-tête](header-control-styles.md)appropriés.</span><span class="sxs-lookup"><span data-stu-id="05ce6-105">You can create a header control by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specifying the [**WC\_HEADER**](common-control-window-classes.md) window class and the appropriate [header control styles](header-control-styles.md).</span></span> <span data-ttu-id="05ce6-106">Cette classe de fenêtre est inscrite lors du chargement de la DLL de contrôles communs.</span><span class="sxs-lookup"><span data-stu-id="05ce6-106">This window class is registered when the common control DLL is loaded.</span></span> <span data-ttu-id="05ce6-107">Pour vous assurer que cette DLL est chargée, utilisez la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) .</span><span class="sxs-lookup"><span data-stu-id="05ce6-107">To ensure that this DLL is loaded, use the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="05ce6-108">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="05ce6-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="05ce6-109">Technologies</span><span class="sxs-lookup"><span data-stu-id="05ce6-109">Technologies</span></span>

-   [<span data-ttu-id="05ce6-110">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="05ce6-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="05ce6-111">Prérequis</span><span class="sxs-lookup"><span data-stu-id="05ce6-111">Prerequisites</span></span>

-   <span data-ttu-id="05ce6-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="05ce6-112">C/C++</span></span>
-   <span data-ttu-id="05ce6-113">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="05ce6-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="05ce6-114">Instructions</span><span class="sxs-lookup"><span data-stu-id="05ce6-114">Instructions</span></span>


<span data-ttu-id="05ce6-115">L’exemple de code C++ suivant appelle d’abord la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) pour charger la dll de contrôle commune.</span><span class="sxs-lookup"><span data-stu-id="05ce6-115">The following C++ code example first calls the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function to load the common control DLL.</span></span> <span data-ttu-id="05ce6-116">Il appelle ensuite la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) pour créer un contrôle header.</span><span class="sxs-lookup"><span data-stu-id="05ce6-116">It then calls the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create a header control.</span></span> <span data-ttu-id="05ce6-117">Le contrôle est initialement masqué.</span><span class="sxs-lookup"><span data-stu-id="05ce6-117">The control is initially hidden.</span></span> <span data-ttu-id="05ce6-118">Le message de [**\_ disposition HDM**](hdm-layout.md) est utilisé pour calculer la taille et la position du contrôle dans la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="05ce6-118">The [**HDM\_LAYOUT**](hdm-layout.md) message is used to calculate the size and position of the control within the parent window.</span></span> <span data-ttu-id="05ce6-119">Le contrôle est ensuite repositionné et rendu visible.</span><span class="sxs-lookup"><span data-stu-id="05ce6-119">The control is then repositioned and made visible.</span></span>



```C++
// DoCreateHeader - creates a header control that is positioned along 
//     the top of the parent window's client area. 
// Returns the handle to the header control. 
// hwndParent - handle to the parent window. 
// 
// Global variable 
//    g_hinst - handle to the application instance 
extern HINSTANCE g_hinst; 
//
// child-window identifier
int ID_HEADER;
//
HWND DoCreateHeader(HWND hwndParent) 
{ 
        HWND hwndHeader; 
        RECT rcParent; 
        HDLAYOUT hdl; 
        WINDOWPOS wp; 
 
        // Ensure that the common control DLL is loaded, and then create 
        // the header control. 
        INITCOMMONCONTROLSEX icex;  //declare an INITCOMMONCONTROLSEX Structure
        icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
        icex.dwICC = ICC_LISTVIEW_CLASSES;   //set dwICC member to ICC_LISTVIEW_CLASSES    
                                             // this loads list-view and header control classes.
    InitCommonControlsEx(&icex); 
 
        if ((hwndHeader = CreateWindowEx(0, WC_HEADER, (LPCTSTR) NULL, 
                WS_CHILD | WS_BORDER | HDS_BUTTONS | HDS_HORZ, 
                0, 0, 0, 0, hwndParent, (HMENU) ID_HEADER, g_hinst, 
                (LPVOID) NULL)) == NULL) 
            return (HWND) NULL; 
 
        // Retrieve the bounding rectangle of the parent window's 
        // client area, and then request size and position values 
        // from the header control. 
        GetClientRect(hwndParent, &rcParent); 
 
        hdl.prc = &rcParent; 
        hdl.pwpos = &wp; 
        if (!SendMessage(hwndHeader, HDM_LAYOUT, 0, (LPARAM) &hdl)) 
            return (HWND) NULL; 
 
        // Set the size, position, and visibility of the header control. 
        SetWindowPos(hwndHeader, wp.hwndInsertAfter, wp.x, wp.y, 
            wp.cx, wp.cy, wp.flags | SWP_SHOWWINDOW); 
 
        return hwndHeader; 
}
```



## <a name="related-topics"></a><span data-ttu-id="05ce6-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="05ce6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05ce6-121">À propos des contrôles Header</span><span class="sxs-lookup"><span data-stu-id="05ce6-121">About Header Controls</span></span>](header-controls.md)
</dt> <dt>

[<span data-ttu-id="05ce6-122">Référence de contrôle header</span><span class="sxs-lookup"><span data-stu-id="05ce6-122">Header Control Reference</span></span>](bumper-header-control-header-control-reference.md)
</dt> <dt>

[<span data-ttu-id="05ce6-123">Utilisation des contrôles Header</span><span class="sxs-lookup"><span data-stu-id="05ce6-123">Using Header Controls</span></span>](using-header-controls.md)
</dt> </dl>

 

 