---
title: Variables d’État OpenGL
description: Les rubriques suivantes répertorient les noms des variables d’État qui peuvent être interrogées.
ms.assetid: f4bc4ec1-a529-4b9e-84af-94caa0ef7131
keywords:
- Variables d’État OpenGL
- variables d’État, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36dee51ba7726277832d94eaf336d03d3c579189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106536059"
---
# <a name="opengl-state-variables"></a>Variables d’État OpenGL

Les rubriques suivantes répertorient les noms des variables d’État qui peuvent être interrogées :

-   [**Variables d’État pour les valeurs actuelles et les données associées**](state-variables-for-current-values-and-associated-data.md)
-   [**Variables d’état de transformation**](transformation-state-variables.md)
-   [**Variables d’état de coloration**](coloring-state-variables.md)
-   [**Variables d’état d’éclairage**](lighting-state-variables.md)
-   [**Variables d’état de pixellisation**](rasterization-state-variables.md)
-   [**Variables d’état de texturation**](texturing-state-variables.md)
-   [**Opérations de pixel**](pixel-operations.md)
-   [**Variables d’état de contrôle trame**](framebuffer-control-state-variables.md)
-   [**Variables d’état de pixel**](pixel-state-variables.md)
-   [**Variables d’état de l’évaluateur**](evaluator-state-variables.md)
-   [**Variables d’état d’indicateur**](hint-state-variables.md)
-   [**Variables d’État dépendantes de l’implémentation**](implementation-dependent-state-variables.md)
-   [**Variables d’état de Pixel-Depth dépendant de l’implémentation**](implementation-dependent-pixel-depth-state-variables.md)
-   [**Variables d’État diverses**](miscellaneous-state-variables.md)

Pour chaque variable, la rubrique répertorie une description, un groupe d’attributs, une valeur initiale ou minimale et la fonction [**glGet \***](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) suggérée à utiliser pour l’obtenir.

Les variables d’État que vous pouvez obtenir à l’aide de [**glGetBooleanv**](glgetbooleanv.md), [**glGetIntegerv**](glgetintegerv.md), [**glGetFloatv**](glgetfloatv.md)ou [**glGetDoublev**](glgetdoublev.md) sont répertoriées avec simplement l’une de ces functionsthe qui est la plus appropriée pour le type de données à retourner. Vous ne pouvez pas obtenir ces variables d’État à l’aide de [**glIsEnabled**](glisenabled.md). Toutefois, vous pouvez obtenir des variables d’État pour lesquelles **glIsEnabled** est listé comme fonction de requête avec **glGetBooleanv**, **glGetIntegerv**, **glGetFloatv** et **glGetDoublev**. Vous pouvez obtenir des variables d’État pour lesquelles toute autre fonction est listée en tant que fonction de requête uniquement à l’aide de cette fonction. Si aucun groupe d’attributs n’est listé, la variable n’appartient à aucun groupe. Toutes les variables d’État que vous pouvez interroger, à l’exception de celles qui sont dépendantes de l’implémentation, ont des valeurs initiales. Pour déterminer la valeur initiale d’une variable pour laquelle aucune valeur initiale n’est indiquée, consultez la référence de cette variable ou la

*Manuel de référence OpenGL*.

 

 




