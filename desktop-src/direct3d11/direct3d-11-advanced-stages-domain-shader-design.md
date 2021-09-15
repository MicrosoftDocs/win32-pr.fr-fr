---
title: Conception d’un nuanceur de domaine
description: Cette rubrique montre comment concevoir un nuanceur de domaine.
ms.assetid: 329d4eb9-8886-401d-8fb4-39e06886998f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a01d6b006c5ffe3afa355abe5e662cb96aa1391
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517085"
---
# <a name="how-to-design-a-domain-shader"></a>Comment : concevoir un nuanceur de domaine

Un nuanceur de domaine est le troisième des trois étapes qui fonctionnent ensemble pour implémenter le [pavage](direct3d-11-advanced-stages-tessellation.md). Le nuanceur de domaine génère la surface Geometry à partir des points de contrôle transformés à partir d’un nuanceur de coque et des coordonnées UV. Cette rubrique montre comment concevoir un nuanceur de domaine.

Un nuanceur de domaine est appelé une fois pour chaque point généré par la fonction fixe du paveur. Les entrées sont les \[ coordonnées UV W \] du point sur le correctif, ainsi que toutes les données de sortie du nuanceur de coque, y compris les points de contrôle et les constantes de patch. La sortie est un vertex défini d’une manière ou d’une autre. Si la sortie est envoyée au nuanceur de pixels, la sortie doit inclure une position (indiquée par une sémantique de position de SV \_ ).

**Pour concevoir un nuanceur de domaine**

1.  Définissez l’attribut de domaine.

    ```
    [domain("quad")]
    ```

    

    Le domaine est défini pour un correctif Quad.

2.  Déclarez l’emplacement sur la coque avec la valeur système d' [emplacement du domaine](/windows/desktop/direct3dhlsl/sv-domainlocation) .

    -   Pour un patch à quatre cœurs, utilisez un float2.
    -   Pour un correctif triple, utilisez un float3 (pour les coordonnées Barycentric)
    -   Pour une isoligne, utilisez un float2.

    Par conséquent, l’emplacement du domaine pour un correctif Quad ressemble à ceci :

    ```
    float2 UV : SV_DomainLocation
    ```

    

3.  Définissez les autres entrées.

    Les autres entrées proviennent du nuanceur de coque et sont définies par l’utilisateur. Cela inclut les points de contrôle d’entrée pour le correctif, dont il peut exister entre 1 et 32 points, et les données de constante de correction d’entrée.

    Les points de contrôle sont définis par l’utilisateur, généralement avec une structure telle que celle-ci (définie dans [Comment : concevoir un nuanceur de coque](direct3d-11-advanced-stages-hull-shader-design.md)) :

    ```
    const OutputPatch<BEZIER_CONTROL_POINT, 16> bezpatch
    ```

    

    Les données de constante de patch sont également définies par l’utilisateur et peuvent ressembler à celle-ci (définie dans [Comment : concevoir un nuanceur de coque](direct3d-11-advanced-stages-hull-shader-design.md)) :

    ```
    HS_CONSTANT_DATA_OUTPUT input
    ```

    

4.  Ajoutez du code défini par l’utilisateur pour calculer les sorties. Cela constitue le corps du nuanceur de domaine.

    Cette structure contient des sorties de nuanceur de domaine définies par l’utilisateur.

    ```
    struct DS_OUTPUT
    {
        float3 vNormal    : NORMAL;
        float2 vUV        : TEXCOORD;
        float3 vTangent   : TANGENT;
        float3 vBiTangent : BITANGENT;
        
        float4 vPosition  : SV_POSITION;
    };
    ```

    

    La fonction prend chaque UV d’entrée (à partir du du paveur) et évalue le correctif de Bézier à cette position.

    ```
    [domain("quad")]
    DS_OUTPUT BezierEvalDS( HS_CONSTANT_DATA_OUTPUT input, 
                            float2 UV : SV_DomainLocation,
                            const OutputPatch<BEZIER_CONTROL_POINT, 16> bezpatch )
    {
        DS_OUTPUT Output;

        // Insert code to compute the output here.

        return Output;    
    }
    ```

    

    La fonction est appelée une fois pour chaque point généré par la fonction Fixed du paveur. Dans la mesure où cet exemple utilise un correctif Quad, l’emplacement du domaine d’entrée ([SV \_ DomainLocation](/windows/desktop/direct3dhlsl/sv-domainlocation)) est un float2 (UV); un correctif triple aura un emplacement d’entrée float3 (coordonnées Barycentric UVW) et une isoligne aura un emplacement de domaine d’entrée float2.

    Les autres entrées de la fonction proviennent directement du nuanceur de coque. Dans cet exemple, il s’agit de 16 points de contrôle, chacun étant un **\_ \_ point de contrôle Bézier**, ainsi que des données constantes de correctifs (**sortie de \_ \_ données \_ de constante HS**). La sortie est un vertex contenant toutes les données de **\_ sortie** souhaitées-DS dans cet exemple.

Après avoir conçu un nuanceur de domaine, consultez [procédure : créer un nuanceur de domaine](direct3d-11-advanced-stages-domain-shader-create.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment utiliser Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Vue d’ensemble de la polygonalisation](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 