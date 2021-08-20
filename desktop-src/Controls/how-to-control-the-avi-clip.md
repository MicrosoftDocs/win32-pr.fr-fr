---
title: Comment contrôler le clip AVI
description: Cette rubrique montre comment utiliser les macros de contrôle d’animation pour lire, arrêter et fermer un clip Audio-Video entrelacé (AVI) associé.
ms.assetid: 4B19F929-B306-4EBF-B82F-6539FAA42BA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fbabd3ea6e0694448e4bd8c01e53161333b2df3904cf1578252bdbe150d3d5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170760"
---
# <a name="how-to-control-the-avi-clip"></a>Comment contrôler le clip AVI

Cette rubrique montre comment utiliser les macros de contrôle d’animation pour lire, arrêter et fermer un clip Audio-Video entrelacé (AVI) associé.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur
-   Fichiers AVI

## <a name="instructions"></a>Instructions


Créez une fonction qui prend comme paramètre un handle vers le contrôle d’animation et un indicateur qui indique l’action à effectuer sur le clip AVI associé.

La fonction de l’exemple C++ suivant appelle l’une des trois macros de contrôle d’animation ([**animer \_ lire**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play), [**animer \_ arrêter**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop), [**animer \_ Fermer**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)) en fonction de la valeur du paramètre *nsortie* . Le handle du contrôle d’animation associé au clip AVI est passé via le paramètre *hwndAnim* .


```C++
// DoAnimation - plays, stops, or closes an animation control's 
//               AVI clip, depending on the value of an action flag. 
// hwndAnim    - handle to an animation control. 
// nAction     - flag that determines whether to play, stop, or close 
//               the AVI clip. 

void DoAnimation(HWND hwndAnim, int nAction) 
{ 
    int const PLAYIT = 1, STOPIT = 2, CLOSEIT = 3; 
    switch (nAction) { 
        case PLAYIT: 
         // Play the clip continuously starting with the 
         // first frame. 
            Animate_Play(hwndAnim, 0, -1, -1); 
            break; 

        case STOPIT: 
            Animate_Stop(hwndAnim); 
            break; 

        case CLOSEIT: 
            Animate_Close(hwndAnim); 
            break; 

        default: 
            break; 
    }
    
    return; 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des contrôles d’animation](animation-control-overview.md)
</dt> <dt>

[Référence de contrôle d’animation](bumper-animation-animation-control-reference.md)
</dt> <dt>

[Utilisation de contrôles d’animation](using-animation-control.md)
</dt> <dt>

[Contrôle d’animation](animation-control-reference.md)
</dt> </dl>

 

 




