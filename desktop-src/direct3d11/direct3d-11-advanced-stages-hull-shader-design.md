---
title: Comment concevoir un nuanceur de coque
description: Cette rubrique montre comment concevoir un nuanceur de coque.
ms.assetid: c11c5652-dd7d-433d-bfa2-9853618ba334
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece816ae33e7f4ecf4d024098e7741f197c423f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517084"
---
# <a name="how-to-design-a-hull-shader"></a>Comment : concevoir un nuanceur de coque

Un nuanceur de coque est la première des trois étapes qui fonctionnent ensemble pour implémenter le [pavage](direct3d-11-advanced-stages-tessellation.md) (les deux autres étapes sont du paveur et un nuanceur de domaine). Cette rubrique montre comment concevoir un nuanceur de coque.

Un nuanceur de coque requiert deux fonctions, le nuanceur de coque principal et une fonction de constante de patch. Le nuanceur de coque implémente des calculs sur chaque point de contrôle ; le nuanceur de coque appelle également la fonction de constante de patch qui implémente les calculs sur chaque correctif.

Une fois que vous avez conçu un nuanceur de coque, consultez [Comment : créer un nuanceur](direct3d-11-advanced-stages-hull-shader-create.md) de coque pour apprendre à créer un nuanceur de coque.

**Pour concevoir un nuanceur de coque**

1.  Définir le contrôle d’entrée du nuanceur de coque et les points de contrôle de sortie.

    ```
    // Input control point
    struct VS_CONTROL_POINT_OUTPUT
    {
        float3 vPosition : WORLDPOS;
        float2 vUV       : TEXCOORD0;
        float3 vTangent  : TANGENT;
    };

    // Output control point
    struct BEZIER_CONTROL_POINT
    {
        float3 vPosition    : BEZIERPOS;
    };
    ```

    

2.  Définir des données de constante de correctif de sortie.

    ```
    // Output patch constant data.
    struct HS_CONSTANT_DATA_OUTPUT
    {
        float Edges[4]        : SV_TessFactor;
        float Inside[2]       : SV_InsideTessFactor;
        
        float3 vTangent[4]    : TANGENT;
        float2 vUV[4]         : TEXCOORD;
        float3 vTanUCorner[4] : TANUCORNER;
        float3 vTanVCorner[4] : TANVCORNER;
        float4 vCWts          : TANWEIGHTS;
    };
    ```

    

    Dans le cas d’un domaine à quatre cœurs, [SV \_ TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor) définit 4 facteurs de pavage Edge (pour paver les bords), puisque la fonction fixe du paveur a besoin de connaître la quantité à paver. Les sorties requises sont différentes pour les domaines triangle et isoligne.

    La fonction Fixed du paveur n’examine pas les autres sorties de nuanceur de coque, telles que d’autres données de constante de correctif ou l’un des points de contrôle. Le nuanceur de domaine, qui est appelé pour chaque point, la fonction fixe du paveur génère, en tant qu’entrée, tous les points de contrôle de sortie du nuanceur de coque et toutes les données de constante de correctif de sortie. le nuanceur évalue le correctif à son emplacement.

