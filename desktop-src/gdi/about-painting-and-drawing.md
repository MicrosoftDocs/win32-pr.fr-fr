---
description: Presque toutes les applications utilisent l’écran pour afficher les données qu’elles manipulent.
ms.assetid: 97d606a0-11d3-49c3-b045-8397f4bcfa54
title: À propos de la peinture et du dessin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcb8ffa5b5c842dcd12d57967f2c20de0391824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991153"
---
# <a name="about-painting-and-drawing"></a>À propos de la peinture et du dessin

Presque toutes les applications utilisent l’écran pour afficher les données qu’elles manipulent. Une application peint des images, dessine des figures et écrit du texte afin que l’utilisateur puisse afficher les données à mesure qu’elles sont créées, modifiées et imprimées. Microsoft Windows offre une prise en charge enrichie de la peinture et du dessin, mais, en raison de la nature des systèmes d’exploitation multitâche, les applications doivent coopérer les unes avec les autres lors de l’accès à l’écran.

Pour que toutes les applications fonctionnent correctement et de manière coopérative, le système gère l’ensemble de la sortie à l’écran. Les applications utilisent Windows comme périphérique de sortie principal plutôt que l’écran lui-même. Le système fournit des contextes de périphérique d’affichage qui correspondent de manière unique aux fenêtres. Les applications utilisent des contextes de périphérique d’affichage pour diriger leur sortie vers les fenêtres spécifiées. Le fait de dessiner dans une fenêtre (en dirigeant la sortie) empêche une application d’interférer avec la sortie d’autres applications et permet aux applications de coexister les unes avec les autres tout en tirant pleinement parti des fonctionnalités graphiques du système.

-   [Quand dessiner dans une fenêtre](when-to-draw-in-a-window.md)
-   [Message de \_ peinture WM](the-wm-paint-message.md)
-   [Dessin sans le \_ message WM Paint](drawing-without-the-wm-paint-message.md)
-   [Système de coordonnées de fenêtre](window-coordinate-system.md)
-   [Régions de fenêtre](window-regions.md)
-   [Arrière-plan de fenêtre](window-background.md)
-   [Fenêtres réduites](minimized-windows.md)
-   [Fenêtres redimensionnées](resized-windows.md)
-   [Zone non cliente](nonclient-area.md)
-   [Zone de mise à jour de la fenêtre enfant](child-window-update-region.md)
-   [Périphériques d’affichage](display-devices.md)
-   [Verrou de mise à jour de fenêtre](window-update-lock.md)
-   [Rectangle englobant cumulé](accumulated-bounding-rectangle.md)

 

 



