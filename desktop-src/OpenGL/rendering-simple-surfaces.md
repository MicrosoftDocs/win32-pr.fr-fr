---
title: Rendu de surfaces simples
description: La bibliothèque GLU comprend un ensemble de fonctions permettant de dessiner différentes surfaces simples (sphères, cylindres, disques et parties de disques) dans divers styles et orientations. Ces fonctions sont décrites en détail dans le manuel de référence OpenGL.
ms.assetid: 403bdf8d-de4c-49e2-87d0-11109061b4c2
keywords:
- Utilitaire OpenGL (GLU), surfaces simples
- GLU (utilitaire OpenGL), surfaces simples
- surfaces simples OpenGL
- Utilitaire OpenGL (GLU), sphères
- GLU (utilitaire OpenGL), sphères
- sphère OpenGL
- Utilitaire OpenGL (GLU), cylindres
- GLU (utilitaire OpenGL), cylindres
- cylindres OpenGL
- Utilitaire OpenGL (GLU), disques
- GLU (utilitaire OpenGL), disques
- disques OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab766c661f89cbdec30b3295dfef8dc85b59f7fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380417"
---
# <a name="rendering-simple-surfaces"></a>Rendu de surfaces simples

La bibliothèque GLU comprend un ensemble de fonctions permettant de dessiner différentes surfaces simples (sphères, cylindres, disques et parties de disques) dans divers styles et orientations. Ces fonctions sont décrites en détail dans le *Manuel de référence OpenGL*.

**Pour afficher des surfaces simples**

1.  Créez un objet quadric avec [**gluNewQuadric**](glunewquadric.md).

    Pour supprimer cet objet une fois que vous avez fini de l’utiliser, utilisez [**gluDeleteQuadric**](gludeletequadric.md).

2.  Spécifiez le style de rendu souhaité, comme indiqué ci-dessous, avec la fonction appropriée (sauf si vous êtes satisfait des valeurs par défaut) :
    -   Indique si les normales de surface doivent être générées et, le cas échéant, s’il doit y avoir une normale par vertex ou une normale par face : [ **gluQuadricNormals**](gluquadricnormals.md)
    -   Indique si des coordonnées de texture doivent être générées : [ **gluQuadricTexture**](gluquadrictexture.md)
    -   Le côté de la quadric doit être considéré comme extérieur et l’intérieur : [ **gluQuadricOrientation**](gluquadricorientation.md)
    -   Indique si le quadric doit être dessiné sous la forme d’un ensemble de polygones, de lignes ou de points : [ **gluQuadricDrawStyle**](gluquadricdrawstyle.md)
3.  Après avoir spécifié le style de rendu, appelez la fonction de rendu pour le type souhaité d’objet quadric : [**gluSphere**](glusphere.md), [**gluCylinder**](glucylinder.md), [**gluDisk**](gludisk.md)ou [**gluPartialDisk**](glupartialdisk.md).

    Si une erreur se produit pendant le rendu, la fonction de gestion des erreurs que vous avez spécifiée avec [*gluQuadricCallBack*](gluquadric.md) est appelée.

Utilisez les arguments *\* RADIUS*, *Height* et similaires plutôt que la fonction [**glScale**](glscale.md) pour mettre à l’échelle les Quadrics, afin de ne pas avoir à renormaliser les normales de longueur d’unité générées. Pour forcer les calculs d’éclairage à une granularité plus fine, en particulier si le matériau specularity est élevé, affectez aux *boucles* et aux arguments des *piles* des valeurs autres que 1.

 

 




