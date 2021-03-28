---
description: Un rectangle est un polygone à quatre côtés dont les côtés opposés sont parallèles et de longueur égale.
ms.assetid: 77d29981-032e-45ba-a06b-c9c992236803
title: Dessiner des rectangles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1c5908ff989f7534536b3a6e84bad2095c096e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863650"
---
# <a name="drawing-rectangles"></a>Dessiner des rectangles

Un rectangle est un polygone à quatre côtés dont les côtés opposés sont parallèles et de longueur égale. Bien qu’une application puisse dessiner un rectangle en appelant la fonction [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) , en fournissant les coordonnées de chaque angle, la fonction [**rectangle**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle) fournit une méthode plus simple. Cette fonction ne requiert que les coordonnées des angles supérieur gauche et inférieur droit. Quand une application appelle la fonction [**rectangle**](/windows/win32/api/wingdi/nf-wingdi-rectangle) , le système dessine le rectangle, à l’exclusion des côtés droits et inférieurs si aucune transformation universelle n’est définie pour le contexte de périphérique donné.

Si une transformation universelle a été définie à l’aide de la fonction [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) ou [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) , le système inclut les bords droits et inférieurs.

En plus de dessiner un rectangle traditionnel, vous pouvez dessiner des rectangles avec des angles arrondis. La fonction [**roundRect**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect) nécessite que l’application fournisse les coordonnées des angles inférieur gauche et supérieur droit, ainsi que la largeur et la hauteur de l’ellipse utilisée pour arrondir chaque angle.

Les applications peuvent utiliser les fonctions suivantes pour manipuler des rectangles.



| Fonction                         | Description                                                        |
|----------------------------------|--------------------------------------------------------------------|
| [**FillRect**](/windows/desktop/api/Winuser/nf-winuser-fillrect)     | Repeint l’intérieur d’un rectangle.                              |
| [**FrameRect**](/windows/desktop/api/Winuser/nf-winuser-framerect)   | Redessine les côtés d’un rectangle.                                  |
| [**InvertRect**](/windows/desktop/api/Winuser/nf-winuser-invertrect) | Inverse les couleurs qui apparaissent à l’intérieur d’un rectangle. |



 

 

 
