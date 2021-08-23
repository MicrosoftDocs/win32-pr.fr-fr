---
description: Les fonctions suivantes sont utilisées avec la peinture et le dessin.
ms.assetid: ec18323e-c13b-4328-83bf-9e4ed4a712b8
title: Fonctions de peinture et de dessin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a51b8acb0ea187c17d220d80f105ad6ae49371688d4eb8671c2a8eb5949b6e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666619"
---
# <a name="painting-and-drawing-functions"></a>Fonctions de peinture et de dessin

Les fonctions suivantes sont utilisées avec la peinture et le dessin.



| Fonction                                       | Description                                                                                                 |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)               | Prépare une fenêtre pour la peinture.                                                                             |
| [**DrawAnimatedRects**](/windows/desktop/api/Winuser/nf-winuser-drawanimatedrects) | Dessine un rectangle et l’anime pour indiquer l’activité de l’icône ou de la fenêtre.                                      |
| [**DrawCaption**](/windows/desktop/api/Winuser/nf-winuser-drawcaption)             | Dessine une légende de fenêtre.                                                                                     |
| [**DrawEdge**](/windows/desktop/api/Winuser/nf-winuser-drawedge)                   | Dessine un ou plusieurs bords du rectangle.                                                                       |
| [**DrawFocusRect**](/windows/desktop/api/Winuser/nf-winuser-drawfocusrect)         | Dessine un rectangle dans le style qui indique que le rectangle a le focus.                                  |
| [**DrawFrameControl**](/windows/desktop/api/Winuser/nf-winuser-drawframecontrol)   | Dessine un contrôle Frame.                                                                                      |
| [**DrawState**](/windows/desktop/api/Winuser/nf-winuser-drawstatea)                 | Affiche une image et applique un effet visuel pour indiquer un État.                                          |
| [**DrawStateProc**](/windows/desktop/api/Winuser/nc-winuser-drawstateproc)         | Fonction de rappel qui restitue une image complexe pour [**DrawState**](/windows/desktop/api/Winuser/nf-winuser-drawstatea).                        |
| [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint)                   | Marque la fin de la peinture dans une fenêtre.                                                                      |
| [**ExcludeUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn)   | Empêche le dessin dans des zones non valides d’une fenêtre.                                                          |
| [**GdiFlush**](/windows/desktop/api/Wingdi/nf-wingdi-gdiflush)                   | Vide le lot actuel du thread appelant.                                                                 |
| [**GdiGetBatchLimit**](/windows/desktop/api/Wingdi/nf-wingdi-gdigetbatchlimit)   | Retourne le nombre maximal d’appels de fonction qui peuvent être accumulés dans le lot actuel du thread appelant. |
| [**GdiSetBatchLimit**](/windows/desktop/api/Wingdi/nf-wingdi-gdisetbatchlimit)   | Définit le nombre maximal d’appels de fonction qui peuvent être accumulés dans le lot actuel du thread appelant.    |
| [**GetBkColor**](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor)               | Retourne la couleur d’arrière-plan d’un contexte de périphérique.                                                          |
| [**GetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)                 | Retourne le mode de combinaison d’arrière-plan pour un contexte de périphérique.                                                       |
| [**GetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect)         | Obtient le rectangle englobant cumulé pour un contexte de périphérique.                                               |
| [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)                     | Obtient le mode de combinaison de premier plan d’un contexte de périphérique.                                                           |
| [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)         | Obtient les coordonnées du plus petit rectangle qui englobe la zone de mise à jour d’une fenêtre.                 |
| [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn)           | Obtient la zone de mise à jour d’une fenêtre.                                                                         |
| [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)             | Obtient le contexte de périphérique pour une fenêtre, y compris la barre de titre, les menus et les barres de défilement.                          |
| [**GetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-getwindowrgn)           | Obtient une copie de la zone de fenêtre d’une fenêtre.                                                               |
| [**GetWindowRgnBox**](/windows/desktop/api/Winuser/nf-winuser-getwindowrgnbox)     | Obtient les dimensions du rectangle englobant le plus étroit pour la zone de fenêtre d’une fenêtre.                   |
| [**GrayString**](/windows/desktop/api/Winuser/nf-winuser-graystringa)               | Dessine du texte gris à un emplacement.                                                                              |
| [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect)       | Ajoute un rectangle à la zone de mise à jour d’une fenêtre.                                                               |
| [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn)         | Invalide la zone cliente dans une région.                                                                |
| [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate)   | Désactive ou active le dessin dans une fenêtre.                                                                    |
| [**OutputProc**](/windows/desktop/api/Winuser/nc-winuser-graystringproc)               | Fonction de rappel utilisée avec la fonction [**GrayString**](/windows/desktop/api/Winuser/nf-winuser-graystringa) . Il est utilisé pour dessiner une chaîne.   |
| [**PaintDesktop**](/windows/desktop/api/Winuser/nf-winuser-paintdesktop)           | Remplit la zone de découpage dans un contexte de périphérique à l’aide d’un modèle.                                               |
| [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)           | Met à jour une région dans la zone cliente d’une fenêtre.                                                                 |
| [**SetBkColor**](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor)               | Définit l’arrière-plan sur une valeur de couleur.                                                                       |
| [**SetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode)                 | Définit le mode de combinaison d’arrière-plan d’un contexte de périphérique.                                                           |
| [**SetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect)         | Contrôle l’accumulation des informations de rectangle englobant pour un contexte de périphérique.                           |
| [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2)                     | Définit le mode de combinaison de premier plan.                                                                               |
| [**SetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn)           | Définit la zone de fenêtre d’une fenêtre.                                                                         |
| [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)           | Met à jour la zone cliente d’une fenêtre.                                                                        |
| [**ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect)           | Valide la zone cliente dans un rectangle.                                                               |
| [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn)             | Valide la zone cliente dans une région.                                                                  |
| [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc)           | Retourne un handle vers la fenêtre associée à un contexte de périphérique.                                            |



 

 

 



