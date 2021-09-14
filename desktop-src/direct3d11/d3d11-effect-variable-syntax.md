---
title: Syntaxe de la variable Effect (Direct3D 11)
description: Une variable Effect est déclarée avec la syntaxe décrite dans cette section.
ms.assetid: c0cfc9dd-2df3-4f38-a0e4-2e494456b3c9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67710642060ffea642434ba2d23a77cec2fb8bc3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012975"
---
# <a name="effect-variable-syntax-direct3d-11"></a>Syntaxe de la variable Effect (Direct3D 11)

Une variable Effect est déclarée avec la syntaxe décrite dans cette section.

## <a name="syntax"></a>Syntaxe

Syntaxe de base :

*Type de données* *VariableName* \[ *:* \]  <  *Annotations* SemanticName  >  \[ = InitialValue \] ;

Pour connaître la syntaxe complète [, consultez Syntaxe de variable (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax) .



| Nom         | Description                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DataType     | Tout type d’accès de [base](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax), de [texture](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type), non ordonné, de nuanceur ou de bloc d’État.                            |
| VariableName | Chaîne ASCII qui identifie de façon unique le nom de la variable d’effet.                                                                                                                   |
| SemanticName | Chaîne ASCII qui indique des informations supplémentaires sur la façon dont une variable doit être utilisée. Une sémantique est une chaîne ASCII qui peut être une valeur système prédéfinie ou une chaîne personnalisée de l’utilisateur. |
| Annotations  | Un ou plusieurs éléments d’informations fournies par l’utilisateur (métadonnées) qui sont ignorés par le système d’effet. Pour obtenir la syntaxe, consultez [syntaxe d’annotation (Direct3D 11)](d3d11-effect-annotation-syntax.md).     |
| InitialValue | Valeur par défaut de la variable.                                                                                                                                                          |



 

Une variable Effect déclarée en dehors de toutes les fonctions est considérée comme globale dans la portée. les variables déclarées dans une fonction sont locales à cette fonction.

## <a name="example"></a>Exemple

Cet exemple illustre les variables numériques à effet global.


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



Cet exemple illustre la déclaration d’une variable de texture globale.


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



L’échantillonnage d’une texture s’effectue à l’aide d’un échantillon de texture. Pour configurer un échantillonneur dans un effet, consultez le [type d’échantillonneur](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).

Cet exemple illustre la déclaration de variables de vue d’accès non ordonnées globales.


```
RWStructuredBuffer<uint> bc : register(u2) < string name="bc"; >;
RWBuffer<uint> bRW;
struct S
{
   uint key;
   uint value;
};
AppendStructuredBuffer<S> asb : register(u5);
RWByteAddressBuffer rwbab : register(u1);
RWStructuredBuffer<uint> rwsb : register(u3);
RWTexture1D<float> rwt1d : register(u1);
RWTexture1DArray<uint> rwt1da : register(u4);
RWTexture2D<uint> rwt2d : register(u2);
RWTexture2DArray<uint> rwt2da : register(u6);
RWTexture3D<uint> rwt3d : register(u7); 
 This example illustrates declaring global shader variables.
VertexShader pVS = CompileShader( vs_5_0, VS() );
HullShader pHS = NULL;
DomainShader pDS = NULL;
GeometryShader pGS = ConstructGSWithSO( CompileShader( gs_5_0, VS() ), 
                                        "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                        "3:Texcoord.xyzw; 3:$SKIP.x;", 
                                        NULL, 
                                        NULL, 
                                        1 );
PixelShader pPS = NULL;
ComputeShader pCS = NULL;
This example illustrates declaring global state block variables.
BlendState myBS[2] < bool IsValid = true; >
{
  {
    BlendEnable[0] = false;
  },
  {
    BlendEnable[0] = true;
    SrcBlendAlpha[0] = Inv_Src_Alpha;
  }
};

RasterizerState myRS
{
      FillMode = Solid;
      CullMode = NONE;
      MultisampleEnable = true;
      DepthClipEnable = false;
};

DepthStencilState myDS
{
    DepthEnable = false;
    DepthWriteMask = Zero;
    DepthFunc = Less;
};
sampler mySS[2] : register(s3) 
{
    {
        Filter = ANISOTROPIC;
        MaxAnisotropy = 3;
    },
    {
        Filter = ANISOTROPIC;
        MaxAnisotropy = 4;
    }
};
  
  
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Format d’effet](d3d11-effect-format.md)
</dt> </dl>

 

 