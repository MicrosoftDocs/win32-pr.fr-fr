---
title: Portage des arcs et des cercles
description: Avec OpenGL, les arcs remplis et les cercles sont dessinés avec les mêmes appels que des arcs et des cercles sans remplissage. Le tableau suivant répertorie les fonctions arc et Circle de l’IRIS GL et leurs fonctions OpenGL équivalentes (GLU).
ms.assetid: b3458192-9cb6-4376-8136-45467584d3d4
keywords:
- Portage du grand livre de l’IRIS, arcs
- Portage à partir de IRIS GL, arcs
- portage vers OpenGL à partir de IRIS GL, arcs
- Portage OpenGL à partir de IRIS GL, arcs
- fonctions de dessin, arcs
- Portage de l’IRIS dans le GL, cercles
- Portage à partir de IRIS GL, cercles
- portage vers OpenGL à partir de IRIS GL, cercles
- Portage OpenGL à partir de IRIS GL, cercles
- fonctions de dessin, cercles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72298caac6495d39c8a5d6cf7441b3b3664180d9e5396fb22106d9e138019b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936218"
---
# <a name="porting-arcs-and-circles"></a>Portage des arcs et des cercles

Avec OpenGL, les arcs remplis et les cercles sont dessinés avec les mêmes appels que des arcs et des cercles sans remplissage. Le tableau suivant répertorie les fonctions arc et Circle de l’IRIS GL et leurs fonctions OpenGL équivalentes (GLU).



| Fonction IRIS GL | Fonction OpenGL                          | Signification                 |
|------------------|------------------------------------------|-------------------------|
| **arcarcf**      | [**gluPartialDisk**](glupartialdisk.md) | Dessine un arc.           |
| **circcircf**    | [**gluDisk**](gludisk.md)               | Dessine un cercle ou un disque. |



 

Vous pouvez effectuer quelques opérations avec des arcs et cercles OpenGL que vous ne pouvez pas faire avec IRIS GL. OpenGL appelle les courbes et les cercles, les disques et les disques partiels, respectivement.

Lorsque vous portez des arcs et des cercles, gardez à l’esprit les points suivants sur OpenGL :

-   Les angles sont mesurés en degrés, et non en dixièmes de degrés.
-   L’angle de début est mesuré à partir de l’axe y positif, et non à partir de l’axe x.
-   L’angle de balayage est désormais dans le sens inverse des aiguilles d’une montre.

??

 

 




