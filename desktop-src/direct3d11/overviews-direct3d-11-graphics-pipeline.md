---
title: Pipeline graphique
description: Cette section décrit le pipeline programmable Direct3D 11.
ms.assetid: 8e7a6f64-0a2b-4ea5-a6a6-7bfb87e27dcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed8e6b0b4d249c46dafe960f4f25a9a7598d6e2c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517525"
---
# <a name="graphics-pipeline"></a>Pipeline graphique

Le pipeline programmable Direct3D 11 est conçu pour générer des graphiques pour les applications de jeu en temps réel. Cette section décrit le pipeline programmable Direct3D 11. Le diagramme suivant illustre le passage de données d’entrée à la sortie à travers chacune des étapes programmables.

![diagramme du flot de données dans le pipeline programmable Direct3D 11](images/d3d11-pipeline-stages.jpg)

Le pipeline Graphics pour Microsoft Direct3D 11 prend en charge les mêmes étapes que le [pipeline graphique Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages), avec des étapes supplémentaires pour prendre en charge les fonctionnalités avancées.

Vous pouvez utiliser le 11API Direct3D pour configurer toutes les étapes. Les étapes qui composent les noyaux de nuanceur courants (blocs rectangulaires arrondis) sont programmables à l’aide du langage de programmation [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) . Comme vous le verrez, cela rend le pipeline extrêmement flexible et adaptable.


## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Étape assembleur d’entrée](d3d10-graphics-programming-guide-input-assembler-stage.md)<br/> | L’API Direct3D 10 et versions ultérieures sépare les zones fonctionnelles du pipeline en étapes ; la première étape du pipeline est l’étape de l’assembleur d’entrée (IA).<br/>                                                                                                                                                                                                                                                                                                                             |
| [Étape nuanceur de sommets](vertex-shader-stage.md)<br/>                                      | L’étape vertex-shader (VS) traite les vertex de l’assembleur d’entrée, en effectuant des opérations par vertex telles que les transformations, l’apparence, la transformation et l’éclairage par vertex. Les nuanceurs vertex fonctionnent toujours sur un vertex d’entrée unique et produisent un seul vertex de sortie. L’étape du nuanceur de sommets doit toujours être active pour que le pipeline s’exécute. Si aucune modification ou transformation de vertex n’est requise, un nuanceur de sommets directs doit être créé et défini sur le pipeline.<br/> |
| [Étapes de pavage](direct3d-11-advanced-stages-tessellation.md)<br/>                 | Le runtime Direct3D 11 prend en charge trois nouvelles étapes qui implémentent la polygonalisation, qui convertit les surfaces de sous-division de faible détail en primitives de détail supérieures sur le GPU. Polygonalisation des vignettes (ou fractionnement) des surfaces de poids fort dans des structures appropriées pour le rendu.<br/>                                                                                                                                                                                                                 |
| [Étape de nuanceur Geometry](geometry-shader-stage.md)<br/>                                  | L’étape Geometry-Shader (GS) exécute un code de nuanceur spécifié par l’application avec des vertex comme entrée et la possibilité de générer des vertex sur la sortie.<br/>                                                                                                                                                                                                                                                                                                                                          |
| [Étape de sortie de flux](d3d10-graphics-programming-guide-output-stream-stage.md)<br/>     | L’objectif de l’étape de flux de sortie est de générer continuellement des données de vertex (ou de diffuser) à partir de l’étape Geometry-Shader (ou de l’étape de nuanceur de vertex si l’étape Geometry-Shader est inactive) vers une ou plusieurs mémoires tampons en mémoire (voir [prise en main avec l’étape Stream-Output](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)). <br/>                                                                                                                       |
| [Étape du rastériseur](d3d10-graphics-programming-guide-rasterizer-stage.md)<br/>           | L’étape de pixellisation convertit les informations vectorielles (composées de formes ou de Primitives) en une image raster (composée de pixels) pour l’affichage de graphiques 3D en temps réel. <br/>                                                                                                                                                                                                                                                                                                 |
| [Étape nuanceur de pixels](pixel-shader-stage.md)<br/>                                        | L’étape de nuanceur de pixels (PS) permet d’effectuer des techniques d’ombrage riches, telles que l’éclairage par pixel et le traitement des messages. Un nuanceur de pixels est un programme qui combine des variables constantes, des données de texture, des valeurs interpolées par vertex et d’autres données pour produire des sorties par pixel. L’étape de rastérisation appelle un nuanceur de pixels une fois pour chaque pixel couvert par une primitive. Toutefois, il est possible de spécifier un nuanceur **null** pour éviter d’exécuter un nuanceur.<br/>                                          |
| [Sortie-étape de fusion](d3d10-graphics-programming-guide-output-merger-stage.md)<br/>     | L’étape de fusion de sortie (OM) génère la couleur de pixel rendue finale à l’aide d’une combinaison de l’état du pipeline, des données de pixels générées par les nuanceurs de pixels, du contenu des cibles de rendu et du contenu des mémoires tampons de profondeur/stencil. L’étape OM est la dernière étape permettant de déterminer les pixels visibles (avec test des stencils de profondeur) et de fusionner les couleurs finales des pixels.<br/>                                                                                              |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nuanceur de calcul](direct3d-11-advanced-stages-compute-shader.md)
</dt> <dt>

[Guide de programmation pour Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

