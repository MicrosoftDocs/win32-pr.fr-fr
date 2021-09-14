---
title: Comment créer une interface clavier pour les barres de défilement standard
description: Bien qu’un contrôle de barre de défilement fournisse une interface clavier intégrée, aucune barre de défilement standard ne le fait.
ms.assetid: 249D0077-6E61-479A-91D5-A4BD9752B82E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b739638d95d9f3e530718f8e9b9e6168069420
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195743"
---
# <a name="how-to-create-a-keyboard-interface-for-standard-scroll-bars"></a>Comment créer une interface clavier pour les barres de défilement standard

Bien qu’un contrôle de barre de défilement fournisse une interface clavier intégrée, aucune barre de défilement standard ne le fait. Pour implémenter une interface clavier pour une barre de défilement standard, une procédure de fenêtre doit traiter le message KeyOut [**WM \_**](/windows/desktop/inputdev/wm-keydown) et examiner le code de la touche virtuelle spécifié par le paramètre *wParam* . Si le code de la touche virtuelle correspond à une touche de direction, la procédure de fenêtre s’envoie un message [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) avec le mot de poids faible du paramètre *wParam* défini sur le code de requête de la barre de défilement appropriée.

Par exemple, quand l’utilisateur appuie sur la touche haut, la procédure de fenêtre reçoit un [**message \_ WM**](/windows/desktop/inputdev/wm-keydown) KeyOut avec *wParam* égal à VK \_ up. En réponse, la procédure de fenêtre s’envoie lui-même un message [**WM \_ VSCROLL**](wm-vscroll.md) avec le mot de poids faible de *wParam* défini sur le code de demande de la \_ programmation SB.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="create-a-keyboard-interface-for-a-standard-scroll-bar"></a>Créer une interface clavier pour une barre de défilement standard

L’exemple de code suivant montre comment inclure une interface clavier pour une barre de défilement standard.


```C++
    case WM_KEYDOWN: 
    {
        WORD wScrollNotify = 0xFFFF;

        switch (wParam) 
        { 
            case VK_UP: 
                wScrollNotify = SB_LINEUP; 
                break; 
 
            case VK_PRIOR: 
                wScrollNotify = SB_PAGEUP; 
                break; 
 
            case VK_NEXT: 
                wScrollNotify = SB_PAGEDOWN; 
                break; 
 
            case VK_DOWN: 
                wScrollNotify = SB_LINEDOWN; 
                break; 
 
            case VK_HOME: 
                wScrollNotify = SB_TOP; 
                break; 
 
            case VK_END: 
                wScrollNotify = SB_BOTTOM; 
                break; 
        } 
 
        if (wScrollNotify != -1) 
            SendMessage(hwnd, WM_VSCROLL, MAKELONG(wScrollNotify, 0), 0L); 
 
        break; 
    }
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des barres de défilement](using-scroll-bars.md)
</dt> <dt>

[Windows démonstration des contrôles communs (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 