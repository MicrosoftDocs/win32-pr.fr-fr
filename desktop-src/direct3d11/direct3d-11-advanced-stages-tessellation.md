---
title: Étapes de pavage
description: Le runtime Direct3D 11 prend en charge trois nouvelles étapes qui implémentent la polygonalisation, qui convertit les surfaces de sous-division de faible détail en primitives de détail supérieures sur le GPU.
ms.assetid: 4ad2fd3e-6e1a-4326-8469-3198acf931dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aacb48ccc2c95ab93ba4f34212e654880d9a369
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2020
ms.locfileid: "104316662"
---
# <a name="tessellation-stages"></a>Étapes de pavage

Le runtime Direct3D 11 prend en charge trois nouvelles étapes qui implémentent la polygonalisation, qui convertit les surfaces de sous-division de faible détail en primitives de détail supérieures sur le GPU. Polygonalisation des vignettes (ou fractionnement) des surfaces de poids fort dans des structures appropriées pour le rendu.

En implémentant la polygonalisation dans le matériel, un pipeline graphique peut évaluer des modèles de détail inférieurs (nombre inférieur de polygones) et un rendu plus détaillé. Bien que le pavage de logiciels puisse être effectué, le pavage implémenté par le matériel peut générer une quantité incroyable de détails visuels (y compris la prise en charge du mappage de déplacement) sans ajouter le détail visuel aux tailles de modèle et aux taux d’actualisation ensuivre.

