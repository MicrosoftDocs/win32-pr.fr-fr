---
title: Portage de courbes NURBS
description: Les fonctions OpenGL de dessin des courbes NURBS sont très similaires aux fonctions de l’IRIS dans le GL. Vous spécifiez des séquences de nœuds et des points de contrôle à l’aide d’une fonction gluNurbsCurve, qui doit être contenue dans une paire gluBeginCurve/gluEndCurve.
ms.assetid: 954e8029-06bd-4072-9b84-53ecba1d05da
keywords:
- Portage de l’IRIS dans le GL, courbes NURBS
- Portage à partir de IRIS GL, courbes NURBS
- portage vers OpenGL à partir de IRIS GL, courbes NURBS
- Portage OpenGL à partir de IRIS GL, courbes NURBS
- Courbes NURBS
- courbes
- Portage de l’IRIS dans le GL, courbes
- Portage à partir de IRIS GL, courbes
- portage vers OpenGL à partir de IRIS GL, courbes
- Portage OpenGL à partir de IRIS GL, courbes
- NURBS (non-uniform rational B-spline)
- B-spline rationnelle non uniforme (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9aa43bcc40c2b6a93eb5690abe4265f792a58a2520e579d536a08520ca4f29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132398"
---
# <a name="porting-nurbs-curves"></a>Portage de courbes NURBS

Les fonctions OpenGL de dessin des courbes NURBS sont très similaires aux fonctions de l’IRIS dans le GL. Vous spécifiez des séquences de nœuds et des points de contrôle à l’aide d’une fonction [**gluNurbsCurve**](glunurbscurve.md) , qui doit être contenue dans une paire de [](glubegincurve.md)  /  [**gluEndCurve**](gluendcurve.md) gluBeginCurve.

Le tableau suivant répertorie les fonctions IRIS GL permettant de dessiner des courbes NURBS et leurs fonctions OpenGL équivalentes.



| Fonction IRIS GL | Fonction OpenGL                        | Signification                     |
|------------------|----------------------------------------|-----------------------------|
| **bgncurve**     | [**gluBeginCurve**](glubegincurve.md) | Commence une définition de courbe.  |
| **nurbscurve**   | [**gluNurbsCurve**](glunurbscurve.md) | Spécifie les attributs de courbe. |
| **endcurve**     | [**gluEndCurve**](gluendcurve.md)     | Met fin à une définition de courbe.    |



 

Associez la position, la texture et les coordonnées de couleur en les présentant comme un **gluNurbsCurve** distinct à l’intérieur de la paire Begin/End. Vous ne pouvez pas effectuer plus d’un appel à **gluNurbsCurve** pour chaque élément de couleur, de position et de texture dans une paire **gluBeginCurve/gluEndCurve** unique. Vous devez effectuer un seul appel pour décrire la position de la courbe (une description du GL \_ Map1 \_ vertex \_ 3 ou du GL \_ Map1 \_ vertex \_ 4). Quand vous appelez **gluEndCurve**, la courbe est fractionnée en segments de ligne, puis rendue.

Le tableau suivant répertorie les types de courbes NURBS de l’IRIS et de l’OpenGL.



| Type de GL IRIS | Type OpenGL                  | Signification                                 |
|--------------|------------------------------|-----------------------------------------|
| N \_ v3d       | Map1 du GL- \_ \_ vertex \_ 3          | Courbe polynomiale.                       |
| N \_ V3DR      | Map1 du GL- \_ \_ vertex \_ 4          | Courbe rationnelle.                         |
|              | \_Repère de \_ texture \_ Map1 GL\_\* | Les points de contrôle sont des coordonnées de texture. |
|              | Map1 GL- \_ \_ normal             | Les points de contrôle sont normaux.             |



 

Pour plus d’informations sur les types d’évaluateurs disponibles, consultez [**glMap1**](glmap1.md).

??

 

 




