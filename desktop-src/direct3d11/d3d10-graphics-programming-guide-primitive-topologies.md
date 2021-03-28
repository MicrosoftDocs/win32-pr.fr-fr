---
title: Topologies de primitive
description: Direct3D 10 et versions ultérieures prennent en charge plusieurs types primitifs (ou topologies) représentés par le type énuméré de la topologie de la \_ primitive D3D \_ . Ces types définissent la façon dont les vertex sont interprétés et rendus par le pipeline.
ms.assetid: 357ad085-fd91-4420-abc3-1c57e8cbb517
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e83f901d4d91d01a3cffedddb343fde7b50c20e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315216"
---
# <a name="primitive-topologies"></a>Topologies de primitive

Direct3D 10 et versions ultérieures prennent en charge plusieurs types primitifs (ou topologies) représentés par le type énuméré de la [**\_ \_ topologie de la primitive D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology) . Ces types définissent la façon dont les vertex sont interprétés et rendus par le pipeline.

-   [Types primitifs de base](#basic-primitive-types)
-   [Contiguïté primitive](#primitive-adjacency)
-   [Direction du vent et positions des sommets de début](#winding-direction-and-leading-vertex-positions)
-   [Génération de plusieurs bandes](#generating-multiple-strips)
-   [Rubriques connexes](#related-topics)

## <a name="basic-primitive-types"></a>Types primitifs de base

Les types primitifs de base suivants sont pris en charge :

-   [Liste des points](/windows/desktop/direct3d9/point-lists)
-   [Liste des lignes](/windows/desktop/direct3d9/line-lists)
-   [Bande](/windows/desktop/direct3d9/line-strips)
-   [Liste de triangles](/windows/desktop/direct3d9/triangle-lists)
-   [Bande TRIANGE](/windows/desktop/direct3d9/triangle-strips)

Pour obtenir une visualisation de chaque type primitif, consultez le diagramme plus loin dans cette rubrique, dans la direction de l' [enroulement et les positions des sommets de début](#winding-direction-and-leading-vertex-positions).

L’étape assembleur d’entrée lit les données à partir des tampons de vertex et d’index, assemble les données dans ces primitives, puis envoie les données aux étapes de pipeline restantes. (Vous pouvez utiliser la méthode [**ID3D11DeviceContext :: IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology) pour spécifier le type primitif de l’étape assembleur d’entrée.)

## <a name="primitive-adjacency"></a>Contiguïté primitive

Tous les types primitifs Direct3D 10 et versions ultérieures (à l’exception de la liste de points) sont disponibles dans deux versions : un type primitif avec contiguïté et un type primitif sans contiguïté. Les primitives avec contiguïté contiennent certains des vertex environnants, tandis que les primitives sans contiguïté contiennent uniquement les vertex de la primitive cible. Par exemple, la primitive de liste de lignes (représentée par la valeur LINELIST de la topologie de la **\_ primitive \_ \_ D3D** ) possède une primitive de liste de lignes correspondante qui inclut l’adjacence (représentée par la valeur de la **\_ topologie primitive D3D \_ \_ LINELIST \_ Adj** .)

Les primitives adjacentes sont destinées à fournir des informations supplémentaires sur votre géométrie et sont visibles uniquement par le biais d’un nuanceur Geometry. L’adjacence est utile pour les nuanceurs de géométrie qui utilisent la détection silhouette, l’extrusion du volume de clichés instantanés, etc.

Supposons, par exemple, que vous souhaitiez dessiner une liste de triangles avec contiguïté. Une liste de triangles contenant 36 sommets (avec contiguïté) produira 6 primitives terminées. Les primitives avec contiguïté (à l’exception des bandes de lignes) contiennent exactement deux fois plus de vertex que la primitive équivalente sans contiguïté, où chaque vertex supplémentaire est un vertex adjacent.

## <a name="winding-direction-and-leading-vertex-positions"></a>Direction du vent et positions des sommets de début

Comme indiqué dans l’illustration suivante, un sommet principal est le premier vertex non adjacent dans une primitive. Un type primitif peut avoir plusieurs sommets de début définis, tant que chacun d’eux est utilisé pour une primitive différente. Pour une bande triangulaire avec contiguïté, les sommets de début sont 0, 2, 4, 6, et ainsi de suite. Pour une ligne avec contiguïté, les sommets de début sont 1, 2, 3, et ainsi de suite. En revanche, une primitive adjacente n’a pas de sommet principal.

L’illustration suivante montre l’ordonnancement des vertex pour tous les types primitifs que l’assembleur d’entrée peut produire.

![diagramme de l’ordonnancement des vertex pour les types primitifs](images/d3d10-primitive-topologies.png)

Les symboles de l’illustration précédente sont décrits dans le tableau suivant.



| Symbole                                                                                   | Nom              | Description                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![symbole pour un vertex](images/d3d10-primitive-topologies-vertex.png)                     | Sommet            | Point dans l’espace 3D.                                                                                                                                                                               |
| ![symbole de direction de l’enroulement](images/d3d10-primitive-topologies-winding-direction.png) | Direction de l’enroulement | Ordre des vertex lors de l’assemblage d’une primitive. Peut être dans le sens inverse des aiguilles d’une montre ; Spécifiez-le en appelant [**ID3D11Device1 :: CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1). |
| ![symbole du sommet de début](images/d3d10-primitive-topologies-leading-vertex.png)       | Sommet principal    | Premier vertex non adjacent dans une primitive qui contient des données à constante.                                                                                                                      |



 

## <a name="generating-multiple-strips"></a>Génération de plusieurs bandes

Vous pouvez générer plusieurs bandes à l’aide de la coupe des bandes. Vous pouvez effectuer une coupure de bande en appelant explicitement la fonction [RestartStrip](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-so-restartstrip) HLSL ou en insérant une valeur d’index spéciale dans le tampon d’index. Cette valeur est-1, qui est 0xFFFFFFFF pour les index 32 bits ou 0xFFFF pour les index 16 bits. Un index de-1 indique un « Cut » ou un « restart » explicite de la bande actuelle. L’index précédent termine la primitive ou la bande précédente, et l’index suivant démarre une nouvelle primitive ou une nouvelle bande. Pour plus d’informations sur la génération de plusieurs bandes, consultez [Geometry-Shader stage](/previous-versions//bb205146(v=vs.85)).

> [!Note]  
> Vous avez besoin d’un matériel de [niveau de fonctionnalité](overviews-direct3d-11-devices-downlevel-intro.md) 10,0 ou supérieur, car tous les matériels 10level9 ne mettent pas en œuvre cette fonctionnalité.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main avec l’étape de Input-Assembler](d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)
</dt> <dt>

[Étapes de pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 