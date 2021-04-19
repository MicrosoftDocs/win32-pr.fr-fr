---
title: Portage des ensembles de paramètres, des liaisons et des ensembles
description: Portage des ensembles de paramètres, des liaisons et des ensembles
ms.assetid: 971feb14-ed39-4492-a62b-9930bdc506e9
keywords:
- Portage de l’IRIS dans le GL, définitions
- Portage à partir de IRIS GL, définitions
- portage vers OpenGL à partir de IRIS GL, définitions
- Portage OpenGL à partir de IRIS GL, définitions
- Portage des liaisons du GL IRIS, liaisons
- Portage à partir de IRIS GL, liaisons
- portage vers OpenGL à partir de IRIS GL, liaisons
- Portage OpenGL depuis IRIS GL, liaisons
- Portage du grand livre de l’IRIS, ensembles
- Portage à partir de IRIS GL, ensembles
- portage vers OpenGL à partir de IRIS GL, ensembles
- Portage OpenGL à partir de IRIS GL, ensembles
- definitions
- lie
- jeux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f9a88253390ee99f5b5870fd7a09e272f1c549
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509784"
---
# <a name="porting-defs-binds-and-sets"></a>Portage des ensembles de paramètres, des liaisons et des ensembles

OpenGL n’a pas de tables de définitions stockées ; vous ne pouvez pas définir des modèles d’éclairage, du matériel, des textures, des styles de ligne ou des modèles en tant qu’objets distincts, comme vous pouvez le faire dans IRIS GL. Ainsi, OpenGL n’a pas d’équivalent direct aux fonctions suivantes de la comptabilité IRIS :

-   **Imdef** et **lier**
-   **tevdef** et **tevbind**
-   **textdef** et **textbind**
-   **definestyle** et **SetStyle**
-   **defpattern** et **setPattern**

Vous pouvez utiliser des listes d’affichage OpenGL pour imiter le mécanisme de définition/liaison de l’IRIS dans le GL. Par exemple, voici une définition de matériau dans IRIS GL :


```C++
float mat() = { 
    AMBIENT, .1, .1, .1, 
    DIFFUSE, 0, .369, .165, 
    SPECULAR, .5, .5, .5, 
    SHININESS, 10, 
    LMNULL 
}; 
lmdef(DEFMATERIAL, 1, 0, mat); 
lmbind(MATERIAL, 1);
```



L’exemple de code OpenGL suivant définit le même matériau dans une liste d’affichage référencée par le numéro de liste défini par **MYMATERIAL**.


```C++
#define MYMATERIAL 10 
 
GLfloat        mat_amb[] = {.1, .1, .1, 1.0}; 
GLfloat        mat_dif[] = {0, .369, .165, 1.0}; 
GLfloat        mat_spec[] = {.5, .5, .5, 1.0}; 
 
glNewList(MYMATERIAL, GL_COMPILE); 
    glMaterialfv(GL_FRONT, GL_AMBIENT, mat_amb); 
    glMaterialfv(GL_FRONT, GL_DIFFUSE, mat_dif); 
    glMaterialfv(GL_FRONT, GL_SHININESS, 10); 
glEndList(); 
 
glCallList( MYMATERIAL );
```



 

 