-   [Avantages de la polygonalisation](#tessellation-benefits)
-   [Nouvelles étapes de pipeline](#new-pipeline-stages)
    -   [Coque-étape du nuanceur](#hull-shader-stage)
    -   [Étape du paveur](#tessellator-stage)
    -   [Étape de nuanceur de domaine](#domain-shader-stage)
-   [API pour l’initialisation des étapes de pavage](#apis-for-initializing-tessellation-stages)
-   [Comment :](#how-tos)
-   [Rubriques connexes](#related-topics)

## <a name="tessellation-benefits"></a>Avantages de la polygonalisation

Mosaïque

-   Économise beaucoup de mémoire et de bande passante, ce qui permet à une application d’afficher des surfaces plus détaillées à partir de modèles de faible résolution. La technique de pavage implémentée dans le pipeline Direct3D 11 prend également en charge le mappage de déplacement, qui peut produire des quantités impressionnantes de détails de surface.
-   Prend en charge des techniques de rendu Scalable, telles que des niveaux de détail continus ou d’affichage, qui peuvent être calculés à la volée.
-   Améliore les performances en effectuant des calculs coûteux à une fréquence inférieure (en effectuant des calculs sur un modèle moins détaillé). Cela peut inclure la fusion de calculs à l’aide de formes Blend ou de cibles morphes pour des calculs réalistes ou physiques pour la détection de collision ou la dynamique de corps souple.

Le pipeline Direct3D 11 implémente le pavage dans le matériel, ce qui permet de décharger le travail du processeur vers le GPU. Cela peut entraîner d’importantes améliorations des performances si une application implémente un grand nombre de cibles morphes et/ou des modèles de déformation/déformation plus sophistiqués. Pour accéder aux nouvelles fonctionnalités de pavage, vous devez vous familiariser avec certaines nouvelles étapes de pipeline.

## <a name="new-pipeline-stages"></a>Nouvelles étapes de pipeline

Pavage utilise le GPU pour calculer une surface plus détaillée à partir d’une surface construite à partir de quatre carreaux, de carreaux de triangle ou d’isolignes. Pour rapprocher la surface de poids fort, chaque correctif est subdivisé en triangles, points ou lignes à l’aide de facteurs de pavage. Le pipeline Direct3D 11 implémente le pavage à l’aide de trois nouvelles étapes de pipeline :

-   [Coque-étape du nuanceur](#hull-shader-stage) : étape de nuanceur programmable qui produit un correctif de géométrie (et des constantes de correction) qui correspondent à chaque correctif d’entrée (quadruple, triangle ou ligne).
-   [Étape du paveur](#tessellator-stage) : étape de pipeline de fonction fixe qui crée un modèle d’échantillonnage du domaine qui représente le correctif de géométrie et génère un ensemble d’objets plus petits (triangles, points ou lignes) qui connectent ces exemples.
-   [Étape de nuanceur de domaine](#domain-shader-stage) : étape de nuanceur programmable qui calcule la position du vertex qui correspond à chaque exemple de domaine.

Le diagramme suivant met en évidence les nouvelles étapes du pipeline Direct3D 11.

![diagramme du pipeline Direct3D 11 qui met en évidence les étapes du nuanceur de coque, du du paveur et du nuanceur de domaine](images/d3d11-pipeline-stages-tessellation.png)

Le diagramme suivant illustre la progression à travers les étapes de pavage. La progression commence par la surface de sous-division de faible détail. La progression met ensuite en évidence le correctif d’entrée avec le correctif de géométrie, les exemples de domaine et les triangles correspondants qui connectent ces exemples. La progression met enfin en évidence les vertex qui correspondent à ces exemples.

![diagramme de la progression de la polygonalisation](images/tess-prog.png)

### <a name="hull-shader-stage"></a>Étape de Hull-Shader

Un nuanceur de coque, qui est appelé une fois par correctif-transforme des points de contrôle d’entrée qui définissent une surface de poids faible dans des points de contrôle qui composent un correctif. Il effectue également des calculs par correctifs pour fournir des données pour l’étape de pavage et l’étape de domaine. Au niveau de la boîte noire la plus simple, l’étape de nuanceur de coque ressemble à ce qui suit.

![diagramme de l’étape de nuanceur de coque](images/d3d11-hull-shader.png)

Un nuanceur de coque est implémenté avec une fonction HLSL et a les propriétés suivantes :

-   L’entrée du nuanceur est comprise entre 1 et 32 points de contrôle.
-   La sortie du nuanceur est comprise entre 1 et 32 points de contrôle, quel que soit le nombre de facteurs de pavage. La sortie des points de contrôle d’un nuanceur de coque peut être consommée par l’étape de nuanceur de domaine. Les données de constantes de correctifs peuvent être consommées par un nuanceur de domaine. les facteurs de pavage peuvent être utilisés par le nuanceur de domaine et l’étape de pavage.
-   Les facteurs de pavage déterminent le degré de subdivision de chaque correctif.
-   Le nuanceur déclare l’État requis par l’étape du paveur. Cela comprend des informations telles que le nombre de points de contrôle, le type de face de patch et le type de partitionnement à utiliser lors de la le pavage. Ces informations apparaissent en tant que déclarations en général au début du code du nuanceur.
-   Si l’étape de nuanceur de coque définit un facteur de pavage de bord sur = 0 ou NaN, le correctif est éliminé. Par conséquent, l’étape du paveur peut ou non s’exécuter, le nuanceur de domaine ne s’exécutera pas et aucune sortie visible ne sera générée pour ce correctif.

À un niveau plus profond, un nuanceur de coque fonctionne en deux phases : une phase de point de contrôle et une phase de constante de patch, qui sont exécutées en parallèle par le matériel. Le compilateur HLSL extrait le parallélisme dans un nuanceur de coque et l’encode en bytecode qui pilote le matériel.

-   La phase du point de contrôle s’exécute une fois pour chaque point de contrôle, la lecture des points de contrôle pour un correctif et la génération d’un point de contrôle de sortie (identifié par un ControlPointID).
-   La phase patch-constant s’exécute une fois par correctif pour générer des facteurs de pavage Edge et d’autres constantes par correctif. En interne, de nombreuses phases à constantes de correctifs peuvent s’exécuter en même temps. La phase patch-constant dispose d’un accès en lecture seule à tous les points de contrôle d’entrée et de sortie.

Voici un exemple de nuanceur de coque :


```
[patchsize(12)]
[patchconstantfunc(MyPatchConstantFunc)]
MyOutPoint main(uint Id : SV_ControlPointID,
     InputPatch<MyInPoint, 12> InPts)
{
     MyOutPoint result;
     
     ...
     
     result = TransformControlPoint( InPts[Id] );

     return result;
}
```



Pour obtenir un exemple qui crée un nuanceur de coque, consultez [Comment : créer un nuanceur de coque](direct3d-11-advanced-stages-hull-shader-create.md).

### <a name="tessellator-stage"></a>Étape du paveur

Le du paveur est une étape de fonction fixe initialisée par la liaison d’un nuanceur de coque au pipeline (voir [How to : Initialize the du paveur stage](direct3d-11-advanced-stages-tessellator-initialize.md)). L’objectif de l’étape du paveur consiste à subdiviser un domaine (quadruple, tri ou ligne) en plusieurs objets plus petits (triangles, points ou lignes). Le du paveur mosaïque un domaine canonique dans un système de coordonnées normalisé (zéro à un). Par exemple, un domaine à quatre cœurs est fractionné sur un carré d’unité.

Le du paveur fonctionne une fois par correctif à l’aide des facteurs de pavage (qui spécifient le degré de précision du domaine à fractionner) et le type de partitionnement (qui spécifie l’algorithme utilisé pour découper un correctif) qui sont transmis à partir de l’étape de nuanceur de coque. Du paveur génère des coordonnées UV (et éventuellement w) et la topologie de surface à l’étape de nuanceur de domaine.

En interne, le du paveur fonctionne en deux phases :

-   La première phase traite les facteurs de pavage, en corrigeant les problèmes d’arrondi, en gérant de très petits facteurs, en réduisant et en combinant des facteurs, à l’aide d’opérations arithmétiques à virgule flottante 32 bits.
-   La deuxième phase génère des listes de points ou de topologies en fonction du type de partitionnement sélectionné. Il s’agit de la tâche principale de l’étape du paveur et utilise des fractions de 16 bits avec l’arithmétique à virgule fixe. L’arithmétique à virgule fixe autorise l’accélération matérielle tout en conservant une précision acceptable. Par exemple, étant donné un correctif à l’échelle du compteur 64, cette précision peut placer des points à une résolution de 2 mm.



| Type de partitionnement | Plage                       |
|----------------------|-----------------------------|
| fractionnaire \_ impair      | \[1... 63\]                  |
| fractionnaire \_ pair     | TessFactor plage : \[ 2.. 64\] |
| entier              | TessFactor plage : \[ 1.. 64\] |
| pow2                 | TessFactor plage : \[ 1.. 64\] |



 

### <a name="domain-shader-stage"></a>Étape de Domain-Shader

Un nuanceur de domaine calcule la position du sommet d’un point subdivisé dans le correctif de sortie. Un nuanceur de domaine est exécuté une fois par point de sortie d’étape du paveur et a un accès en lecture seule aux coordonnées UV de sortie de l’étape du paveur, au correctif de sortie du nuanceur de coque et aux constantes de correctif de sortie du nuanceur de coque, comme le montre le diagramme suivant.

![diagramme de l’étape du nuanceur de domaine](images/d3d11-domain-shader.png)

Les propriétés du nuanceur de domaine sont les suivantes :

-   Un nuanceur de domaine est appelé une fois par coordonnée de sortie à partir de l’étape du paveur.
-   Un nuanceur de domaine consomme des points de contrôle de sortie à partir de l’étape de nuanceur de coque.
-   Un nuanceur de domaine génère la position d’un vertex.
-   Les entrées sont les sorties de nuanceur de coque, y compris les points de contrôle, les données de constante de correctif et les facteurs de pavage. Les facteurs de pavage peuvent inclure les valeurs utilisées par la fonction fixe du paveur ainsi que les valeurs brutes (avant l’arrondissement par pavage d’entiers, par exemple), ce qui facilite la géomorphation, par exemple.

Une fois le nuanceur de domaine terminé, la polygonalisation est terminée et les données du pipeline continuent à l’étape de pipeline suivante (nuanceur de géométrie, nuanceur de pixels, etc.). Un nuanceur Geometry qui attend des primitives avec contiguïté (par exemple, 6 sommets par triangle) n’est pas valide quand la polygonalisation est active (cela entraîne un comportement non défini, dont la couche de débogage se plaindra).

Voici un exemple de nuanceur de domaine :


```
void main( out    MyDSOutput result, 
           float2 myInputUV : SV_DomainPoint, 
           MyDSInput DSInputs,
           OutputPatch<MyOutPoint, 12> ControlPts, 
           MyTessFactors tessFactors)
{
     ...

     result.Position = EvaluateSurfaceUV(ControlPoints, myInputUV);
}
```



## <a name="apis-for-initializing-tessellation-stages"></a>API pour l’initialisation des étapes de pavage

La facettisation est implémentée avec deux nouvelles étapes de nuanceur programmables : un nuanceur de coque et un nuanceur de domaine. Ces nouvelles étapes de nuanceur sont programmées avec du code HLSL qui est défini dans le nuancier Model 5. Les nouvelles cibles de nuanceur sont : HS \_ 5 \_ 0 et DS \_ 5 \_ 0. À l’instar de toutes les étapes de nuanceur programmables, le code du matériel est extrait des nuanceurs compilés passés dans le runtime quand les nuanceurs sont liés au pipeline à l’aide d’API telles que [**DSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader) et [**HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader). Mais tout d’abord, le nuanceur doit être créé à l’aide d’API telles que [**CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader) et [**CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader).

Activez le pavage en créant un nuanceur de coque et en le liant à l’étape de nuanceur de coque (cela configure automatiquement l’étape du paveur). Pour générer les positions finales des vertex à partir des correctifs fractionnés, vous devez également créer un nuanceur de domaine et le lier à l’étape de nuanceur de domaine. Une fois le pavage activé, l’entrée de données de l’étape assembleur d’entrée doit être une donnée de correctif. Autrement dit, la topologie de l’assembleur d’entrée doit être une topologie à constante de correctif à partir de la [**\_ \_ topologie primitive d3d11**](/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)) définie avec [**IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology).

Pour désactiver le pavage, affectez la valeur **null** au nuanceur de coque et au nuanceur de domaine. Ni l’étape Geometry-Shader, ni l’étape Stream-output ne peuvent lire les points de contrôle de sortie de nuanceur-nuanceur ou les données de correctifs.

-   Nouvelles topologies pour l’étape assembleur d’entrée, qui sont des extensions à cette énumération.

    ```
    enum D3D11_PRIMITIVE_TOPOLOGY
    ```

    

    La topologie est définie sur l’étape assembleur d’entrée à l’aide de [ **IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology)

-   Bien entendu, les nouvelles étapes de nuanceur programmables requièrent que l’autre État soit défini, pour lier des mémoires tampons constantes, des exemples et des ressources de nuanceur aux étapes de canalisation appropriées. Ces nouvelles méthodes ID3D11Device sont implémentées pour définir cet État.
    -   [**DSGetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetconstantbuffers)
    -   [**DSGetSamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetsamplers)
    -   [**DSGetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetshader)
    -   [**DSGetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetshaderresources)
    -   [**DSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetconstantbuffers)
    -   [**DSSetSamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetsamplers)
    -   [**DSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader)
    -   [**DSSetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshaderresources)
    -   [**HSGetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetconstantbuffers)
    -   [**HSGetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetshaderresources)
    -   [**HSGetSamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetsamplers)
    -   [**HSGetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetshader)
    -   [**HSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetconstantbuffers)
    -   [**HSSetSamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetsamplers)
    -   [**HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader)
    -   [**HSSetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshaderresources)

## <a name="how-tos"></a>Comment :

La documentation contient également des exemples d’initialisation des étapes de pavage.



| Élément                                                                                                                                                                                                                                                                                           | Description                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="How_To__Create_a_Hull_Shader"></span><span id="how_to__create_a_hull_shader"></span><span id="HOW_TO__CREATE_A_HULL_SHADER"></span>[Comment : créer un nuanceur de coque](direct3d-11-advanced-stages-hull-shader-create.md)<br/>                                                     | Créez un nuanceur de coque.<br/>              |
| <span id="How_To__Design_a_Hull_Shader"></span><span id="how_to__design_a_hull_shader"></span><span id="HOW_TO__DESIGN_A_HULL_SHADER"></span>[Comment : concevoir un nuanceur de coque](direct3d-11-advanced-stages-hull-shader-design.md)<br/>                                                     | Concevoir un nuanceur de coque.<br/>              |
| <span id="How_To__Initialize_the_Tessellator_Stage"></span><span id="how_to__initialize_the_tessellator_stage"></span><span id="HOW_TO__INITIALIZE_THE_TESSELLATOR_STAGE"></span>[Comment : initialiser l’étape du paveur](direct3d-11-advanced-stages-tessellator-initialize.md)<br/> | Initialisez l’étape de pavage.<br/> |
| <span id="How_To__Create_a_Domain_Shader"></span><span id="how_to__create_a_domain_shader"></span><span id="HOW_TO__CREATE_A_DOMAIN_SHADER"></span>[Comment : créer un nuanceur de domaine](direct3d-11-advanced-stages-domain-shader-create.md)<br/>                                           | Créez un nuanceur de domaine.<br/>            |
| <span id="How_To__Design_a_Domain_Shader"></span><span id="how_to__design_a_domain_shader"></span><span id="HOW_TO__DESIGN_A_DOMAIN_SHADER"></span>[Comment : concevoir un nuanceur de domaine](direct3d-11-advanced-stages-domain-shader-design.md)<br/>                                           | Créez un nuanceur de domaine.<br/>            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pipeline graphique](overviews-direct3d-11-graphics-pipeline.md)
</dt> </dl>

 

