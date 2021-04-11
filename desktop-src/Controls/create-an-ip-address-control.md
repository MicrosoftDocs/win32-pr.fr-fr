---
title: Comment créer un contrôle d’adresse IP
description: Cette rubrique montre comment créer une instance d’un contrôle d’adresse IP.
ms.assetid: E4DBECA6-B3F2-405F-8D95-32FA2334114D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8427a5695c0b9c79c19d328f4abc2ab0ffb2e5a
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104102569"
---
# <a name="how-to-create-an-ip-address-control"></a><span data-ttu-id="bf2dc-103">Comment créer un contrôle d’adresse IP</span><span class="sxs-lookup"><span data-stu-id="bf2dc-103">How to Create an IP Address Control</span></span>

<span data-ttu-id="bf2dc-104">Cette rubrique montre comment créer une instance d’un contrôle d’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="bf2dc-104">This topic demonstrates how to create an instance of an IP address control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="bf2dc-105">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="bf2dc-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="bf2dc-106">Technologies</span><span class="sxs-lookup"><span data-stu-id="bf2dc-106">Technologies</span></span>

-   [<span data-ttu-id="bf2dc-107">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="bf2dc-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="bf2dc-108">Prérequis</span><span class="sxs-lookup"><span data-stu-id="bf2dc-108">Prerequisites</span></span>

-   <span data-ttu-id="bf2dc-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="bf2dc-109">C/C++</span></span>
-   <span data-ttu-id="bf2dc-110">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="bf2dc-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="bf2dc-111">Instructions</span><span class="sxs-lookup"><span data-stu-id="bf2dc-111">Instructions</span></span>


<span data-ttu-id="bf2dc-112">Avant de créer un contrôle d’adresse IP, chargez la DLL des contrôles communs en appelant [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex).</span><span class="sxs-lookup"><span data-stu-id="bf2dc-112">Before creating an IP address control, load the common controls DLL by calling [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex).</span></span> <span data-ttu-id="bf2dc-113">Utilisez ensuite la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) pour créer un contrôle d’adresse IP d’instance.</span><span class="sxs-lookup"><span data-stu-id="bf2dc-113">Then use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create an instance IP address control.</span></span> <span data-ttu-id="bf2dc-114">Le nom de classe du contrôle est [**WC \_ IPAddress**](common-control-window-classes.md).</span><span class="sxs-lookup"><span data-stu-id="bf2dc-114">The class name for the control is [**WC\_IPADDRESS**](common-control-window-classes.md).</span></span> <span data-ttu-id="bf2dc-115">Utilisez le style [**WS \_ Child**](/windows/desktop/winmsg/window-styles) , car aucune constante de style spécifique n’est associée au contrôle d’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="bf2dc-115">Use the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) style, because there is no specific style constant associated with the IP address control.</span></span>

<span data-ttu-id="bf2dc-116">Dans l’exemple de code C++ suivant, la fonction définie par l’application appelle d’abord [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) et définit le membre **dwICC** de la structure [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) sur les [**\_ \_ classes Internet ICC**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex), qui spécifie la classe d’adresses IP.</span><span class="sxs-lookup"><span data-stu-id="bf2dc-116">In the following C++ code example, the application-defined function first calls [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) and sets the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure to [**ICC\_INTERNET\_CLASSES**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex), which specifies the IP address class.</span></span> <span data-ttu-id="bf2dc-117">Il appelle ensuite [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) pour créer une instance du contrôle d’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="bf2dc-117">It then calls [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) to create an instance of the IP address control.</span></span>


```C++
// CreateIPAdressFld - creates a IPAddress control.
// Returns the handle to the new control
// TO DO:  calling procedure needs to check whether the handle is NULL, in case 
// of an error in creation.
// int xcoord, ycoord the coordinates of location of the control in the parent window
// HINST hInst is the global handle to the application instance.
// HWND  hWndParent is the handle to the control's parent window. 
//
//
HWND CreateIPAddressFld (HWND hwndParent, int xcoord, int ycoord) 
{     
     
    INITCOMMONCONTROLSEX icex;
    
    // Ensure that the common control DLL is loaded. 
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC  = ICC_INTERNET_CLASSES ;
    InitCommonControlsEx(&icex); 
    
    // Create the IPAddress control.        
    HWND hWndIPAddressFld = CreateWindow(WC_IPADDRESS, 
                                L"", 
                                WS_CHILD | WS_OVERLAPPED | WS_VISIBLE, 
                                xcoord, 
                                ycoord,
                                150, 
                                20,  
                                hwndParent, 
                                NULL, 
                                hInst, 
                                NULL); 
                                
    return (hWndIPAddressFld);
}
```



## <a name="related-topics"></a><span data-ttu-id="bf2dc-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bf2dc-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf2dc-119">Référence de contrôle d’adresse IP</span><span class="sxs-lookup"><span data-stu-id="bf2dc-119">IP Address Control Reference</span></span>](bumper-ip-address-control-ip-address-control-reference.md)
</dt> <dt>

[<span data-ttu-id="bf2dc-120">À propos des contrôles d’adresse IP</span><span class="sxs-lookup"><span data-stu-id="bf2dc-120">About IP Address Controls</span></span>](ip-address-controls.md)
</dt> <dt>

[<span data-ttu-id="bf2dc-121">Utilisation des contrôles d’adresse IP</span><span class="sxs-lookup"><span data-stu-id="bf2dc-121">Using IP Address Controls</span></span>](using-ip-address-controls.md)
</dt> </dl>

 

 