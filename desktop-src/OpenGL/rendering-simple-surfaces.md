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
ms.openlocfilehash: 4010a9cc1c0cfac58f1a99572ebae43233dce552237c17f42d66cc1c50013986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776829"
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

 

 




