---
title: Portage des sphères
description: En cas de portage vers OpenGL, gardez les points suivants à l’esprit
ms.assetid: ca6bb515-076d-45fc-bcdd-3d71877560fb
keywords:
- Portage de l’IRIS dans le GL, sphères
- Portage à partir de IRIS GL, sphères
- portage vers OpenGL depuis IRIS GL, sphères
- Portage OpenGL depuis IRIS GL, sphères
- fonctions de dessin, sphères
- sphères
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1e0666393e923767d342d215622e0ed58bfa7b1b620e045a0054b31918a7a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358308"
---
# <a name="porting-spheres"></a>Portage des sphères

En cas de portage vers OpenGL, gardez les points suivants à l’esprit :

-   Vous ne pouvez pas contrôler le type de primitives utilisées pour dessiner la sphère. Vous pouvez contrôler la précision de dessin d’une autre façon : utilisez les paramètres tranches et piles. Les tranches sont longitudinales ; les piles sont correspondantes.
-   Les sphères sont dessinées au centre de l’origine. Au lieu de spécifier l’emplacement, comme vous le feriez avec la fonction IRIS GL **sphdraw** , faites précéder un appel à la fonction Glu [**gluSphere**](glusphere.md) d’une traduction.
-   La bibliothèque de sphères n’est pas encore disponible pour OpenGL.

Le tableau suivant répertorie les fonctions IRIS GL pour le dessin des sphères et leurs fonctions GLU équivalentes, le cas échéant.



| Fonction IRIS GL | GLU fonction)                                 | Signification                                       |
|------------------|----------------------------------------------|-----------------------------------------------|
| **sphobj**       | [**gluNewQuadric**](glunewquadric.md)       | Crée un objet Sphere.                  |
| **sphfree**      | [**gluDeleteQuadric**](gludeletequadric.md) | Supprime l’objet Sphere et la mémoire libre utilisés.   |
| **sphdraw**      | [**gluSphere**](glusphere.md)               | Dessine une sphère.                               |
| **sphmode**      |                                              | Définit les attributs de sphère.                       |
| **sphrotmatrix** |                                              | Contrôle l’orientation de la sphère.                  |
| **sphgnpolys**   |                                              | Retourne le nombre de polygones dans la sphère actuelle. |



 

??

 

 




