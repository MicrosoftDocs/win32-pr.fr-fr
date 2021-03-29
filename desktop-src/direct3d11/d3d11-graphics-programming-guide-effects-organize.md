---
title: Organisation de l’État dans un effet (Direct3D 11)
description: Avec Direct3D 11, l’état d’effet de certaines étapes de pipeline est organisé par structures.
ms.assetid: e5057f94-69dd-4219-a5f4-569e48502475
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a0523dd8abdabde29a5485b8d3b1e6d13b9429
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990960"
---
# <a name="organizing-state-in-an-effect-direct3d-11"></a><span data-ttu-id="cc00b-103">Organisation de l’État dans un effet (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="cc00b-103">Organizing State in an Effect (Direct3D 11)</span></span>

<span data-ttu-id="cc00b-104">Avec Direct3D 11, l’état d’effet de certaines étapes de pipeline est organisé par structures.</span><span class="sxs-lookup"><span data-stu-id="cc00b-104">With Direct3D 11, effect state for certain pipeline stages is organized by structures.</span></span> <span data-ttu-id="cc00b-105">Voici les structures :</span><span class="sxs-lookup"><span data-stu-id="cc00b-105">Here are the structures:</span></span>



| <span data-ttu-id="cc00b-106">État du pipeline</span><span class="sxs-lookup"><span data-stu-id="cc00b-106">Pipeline State</span></span> | <span data-ttu-id="cc00b-107">Structure</span><span class="sxs-lookup"><span data-stu-id="cc00b-107">Structure</span></span>                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc00b-108">Rastérisation</span><span class="sxs-lookup"><span data-stu-id="cc00b-108">Rasterization</span></span>  | [<span data-ttu-id="cc00b-109">**D3D11 \_ rastériseur \_ desc**</span><span class="sxs-lookup"><span data-stu-id="cc00b-109">**D3D11\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)                                                           |
| <span data-ttu-id="cc00b-110">Fusion de sortie</span><span class="sxs-lookup"><span data-stu-id="cc00b-110">Output Merger</span></span>  | <span data-ttu-id="cc00b-111">[**D3d11 \_ DESC \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) et [ **d3d11 \_ profondeur \_ du \_ stencil**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="cc00b-111">[**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) and [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span></span> |
| <span data-ttu-id="cc00b-112">Nuanceurs</span><span class="sxs-lookup"><span data-stu-id="cc00b-112">Shaders</span></span>        | <span data-ttu-id="cc00b-113">Voir ci-dessous</span><span class="sxs-lookup"><span data-stu-id="cc00b-113">See below</span></span>                                                                                                          |



 

<span data-ttu-id="cc00b-114">Pour les étapes du nuanceur, où le nombre de modifications d’État doit être plus contrôlé par une application, l’État a été divisé en état de mémoire tampon constante, état de l’échantillonneur, état de la ressource du nuanceur et état d’affichage de l’accès non ordonné (pour les nuanceurs de pixels et de calcul).</span><span class="sxs-lookup"><span data-stu-id="cc00b-114">For the shader stages, where the number of state changes need to be more controlled by an application, the state has been divided up into constant buffer state, sampler state, shader resource state, and unordered access view state (for pixel and compute shaders).</span></span> <span data-ttu-id="cc00b-115">Cela permet à une application conçue pour mettre à jour uniquement l’État qui change, ce qui améliore les performances en réduisant la quantité de données qui doit être transmise au GPU.</span><span class="sxs-lookup"><span data-stu-id="cc00b-115">This allows an application that is carefully designed to update only the state that is changing, which improves performance by reducing the amount of data that needs to be passed to the GPU.</span></span>

<span data-ttu-id="cc00b-116">Comment organiser l’état du pipeline en conséquence ?</span><span class="sxs-lookup"><span data-stu-id="cc00b-116">So how do you organize the pipeline state in an effect?</span></span>

<span data-ttu-id="cc00b-117">La réponse est que l’ordre n’a pas d’importance.</span><span class="sxs-lookup"><span data-stu-id="cc00b-117">The answer is, the order doesn't matter.</span></span> <span data-ttu-id="cc00b-118">Les variables globales n’ont pas besoin d’être situées en haut.</span><span class="sxs-lookup"><span data-stu-id="cc00b-118">Global variables do not have to be located at the top.</span></span> <span data-ttu-id="cc00b-119">Toutefois, tous les exemples du kit de développement logiciel (SDK) suivent le même ordre, car il est recommandé d’organiser les données de la même façon.</span><span class="sxs-lookup"><span data-stu-id="cc00b-119">However, all the samples in the SDK follow the same order, as it is good practice to organize the data the same way.</span></span> <span data-ttu-id="cc00b-120">Il s’agit donc d’une brève description de l’ordonnancement des données dans les exemples du kit de développement logiciel (SDK) DirectX.</span><span class="sxs-lookup"><span data-stu-id="cc00b-120">So this is a brief description of the data ordering in the DirectX SDK samples.</span></span>

-   [<span data-ttu-id="cc00b-121">Variables globales</span><span class="sxs-lookup"><span data-stu-id="cc00b-121">Global Variables</span></span>](#global-variables)
-   [<span data-ttu-id="cc00b-122">Nuanceurs</span><span class="sxs-lookup"><span data-stu-id="cc00b-122">Shaders</span></span>](#shaders)
-   [<span data-ttu-id="cc00b-123">Groupes, techniques et passes</span><span class="sxs-lookup"><span data-stu-id="cc00b-123">Groups, Techniques, and Passes</span></span>](#groups-techniques-and-passes)

## <a name="global-variables"></a><span data-ttu-id="cc00b-124">Variables globales</span><span class="sxs-lookup"><span data-stu-id="cc00b-124">Global Variables</span></span>

<span data-ttu-id="cc00b-125">Tout comme la pratique C standard, les variables globales sont déclarées en premier, en haut du fichier.</span><span class="sxs-lookup"><span data-stu-id="cc00b-125">Just like standard C practice, global variables are declared first, at the top of the file.</span></span> <span data-ttu-id="cc00b-126">Le plus souvent, il s’agit de variables qui seront initialisées par une application, puis utilisées dans un effet.</span><span class="sxs-lookup"><span data-stu-id="cc00b-126">Most often, these are variables that will be initialized by an application, and then used in an effect.</span></span> <span data-ttu-id="cc00b-127">Parfois, elles sont initialisées et jamais modifiées, à l’heure où elles sont mises à jour toutes les trames.</span><span class="sxs-lookup"><span data-stu-id="cc00b-127">Sometimes they are initialized and never changed, other times they are updated every frame.</span></span> <span data-ttu-id="cc00b-128">Tout comme les règles de portée de fonction C, les variables d’effet déclarées en dehors de la portée des fonctions Effects sont visibles tout au long de l’effet. toute variable déclarée à l’intérieur d’une fonction Effect n’est visible que dans cette fonction.</span><span class="sxs-lookup"><span data-stu-id="cc00b-128">Just like C function scope rules, effect variables declared outside of the scope of effect functions are visible throughout the effect; any variable declared inside of an effect function is only visible within that function.</span></span>

<span data-ttu-id="cc00b-129">Voici un exemple des variables déclarées dans BasicHLSL10. fx.</span><span class="sxs-lookup"><span data-stu-id="cc00b-129">Here is an example of the variables declared in BasicHLSL10.fx.</span></span>


```
// Global variables
float4 g_MaterialAmbientColor;      // Material's ambient color

Texture2D g_MeshTexture;            // Color texture for mesh

float    g_fTime;                   // App's time in seconds
float4x4 g_mWorld;                  // World matrix for object
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix


// Texture samplers
SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};
```



<span data-ttu-id="cc00b-130">La syntaxe des variables Effects est plus détaillée dans la [syntaxe de variable d’effet (Direct3D 11)](d3d11-effect-variable-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="cc00b-130">The syntax for effect variables is more fully detailed in [Effect Variable Syntax (Direct3D 11)](d3d11-effect-variable-syntax.md).</span></span> <span data-ttu-id="cc00b-131">La syntaxe des échantillonneurs de texture d’effet est plus détaillée dans le [type d’échantillonneur (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).</span><span class="sxs-lookup"><span data-stu-id="cc00b-131">The syntax for effect texture samplers is more fully detailed in [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).</span></span>

## <a name="shaders"></a><span data-ttu-id="cc00b-132">Nuanceurs</span><span class="sxs-lookup"><span data-stu-id="cc00b-132">Shaders</span></span>

<span data-ttu-id="cc00b-133">Les nuanceurs sont de petits programmes exécutables.</span><span class="sxs-lookup"><span data-stu-id="cc00b-133">Shaders are small executable programs.</span></span> <span data-ttu-id="cc00b-134">Vous pouvez considérer les nuanceurs comme l’encapsulation de l’état du nuanceur, puisque le code HLSL implémente la fonctionnalité de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="cc00b-134">You can think of shaders as encapsulating shader state, since the HLSL code implements the shader functionality.</span></span> <span data-ttu-id="cc00b-135">Le pipeline graphique jusqu’à cinq types différents de nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="cc00b-135">The graphics pipeline up to five different kinds of shaders.</span></span>

-   <span data-ttu-id="cc00b-136">Nuanceurs de vertex : opèrent sur les données de vertex.</span><span class="sxs-lookup"><span data-stu-id="cc00b-136">Vertex shaders - Operate on vertex data.</span></span> <span data-ttu-id="cc00b-137">Un vertex dans produit un sommet.</span><span class="sxs-lookup"><span data-stu-id="cc00b-137">One vertex in yields one vertex out.</span></span>
-   <span data-ttu-id="cc00b-138">Nuanciers de coque : opèrent sur les données des correctifs.</span><span class="sxs-lookup"><span data-stu-id="cc00b-138">Hull shaders - Operate on patch data.</span></span> <span data-ttu-id="cc00b-139">Phase du point de contrôle : un appel produit un point de contrôle ; Pour chaque phase de bifurcation et de jointure : un correctif produit une quantité de données constantes de correctifs.</span><span class="sxs-lookup"><span data-stu-id="cc00b-139">Control Point Phase: one invocation yields one control point; For each Fork and Join Phases: one patch yields some amount of patch constant data.</span></span>
-   <span data-ttu-id="cc00b-140">Nuanceurs de domaine-opèrent sur les données Primitives.</span><span class="sxs-lookup"><span data-stu-id="cc00b-140">Domain shaders - Operate on primitive data.</span></span> <span data-ttu-id="cc00b-141">Une primitive peut générer 0, 1 ou plusieurs Primitives.</span><span class="sxs-lookup"><span data-stu-id="cc00b-141">One primitive may yield 0, 1, or many primitives out.</span></span>
-   <span data-ttu-id="cc00b-142">Nuanceurs Geometry : opère sur les données Primitives.</span><span class="sxs-lookup"><span data-stu-id="cc00b-142">Geometry shaders - Operate on primitive data.</span></span> <span data-ttu-id="cc00b-143">Une primitive dans peut donner 0, 1 ou plusieurs Primitives.</span><span class="sxs-lookup"><span data-stu-id="cc00b-143">One primitive in may yield 0, 1, or many primitives out.</span></span>
-   <span data-ttu-id="cc00b-144">Nuanceurs de pixels : opèrent sur les données de pixels.</span><span class="sxs-lookup"><span data-stu-id="cc00b-144">Pixel shaders - Operate on pixel data.</span></span> <span data-ttu-id="cc00b-145">Un pixel dans produit une sortie de 1 pixel (sauf si le pixel n’est pas éliminé d’un rendu).</span><span class="sxs-lookup"><span data-stu-id="cc00b-145">One pixel in yields 1 pixel out (unless the pixel is culled out of a render).</span></span>

<span data-ttu-id="cc00b-146">Le pipeline du nuanceur de calcul utilise un nuanceur :</span><span class="sxs-lookup"><span data-stu-id="cc00b-146">The compute shader pipeline uses one shader:</span></span>

-   <span data-ttu-id="cc00b-147">Nuanciers de calcul : opère sur tout type de données.</span><span class="sxs-lookup"><span data-stu-id="cc00b-147">Compute shaders - Operate on any kind of data.</span></span> <span data-ttu-id="cc00b-148">La sortie est indépendante du nombre de threads.</span><span class="sxs-lookup"><span data-stu-id="cc00b-148">The output is independent of the number of threads.</span></span>

<span data-ttu-id="cc00b-149">Les nuanceurs sont des fonctions locales et suivent les règles de fonction de style C.</span><span class="sxs-lookup"><span data-stu-id="cc00b-149">Shaders are local functions and follow C style function rules.</span></span> <span data-ttu-id="cc00b-150">Lorsqu’un effet est compilé, chaque nuanceur est compilé et un pointeur vers chaque fonction de nuanceur est stocké en interne.</span><span class="sxs-lookup"><span data-stu-id="cc00b-150">When an effect is compiled, each shader is compiled and a pointer to each shader function is stored internally.</span></span> <span data-ttu-id="cc00b-151">Une interface ID3D11Effect est retournée lorsque la compilation réussit.</span><span class="sxs-lookup"><span data-stu-id="cc00b-151">An ID3D11Effect interface is returned when compilation is successful.</span></span> <span data-ttu-id="cc00b-152">À ce stade, l’effet compilé est dans un format intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="cc00b-152">At this point the compiled effect is in an intermediate format.</span></span>

<span data-ttu-id="cc00b-153">Pour obtenir plus d’informations sur les nuanceurs compilés, vous devez utiliser la réflexion du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="cc00b-153">To find out more information about the compiled shaders, you will need to use shader reflection.</span></span> <span data-ttu-id="cc00b-154">Cela revient essentiellement à demander au runtime de décompiler les nuanceurs et de retourner des informations sur le code du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="cc00b-154">This is essentially like asking the runtime to decompile the shaders, and return information back to you about the shader code.</span></span>


```
struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; // vertex position 
    float4 Diffuse    : COLOR0;      // vertex diffuse color
    float2 TextureUV  : TEXCOORD0;   // vertex texture coords 
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    float3 vNormalWorldSpace;
 
    ....    
    
    return Output;    
}


struct PS_OUTPUT
{
    float4 RGBColor : SV_Target;  // Pixel color
};

PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    if( bTexture )
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;
    ....

    return Output;
}
```



<span data-ttu-id="cc00b-155">La syntaxe des nuanceurs Effects est plus détaillée dans la syntaxe de la [fonction Effect (Direct3D 11)](d3d11-effect-function-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="cc00b-155">The syntax for effect shaders is more fully detailed in [Effect Function Syntax (Direct3D 11)](d3d11-effect-function-syntax.md).</span></span>

## <a name="groups-techniques-and-passes"></a><span data-ttu-id="cc00b-156">Groupes, techniques et passes</span><span class="sxs-lookup"><span data-stu-id="cc00b-156">Groups, Techniques, and Passes</span></span>

<span data-ttu-id="cc00b-157">Un groupe est un ensemble de techniques.</span><span class="sxs-lookup"><span data-stu-id="cc00b-157">A group is a collection of techniques.</span></span> <span data-ttu-id="cc00b-158">Une technique est une collection de passes de rendu (il doit y avoir au moins une passe).</span><span class="sxs-lookup"><span data-stu-id="cc00b-158">A technique is a collection of rendering passes (there must be at least one pass).</span></span> <span data-ttu-id="cc00b-159">Chaque passe d’effet (qui est similaire à une seule passe dans une boucle de rendu) définit l’état du nuanceur et tout autre État de pipeline nécessaire pour afficher la géométrie.</span><span class="sxs-lookup"><span data-stu-id="cc00b-159">Each effect pass (which is similar in scope to a single pass in a render loop) defines the shader state and any other pipeline state necessary to render geometry.</span></span>

<span data-ttu-id="cc00b-160">Les groupes sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="cc00b-160">Groups are optional.</span></span> <span data-ttu-id="cc00b-161">Il y a un seul groupe sans nom qui englobe toutes les techniques globales.</span><span class="sxs-lookup"><span data-stu-id="cc00b-161">There is a single, unnamed group which encompasses all global techniques.</span></span> <span data-ttu-id="cc00b-162">Tous les autres groupes doivent être nommés.</span><span class="sxs-lookup"><span data-stu-id="cc00b-162">All other groups must be named.</span></span>

<span data-ttu-id="cc00b-163">Voici un exemple d’une technique (qui comprend une passe) à partir de BasicHLSL10. fx.</span><span class="sxs-lookup"><span data-stu-id="cc00b-163">Here is an example of one technique (which includes one pass) from BasicHLSL10.fx.</span></span>


```
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, RenderSceneVS( 1, true, true ) ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}

fxgroup g0
{
    technique11 RunComputeShader
    {
        pass P0
        {
            SetComputeShader( CompileShader( cs_5_0, CS() ) );
        }
    }
}

```



<span data-ttu-id="cc00b-164">La syntaxe des nuanceurs d’effets est plus détaillée dans la [syntaxe de technique d’effet (Direct3D 11)](d3d11-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="cc00b-164">The syntax for effect shaders is more fully detailed in [Effect Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc00b-165">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cc00b-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc00b-166">Effets (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="cc00b-166">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 