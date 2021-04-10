---
title: Traitement des notifications ComboBoxEx
description: Cette rubrique montre comment traiter les messages de notification ComboBoxEx.
ms.assetid: 375634BC-CDD6-4D72-A41E-FCBFCBFE7F03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a9787e22aa01d51478ca55f0dde5d7ac944decb
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103941512"
---
# <a name="how-to-process-comboboxex-notifications"></a><span data-ttu-id="bde11-103">Traitement des notifications ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="bde11-103">How to Process ComboBoxEx Notifications</span></span>

<span data-ttu-id="bde11-104">Cette rubrique montre comment traiter les messages de notification ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="bde11-104">This topic demonstrates how to process ComboBoxEx notification messages.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="bde11-105">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="bde11-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="bde11-106">Technologies</span><span class="sxs-lookup"><span data-stu-id="bde11-106">Technologies</span></span>

-   [<span data-ttu-id="bde11-107">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="bde11-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="bde11-108">Prérequis</span><span class="sxs-lookup"><span data-stu-id="bde11-108">Prerequisites</span></span>

-   <span data-ttu-id="bde11-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="bde11-109">C/C++</span></span>
-   <span data-ttu-id="bde11-110">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="bde11-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="bde11-111">Instructions</span><span class="sxs-lookup"><span data-stu-id="bde11-111">Instructions</span></span>


<span data-ttu-id="bde11-112">Un contrôle ComboBoxEx informe sa fenêtre parente d’événements en envoyant des messages de [**\_ notification WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="bde11-112">A ComboBoxEx control notifies its parent window of events by sending [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="bde11-113">Il transmet également les messages de notification de [**\_ commande WM**](/windows/desktop/menurc/wm-command) qu’il reçoit de la zone de liste déroulante qu’il contient à la fenêtre parente à traiter.</span><span class="sxs-lookup"><span data-stu-id="bde11-113">It also passes the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) notification messages that it receives from the combo box contained within it to the parent window to be processed.</span></span> <span data-ttu-id="bde11-114">Par conséquent, votre application doit être préparée à traiter les messages de **\_ notification WM** à partir des messages de **\_ commande** ComboBoxEx et WM qui sont transférés à partir du contrôle de zone de liste déroulante enfant ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="bde11-114">Therefore, your application must be prepared to process **WM\_NOTIFY** messages from the ComboBoxEx and **WM\_COMMAND** messages that are forwarded from the ComboBoxEx child combo box control.</span></span>

<span data-ttu-id="bde11-115">L’exemple de cette section gère les messages [**WM \_ Notify**](wm-notify.md) et la [**\_ commande WM**](/windows/desktop/menurc/wm-command) à partir d’un contrôle ComboBoxEx en appelant une fonction définie par l’application correspondante pour traiter ces messages.</span><span class="sxs-lookup"><span data-stu-id="bde11-115">The example in this section handles the [**WM\_NOTIFY**](wm-notify.md) and [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages from a ComboBoxEx control by calling a corresponding application-defined function to process these messages.</span></span>

## <a name="complete-example"></a><span data-ttu-id="bde11-116">Exemple complet</span><span class="sxs-lookup"><span data-stu-id="bde11-116">Complete example</span></span>


```C++
LRESULT CALLBACK WndProc (HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam)
{
    switch(msg){

        case WM_COMMAND: // notification from the child ComboBox within the ComboBoxEx control.
            if((HWND)lParam == g_hwndCB)
                DoOldNotify(hwnd,  wParam);  
            break;

        case WM_NOTIFY: // notification from the ComboBoxEx control
            return (DoCBEXNotify(hwnd, lParam));

        case WM_PAINT:
            hdc = BeginPaint(hwnd, &ps);
            EndPaint(hwnd, &ps);
            break;

        case WM_DESTROY:
            PostQuitMessage(0);
            break;

        default:
            return DefWindowProc(hwnd, msg, wParam, lParam);
            break;
    }

    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="bde11-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bde11-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bde11-118">À propos des contrôles ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="bde11-118">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> <dt>

[<span data-ttu-id="bde11-119">Référence du contrôle ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="bde11-119">ComboBoxEx Control Reference</span></span>](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[<span data-ttu-id="bde11-120">Utilisation des contrôles ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="bde11-120">Using ComboBoxEx Controls</span></span>](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[<span data-ttu-id="bde11-121">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="bde11-121">ComboBoxEx</span></span>](comboboxex-control-reference.md)
</dt> </dl>

 

 