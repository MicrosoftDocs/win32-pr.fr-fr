---
description: Une variable Effect est déclarée avec la syntaxe suivante.
ms.assetid: 53939c65-3725-44cc-bec6-775c3b921770
title: Syntaxe de la variable Effect (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8068571ff393e83ba0ae11eb2f9cb62f0bbb49df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393100"
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

 

 
