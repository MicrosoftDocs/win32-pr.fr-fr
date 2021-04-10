---
title: Comment utiliser les contrôles de pagineur
description: Cette section décrit comment implémenter le contrôle de pagineur dans votre application.
ms.assetid: 5703FE4B-987E-49DA-9741-F8B45AD26467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586bfff0c8d8097c4b0e861506bb73f55467b711
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031940"
---
# <a name="how-to-use-pager-controls"></a>Comment utiliser les contrôles de pagineur

Cette section décrit comment implémenter le contrôle de pagineur dans votre application.

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions

### <a name="initialize-a-pager-control"></a>Initialiser un contrôle de pagineur

Pour utiliser le contrôle de pagineur, vous devez appeler la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) avec l' \_ indicateur de classe PAGESCROLLER ICC \_ défini dans le membre **dwICC** de la structure [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) .

### <a name="create-a-pager-control"></a>Créer un contrôle de pagineur

Utilisez l’API [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) pour créer un contrôle de pagineur. Le nom de classe du contrôle est [**WC \_ PAGESCROLLER**](common-control-window-classes.md), qui est défini dans commctrl. h. Le [**style \_ Horiz PG**](pager-control-styles.md) est utilisé pour créer un pagineur horizontal et le style [**PG \_ vert**](pager-control-styles.md) est utilisé pour créer un pagineur vertical. Étant donné qu’il s’agit d’un contrôle enfant, le style [**WS \_ Child**](/windows/desktop/winmsg/window-styles) doit également être utilisé.

Une fois le contrôle de pagineur créé, vous souhaiterez probablement lui assigner une fenêtre qu’il contient. Si la fenêtre contenue est une fenêtre enfant, vous devez faire de la fenêtre enfant un enfant du contrôle de pagineur afin que la taille et la position soient calculées correctement. Vous assignez ensuite la fenêtre au contrôle pager avec le message [**PGM \_ SETCHILD**](pgm-setchild.md) . N’oubliez pas que ce message ne modifie pas réellement la fenêtre parente de la fenêtre contenue ; elle affecte simplement la fenêtre contenue. Si la fenêtre contenue est l’un des contrôles communs, elle doit avoir le style [**CCS \_ NORESIZE**](common-control-styles.md) pour empêcher le contrôle d’essayer de se redimensionner à la taille du contrôle de pagineur.

### <a name="process-pager-control-notifications"></a>Traiter les notifications de contrôle de pagineur

Au minimum, il est nécessaire de traiter la notification [PGN \_ CALCSIZE](pgn-calcsize.md) . Si vous ne traitez pas cette notification et que vous entrez une valeur pour la largeur ou la hauteur, les flèches de défilement dans le contrôle de pagineur ne seront pas affichées. Cela est dû au fait que le contrôle de pagineur utilise la largeur ou la hauteur fournie dans la \_ notification CALCSIZE PGN pour déterminer la taille idéale de la fenêtre contenue.

L’exemple suivant montre comment traiter le cas de notification [ \_ CALCSIZE PGN](pgn-calcsize.md) . Dans cet exemple, la fenêtre contenue est un contrôle de barre d’outils qui contient un nombre inconnu de boutons à une taille inconnue. L’exemple montre comment utiliser le message [**to \_ GETMAXSIZE**](tb-getmaxsize.md) pour déterminer la taille de tous les éléments de la barre d’outils. L’exemple place ensuite la largeur de tous les éléments dans le membre **iWidth** de la structure [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) qui est passée à la notification.


```C++
case PGN_SCROLL:{

    LPNMPGSCROLL pScroll = (LPNMPGSCROLL)lParam;
 
    switch(pScroll->iDir){
     
        case PGF_SCROLLLEFT:
        case PGF_SCROLLRIGHT:
        case PGF_SCROLLUP:
        case PGF_SCROLLDOWN:
     
            pScroll->iScroll = 20;
        
            break;
        }
    }
  
return 0;
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles de pagineur](using-pager-controls.md)
</dt> <dt>

[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 