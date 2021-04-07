---
title: Comment créer un contrôle d’animation
description: Cette rubrique montre comment créer un contrôle d’animation.
ms.assetid: 5852B636-F3D0-47A4-82F6-8BE570013E1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4ff190617996e42e6580b82311fb51f4248000
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028832"
---
# <a name="how-to-create-an-animation-control"></a><span data-ttu-id="f049b-103">Comment créer un contrôle d’animation</span><span class="sxs-lookup"><span data-stu-id="f049b-103">How to Create an Animation Control</span></span>

<span data-ttu-id="f049b-104">Cette rubrique montre comment créer un contrôle d’animation.</span><span class="sxs-lookup"><span data-stu-id="f049b-104">This topic demonstrates how to create an animation control.</span></span> <span data-ttu-id="f049b-105">L’exemple de code C++ qui l’accompagne crée un contrôle d’animation dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f049b-105">The accompanying C++ code example creates an animation control in a dialog box.</span></span> <span data-ttu-id="f049b-106">Il positionne le contrôle d’animation sous un contrôle spécifié et définit les dimensions du contrôle d’animation en fonction des dimensions d’un cadre dans le clip Audio-Video entrelacé (AVI).</span><span class="sxs-lookup"><span data-stu-id="f049b-106">It positions the animation control below a specified control, and sets the dimensions of the animation control based on the dimensions of a frame in the Audio-Video Interleaved (AVI) clip.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="f049b-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="f049b-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f049b-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="f049b-108">Technologies</span></span>

