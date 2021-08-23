---
title: Utilisation des évaluateurs
description: Utilisation des évaluateurs
ms.assetid: a5a99d0a-526e-4492-90c4-a6b9fdbdff16
keywords:
- OpenGL, évaluateurs
- évaluateurs OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4bb6808ad1898b0c98906a543291c700ee61257a35befa8886789f3f8b7e31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553489"
---
# <a name="using-evaluators"></a>Utilisation des évaluateurs

Les fonctions de l’évaluateur OpenGL vous permettent d’utiliser un mappage polynomial pour produire des vertex, des normales, des coordonnées de texture et des couleurs. Ces valeurs calculées sont ensuite transmises au pipeline de traitement comme si elles avaient été spécifiées directement. Les fonctions de l’évaluateur sont également la base des fonctions NURBS (B-spline rationnelles non uniformes) qui vous permettent de définir des courbes et des surfaces, comme décrit dans Bibliothèque de l' [utilitaire OpenGL](opengl-utility-library.md).

La première étape de l’utilisation des évaluateurs consiste à définir le mappage polynomial approprié à une ou deux dimensions à l’aide de [**glMap \***](glmap1.md). Vous pouvez ensuite spécifier et évaluer les valeurs de domaine pour ce mappage de l’une des deux manières suivantes :

-   Définissez une série de valeurs de domaine uniformément espacées à mapper à l’aide de [**glMapGrid**](glmapgrid-functions.md) , puis évaluez un sous-ensemble rectangulaire de cette grille avec [**glEvalMesh**](glevalmesh-functions.md). Un point unique de la grille peut être évalué à l’aide de [**glEvalPoint**](glevalpoint.md).
-   Spécifiez explicitement une valeur de domaine souhaitée comme argument, qui évalue les mappages à cette valeur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence des évaluateurs](evaluators-reference.md)
</dt> </dl>

 

 




