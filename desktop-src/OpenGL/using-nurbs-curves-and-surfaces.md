---
title: Utilisation des courbes et des surfaces NURBS
description: Les fonctions NURBS B-spline (NURBS) non uniformes fournissent des descriptions générales et puissantes des courbes et des surfaces en deux et trois dimensions, convertissant les courbes et les surfaces en évaluateurs OpenGL.
ms.assetid: 0b55659d-9fa2-47fc-ae15-0c296bd94dcb
keywords:
- Utilitaire OpenGL (GLU), logique B-spline rationnelle non uniforme (NURBS)
- GLU (utilitaire OpenGL), logique B-spline rationnelle non uniforme (NURBS)
- B-spline rationnelle non uniforme (NURBS) OpenGL
- NURBS (non-uniform rational B-spline) OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c1b366571be7a9210576e78540c77970667aca2f37ec8a092de07edb97493d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932769"
---
# <a name="using-nurbs-curves-and-surfaces"></a>Utilisation des courbes et des surfaces NURBS

Les fonctions NURBS B-spline (NURBS) non uniformes fournissent des descriptions générales et puissantes des courbes et des surfaces en deux et trois dimensions, convertissant les courbes et les surfaces en évaluateurs OpenGL. Les fonctions NURBS peuvent représenter une géométrie dans de nombreux systèmes de conception mécanique assistée par ordinateur. Ils peuvent afficher des courbes et des surfaces dans divers styles, et ils peuvent gérer automatiquement la sous-division adaptative qui tessellates le domaine en triangles plus petits dans les régions de bords haute courbure et à proximité des silhouettes. Les fonctions NURBS sont classées dans les catégories suivantes.

Pour gérer un objet NURBS, utilisez :

-   [**gluNewNurbsRenderer**](glunewnurbsrenderer.md) (créer un objet NURBS)
-   [**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) (supprime un objet NURBS)
-   [*gluNurbsCallback*](glunurbs.md) (établit une fonction de gestion des erreurs)

Pour spécifier les courbes souhaitées, utilisez :

-   [**gluBeginCurve**](glubegincurve.md)
-   [**gluNurbsCurve**](glunurbscurve.md)
-   [**gluEndCurve**](gluendcurve.md)

Pour spécifier les surfaces souhaitées, utilisez :

-   [**gluBeginSurface**](glubeginsurface.md)
-   [**gluNurbsSurface**](glunurbssurface.md)
-   [**gluEndSurface**](gluendsurface.md)

Vous pouvez également spécifier une zone de suppression, qui définit un sous-ensemble du domaine de la surface NURBS à évaluer afin de pouvoir créer des surfaces qui ont des limites lissées ou qui contiennent des trous.

Pour spécifier la région de suppression, utilisez :

-   [**gluBeginTrim**](glubegintrim.md)
-   [**gluPwlCurve**](glupwlcurve.md)
-   [**gluNurbsCurve**](glunurbscurve.md)
-   [**gluEndTrim**](gluendtrim.md)

Comme avec les objets quadric, vous pouvez contrôler le rendu des courbes et des surfaces NURBS. Vous pouvez déterminer les éléments suivants :

-   Indique s’il faut ignorer une courbe ou une surface dont le Polyhedron de contrôle se trouve en dehors de la fenêtre d’affichage actuelle.
-   Longueur maximale (en pixels) des bords des polygones utilisés pour le rendu des courbes et des surfaces.
-   Si vous allez utiliser la matrice de projection, la matrice modelview et la fenêtre d’affichage du serveur OpenGL ou les fournir explicitement avec [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md).

Utilisez [**gluNurbsProperty**](glunurbsproperty.md) pour définir ces propriétés, ou utilisez les valeurs par défaut. Vous pouvez interroger un objet NURBS sur son style de rendu avec [**gluGetNurbsProperty**](glugetnurbsproperty.md).

 

 