-   [<span data-ttu-id="f049b-109">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="f049b-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="f049b-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="f049b-110">Prerequisites</span></span>

-   <span data-ttu-id="f049b-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="f049b-111">C/C++</span></span>
-   <span data-ttu-id="f049b-112">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="f049b-112">Windows User Interface Programming</span></span>
-   <span data-ttu-id="f049b-113">Fichiers AVI</span><span class="sxs-lookup"><span data-stu-id="f049b-113">AVI files</span></span>

## <a name="instructions"></a><span data-ttu-id="f049b-114">Instructions</span><span class="sxs-lookup"><span data-stu-id="f049b-114">Instructions</span></span>

### <a name="step-1-create-an-instance-of-the-animation-control"></a><span data-ttu-id="f049b-115">Étape 1 : créer une instance du contrôle d’animation.</span><span class="sxs-lookup"><span data-stu-id="f049b-115">Step 1: Create an instance of the animation control.</span></span>

<span data-ttu-id="f049b-116">Utilisez la macro [**animer \_ créer**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) pour créer une instance du contrôle d’animation.</span><span class="sxs-lookup"><span data-stu-id="f049b-116">Use the [**Animate\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) macro to create an instance of the animation control.</span></span>


```C++
// IDC_ANIMATE - identifier of the animation control. 
// hwndDlg - handle to the dialog box.
RECT rc;
hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
    WS_BORDER | WS_CHILD, g_hinst); 
```



### <a name="step-2-position-the-animation-control"></a><span data-ttu-id="f049b-117">Étape 2 : Positionner le contrôle d’animation.</span><span class="sxs-lookup"><span data-stu-id="f049b-117">Step 2: Position the animation control.</span></span>

<span data-ttu-id="f049b-118">Obtient les coordonnées d’écran du bouton de contrôle spécifié.</span><span class="sxs-lookup"><span data-stu-id="f049b-118">Get the screen coordinates of the specified control button.</span></span>


```C++
// nIDCtl - identifier of the control below which the animation control is to be positioned.
GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 
```



<span data-ttu-id="f049b-119">Convertit les coordonnées du coin inférieur gauche en coordonnées clientes.</span><span class="sxs-lookup"><span data-stu-id="f049b-119">Convert the coordinates of the lower-left corner to client coordinates.</span></span>


```C++
POINT pt;
pt.x = rc.left; 
pt.y = rc.bottom; 
ScreenToClient(hwndDlg, &pt); 
```



<span data-ttu-id="f049b-120">Placez le contrôle d’animation sous le bouton de contrôle spécifié.</span><span class="sxs-lookup"><span data-stu-id="f049b-120">Position the animation control below the specified control button.</span></span>


```C++
// CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
    CX_FRAME, CY_FRAME, 
    SWP_NOZORDER | SWP_DRAWFRAME);
```



### <a name="step-3-open-the-avi-clip"></a><span data-ttu-id="f049b-121">Étape 3 : Ouvrez le clip AVI.</span><span class="sxs-lookup"><span data-stu-id="f049b-121">Step 3: Open the AVI clip.</span></span>

<span data-ttu-id="f049b-122">Appelez la macro [**animer \_ ouvrir**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) pour ouvrir le clip AVI et afficher le premier frame dans le contrôle d’animation.</span><span class="sxs-lookup"><span data-stu-id="f049b-122">Call the [**Animate\_Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) macro to open the AVI clip and display the first frame in the animation control.</span></span> <span data-ttu-id="f049b-123">Appelez la fonction **ShowWindow** pour rendre le contrôle d’animation visible.</span><span class="sxs-lookup"><span data-stu-id="f049b-123">Call the **ShowWindow** function to make the animation control visible.</span></span>


```C++
Animate_Open(hwndAnim, "SEARCH.AVI"); 
ShowWindow(hwndAnim, SW_SHOW); 
```



## <a name="complete-example"></a><span data-ttu-id="f049b-124">Exemple complet</span><span class="sxs-lookup"><span data-stu-id="f049b-124">Complete example</span></span>


```C++
// CreateAnimationCtrl - creates an animation control, positions it 
//                       below the specified control in a dialog box, 
//                       and opens the AVI clip for the animation control. 
// Returns the handle to the animation control. 
// hwndDlg             - handle to the dialog box. 
// nIDCtl              - identifier of the control below which the animation control 
//                       is to be positioned. 
// 
// Constants 
//     IDC_ANIMATE - identifier of the animation control. 
//     CX_FRAME, CY_FRAME - width and height of the frames 
//     in the AVI clip. 

HWND CreateAnimationCtrl(HWND hwndDlg, int nIDCtl) 
{ 
    HWND hwndAnim = NULL;    
    
    // Create the animation control.
    // IDC_ANIMATE - identifier of the animation control. 
    // hwndDlg - handle to the dialog box.
    RECT rc;
    hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
        WS_BORDER | WS_CHILD, g_hinst); 

    // Get the screen coordinates of the specified control button.
    // nIDCtl - identifier of the control below which the animation control is to be positioned.
    GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 

    // Convert the coordinates of the lower-left corner to 
    // client coordinates.
    POINT pt;
    pt.x = rc.left; 
    pt.y = rc.bottom; 
    ScreenToClient(hwndDlg, &pt); 

    // Position the animation control below the Stop button.
    // CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
    SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
        CX_FRAME, CY_FRAME, 
        SWP_NOZORDER | SWP_DRAWFRAME);

    // Open the AVI clip, and show the animation control.
    Animate_Open(hwndAnim, "SEARCH.AVI"); 
    ShowWindow(hwndAnim, SW_SHOW); 

    return hwndAnim; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="f049b-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f049b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f049b-126">À propos des contrôles d’animation</span><span class="sxs-lookup"><span data-stu-id="f049b-126">About Animation Controls</span></span>](animation-control-overview.md)
</dt> <dt>

[<span data-ttu-id="f049b-127">Référence de contrôle d’animation</span><span class="sxs-lookup"><span data-stu-id="f049b-127">Animation Control Reference</span></span>](bumper-animation-animation-control-reference.md)
</dt> <dt>

[<span data-ttu-id="f049b-128">Utilisation de contrôles d’animation</span><span class="sxs-lookup"><span data-stu-id="f049b-128">Using Animation Controls</span></span>](using-animation-control.md)
</dt> <dt>

[<span data-ttu-id="f049b-129">Animation</span><span class="sxs-lookup"><span data-stu-id="f049b-129">Animation</span></span>](animation-control-reference.md)
</dt> </dl>

 

 




