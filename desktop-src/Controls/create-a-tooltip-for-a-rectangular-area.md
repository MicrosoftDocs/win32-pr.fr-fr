---
title: Comment créer une info-bulle pour une zone rectangulaire
description: L’exemple suivant montre comment créer un contrôle ToolTip standard pour l’ensemble de la zone client d’une fenêtre.
ms.assetid: 6AF1CE6E-AD63-4F84-9759-14FE4F16092B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8daf62bf2ba85c8750fd07a1b9122b0360fc11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127223649"
---
# <a name="how-to-create-a-tooltip-for-a-rectangular-area"></a>Comment créer une info-bulle pour une zone rectangulaire

L’exemple suivant montre comment créer un contrôle ToolTip standard pour l’ensemble de la zone client d’une fenêtre.

L’illustration suivante montre l’info-bulle qui s’affiche lorsque le pointeur de la souris se trouve dans la fenêtre cliente d’une boîte de dialogue. Le handle de la boîte de dialogue a été passé à la fonction illustrée dans l’exemple précédent.

![capture d’écran d’une boîte de dialogue ; le pointeur de la souris se trouve dans la fenêtre du client et une info-bulle est visible](images/tt-rectangle.png)

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="create-a-tooltip-for-a-rectangular-area"></a>Créer une info-bulle pour une zone rectangulaire

L’exemple suivant montre comment créer un contrôle ToolTip standard pour l’ensemble de la zone client d’une fenêtre.


```C++
void CreateToolTipForRect(HWND hwndParent)
{
    // Create a tooltip.
    HWND hwndTT = CreateWindowEx(WS_EX_TOPMOST, TOOLTIPS_CLASS, NULL, 
                                 WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP, 
                                 CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, 
                                 hwndParent, NULL, g_hInst,NULL);

    SetWindowPos(hwndTT, HWND_TOPMOST, 0, 0, 0, 0, 
                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE);

    // Set up "tool" information. In this case, the "tool" is the entire parent window.
    
    TOOLINFO ti = { 0 };
    ti.cbSize   = sizeof(TOOLINFO);
    ti.uFlags   = TTF_SUBCLASS;
    ti.hwnd     = hwndParent;
    ti.hinst    = g_hInst;
    ti.lpszText = TEXT("This is your tooltip string.");;
    
    GetClientRect (hwndParent, &ti.rect);

    // Associate the tooltip with the "tool" window.
    SendMessage(hwndTT, TTM_ADDTOOL, 0, (LPARAM) (LPTOOLINFO) &ti); 
} 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

 




