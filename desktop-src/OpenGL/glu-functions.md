---
title: GLU, fonctions
description: GLU, fonctions
ms.assetid: 8304a291-1a26-42bc-8887-386732980722
keywords:
- OpenGL, GLU, fonctions de la bibliothèque
- Référence OpenGL, fonctions de la bibliothèque GLU
- Bibliothèque GLU, fonctions
- Utilitaire OpenGL (GLU), fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4483b364d2d67daff0bbc04b9a30cd7cdb3059f3977f763b247f77be74d62f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777699"
---
# <a name="glu-functions"></a>GLU, fonctions

Cette section comprend des pages de référence, classées par ordre alphabétique, pour toutes les fonctions de la bibliothèque d’utilitaires OpenGL. Pour obtenir des informations générales sur ces fonctions, consultez [OpenGL Utility Library](opengl-utility-library.md).



| Fonction                                                                                           | Description                                                                                              |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**gluBeginCurve**](glubegincurve.md), [ **gluEndCurve**](gluendcurve.md)                         | Délimitez une définition de courbe B-spline rationnelle ([NURBS](using-nurbs-curves-and-surfaces.md)) non uniforme. |
| [**gluBeginPolygon**](glubeginpolygon.md), [ **gluEndPolygon**](gluendpolygon.md)                 | Délimiter une description de polygone.                                                                           |
| [**gluBeginSurface**](glubeginsurface.md), [ **gluEndSurface**](gluendsurface.md)                 | Délimiter une définition de surface NURBS.                                                                      |
| [**gluBeginTrim**](glubegintrim.md), [ **gluEndTrim**](gluendtrim.md)                             | Délimiter une définition de boucle de suppression NURBS.                                                                |
| [**gluBuild1DMipmaps**](glubuild1dmipmaps.md)                                                     | Crée des des mipmaps 1D.                                                                                     |
| [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)                                                     | Crée un des mipmaps 2D.                                                                                     |
| [**gluCylinder**](glucylinder.md)                                                                 | Dessine un cylindre.                                                                                        |
| [**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md)                                           | Détruit un objet NURBS.                                                                                 |
| [**gluDeleteQuadric**](gludeletequadric.md)                                                       | Détruit un objet quadric.                                                                               |
| [**gluDeleteTess**](gludeletetess.md)                                                             | Détruit un objet de pavage.                                                                          |
| [**gluDisk**](gludisk.md)                                                                         | Dessine un disque.                                                                                            |
| [**gluErrorString**](gluerrorstring.md)                                                           | Produit une chaîne d’erreur à partir d’un code d’erreur OpenGL ou GLU. La chaîne d’erreur est ANSI uniquement.                |
| [**gluGetNurbsProperty**](glugetnurbsproperty.md)                                                 | Récupère une propriété NURBS.                                                                              |
| [**gluGetString**](glugetstring.md)                                                               | Récupère une chaîne qui décrit le numéro de version de GLU ou les appels d’extension GLU pris en charge.               |
| [**gluGetTessProperty**](glugettessproperty.md)                                                   | Récupère une propriété d’objet de pavage.                                                                |
| [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md)                                         | Charge les matrices d’échantillonnage et d’élimination NURBS.                                                               |
| [**gluLookAt**](glulookat.md)                                                                     | Définit une transformation d’affichage.                                                                        |
| [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)                                                 | Crée un objet NURBS.                                                                                  |
| [**gluNewQuadric**](glunewquadric.md)                                                             | Crée un objet quadric.                                                                                |
| [**gluNewTess**](glunewtess.md)                                                                   | Crée un objet de pavage.                                                                           |
| [**gluNextContour**](glunextcontour.md)                                                           | Marque le début d’un autre contour.                                                                  |
| [*gluNurbsCallback*](glunurbs.md)                                                                 | Définit un rappel pour un objet NURBS.                                                                   |
| [**gluNurbsCurve**](glunurbscurve.md)                                                             | Définit la forme d’une courbe NURBS.                                                                      |
| [**gluNurbsProperty**](glunurbsproperty.md)                                                       | Définit une propriété NURBS.                                                                                   |
| [**gluNurbsSurface**](glunurbssurface.md)                                                         | Définit la forme d’une surface NURBS.                                                                    |
| [**gluOrtho2D**](gluortho2d.md)                                                                   | Définit une matrice de projection orthographique 2D.                                                            |
| [**gluPartialDisk**](glupartialdisk.md)                                                           | Dessine un arc de disque.                                                                                  |
| [**gluPerspective**](gluperspective.md)                                                           | Configure une matrice de projection de perspective.                                                                 |
| [**gluPickMatrix**](glupickmatrix.md)                                                             | Définit une région de prélèvement.                                                                                |
| [**gluProject**](gluproject.md)                                                                   | Cartes les coordonnées de l’objet aux coordonnées de la fenêtre.                                                           |
| [**gluPwlCurve**](glupwlcurve.md)                                                                 | Décrit une courbe de rognage de NURBS linéaire par morceaux.                                                       |
| [*gluQuadricCallback*](gluquadric.md)                                                             | Définit un rappel pour un objet quadric.                                                                 |
| [**gluQuadricDrawStyle**](gluquadricdrawstyle.md)                                                 | Spécifie le style de dessin souhaité pour Quadrics.                                                           |
| [**gluQuadricNormals**](gluquadricnormals.md)                                                     | Spécifie le type de normal à utiliser pour Quadrics.                                              |
| [**gluQuadricOrientation**](gluquadricorientation.md)                                             | Spécifie l’orientation à l’intérieur ou à l’extérieur de Quadrics.                                                    |
| [**gluQuadricTexture**](gluquadrictexture.md)                                                     | Spécifie si les Quadrics doivent être texturées.                                                           |
| [**gluScaleImage**](gluscaleimage.md)                                                             | Met à l’échelle une image à une taille arbitraire.                                                                    |
| [**gluSphere**](glusphere.md)                                                                     | Dessine une sphère.                                                                                          |
| [**gluTessBeginContour**](glutessbegincontour.md), [ **gluTessEndContour**](glutessendcontour.md) | Délimitez une description du contour.                                                                           |
| [**gluTessBeginPolygon**](glutessbeginpolygon.md), [ **gluTessEndPolygon**](glutessendpolygon.md) | Délimiter une description de polygone.                                                                           |
| [*gluTessCallback*](glutess.md)                                                                   | Définit un rappel pour un objet de pavage.                                                            |
| [**gluTessNormal**](glutessnormal.md)                                                             | Spécifie un normal pour un polygone.                                                                        |
| [**gluTessProperty**](glutessproperty.md)                                                         | Définit la propriété d’un objet de pavage.                                                              |
| [**gluTessVertex**](glutessvertex.md)                                                             | Spécifie un sommet sur un polygone.                                                                         |
| [**gluUnProject**](gluunproject.md)                                                               | Cartes les coordonnées de la fenêtre aux coordonnées de l’objet.                                                           |



 

 

 




