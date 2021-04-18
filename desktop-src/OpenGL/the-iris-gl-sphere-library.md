---
title: Bibliothèque de sphères du GL IRIS
description: OpenGL ne prend pas en charge la bibliothèque de sphères du GL IRIS. Vous pouvez remplacer vos appels de la bibliothèque de sphères par des routines Quadrics à partir de la bibliothèque GLU. Pour plus d’informations sur la bibliothèque GLU, consultez le Guide de programmation Open GL et la bibliothèque de l’utilitaire OpenGL.
ms.assetid: 2b7e6a3d-d2d0-4b54-8dff-8c4d6b113007
keywords:
- Portage du GL IRIS, bibliothèque Sphere
- Portage à partir de IRIS GL, bibliothèque de sphères
- portage vers OpenGL à partir de IRIS GL, bibliothèque de sphères
- Portage OpenGL depuis IRIS GL, bibliothèque de sphères
- fonctions de dessin, bibliothèque de sphères
- bibliothèque de sphères
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586974c5874aee73121e536cbadca4564a18c250
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310361"
---
# <a name="the-iris-gl-sphere-library"></a>Bibliothèque de sphères du GL IRIS

OpenGL ne prend pas en charge la bibliothèque de sphères du GL IRIS. Vous pouvez remplacer vos appels de la bibliothèque de sphères par des routines Quadrics à partir de la bibliothèque GLU. Pour plus d’informations sur la bibliothèque GLU, consultez le *Guide de programmation Open GL* et la bibliothèque de l' [utilitaire OpenGL](opengl-utility-library.md).

Le tableau suivant répertorie les fonctions Quadrics OpenGL.



| Fonction OpenGL                                        | Signification                                                          |
|--------------------------------------------------------|------------------------------------------------------------------|
| [**gluNewQuadric**](glunewquadric.md)                 | Crée un nouvel objet quadric.                                    |
| [**gluDeleteQuadric**](gludeletequadric.md)           | Supprime un objet quadric.                                        |
| [*gluQuadricCallback*](gluquadric.md)                 | Associe un rappel à un objet quadric, pour la gestion des erreurs. |
| [**gluQuadricNormals**](gluquadricnormals.md)         | Spécifie les normales : aucune normale, une par face ou une par vertex.  |
| [**gluQuadricOrientation**](gluquadricorientation.md) | Spécifie la direction des normales : vers l’extérieur ou vers l’intérieur.               |
| [**gluQuadricTexture**](gluquadrictexture.md)         | Active ou désactive la génération des coordonnées de texture.                   |
| [**gluQuadricDrawstyle**](gluquadricdrawstyle.md)     | Spécifie le style de dessin : polygones, lignes, points, etc.     |
| [**gluSphere**](glusphere.md)                         | Dessine une sphère.                                                  |
| [**gluCylinder**](glucylinder.md)                     | Dessine un cylindre ou un cône.                                        |
| [**gluPartialDisk**](glupartialdisk.md)               | Dessine un arc.                                                    |
| [**gluDisk**](gludisk.md)                             | Dessine un cercle ou un disque.                                          |



 

Vous pouvez utiliser un objet quadric pour tous les Quadrics que vous souhaitez afficher de la même manière. L’exemple de code suivant utilise deux objets quadric pour dessiner quatre Quadrics, deux d’entre eux texturés.


```C++
GLUquadricObj    *texturedQuad, *plainQuad; 
 
texturedQuad = gluNewQuadric(void); 
gluQuadricTexture(texturedQuad, GL_TRUE); 
gluQuadricOrientation(texturedQuad, GLU_OUTSIDE); 
gluQuadricDrawStyle(texturedQuad, GLU_FILL); 
 
plainQuad = gluNewQuadric(void); 
gluQuadricDrawStyle(plainQuad, GLU_LINE); 
 
glColor3f (1.0, 1.0, 1.0); 
 
gluSphere(texturedQuad, 5.0, 20, 20); 
glTranslatef(10.0, 10.0, 0.0); 
gluCylinder(texturedQuad, 2.5, 5, 5, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluDisk(plainQuad, 2.0, 5.0, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluSphere(plainQuad, 5.0, 20, 20);
```



 

 




