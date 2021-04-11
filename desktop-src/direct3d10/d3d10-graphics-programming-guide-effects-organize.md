---
description: 'Avec Direct3D 10, l’état d’effet de certaines étapes de pipeline est organisé selon les structures suivantes :'
ms.assetid: 674ed278-102c-43da-a6bf-58e084df151e
title: Organisation de l’État dans un effet (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79cbea90c4d42d0a24ec7e35815616bf6698f72f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110382"
---
# <a name="organizing-state-in-an-effect-direct3d-10"></a><span data-ttu-id="3ac1e-103">Organisation de l’État dans un effet (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="3ac1e-103">Organizing State in an Effect (Direct3D 10)</span></span>

<span data-ttu-id="3ac1e-104">Avec Direct3D 10, l’état d’effet de certaines étapes de pipeline est organisé selon les structures suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ac1e-104">With Direct3D 10, effect state for certain pipeline stages is organized by the following structures:</span></span>



| <span data-ttu-id="3ac1e-105">État du pipeline</span><span class="sxs-lookup"><span data-stu-id="3ac1e-105">Pipeline State</span></span>  | <span data-ttu-id="3ac1e-106">Structure</span><span class="sxs-lookup"><span data-stu-id="3ac1e-106">Structure</span></span>                                                                                                          |
|-----------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ac1e-107">Assembleur d'entrée</span><span class="sxs-lookup"><span data-stu-id="3ac1e-107">Input Assembler</span></span> | [<span data-ttu-id="3ac1e-108">**Description de l' \_ élément d’entrée D3D10 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ac1e-108">**D3D10\_INPUT\_ELEMENT\_DESC**</span></span>](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)                                                    |
| <span data-ttu-id="3ac1e-109">Rastérisation</span><span class="sxs-lookup"><span data-stu-id="3ac1e-109">Rasterization</span></span>   | [<span data-ttu-id="3ac1e-110">**D3D10 \_ rastériseur \_ desc**</span><span class="sxs-lookup"><span data-stu-id="3ac1e-110">**D3D10\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)                                                           |
| <span data-ttu-id="3ac1e-111">Fusion de sortie</span><span class="sxs-lookup"><span data-stu-id="3ac1e-111">Output Merger</span></span>   | <span data-ttu-id="3ac1e-112">[**D3D10 \_ DESC \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) et [ **D3D10 \_ profondeur \_ du \_ stencil**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="3ac1e-112">[**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) and [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span></span> |



 

<span data-ttu-id="3ac1e-113">Pour les étapes du nuanceur, où le nombre de modifications d’État doit être plus contrôlé par une application, l’État a été divisé en état de mémoire tampon constante, état de l’échantillonneur et état de ressource de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-113">For the shader stages, where the number of state changes need to be more controlled by an application, the state has been divided up into constant buffer state, sampler state, and shader resource state.</span></span> <span data-ttu-id="3ac1e-114">Cela permet à une application conçue pour mettre à jour uniquement l’État qui change, ce qui améliore les performances en réduisant la quantité de données qui doit être transmise au GPU.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-114">This allows an application that is carefully designed to update only the state that is changing, which improves performance by reducing the amount of data that needs to be passed to the GPU.</span></span>

<span data-ttu-id="3ac1e-115">Comment organiser l’état du pipeline en conséquence ?</span><span class="sxs-lookup"><span data-stu-id="3ac1e-115">So how do you organize the pipeline state in an effect?</span></span>

<span data-ttu-id="3ac1e-116">La réponse est que l’ordre n’a pas d’importance.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-116">The answer is, the order doesn't matter.</span></span> <span data-ttu-id="3ac1e-117">Les variables globales n’ont pas besoin d’être situées en haut.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-117">Global variables do not have to be located at the top.</span></span> <span data-ttu-id="3ac1e-118">Toutefois, tous les exemples du kit de développement logiciel (SDK) suivent le même ordre, car il est recommandé d’organiser les données de la même façon.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-118">However, all the samples in the SDK follow the same order, as it is good practice to organize the data the same way.</span></span> <span data-ttu-id="3ac1e-119">Il s’agit donc d’une brève description de l’ordonnancement des données dans les exemples du kit de développement logiciel (SDK) DirectX.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-119">So this is a brief description of the data ordering in the DirectX SDK samples.</span></span>

-   [<span data-ttu-id="3ac1e-120">Variables globales</span><span class="sxs-lookup"><span data-stu-id="3ac1e-120">Global Variables</span></span>](#global-variables)
-   [<span data-ttu-id="3ac1e-121">Nuanceurs</span><span class="sxs-lookup"><span data-stu-id="3ac1e-121">Shaders</span></span>](#shaders)
-   [<span data-ttu-id="3ac1e-122">Techniques et passes</span><span class="sxs-lookup"><span data-stu-id="3ac1e-122">Techniques and Passes</span></span>](#techniques-and-passes)

## <a name="global-variables"></a><span data-ttu-id="3ac1e-123">Variables globales</span><span class="sxs-lookup"><span data-stu-id="3ac1e-123">Global Variables</span></span>

<span data-ttu-id="3ac1e-124">Tout comme la pratique C standard, les variables globales sont déclarées en premier, en haut du fichier.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-124">Just like standard C practice, global variables are declared first, at the top of the file.</span></span> <span data-ttu-id="3ac1e-125">Le plus souvent, il s’agit de variables qui seront initialisées par une application, puis utilisées dans un effet.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-125">Most often, these are variables that will be initialized by an application, and then used in an effect.</span></span> <span data-ttu-id="3ac1e-126">Parfois, elles sont initialisées et jamais modifiées, à l’heure où elles sont mises à jour toutes les trames.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-126">Sometimes they are initialized and never changed, other times they are updated every frame.</span></span> <span data-ttu-id="3ac1e-127">Tout comme les règles de portée de fonction C, les variables d’effet déclarées en dehors de la portée des fonctions Effects sont visibles tout au long de l’effet. toute variable déclarée à l’intérieur d’une fonction Effect n’est visible que dans cette fonction.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-127">Just like C function scope rules, effect variables declared outside of the scope of effect functions are visible throughout the effect; any variable declared inside of an effect function is only visible within that function.</span></span>

<span data-ttu-id="3ac1e-128">Voici un exemple des variables déclarées dans BasicHLSL10. fx.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-128">Here is an example of the variables declared in BasicHLSL10.fx.</span></span>


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



<span data-ttu-id="3ac1e-129">La syntaxe des variables Effects est plus détaillée dans la [syntaxe des variables d’effet (Direct3D 10)](d3d10-effect-variable-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="3ac1e-129">The syntax for effect variables is more fully detailed in [Effect Variable Syntax (Direct3D 10)](d3d10-effect-variable-syntax.md).</span></span> <span data-ttu-id="3ac1e-130">La syntaxe des échantillonneurs de texture d’effet est plus détaillée dans le [type d’échantillonneur (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="3ac1e-130">The syntax for effect texture samplers is more fully detailed in [Sampler Type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md).</span></span>

## <a name="shaders"></a><span data-ttu-id="3ac1e-131">Nuanceurs</span><span class="sxs-lookup"><span data-stu-id="3ac1e-131">Shaders</span></span>

<span data-ttu-id="3ac1e-132">Les nuanceurs sont de petits programmes exécutables.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-132">Shaders are small executable programs.</span></span> <span data-ttu-id="3ac1e-133">Vous pouvez considérer les nuanceurs comme l’encapsulation de l’état du nuanceur, puisque le code HLSL implémente la fonctionnalité de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-133">You can think of shaders as encapsulating shader state, since the HLSL code implements the shader functionality.</span></span> <span data-ttu-id="3ac1e-134">Le pipeline utilise trois types différents de nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-134">The pipeline uses three different kinds of shaders.</span></span>

-   <span data-ttu-id="3ac1e-135">Nuanceurs de vertex : opèrent sur les données de vertex.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-135">Vertex shaders - Operate on vertex data.</span></span> <span data-ttu-id="3ac1e-136">Un vertex dans produit un sommet.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-136">One vertex in yields one vertex out.</span></span>
-   <span data-ttu-id="3ac1e-137">Nuanceurs Geometry : opère sur les données Primitives.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-137">Geometry shaders - Operate on primitive data.</span></span> <span data-ttu-id="3ac1e-138">Une primitive dans peut donner 0, 1 ou plusieurs Primitives.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-138">One primitive in may yield 0, 1, or many primitives out.</span></span>
-   <span data-ttu-id="3ac1e-139">Nuanceurs de pixels : opèrent sur les données de pixels.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-139">Pixel shaders - Operate on pixel data.</span></span> <span data-ttu-id="3ac1e-140">Un pixel dans produit une sortie de 1 pixel (sauf si le pixel n’est pas éliminé d’un rendu).</span><span class="sxs-lookup"><span data-stu-id="3ac1e-140">One pixel in yields 1 pixel out (unless the pixel is culled out of a render).</span></span>

<span data-ttu-id="3ac1e-141">Les nuanceurs sont des fonctions locales et suivent les règles de fonction de style C.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-141">Shaders are local functions and follow C style function rules.</span></span> <span data-ttu-id="3ac1e-142">Lorsqu’un effet est compilé, chaque nuanceur est compilé et un pointeur vers chaque fonction de nuanceur est stocké en interne.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-142">When an effect is compiled, each shader is compiled and a pointer to each shader function is stored internally.</span></span> <span data-ttu-id="3ac1e-143">Une interface ID3D10Effect est retournée lorsque la compilation réussit.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-143">An ID3D10Effect interface is returned when compilation is successful.</span></span> <span data-ttu-id="3ac1e-144">À ce stade, l’effet compilé est dans un format intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-144">At this point the compiled effect is in an intermediate format.</span></span>

<span data-ttu-id="3ac1e-145">Pour obtenir plus d’informations sur les nuanceurs compilés, vous devez utiliser la réflexion du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-145">To find out more information about the compiled shaders, you will need to use shader reflection.</span></span> <span data-ttu-id="3ac1e-146">Cela revient essentiellement à demander au runtime de décompiler les nuanceurs et de retourner des informations sur le code du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-146">This is essentially like asking the runtime to decompile the shaders, and return information back to you about the shader code.</span></span>


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



<span data-ttu-id="3ac1e-147">La syntaxe des nuanceurs Effects est plus détaillée dans la syntaxe de la [fonction Effect (Direct3D 10)](d3d10-effect-function-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="3ac1e-147">The syntax for effect shaders is more fully detailed in [Effect Function Syntax (Direct3D 10)](d3d10-effect-function-syntax.md).</span></span>

## <a name="techniques-and-passes"></a><span data-ttu-id="3ac1e-148">Techniques et passes</span><span class="sxs-lookup"><span data-stu-id="3ac1e-148">Techniques and Passes</span></span>

<span data-ttu-id="3ac1e-149">Une technique est une collection de passes de rendu (il doit y avoir au moins une passe).</span><span class="sxs-lookup"><span data-stu-id="3ac1e-149">A technique is a collection of rendering passes (there must be at least one pass).</span></span> <span data-ttu-id="3ac1e-150">Chaque passe d’effet (qui est similaire à une seule passe dans une boucle de rendu) définit l’état du nuanceur et tout autre État de pipeline nécessaire pour afficher la géométrie.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-150">Each effect pass (which is similar in scope to a single pass in a render loop) defines the shader state and any other pipeline state necessary to render geometry.</span></span>

<span data-ttu-id="3ac1e-151">Voici un exemple d’une technique (qui comprend une passe) à partir de BasicHLSL10. fx.</span><span class="sxs-lookup"><span data-stu-id="3ac1e-151">Here is an example of one technique (which includes one pass) from BasicHLSL10.fx.</span></span>


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
```



<span data-ttu-id="3ac1e-152">La syntaxe des nuanceurs d’effets est plus détaillée dans la [syntaxe de technique d’effet (Direct3D 10)](d3d10-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="3ac1e-152">The syntax for effect shaders is more fully detailed in [Effect Technique Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ac1e-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3ac1e-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ac1e-154">Effets (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="3ac1e-154">Effects (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 
