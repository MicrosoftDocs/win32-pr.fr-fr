---
description: L’écriture d’un effet nécessite que vous compreniez la syntaxe d’effet et que vous génériez les informations d’État requises. Vous pouvez ajouter l’état du nuanceur, la texture et l’état de l’échantillonneur, ainsi que l’état du pipeline que votre application requiert en effet.
ms.assetid: 361dd260-526a-4484-8dc9-3857874e5023
title: Écriture d’un effet (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d625d09f57b68f6447982769d0ff4d4731e6aaaeff330b1cec639c4dffec8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068799"
---
# <a name="writing-an-effect-direct3d-9"></a>Écriture d’un effet (Direct3D 9)

L’écriture d’un effet nécessite que vous compreniez la syntaxe d’effet et que vous génériez les informations d’État requises. Vous pouvez ajouter l’état du nuanceur, la texture et l’état de l’échantillonneur, ainsi que l’état du pipeline que votre application requiert en effet.

La syntaxe d’effet est détaillée dans le [format d’effet (Direct3D 9)](dx9-graphics-reference-effects-file-format.md). Un effet est généralement encapsulé dans un fichier d’effet (. FX), mais peut également être écrit sous la forme d’une chaîne de texte dans une application.

## <a name="effect-example"></a>Exemple d’effet

Les effets contiennent trois types d’État : l’état du nuanceur, la texture et l’état de l’échantillonneur, ainsi que l’état du pipeline. Voici un exemple d’effet de l' [exemple BasicHLSL](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx):


```
// Global variables
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
int g_nNumLights;

float3 g_LightDir[3];               // Light's direction in world space
float4 g_LightDiffuse[3];           // Light's diffuse color
float4 g_LightAmbient;              // Light's ambient color

texture g_MeshTexture;              // Color texture for mesh

float    g_fTime;                   // App's time in seconds
float4x4 g_mWorld;                  // World matrix for object
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
// Texture samplers
sampler MeshTextureSampler = 
sampler_state
{
    Texture = <g_MeshTexture>;
    MipFilter = LINEAR;
    MinFilter = LINEAR;
    MagFilter = LINEAR;
};
struct VS_OUTPUT
{
    float4 Position   : POSITION;   // vertex position 
    float2 TextureUV  : TEXCOORD0;  // vertex texture coords 
    float4 Diffuse    : COLOR0;     // vertex diffuse color
};
VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    float3 vNormalWorldSpace;
  
    float4 vAnimatedPos = vPos;
    
    // Animation the vertex based on time and the vertex's object space position
    if( bAnimate )
        vAnimatedPos += float4(vNormal, 0) * (sin(g_fTime+5.5)+0.5)*5;
    
    // Transform the position from object space to homogeneous projection space
    Output.Position = mul(vAnimatedPos, g_mWorldViewProjection);
    
    // Transform the normal from object space to world space    
    vNormalWorldSpace = normalize(mul(vNormal, (float3x3)g_mWorld));
    
    // Compute simple directional lighting equation
    float3 vTotalLightDiffuse = float3(0,0,0);
    for(int i=0; i < nNumLights; i++ )
        vTotalLightDiffuse += g_LightDiffuse[i] * max(0,dot(vNormalWorldSpace, g_LightDir[i]));
        
    Output.Diffuse.rgb = g_MaterialDiffuseColor * vTotalLightDiffuse + 
                         g_MaterialAmbientColor * g_LightAmbient;   
    Output.Diffuse.a = 1.0f; 
    
    // Just copy the texture coordinate through
    if( bTexture ) 
        Output.TextureUV = vTexCoord0; 
    else
        Output.TextureUV = 0; 
    
    return Output;    
}
struct PS_OUTPUT
{
    float4 RGBColor : COLOR0;  // Pixel color    
};
PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    // Lookup mesh texture and modulate it with diffuse
    if( bTexture )
        Output.RGBColor = tex2D(MeshTextureSampler, In.TextureUV) * In.Diffuse;
    else
        Output.RGBColor = In.Diffuse;

    return Output;
}
technique RenderSceneWithTexture1Light
{
    pass P0
    {          
        VertexShader = compile vs_1_1 RenderSceneVS( 1, true, true );
        PixelShader  = compile ps_1_1 RenderScenePS( true ); 
    }
}
```



Cet effet contient les éléments suivants :

-   État du nuanceur, qui est l’ensemble de l’état associé au nuanceur de sommets et au nuanceur de pixels. Cela est défini par les fonctions de nuanceur de vertex et de pixels, les variables globales dont ils ont besoin, ainsi que leurs structures de données d’entrée et de sortie, qui sont toutes répertoriées ici :

    ```
    struct VS_OUTPUT
    {  ...  };
    VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                             ...
    {  ...  }

    struct PS_OUTPUT
    {  ...  };
    PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                             uniform bool bTexture ) 
    {  ...  }
    ```

    

-   L’état de la texture et de l’échantillonneur, qui sont les variables globales pour l’objet texture et l’objet échantillonneur :

    ```
    texture g_MeshTexture;              // Color texture for mesh

    sampler MeshTextureSampler = 
    sampler_state
    {
       ...
    };
    ```

    

-   État de l’autre effet. Aucun autre État d’effet n’est explicitement utilisé dans cet exemple. Dans ce cas, il s’agit de la technique à l’intérieur de la passe à laquelle elle s’est appliquée :

    ```
    technique RenderSceneWithTexture1Light
    {
        pass P0
        {          
            // Any other effect state can be set here.

            VertexShader = compile vs_1_1 RenderSceneVS( 1, true, true );
            PixelShader  = compile ps_1_1 RenderScenePS( true ); 
        }
    }
    
    ```

    

## <a name="effects-contain-one-or-more-techniques-and-passes"></a>Les effets contiennent une ou plusieurs techniques et passes

Les options de rendu des effets sont contrôlées par l’ajout de techniques et de passes.

Vous pouvez créer des effets avec des passes supplémentaires pour faciliter les effets de rendu plus complexes. Une technique prend en charge un nombre arbitraire de passes :


```
technique T0
{
    pass P0
    { ... }

    pass P1
    { ... }

    ...

    pass Pn
    { ... }
}
```



Les effets peuvent également être créés à l’aide d’un nombre arbitraire de techniques.


```
technique T0
{
    pass P0
    { ... }
}

technique T1
{
    pass P0
    { ... }

    pass P1
    { ... }
}

...

technique Tn
{
    pass P0
    { ... }
}

technique TVertexShaderOnly
{
    pass P0
    {
        VertexShader =
        asm
        {
         // assembly-language shader code goes here
         ...
        };
    }
}
```



Les techniques et les passes peuvent recevoir des noms arbitraires.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Effets](effects.md)
</dt> </dl>

 

 



