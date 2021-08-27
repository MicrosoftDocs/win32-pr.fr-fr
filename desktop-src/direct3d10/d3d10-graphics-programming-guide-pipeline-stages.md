---
description: Le pipeline programmable Direct3D 10 est conçu pour générer des graphiques pour les applications de jeu en temps réel. Le diagramme suivant illustre le passage de données d’entrée à la sortie à travers chacune des étapes programmables.
ms.assetid: 3ead6c7c-c7cc-48f1-81d5-b4b67326d610
title: Étapes de pipeline (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 942e2594f1f2eeb83f92b3ee517804a68b6074d85bf5c9205828a08e024112df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119973"
---
# <a name="pipeline-stages-direct3d-10"></a>Étapes de pipeline (Direct3D 10)

Le pipeline programmable Direct3D 10 est conçu pour générer des graphiques pour les applications de jeu en temps réel. Le diagramme suivant illustre le passage de données d’entrée à la sortie à travers chacune des étapes programmables.

![diagramme du flot de données dans le pipeline programmable Direct3D 10](images/d3d10-pipeline-stages.png)

Toutes les étapes peuvent être configurées à l’aide de l’API. Les étapes comportant des cœurs de nuanceur courants (blocs rectangulaires arrondis) sont programmables à l’aide du langage de programmation HLSL. Comme vous le verrez, cela rend le pipeline extrêmement flexible et adaptable. L’objectif de chacune de ces étapes est indiqué ci-dessous.

-   [Étape d’assembleur d’entrée](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) : l’étape assembleur d’entrée est chargée de fournir des données (triangles, lignes et points) au pipeline.
-   [Étape du nuanceur de vertex](https://www.bing.com/search?q=Vertex-Shader+Stage). Cette étape traite les vertex, généralement par le biais d’opérations de type transformation, application d’apparence et éclairage. Un nuanceur de vertex prend toujours un seul vertex d’entrée et produit un seul vertex de sortie.
-   [Geometry : étape de nuanceur](https://www.bing.com/search?q=Geometry-Shader+Stage) : la phase Geometry-Shader traite les primitives entières. Son entrée est une primitive complète (qui est trois vertex pour un triangle, deux sommets pour une ligne ou un seul vertex pour un point). En outre, chaque primitive peut également inclure les données de vertex pour toutes les primitives adjacentes à un bord. Cela peut inclure au plus trois vertex supplémentaires pour un triangle ou deux sommets supplémentaires pour une ligne. Le nuanceur Geometry prend également en charge l’amplification et la désamplification Geometry limitées. En fonction d’une primitive d’entrée, le nuanceur Geometry peut ignorer la primitive ou émettre une ou plusieurs nouvelles primitives.
-   [Étape de flux de sortie](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md) : l’étape flux-sortie est conçue pour diffuser en continu des données primitives du pipeline vers la mémoire de façon à ce que le rastériseur. Les données peuvent être diffusées vers la sortie et/ou dans le rastériseur. Les données diffusées dans la mémoire peuvent être renvoyées dans le pipeline en tant que données d’entrée ou lues par le processeur.
-   [Étape de rastérisation](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md) : le rastériseur est chargé de découper les primitives, de préparer les primitives pour le nuanceur de pixels et de déterminer comment appeler les nuanceurs de pixels.
-   [Étape du nuanceur de pixels](https://www.bing.com/search?q=Pixel-Shader+Stage). Cette étape reçoit les données interpolées pour une primitive et génère des données par pixel telles que la couleur.
-   [Étape de fusion de sortie](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) : l’étape de fusion de sortie est chargée de combiner différents types de données de sortie (valeurs de nuanceur de pixels, informations de profondeur et de stencil) avec le contenu de la cible de rendu et les mémoires tampons de profondeur/stencil pour générer le résultat final du pipeline.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
