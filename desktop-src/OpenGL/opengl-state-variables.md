---
title: Variables d’État OpenGL
description: Les rubriques suivantes répertorient les noms des variables d’État qui peuvent être interrogées.
ms.assetid: f4bc4ec1-a529-4b9e-84af-94caa0ef7131
keywords:
- Variables d’État OpenGL
- variables d’État, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8164cebd065a69f923e908a26bf2ce80357312c73c35f12bc2066c63db91eff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936768"
---
# <a name="opengl-state-variables"></a>Variables d’État OpenGL

Les rubriques suivantes répertorient les noms des variables d’État qui peuvent être interrogées :

-   [**Variables d’état pour les valeurs actuelles et les données associées**](state-variables-for-current-values-and-associated-data.md)
-   [**Transformation, variables d’état**](transformation-state-variables.md)
-   [**Coloration, variables d’état**](coloring-state-variables.md)
-   [**Éclairage, variables d’état**](lighting-state-variables.md)
-   [**Rastérisation, variables d’état**](rasterization-state-variables.md)
-   [**Texture, variables d’état**](texturing-state-variables.md)
-   [**Pixel, opérations**](pixel-operations.md)
-   [**Contrôle Framebuffer, variables d’état**](framebuffer-control-state-variables.md)
-   [**Pixel, variables d’état**](pixel-state-variables.md)
-   [**Évaluateur, variables d’état**](evaluator-state-variables.md)
-   [**Hint, variables d’état**](hint-state-variables.md)
-   [**Variables d’état dépendantes de l’implémentation**](implementation-dependent-state-variables.md)
-   [**Densité de pixels, variables d’état dépendantes de l’implémentation**](implementation-dependent-pixel-depth-state-variables.md)
-   [**Variables d’état diverses**](miscellaneous-state-variables.md)

Pour chaque variable, la rubrique répertorie une description, un groupe d’attributs, une valeur initiale ou minimale et la fonction [**glGet \***](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) suggérée à utiliser pour l’obtenir.

Les variables d’État que vous pouvez obtenir à l’aide de [**glGetBooleanv**](glgetbooleanv.md), [**glGetIntegerv**](glgetintegerv.md), [**glGetFloatv**](glgetfloatv.md)ou [**glGetDoublev**](glgetdoublev.md) sont répertoriées avec simplement l’une de ces functionsthe qui est la plus appropriée pour le type de données à retourner. Vous ne pouvez pas obtenir ces variables d’État à l’aide de [**glIsEnabled**](glisenabled.md). Toutefois, vous pouvez obtenir des variables d’État pour lesquelles **glIsEnabled** est listé comme fonction de requête avec **glGetBooleanv**, **glGetIntegerv**, **glGetFloatv** et **glGetDoublev**. Vous pouvez obtenir des variables d’État pour lesquelles toute autre fonction est listée en tant que fonction de requête uniquement à l’aide de cette fonction. Si aucun groupe d’attributs n’est listé, la variable n’appartient à aucun groupe. Toutes les variables d’État que vous pouvez interroger, à l’exception de celles qui sont dépendantes de l’implémentation, ont des valeurs initiales. Pour déterminer la valeur initiale d’une variable pour laquelle aucune valeur initiale n’est indiquée, consultez la référence de cette variable ou la

*Manuel de référence OpenGL*.

 

 




