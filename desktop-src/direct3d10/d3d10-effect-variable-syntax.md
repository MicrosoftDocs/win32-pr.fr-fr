---
description: Une variable Effect est déclarée avec la syntaxe suivante.
ms.assetid: 53939c65-3725-44cc-bec6-775c3b921770
title: Syntaxe de la variable Effect (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2422ba2cebf18c72a14d621ef13a98700aefd2858169c6e96566b455ec21d2ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497709"
---
# <a name="effect-variable-syntax-direct3d-10"></a>Syntaxe de la variable Effect (Direct3D 10)

Une variable Effect est déclarée avec la syntaxe suivante.

## <a name="syntax"></a>Syntaxe

*Type de données* *VariableName* \[ :  \]  <  *Annotations* SemanticName > ;



| Nom         | Description                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DataType     | N’importe quel type de [base](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md) ou de [texture](../direct3dhlsl/dx-graphics-hlsl-to-type.md) .                                                                        |
| VariableName | Chaîne ASCII qui identifie de façon unique le nom de la variable d’effet.                                                                                                                   |
| SemanticName | Chaîne ASCII qui indique des informations supplémentaires sur la façon dont une variable doit être utilisée. Une sémantique est une chaîne ASCII qui peut être une valeur système prédéfinie ou une chaîne personnalisée de l’utilisateur. |
| Annotations  | Un ou plusieurs éléments d’informations fournies par l’utilisateur (métadonnées) qui sont ignorés par le système d’effet. Pour obtenir la syntaxe, consultez [syntaxe d’annotation (Direct3D 10)](d3d10-effect-annotation-syntax.md).     |



 

Une variable Effect déclarée en dehors de toutes les fonctions est considérée comme globale dans la portée. les variables déclarées dans une fonction sont locales à cette fonction.

## <a name="example"></a>Exemple

L' [exemple BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) utilise des variables globales sans sémantique pour les couleurs matérielles, les propriétés de lumière et les matrices de transformation.

Cet exemple illustre des variables d’effet global.


```
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
float3 g_LightDir[3];               // Light's direction in world space
float4x4 g_mWorld;                  // World matrix for object
```



Cet exemple illustre des variables d’effet qui sont locales à une fonction de nuanceur.


```
VS_OUTPUT RenderSceneVS( ... )
{
    float3 vNormalWorldSpace;
    float4 vAnimatedPos;

    // shader body
}
```



Cet exemple illustre les paramètres de fonction qui ont une sémantique.


```
VS_OUTPUT RenderSceneVS( float4 vPos : SV_POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
  ...
}
```



Cet exemple illustre la déclaration d’une variable de texture.


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



L’échantillonnage d’une texture s’effectue à l’aide d’un échantillon de texture. Pour configurer un échantillonneur dans un effet, consultez le [type d’échantillonneur](../direct3dhlsl/dx-graphics-hlsl-sampler.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Format d’effet](d3d10-effect-format.md)
</dt> </dl>

 

 
