---
title: Comment traiter des messages de notification TrackBar
description: Trackbars notifier la fenêtre parente des actions de l’utilisateur en lui envoyant un \_ message WM HSCROLL ou WM \_ VSCROLL.
ms.assetid: 83F47A3E-E607-49C2-A8B5-BC8A321D90BB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c723ad1bebb5c9f3ec8c4e7aefdc658e0881aef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672205"
---
# <a name="how-to-process-trackbar-notification-messages"></a><span data-ttu-id="916bb-103">Comment traiter des messages de notification TrackBar</span><span class="sxs-lookup"><span data-stu-id="916bb-103">How to Process Trackbar Notification Messages</span></span>

<span data-ttu-id="916bb-104">Trackbars notifier la fenêtre parente des actions de l’utilisateur en lui envoyant un message [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="916bb-104">Trackbars notify their parent window of user actions by sending the parent a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="916bb-105">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="916bb-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="916bb-106">Technologies</span><span class="sxs-lookup"><span data-stu-id="916bb-106">Technologies</span></span>

-   [<span data-ttu-id="916bb-107">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="916bb-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="916bb-108">Prérequis</span><span class="sxs-lookup"><span data-stu-id="916bb-108">Prerequisites</span></span>

-   <span data-ttu-id="916bb-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="916bb-109">C/C++</span></span>
-   <span data-ttu-id="916bb-110">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="916bb-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="916bb-111">Instructions</span><span class="sxs-lookup"><span data-stu-id="916bb-111">Instructions</span></span>

### <a name="process-trackbar-notification-messages"></a><span data-ttu-id="916bb-112">Traiter les messages de notification TrackBar</span><span class="sxs-lookup"><span data-stu-id="916bb-112">Process Trackbar Notification Messages</span></span>

<span data-ttu-id="916bb-113">L’exemple de code suivant est une fonction qui est appelée lorsque la fenêtre parente de TrackBar reçoit un message [**WM \_ HSCROLL**](wm-hscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="916bb-113">The following code example is a function that is called when the trackbar's parent window receives a [**WM\_HSCROLL**](wm-hscroll.md) message.</span></span> <span data-ttu-id="916bb-114">Dans cet exemple, le TrackBar a le style [**tbs \_ ENABLESELRANGE**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="916bb-114">The trackbar in this example has the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style.</span></span> <span data-ttu-id="916bb-115">La position du curseur est comparée à la plage de sélection et le curseur est déplacé vers la position de début ou de fin de la plage de sélection, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="916bb-115">The position of the slider is compared to the selection range, and the slider is moved to the starting or ending position of the selection range when necessary.</span></span>


```
// TBNotifications - handles trackbar notifications received 
// in the wParam parameter of WM_HSCROLL. This function simply 
// ensures that the slider remains within the selection range. 

VOID WINAPI TBNotifications( 
    WPARAM wParam,  // wParam of WM_HSCROLL message 
    HWND hwndTrack, // handle of trackbar window 
    UINT iSelMin,   // minimum value of trackbar selection 
    UINT iSelMax)   // maximum value of trackbar selection 
    { 
    DWORD dwPos;    // current position of slider 

    switch (LOWORD(wParam)) { 
    
        case TB_ENDTRACK:
          
            dwPos = SendMessage(hwndTrack, TBM_GETPOS, 0, 0); 
            
            if (dwPos > iSelMax) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMax); 
                    
            else if (dwPos < iSelMin) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMin); 
            
            break; 

        default: 
        
            break; 
        } 
} 
```



## <a name="remarks"></a><span data-ttu-id="916bb-116">Notes</span><span class="sxs-lookup"><span data-stu-id="916bb-116">Remarks</span></span>

<span data-ttu-id="916bb-117">Une boîte de dialogue qui contient un TrackBar de style de type [**tbs \_**](trackbar-control-styles.md) peut utiliser cette fonction lorsqu’elle reçoit un message [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="916bb-117">A dialog box that contains a [**TBS\_VERT**](trackbar-control-styles.md) style trackbar can use this function when it receives a [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="916bb-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="916bb-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="916bb-119">Utilisation des contrôles TrackBar</span><span class="sxs-lookup"><span data-stu-id="916bb-119">Using Trackbar Controls</span></span>](using-trackbar-controls.md)
</dt> </dl>

 

 