3.  Définissez une fonction de constante de patch. Une fonction de constante de patch s’exécute une fois pour chaque correctif pour calculer toutes les données qui sont constantes pour le correctif entier (par opposition aux données de point de contrôle, qui sont calculées dans le nuanceur de coque).

    ```
    
    #define MAX_POINTS 32

    // Patch Constant Function
    HS_CONSTANT_DATA_OUTPUT SubDToBezierConstantsHS( 
        InputPatch<VS_CONTROL_POINT_OUTPUT, MAX_POINTS> ip,
        uint PatchID : SV_PrimitiveID )
    {   
        HS_CONSTANT_DATA_OUTPUT Output;

        // Insert code to compute Output here
        
        return Output;
    }
    ```

    

    Les propriétés de la fonction patch constant sont les suivantes :

    -   Une entrée spécifie une variable contenant un ID de correctif et est identifiée par la valeur système **SV \_ PrimitiveID** (voir [sémantiques](../direct3dhlsl/dx-graphics-hlsl-semantics.md) dans le nuancier modèle 4).
    -   Un paramètre d’entrée correspond aux points de contrôle d’entrée, déclarés dans la **\_ sortie du \_ point \_ de contrôle vs** dans cet exemple. Une fonction patch peut voir tous les points de contrôle d’entrée pour chaque correctif, il y a 32 points de contrôle par correctif dans cet exemple.
    -   Au minimum, la fonction doit calculer les facteurs de pavage par correctif pour l’étape du paveur qui sont identifiés avec [SV \_ TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor). Un domaine quadruple nécessite quatre facteurs de pavage pour les bords et deux facteurs supplémentaires (identifiés par [SV \_ InsideTessFactor](/windows/desktop/direct3dhlsl/sv-insidetessfactor)) pour le pavage dans le correctif. La fonction Fixed du paveur n’examine pas les autres sorties de nuanceur de coque (telles que les données de constante de correctif ou l’un des points de contrôle).
    -   Les sorties sont généralement définies par une structure et sont identifiées par la sortie de données de la **\_ constante \_ \_ HS** dans cet exemple ; la structure dépend du type de domaine et serait différente pour les domaines de triangle ou d’isoligne.

    Un nuanceur de domaine en revanche est appelé pour chaque point que la fonction fixe du paveur génère et doit afficher les points de contrôle de sortie et les données de constante de correctif de sortie (à la fois à partir du nuanceur de coque) pour évaluer un correctif à son emplacement.

4.  Définissez un nuanceur de coque. Un nuanceur de coque identifie les propriétés d’un correctif, y compris une fonction de constante de patch. Un nuanceur de coque est appelé une fois pour chaque point de contrôle de sortie.

    ```
    [domain("quad")]
    [partitioning("integer")]
    [outputtopology("triangle_cw")]
    [outputcontrolpoints(16)]
    [patchconstantfunc("SubDToBezierConstantsHS")]
    BEZIER_CONTROL_POINT SubDToBezierHS( 
        InputPatch<VS_CONTROL_POINT_OUTPUT, MAX_POINTS> ip, 
        uint i : SV_OutputControlPointID,
        uint PatchID : SV_PrimitiveID )
    {
        VS_CONTROL_POINT_OUTPUT Output;

        // Insert code to compute Output here.
        
        return Output;
    }
    ```

    

    Un nuanceur de coque utilise les attributs suivants :

    -   Attribut de [domaine](/windows/desktop/direct3dhlsl/sm5-attributes-domain) .
    -   Attribut de [partitionnement](/windows/desktop/direct3dhlsl/sm5-attributes-partitioning) .
    -   Attribut [outputtopology](/windows/desktop/direct3dhlsl/sm5-attributes-outputtopology) .
    -   Attribut [outputcontrolpoints](/windows/desktop/direct3dhlsl/sm5-attributes-outputcontrolpoints) .
    -   Attribut [patchconstantfunc](/windows/desktop/direct3dhlsl/sm5-attributes-patchconstantfunc) . Un nuanceur de coque calcule les points de contrôle de sortie. il y a 16 points de contrôle Bézier de sortie dans cet exemple.

Tous les points de contrôle d’entrée (identifiés par la **\_ sortie du \_ point \_ de contrôle vs**) sont visibles pour chaque appel de nuanceur de coque. Dans cet exemple, il y a 32 points de contrôle d’entrée.

Un nuanceur de coque est appelé une fois par point de contrôle de sortie (identifié avec [SV \_ OutputControlPointID](/windows/desktop/direct3dhlsl/sv-outputcontrolpointid)) pour chaque correctif (identifié avec SV \_ PrimitiveID). L’objectif de ce nuanceur particulier est de calculer la sortie *i*, qui a été définie pour être un point de contrôle Bézier (cet exemple comporte 16 points de contrôle de sortie définis par outputcontrolpoints).

Un nuanceur de coque exécute une routine une fois par correctif (fonction de constante de patch) pour calculer des données de constantes de correctifs (facteurs de pavage au minimum). Séparément, un nuanceur de coque exécute une fonction de constante de patch (appelée SubDToBezierConstantsHS) sur chaque correctif pour calculer des données constantes de correctif, telles que les facteurs de pavage pour l’étape du paveur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment utiliser Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Vue d’ensemble de la polygonalisation](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 