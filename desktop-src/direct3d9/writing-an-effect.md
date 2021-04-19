---
description: L’écriture d’un effet nécessite que vous compreniez la syntaxe d’effet et que vous génériez les informations d’État requises. Vous pouvez ajouter l’état du nuanceur, la texture et l’état de l’échantillonneur, ainsi que l’état du pipeline que votre application requiert en effet.
ms.assetid: 361dd260-526a-4484-8dc9-3857874e5023
title: Écriture d’un effet (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e0f456c5a2bce66f782b4da7d426de5c86bbb33
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513878"
---
# <a name="writing-an-effect-direct3d-9"></a><span data-ttu-id="5f96c-104">Écriture d’un effet (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5f96c-104">Writing an Effect (Direct3D 9)</span></span>

<span data-ttu-id="5f96c-105">L’écriture d’un effet nécessite que vous compreniez la syntaxe d’effet et que vous génériez les informations d’État requises.</span><span class="sxs-lookup"><span data-stu-id="5f96c-105">Writing an effect requires that you understand effect syntax, and generate the required state information.</span></span> <span data-ttu-id="5f96c-106">Vous pouvez ajouter l’état du nuanceur, la texture et l’état de l’échantillonneur, ainsi que l’état du pipeline que votre application requiert en effet.</span><span class="sxs-lookup"><span data-stu-id="5f96c-106">You can add shader state, texture and sampler state, and all of the pipeline state that your application requires in an effect.</span></span>

<span data-ttu-id="5f96c-107">La syntaxe d’effet est détaillée dans le [format d’effet (Direct3D 9)](dx9-graphics-reference-effects-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="5f96c-107">The effect syntax is detailed in the [Effect Format (Direct3D 9)](dx9-graphics-reference-effects-file-format.md).</span></span> <span data-ttu-id="5f96c-108">Un effet est généralement encapsulé dans un fichier d’effet (. FX), mais peut également être écrit sous la forme d’une chaîne de texte dans une application.</span><span class="sxs-lookup"><span data-stu-id="5f96c-108">An effect is typically encapsulated into an effect file (.fx) but could also be written as a text string in an application.</span></span>

## <a name="effect-example"></a><span data-ttu-id="5f96c-109">Exemple d’effet</span><span class="sxs-lookup"><span data-stu-id="5f96c-109">Effect Example</span></span>

<span data-ttu-id="5f96c-110">Les effets contiennent trois types d’État : l’état du nuanceur, la texture et l’état de l’échantillonneur, ainsi que l’état du pipeline.</span><span class="sxs-lookup"><span data-stu-id="5f96c-110">Effects contain three types of state: shader state, texture and sampler state, and pipeline state.</span></span> <span data-ttu-id="5f96c-111">Voici un exemple d’effet de l' [exemple BasicHLSL](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx):</span><span class="sxs-lookup"><span data-stu-id="5f96c-111">Here is an example of an effect from the [BasicHLSL Sample](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx):</span></span>


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



<span data-ttu-id="5f96c-112">Cet effet contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="5f96c-112">This effect contains:</span></span>

-   <span data-ttu-id="5f96c-113">État du nuanceur, qui est l’ensemble de l’état associé au nuanceur de sommets et au nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="5f96c-113">The shader state, which is all of the state associated with the vertex shader and pixel shader.</span></span> <span data-ttu-id="5f96c-114">Cela est défini par les fonctions de nuanceur de vertex et de pixels, les variables globales dont ils ont besoin, ainsi que leurs structures de données d’entrée et de sortie, qui sont toutes répertoriées ici :</span><span class="sxs-lookup"><span data-stu-id="5f96c-114">This is defined by the vertex and pixel shader functions, any global variables they require, and their input and output data structures, all of which are listed here:</span></span>

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

    

-   <span data-ttu-id="5f96c-115">L’état de la texture et de l’échantillonneur, qui sont les variables globales pour l’objet texture et l’objet échantillonneur :</span><span class="sxs-lookup"><span data-stu-id="5f96c-115">Texture and sampler state, which are the global variables for the texture object and the sampler object:</span></span>

    ```
    texture g_MeshTexture;              // Color texture for mesh

    sampler MeshTextureSampler = 
    sampler_state
    {
       ...
    };
    ```

    

-   <span data-ttu-id="5f96c-116">État de l’autre effet.</span><span class="sxs-lookup"><span data-stu-id="5f96c-116">The other effect state.</span></span> <span data-ttu-id="5f96c-117">Aucun autre État d’effet n’est explicitement utilisé dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="5f96c-117">There is no other effect state explicitly used in this example.</span></span> <span data-ttu-id="5f96c-118">Dans ce cas, il s’agit de la technique à l’intérieur de la passe à laquelle elle s’est appliquée :</span><span class="sxs-lookup"><span data-stu-id="5f96c-118">If there were, it would be the technique inside of the pass to which it applied:</span></span>

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

    

## <a name="effects-contain-one-or-more-techniques-and-passes"></a><span data-ttu-id="5f96c-119">Les effets contiennent une ou plusieurs techniques et passes</span><span class="sxs-lookup"><span data-stu-id="5f96c-119">Effects Contain One or More Techniques and Passes</span></span>

<span data-ttu-id="5f96c-120">Les options de rendu des effets sont contrôlées par l’ajout de techniques et de passes.</span><span class="sxs-lookup"><span data-stu-id="5f96c-120">Effect rendering options are controlled by adding techniques and passes.</span></span>

<span data-ttu-id="5f96c-121">Vous pouvez créer des effets avec des passes supplémentaires pour faciliter les effets de rendu plus complexes.</span><span class="sxs-lookup"><span data-stu-id="5f96c-121">Effects can be created with additional passes to facilitate more complex rendering effects.</span></span> <span data-ttu-id="5f96c-122">Une technique prend en charge un nombre arbitraire de passes :</span><span class="sxs-lookup"><span data-stu-id="5f96c-122">A technique supports an arbitrary number of passes:</span></span>


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



<span data-ttu-id="5f96c-123">Les effets peuvent également être créés à l’aide d’un nombre arbitraire de techniques.</span><span class="sxs-lookup"><span data-stu-id="5f96c-123">Effects can also be created with an arbitrary number of techniques.</span></span>


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



<span data-ttu-id="5f96c-124">Les techniques et les passes peuvent recevoir des noms arbitraires.</span><span class="sxs-lookup"><span data-stu-id="5f96c-124">The techniques and passes can be given arbitrary names.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f96c-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5f96c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f96c-126">Effets</span><span class="sxs-lookup"><span data-stu-id="5f96c-126">Effects</span></span>](effects.md)
</dt> </dl>

 

 



