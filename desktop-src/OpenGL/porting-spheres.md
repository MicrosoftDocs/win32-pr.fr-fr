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
ms.openlocfilehash: 9f48ac31c0204111173d9eb2d31a3119873ef45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380113"
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

 

 




