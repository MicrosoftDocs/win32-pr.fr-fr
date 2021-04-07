---
title: Utilisation des fenêtres d’amis
description: En définissant d’autres contrôles en tant que fenêtres d’amis pour un TrackBar, vous pouvez positionner automatiquement ces contrôles aux extrémités du TrackBar en tant qu’étiquettes.
ms.assetid: 5797AA55-BD8D-407A-8896-08EE0DDC7E30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eca9a4e3b3049f8d4cf7515879d91a096f5a9e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029044"
---
# <a name="how-to-use-buddy-windows"></a><span data-ttu-id="6a558-103">Utilisation des fenêtres d’amis</span><span class="sxs-lookup"><span data-stu-id="6a558-103">How to Use Buddy Windows</span></span>

<span data-ttu-id="6a558-104">En définissant d’autres contrôles en tant que fenêtres d’amis pour un TrackBar, vous pouvez positionner automatiquement ces contrôles aux extrémités du TrackBar en tant qu’étiquettes.</span><span class="sxs-lookup"><span data-stu-id="6a558-104">By setting other controls as buddy windows for a trackbar, you can automatically position those controls at the ends of the trackbar as labels.</span></span>

<span data-ttu-id="6a558-105">L’illustration suivante montre un TrackBar horizontal et vertical, tous deux avec des contrôles statiques comme fenêtres associées.</span><span class="sxs-lookup"><span data-stu-id="6a558-105">The following illustration shows a horizontal and a vertical trackbar, both with static controls as buddy windows.</span></span>

![capture d’écran montrant une boîte de dialogue avec un TrackBar horizontal et un TrackBar vertical](images/tkb-buddy.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="6a558-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="6a558-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="6a558-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="6a558-108">Technologies</span></span>

-   [<span data-ttu-id="6a558-109">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="6a558-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="6a558-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="6a558-110">Prerequisites</span></span>

-   <span data-ttu-id="6a558-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="6a558-111">C/C++</span></span>
-   <span data-ttu-id="6a558-112">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="6a558-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="6a558-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="6a558-113">Instructions</span></span>

### <a name="use-buddy-windows"></a><span data-ttu-id="6a558-114">Utiliser les fenêtres d’amis</span><span class="sxs-lookup"><span data-stu-id="6a558-114">Use Buddy Windows</span></span>

<span data-ttu-id="6a558-115">L’exemple de code suivant crée les fenêtres d’amis présentées dans l’illustration.</span><span class="sxs-lookup"><span data-stu-id="6a558-115">The following code example creates the buddy windows shown in the illustration.</span></span>


```
void LabelTrackbarsWithBuddies(HWND hDlg)
{
    HWND hwndTrackbar;
    HWND hwndBuddy;
    
    const int staticWidth   = 50;
    const int staticHeight  = 20;

//======================================================
// For horizontal Trackbar.

    hwndTrackbar = GetDlgItem(hDlg, IDC_SLIDER1);

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Left", SS_RIGHT | WS_CHILD | WS_VISIBLE, 
                                    0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                                    
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)TRUE, (LPARAM)hwndBuddy);
    
    //-------------------------------------------------

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Right", SS_LEFT | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                                
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)FALSE, (LPARAM)hwndBuddy);
    
//======================================================    
// For vertical Trackbar.
    
    hwndTrackbar = GetDlgItem(hDlg, IDC_SLIDER2);

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Top", SS_CENTER | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                               
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)TRUE, (LPARAM)hwndBuddy);

    //-------------------------------------------------

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Bottom", SS_CENTER | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                               
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)FALSE, (LPARAM)hwndBuddy);
}
```



## <a name="remarks"></a><span data-ttu-id="6a558-116">Notes</span><span class="sxs-lookup"><span data-stu-id="6a558-116">Remarks</span></span>

<span data-ttu-id="6a558-117">**IDC \_ SLIDER1** et **IDC \_ SLIDER2** sont trackbars créés dans l’éditeur de ressources.</span><span class="sxs-lookup"><span data-stu-id="6a558-117">**IDC\_SLIDER1** and **IDC\_SLIDER2** are trackbars created in the resource editor.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a558-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6a558-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a558-119">Utilisation des contrôles TrackBar</span><span class="sxs-lookup"><span data-stu-id="6a558-119">Using Trackbar Controls</span></span>](using-trackbar-controls.md)
</dt> </dl>

 

 




