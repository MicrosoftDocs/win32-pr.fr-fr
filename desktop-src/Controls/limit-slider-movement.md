---
title: Comment limiter le mouvement d’un curseur
description: Comme décrit dans à propos des contrôles TrackBar, il est possible de définir une partie off de la plage TrackBar en tant que plage de sélection. L’une des finalités d’une plage de sélection consiste à limiter le déplacement du curseur, en faisant en sorte que certaines parties de la plage complète soient délimitées.
ms.assetid: 9DD8BB11-EC6F-4695-BA56-5061F6EA5436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5414ddf72c44dcaed85afde349f0b9f813ed0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839590"
---
# <a name="how-to-limit-slider-movement"></a>Comment limiter le mouvement d’un curseur

Comme décrit dans [à propos des contrôles TrackBar](trackbar-controls.md), il est possible de définir une partie off de la plage TrackBar en tant que plage de sélection. L’une des finalités d’une plage de sélection consiste à limiter le déplacement du curseur, en faisant en sorte que certaines parties de la plage complète soient délimitées.

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions

### <a name="limit-slider-movement"></a>Limiter le déplacement du curseur

L’exemple de code suivant limite le déplacement du curseur en réinitialisant la position du curseur à chaque fois qu’il est déplacé en dehors de la plage de sélection.


```
case WM_HSCROLL:
    {
        HWND hTrackbar = GetDlgItem(hDlg, IDC_SLIDER1);
        
        if (hTrackbar == (HWND)lParam)
        {
            int newPos    = SendMessage(hTrackbar, TBM_GETPOS, 0, 0);
            int selStart  = SendMessage(hTrackbar, TBM_GETSELSTART, 0, 0);
            int selEnd    = SendMessage(hTrackbar, TBM_GETSELEND, 0, 0);
            
            if (newPos > selEnd)
            {
                SendMessage(hTrackbar, TBM_SETPOS, (WPARAM)TRUE, (LPARAM)selEnd);
            }
            
            else if (newPos < selStart)
            {
                SendMessage(hTrackbar, TBM_SETPOS, (WPARAM)TRUE, (LPARAM)selStart);
            }
        }
        
        break;
    }
```



## <a name="remarks"></a>Notes

Cet extrait de code fait partie de la procédure de fenêtre d’une boîte de dialogue.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles TrackBar](using-trackbar-controls.md)
</dt> </dl>

 

 




