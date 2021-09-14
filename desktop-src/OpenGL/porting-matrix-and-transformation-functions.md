---
title: Fonctions de transformation et de matrice de Portage
description: IRIS GL et OpenGL gèrent les matrices et les transformations de la même manière.
ms.assetid: 732ba65a-d776-43ea-a605-0f59209c9a46
keywords:
- Portage de l’IRIS dans le GL, matrices
- Portage à partir de IRIS GL, matrices
- portage vers OpenGL à partir de IRIS GL, matrices
- Portage OpenGL à partir de IRIS GL, matrices
- matrices
- Portage de l’IRIS dans le GL, transformations
- Portage à partir de IRIS GL, transformations
- portage vers OpenGL à partir de IRIS GL, transformations
- Portage OpenGL depuis IRIS GL, transformations
- transformations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c6219640085370202b8dbebad9a2e9d4992b4f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127020965"
---
# <a name="porting-matrix-and-transformation-functions"></a>Fonctions de transformation et de matrice de Portage

IRIS GL et OpenGL gèrent les matrices et les transformations de la même manière. Toutefois, il existe plusieurs différences à garder à l’esprit lors du Portage de code à partir de IRIS GL :

-   Dans OpenGL, vous êtes toujours en mode double matrice ; Il n’existe pas de mode à matrice unique.
-   Les angles sont mesurés en degrés, au lieu de dixièmes de degrés.
-   Les appels de matrice de projection, comme [**glFrustum**](glfrustum.md) et [**glOrtho**](glortho.md), s’multiplient désormais par la matrice actuelle, au lieu d’être chargées dans la matrice actuelle.
-   La fonction OpenGL, [**glRotate**](glrotate.md), est très différente de la **rotation**. Vous pouvez effectuer une rotation autour d’un axe arbitraire, au lieu d’être limité aux axes x, y et z. Par exemple, vous pouvez traduire :

    ```C++
    rotate(200*(i+1), 'z');
    ```

    

    to:

    ```C++
    glRotate(.1*(200*(i+1), 0.0, 0.0, 1.0);
    ```

    

    Lors de la conversion de **Rotate** en **glRotate** , vous basculez vers degrés à partir de dixièmes de degrés et remplacez « z » par un vecteur pour l’axe z.

-   OpenGL n’a pas d’équivalent à la fonction **polarview** . Vous pouvez le remplacer facilement par une traduction et trois rotations. Par exemple, vous pouvez traduire :

    ```C++
    polarview(distance, azimuth, incidence, twist);
     
    ```

    

    to:

    ```C++
    glTranslatef( 0.0, 0.0, -distance); 
    glRotatef( -twist * 10.0, 0.0, 0.0, 1.0); 
    glRotatef( -incidence * 10.0, 1.0, 0.0, 0.0); 
    glRotatef( -azimuth * 10.0, 0.0, 0.0, 1.0);
    ```

    

Le tableau suivant répertorie les fonctions de matrice OpenGL et leurs fonctions équivalentes de la comptabilité IRIS.



| Fonction IRIS GL              | Fonction OpenGL                                                                        | Signification                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **mmode**                     | [**glMatrixMode**](glmatrixmode.md)                                                   | Définit le mode matrice actuel.                                                                                                                                                      |
|                               | [**glLoadIdentity**](glloadidentity.md)                                               | Remplace la matrice actuelle par la matrice d’identité.                                                                                                                              |
| **loadmatrix**                | [**glLoadMatrixf**](glloadmatrix.md),[**glLoadMatrixd**](glloadmatrix.md)<br/> | Remplace la matrice actuelle par la matrice spécifiée.                                                                                                                             |
| **multmatrix**                | [**glMultMatrixf**](glmultmatrix.md),[**glMultMatrixd**](glmultmatrix.md)<br/> | Multiplie la matrice actuelle par la matrice spécifiée (Notez que **multmatrix** prémultiplié).                                                                            |
| **mapw**, **mapw2**           | [**gluUnProject**](gluunproject.md)                                                   | Projette les coordonnées de l’espace universel dans l’espace de l’objet (voir aussi [**gluProject**](gluproject.md)).                                                                                  |
| **Ortho**                     | [**glOrtho**](glortho.md)                                                             | Multiplie la matrice actuelle par une matrice de projection orthographique.                                                                                                                |
| **ortho2**                    | [**gluOrtho2D**](gluortho2d.md)                                                       | Définit une matrice de projection orthographique à deux dimensions.                                                                                                                      |
| **perception**               | [**gluPerspective**](gluperspective.md)                                               | Définit une matrice de projection de perspective.                                                                                                                                       |
| **picksize**                  | [**gluPickMatrix**](glupickmatrix.md)                                                 | Définit une région de prélèvement.                                                                                                                                                      |
| **popmatrix**                 | [**glPopMatrix**](glpopmatrix.md)                                                     | Exécute un pop de la pile de matrice actuelle, en remplaçant la matrice actuelle par celle qui est située au-dessous.                                                                                                 |
| **pushmatrix**                | [**glPushMatrix**](glpushmatrix.md)                                                   | Exécute un push de la pile de matrice actuelle d’une unité, en dupliquant la matrice actuelle.                                                                                                       |
| **rotation**,**rot**<br/> | [**glRotated**](glrotate.md),[**glRotatef**](glrotate.md)<br/>                 | Fait pivoter le système de coordonnées actuel d’après l’origine par rapport au point donné. Notez que la **rotation pivotait** uniquement sur les axes x, y et z. |
| **scale**                     | [**glScaled**](glscale.md),[**glScalef**](glscale.md)<br/>                     | Multiplie la matrice actuelle par une matrice de mise à l’échelle.                                                                                                                                 |
| **traduire**                 | [**glTranslatef**](gltranslate.md),[**glTranslated**](gltranslate.md)<br/>     | Déplace l’origine du système de coordonnées jusqu’au point spécifié, en multipliant la matrice actuelle par une matrice de translation.                                                              |
| **fenetre**                    | [**glFrustum**](glfrustum.md)                                                         | Coordonnées données pour les plans de découpage, multiplie la matrice actuelle par une matrice de perspective.                                                                                  |



 

OpenGL a trois modes de matrice, qui sont définis avec [**glMatrixMode**](glmatrixmode.md). Le tableau suivant répertorie les modes disponibles en tant que paramètres pour **glMatrixMode**.



| Mode matriciel du GL de l’IRIS | Mode OpenGL    | Signification                                  | Profondeur minimale de la pile |
|---------------------|----------------|------------------------------------------|-----------------|
| **MTEXTURE**        | \_texture GL    | Opère sur la pile de matrices de texture.    | 2               |
| **MVIEWING**        | \_MODELVIEW GL  | Opère sur la pile de matrices de la vue de modèle. | 32              |
| **MPROJECTION**     | \_projection GL | Opère sur la pile de matrice de projection. | 2               |



 

 

 





