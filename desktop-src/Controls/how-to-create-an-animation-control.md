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
# <a name="how-to-create-an-animation-control"></a>Comment créer un contrôle d’animation

Cette rubrique montre comment créer un contrôle d’animation. L’exemple de code C++ qui l’accompagne crée un contrôle d’animation dans une boîte de dialogue. Il positionne le contrôle d’animation sous un contrôle spécifié et définit les dimensions du contrôle d’animation en fonction des dimensions d’un cadre dans le clip Audio-Video entrelacé (AVI).

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows
-   Fichiers AVI

## <a name="instructions"></a>Instructions

### <a name="step-1-create-an-instance-of-the-animation-control"></a>Étape 1 : créer une instance du contrôle d’animation.

Utilisez la macro [**animer \_ créer**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) pour créer une instance du contrôle d’animation.


```C++
// IDC_ANIMATE - identifier of the animation control. 
// hwndDlg - handle to the dialog box.
RECT rc;
hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
    WS_BORDER | WS_CHILD, g_hinst); 
```



### <a name="step-2-position-the-animation-control"></a>Étape 2 : Positionner le contrôle d’animation.

Obtient les coordonnées d’écran du bouton de contrôle spécifié.


```C++
// nIDCtl - identifier of the control below which the animation control is to be positioned.
GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 
```



Convertit les coordonnées du coin inférieur gauche en coordonnées clientes.


```C++
POINT pt;
pt.x = rc.left; 
pt.y = rc.bottom; 
ScreenToClient(hwndDlg, &pt); 
```



Placez le contrôle d’animation sous le bouton de contrôle spécifié.


```C++
// CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
    CX_FRAME, CY_FRAME, 
    SWP_NOZORDER | SWP_DRAWFRAME);
```



### <a name="step-3-open-the-avi-clip"></a>Étape 3 : Ouvrez le clip AVI.

Appelez la macro [**animer \_ ouvrir**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) pour ouvrir le clip AVI et afficher le premier frame dans le contrôle d’animation. Appelez la fonction **ShowWindow** pour rendre le contrôle d’animation visible.


```C++
Animate_Open(hwndAnim, "SEARCH.AVI"); 
ShowWindow(hwndAnim, SW_SHOW); 
```



## <a name="complete-example"></a>Exemple complet


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des contrôles d’animation](animation-control-overview.md)
</dt> <dt>

[Référence de contrôle d’animation](bumper-animation-animation-control-reference.md)
</dt> <dt>

[Utilisation de contrôles d’animation](using-animation-control.md)
</dt> <dt>

[Animation](animation-control-reference.md)
</dt> </dl>

 

 




