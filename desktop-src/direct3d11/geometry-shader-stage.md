---
title: Étape de nuanceur Geometry
description: L’étape Geometry-Shader (GS) exécute un code de nuanceur spécifié par l’application avec des vertex comme entrée et la possibilité de générer des vertex sur la sortie.
ms.assetid: F3208862-980E-403F-9154-13B34A882787
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d568b9eb62b2545721acebfda865f7f2553597fb999a3a647164106c836369
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952909"
---
# <a name="geometry-shader-stage"></a>Étape de nuanceur Geometry

L’étape Geometry-Shader (GS) exécute un code de nuanceur spécifié par l’application avec des vertex comme entrée et la possibilité de générer des vertex sur la sortie.

## <a name="the-geometry-shader"></a>Nuanceur Geometry

Contrairement aux nuanceurs de vertex, qui opèrent sur un seul vertex, les entrées du nuanceur Geometry sont les vertex pour une primitive complète (deux sommets pour les lignes, trois vertex pour les triangles ou un seul vertex pour le point). Les nuanceurs de géométrie peuvent également intégrer les données de vertex pour les primitives adjacentes à la périphérie comme entrée (deux sommets supplémentaires pour une ligne, trois supplémentaires pour un triangle). L’illustration suivante montre un triangle et une ligne avec des vertex adjacents.

![illustration d’un triangle et d’une ligne avec des vertex adjacents](images/d3d10-gs.png)

|     | Type                |
|-----|-----------------|
| **TV**  | Sommet de triangle |
| **ALTERNATIF**  | Sommet adjacent |
| **LV**  | Sommet de ligne     |



 

L’étape Geometry-shader peut utiliser la \_ [valeur générée](d3d10-graphics-programming-guide-input-assembler-stage-using.md) par le système SV PrimitiveID qui est générée automatiquement par l’IA. Cela permet de récupérer ou de calculer des données par primitives si vous le souhaitez.

L’étape Geometry-Shader est en charge de la génération de plusieurs vertex formant une seule topologie sélectionnée (les topologies de sortie de l’étape GS disponibles sont : tristrip, linestrip et PointList). Le nombre de primitives émises peut varier librement au sein de n’importe quel appel du nuanceur Geometry, bien que le nombre maximal de vertex pouvant être émis doive être déclaré statiquement. Les longueurs de bande émises à partir d’un appel de nuanceur Geometry peuvent être arbitraires et de nouvelles bandes peuvent être créées via la fonction HLSL [RestartStrip](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-so-restartstrip) .

La sortie du nuanceur Geometry peut être alimentée à l’étape de rastérisation et/ou à une mémoire tampon de vertex en mémoire via l’étape de sortie de flux. La sortie alimentée en mémoire est étendue à des listes point/ligne/triangle individuelles (exactement telles qu’elles sont transmises au rastériseur).

Lorsqu’un nuanceur Geometry est actif, il est appelé une fois pour chaque primitive passée ou générée précédemment dans le pipeline. Chaque appel du nuanceur Geometry considère comme entrée les données pour l’appel de la primitive, qu’il s’agisse d’un point unique, d’une ligne unique ou d’un triangle unique. Une bande de triangles de plus tôt dans le pipeline se traduirait par un appel du nuanceur Geometry pour chaque triangle de la bande (comme si la bande était développée dans une liste de triangles). Toutes les données d’entrée pour chaque vertex de la primitive individuelle sont disponibles (par exemple, 3 sommets pour triangle), ainsi que les données adjacentes du vertex, le cas échéant/disponibles.

Un nuanceur Geometry génère des données d’un vertex à la fois en ajoutant des sommets à un objet de flux de sortie. La topologie des flux est déterminée par une déclaration fixe, en choisissant l’une des suivantes : PointStream, LineStream ou TriangleStream comme sortie de l’étape GS. Il existe trois types d’objets de flux disponibles, PointStream, LineStream et TriangleStream, qui sont tous des objets basés sur un modèle. La topologie de la sortie est déterminée par le type d’objet respectif, tandis que le format des vertex ajoutés au flux est déterminé par le type de modèle. L’exécution d’une instance geometry Shader est atomique d’autres appels, à ceci près que les données ajoutées aux flux sont en série. Les sorties d’un appel donné d’un nuanceur Geometry sont indépendantes des autres appels (bien que le classement soit respecté). Un nuanceur de géométrie qui génère des bandes de triangle démarre une nouvelle bande à chaque appel.

Quand une sortie de nuanceur Geometry est identifiée comme une valeur interprétée par le système (par exemple \_ , SV RenderTargetArrayIndex ou SV \_ position), le matériel examine ces données et effectue un comportement dépendant de la valeur, en plus de pouvoir passer les données elles-mêmes à l’étape de nuanceur suivante pour l’entrée. Lorsque la sortie de ce type de données du nuanceur Geometry a un sens pour le matériel au niveau de la primitive (par exemple, SV \_ RenderTargetArrayIndex ou SV \_ ViewportArrayIndex), \_ \[ \] \_ les données par primitives sont extraites du sommet de début émis pour la primitive, et non de la même façon.

Les primitives partiellement terminées peuvent être générées par le nuanceur Geometry si le nuanceur Geometry se termine et que la primitive est incomplète. Les primitives incomplètes sont ignorées silencieusement. Cela est similaire à la façon dont l’IA traite les primitives partiellement terminées.

Le nuanceur Geometry peut effectuer des opérations d’échantillonnage de charge et de texture où les dérivés de l’espace écran ne sont pas nécessaires (samplelevel, samplecmplevelzero, samplegrad).

Les algorithmes qui peuvent être implémentés dans le nuanceur Geometry sont les suivants :

-   Expansion point Sprite
-   Systèmes de particule dynamiques
-   Génération de fourrure/fin
-   Génération du volume de cliché instantané
-   Rendu à passage unique-à-carte cubique
-   Échange de matériel Per-Primitive
-   Per-Primitive la configuration des matériaux, y compris la génération de coordonnées Barycentric en tant que données primitives afin qu’un nuanceur de pixels puisse effectuer une interpolation d’attributs personnalisés (pour obtenir un exemple d’interpolation normale d’ordre supérieur, consultez l' [exemple CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pipeline graphique](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Étapes de pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 