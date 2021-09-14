---
title: Portage des commandes de point de terminaison/fin
description: IRIS GL utilise le paradigme Begin/End mais a une fonction différente pour chaque primitive graphique.
ms.assetid: 4191344b-614a-42d6-8a31-7a708f17371e
keywords:
- Le portage du GL IRIS, commandes BGN/fin
- Portage à partir de commandes IRIS GL, BGN/fin
- portage vers OpenGL à partir des commandes IRIS GL, BGN/fin
- Portage OpenGL à partir des commandes IRIS GL, BGN/fin
- fonctions de dessin, commandes BGN/fin
- commandes BGN/fin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25118d4e5050ea22d4b18fab596dfb9c92f562e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127020973"
---
# <a name="porting-bgnend-commands"></a>Portage des commandes de point de terminaison/fin

IRIS GL utilise le paradigme Begin/End mais a une fonction différente pour chaque primitive graphique. Par exemple, vous utilisez probablement **bgnpolygon** et **endpolygon** pour dessiner des polygones, et **bgnline** et **lignefin** pour dessiner des lignes. Dans OpenGL, vous utilisez la [](glbegin.md)  /  structure [**glEnd**](glend.md) glBegin pour les deux. Dans OpenGL, vous dessinez la plupart des objets géométriques en encadrant une série de fonctions qui spécifient des vertex, des normales, des textures et des couleurs entre les paires d’appels **glBegin** et **glEnd** . Par exemple :

``` syntax
void glBegin( GLenum mode) ; 
   /* vertex list, colors, normals, textures, materials */ 
void glEnd( void );
```

La fonction **glBegin** accepte un paramètre unique qui spécifie le mode dessin, et donc la primitive. Voici un exemple de code OpenGL qui dessine un polygone, puis une ligne :

``` syntax
glBegin( GL_POLYGON ) ; 
   glVertex2f(20.0, 10.0); 
   glVertex2f(10.0, 30.0); 
   glVertex2f(20.0, 50.0); 
   glVertex2f(40.0, 50.0); 
   glVertex2f(50.0, 30.0); 
   glVertex2f(40.0, 10.0); 
glEnd(); 
glBegin( GL_LINES ) ; 
   glVertex2i(100,100); 
   glVertex2i(500,500); 
glEnd();
```

Avec OpenGL, vous dessinez différents objets géométriques en spécifiant des paramètres différents pour [**glBegin**](glbegin.md). Le tableau suivant répertorie les paramètres **GlBegin** OpenGL qui correspondent aux fonctions d’IRIS GL équivalentes.



| Fonction IRIS GL  | Valeur du mode glBegin | Signification                                                                                  |
|-------------------|-----------------------|------------------------------------------------------------------------------------------|
| **bgnpoint**      | POINTS du GL \_            | Points individuels.                                                                       |
| **bgnline**       | \_bande de lignes GL \_       | Série de segments de ligne connectés.                                                       |
| **bgnclosedline** | \_boucle de lignes GL \_        | Série de segments de ligne connectés, avec un segment ajouté entre le premier et le dernier vertex. |
|                   | \_lignes GL             | Paires de vertex interprétées comme des segments de ligne individuels.                               |
| **bgnpolygon**    | Polygone du GL \_           | Limite d’un polygone convexe simple.                                                     |
|                   | \_TRIangles GL         | Triples de vertex interprétés comme des triangles.                                            |
| **bgntmesh**      | \_bande triangulaire GL \_   | Bandes liées de triangles.                                                              |
|                   | \_ventilateur à triangles GL \_     | Ventilateurs liés d’un triangle.                                                                |
|                   | à \_ quatre processeurs GL             | Quadruples de vertex interprétés comme quadrangulaires.                                    |
| **bgnqstrip**     | à \_ quatre \_ bandes GL       | Bandes liées de quadrilatères.                                                         |



 

Pour plus d’informations sur les différences entre les maillages de triangle, les bandes et les fans, consultez [Portage des triangles](porting-triangles.md).

Il n’existe pas de limite au nombre de vertex que vous pouvez spécifier entre une paire [**glBegin**](glbegin.md)  /  [**glEnd**](glend.md) .

En plus de spécifier des vertex à l’intérieur d’une paire **glBegin**  /  **glEnd** , vous pouvez spécifier une valeur normale actuelle, des coordonnées de texture actuelles et une couleur actuelle. Le tableau suivant répertorie les commandes valides à l’intérieur d’une paire **glBegin**  /  **glEnd** .



| Fonction IRIS GL        | Fonction OpenGL                                                      | Signification                                          |
|-------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| **v2**, **v3**, **v4**  | [glVertex](glvertex-functions.md)                                   | Définit les coordonnées des sommets.                         |
| **RGBColor**, **cpack** | [glColor](glcolor-functions.md)                                     | Définit la couleur actuelle.                              |
| **color**               | [glIndex](glindex-functions.md)                                     | Définit l’index de couleur actuel.                        |
| **n3f**                 | [glNormal](glnormal-functions.md)                                   | Définit les coordonnées du vecteur normal.                  |
|                         | [glEvalCoord](glevalcoord-functions.md)                             | Évalue les mappages à un et à deux dimensions activés. |
| **callobj**             | [**glCallList**](glcalllist.md), [ **glCallLists**](glcalllists.md) | Exécute une ou plusieurs listes d’affichage.                        |
| **H2**                  | [glTexCoord](gltexcoord-functions.md)                               | Définit les coordonnées de la texture.                        |
|                         | [glEdgeFlag](gledgeflag-functions.md)                               | Contrôle les bords du dessin.                          |
| **lmbind**              | [glMaterial](glmaterial-functions.md)                               | Définit les propriétés de matériau.                        |



 

> [!Note]
>
> Si vous utilisez une fonction OpenGL différente de celle indiquée dans le tableau précédent à l’intérieur d’une paire [**glBegin**](glbegin.md)  /  [**glEnd**](glend.md) , vous obtiendrez des résultats imprévisibles ou éventuellement une erreur.

 

 

 




