---
title: État de l’effet défini (Direct3D 11)
description: Certaines constantes d’effet doivent uniquement être initialisées. Consultez le code de base pour définir des variables d’effet dans Direct3D 12.
ms.assetid: f94ba82e-fc67-4e4d-a49d-20e1163bdff7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65c64f9e642e867e9398722d4590a4c2ce9193b4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407662"
---
# <a name="set-effect-state-direct3d-11"></a><span data-ttu-id="7946b-104">État de l’effet défini (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="7946b-104">Set Effect State (Direct3D 11)</span></span>

<span data-ttu-id="7946b-105">Certaines constantes d’effet doivent uniquement être initialisées.</span><span class="sxs-lookup"><span data-stu-id="7946b-105">Some effect constants only need to be initialized.</span></span> <span data-ttu-id="7946b-106">Une fois initialisé, l’état de l’effet est défini sur l’appareil pour l’ensemble de la boucle de rendu.</span><span class="sxs-lookup"><span data-stu-id="7946b-106">Once initialized, the effect state is set to the device for the entire render loop.</span></span> <span data-ttu-id="7946b-107">D’autres variables doivent être mises à jour chaque fois que la boucle de rendu est appelée.</span><span class="sxs-lookup"><span data-stu-id="7946b-107">Other variables need to be updated each time the render loop is called.</span></span> <span data-ttu-id="7946b-108">Le code de base pour définir des variables d’effet est illustré ci-dessous, pour chacun des types de variables.</span><span class="sxs-lookup"><span data-stu-id="7946b-108">The basic code for setting effect variables is shown below, for each of the types of variables.</span></span>

<span data-ttu-id="7946b-109">Un effet encapsule tout l’état de rendu requis pour effectuer une passe de rendu.</span><span class="sxs-lookup"><span data-stu-id="7946b-109">An effect encapsulates all of the render state required to do a rendering pass.</span></span> <span data-ttu-id="7946b-110">En termes d’API, il existe trois types d’État encapsulés dans un effet.</span><span class="sxs-lookup"><span data-stu-id="7946b-110">In terms of the API, there are three types of state encapsulated in an effect.</span></span>

-   [<span data-ttu-id="7946b-111">État constant</span><span class="sxs-lookup"><span data-stu-id="7946b-111">Constant State</span></span>](#constant-state)
-   [<span data-ttu-id="7946b-112">État du nuanceur</span><span class="sxs-lookup"><span data-stu-id="7946b-112">Shader State</span></span>](#shader-state)
-   [<span data-ttu-id="7946b-113">État de la texture</span><span class="sxs-lookup"><span data-stu-id="7946b-113">Texture State</span></span>](#texture-state)

## <a name="constant-state"></a><span data-ttu-id="7946b-114">État constant</span><span class="sxs-lookup"><span data-stu-id="7946b-114">Constant State</span></span>

<span data-ttu-id="7946b-115">Tout d’abord, déclarez les variables dans un effet à l’aide des types de données HLSL.</span><span class="sxs-lookup"><span data-stu-id="7946b-115">First, declare variables in an effect using HLSL data types.</span></span>


```
//--------------------------------------------------------------------------------------
// Global variables
//--------------------------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
int g_nNumLights;

float3 g_LightDir[3];               // Light's direction in world space
float4 g_LightDiffuse[3];           // Light's diffuse color
float4 g_LightAmbient;              // Light's ambient color

Texture2D g_MeshTexture;            // Color texture for mesh

float    g_fTime;                   // App's time in seconds
float4x4 g_mWorld;                  // World matrix for object
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
```



<span data-ttu-id="7946b-116">Ensuite, déclarez les variables de l’application qui peuvent être définies par l’application, puis mettez à jour les variables d’effet.</span><span class="sxs-lookup"><span data-stu-id="7946b-116">Second, declare variables in the application that can be set by the application, and will then update the effect variables.</span></span>


```
           
    D3DXMATRIX  mWorldViewProjection;
    D3DXVECTOR3 vLightDir[MAX_LIGHTS];
    D3DXVECTOR4 vLightDiffuse[MAX_LIGHTS];
    D3DXMATRIX  mWorld;
    D3DXMATRIX  mView;
    D3DXMATRIX  mProj;

    // Get the projection and view matrix from the camera class
    mWorld = g_mCenterMesh * *g_Camera.GetWorldMatrix();
    mProj = *g_Camera.GetProjMatrix();
    mView = *g_Camera.GetViewMatrix();

    
OnD3D11CreateDevice()
{
  ...
    g_pLightDir = g_pEffect11->GetVariableByName( "g_LightDir" )->AsVector();
    g_pLightDiffuse = g_pEffect11->GetVariableByName( "g_LightDiffuse" )->AsVector();
    g_pmWorldViewProjection = g_pEffect11->GetVariableByName( 
        "g_mWorldViewProjection" )->AsMatrix();
    g_pmWorld = g_pEffect11->GetVariableByName( "g_mWorld" )->AsMatrix();
    g_pfTime = g_pEffect11->GetVariableByName( "g_fTime" )->AsScalar();
    g_pMaterialAmbientColor = g_pEffect11->GetVariableByName("g_MaterialAmbientColor")->AsVector();
    g_pMaterialDiffuseColor = g_pEffect11->GetVariableByName( 
        "g_MaterialDiffuseColor" )->AsVector();
    g_pnNumLights = g_pEffect11->GetVariableByName( "g_nNumLights" )->AsScalar();
}
```



<span data-ttu-id="7946b-117">Enfin, utilisez les méthodes de mise à jour pour définir la valeur des variables de l’application dans les variables d’effet.</span><span class="sxs-lookup"><span data-stu-id="7946b-117">Third, use the update methods to set the value of the variables in the application in the effect variables.</span></span>


```
           
OnD3D11FrameRender()
{
    ...
    g_pLightDir->SetRawValue( vLightDir, 0, sizeof(D3DXVECTOR3)*MAX_LIGHTS );
    g_pLightDiffuse->SetFloatVectorArray( (float*)vLightDiffuse, 0, MAX_LIGHTS );
    g_pmWorldViewProjection->SetMatrix( (float*)&mWorldViewProjection );
    g_pmWorld->SetMatrix( (float*)&mWorld );
    g_pfTime->SetFloat( (float)fTime );
    g_pnNumLights->SetInt( g_nNumActiveLights );
}
```



### <a name="two-ways-to-get-the-state-in-an-effect-variable"></a><span data-ttu-id="7946b-118">Deux façons d’afficher l’État dans une variable Effect</span><span class="sxs-lookup"><span data-stu-id="7946b-118">Two Ways to Get the State in an Effect Variable</span></span>

<span data-ttu-id="7946b-119">Il existe deux façons d’accéder à l’État contenu dans une variable Effect.</span><span class="sxs-lookup"><span data-stu-id="7946b-119">There are two ways to get the state contained in an effect variable.</span></span> <span data-ttu-id="7946b-120">En fonction d’un effet qui a été chargé en mémoire.</span><span class="sxs-lookup"><span data-stu-id="7946b-120">Given an effect that has been loaded into memory.</span></span>

<span data-ttu-id="7946b-121">L’une des méthodes consiste à obtenir l’état de l’échantillonneur à partir d’un [**ID3DX11EffectVariable**](id3dx11effectvariable.md) qui a été casté en tant qu’interface d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="7946b-121">One way is to get the sampler state from an [**ID3DX11EffectVariable**](id3dx11effectvariable.md) that has been cast as a sampler interface.</span></span>


```
D3D11_SAMPLER_DESC sampler_desc;
ID3D11EffectSamplerVariable* l_pD3D11EffectVariable = NULL;
if( g_pEffect11 )
{
    l_pD3D11EffectVariable = g_pEffect11->GetVariableByName( "MeshTextureSampler" )->AsSampler();
    if( l_pD3D11EffectVariable->IsValid() )
        hr = (l_pD3D11EffectVariable->GetBackingStore( 0, 
            &sampler_desc );
}
```



<span data-ttu-id="7946b-122">L’autre méthode consiste à récupérer l’état de l’échantillonneur à partir d’un [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate).</span><span class="sxs-lookup"><span data-stu-id="7946b-122">The other way is to get the sampler state from an [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate).</span></span>


```
ID3D11SamplerState* l_ppSamplerState = NULL;
D3D11_SAMPLER_DESC sampler_desc;
ID3D11EffectSamplerVariable* l_pD3D11EffectVariable = NULL;
if( g_pEffect11 )
{
    l_pD3D11EffectVariable = g_pEffect11->GetVariableByName( "MeshTextureSampler" )->AsSampler();
    if( l_pD3D11EffectVariable->IsValid )
    {
        hr = l_pD3D11EffectVariable->GetSampler( 0, 
            &l_ppSamplerState );
        if( l_ppSamplerState )
            l_ppSamplerState->GetDesc( &sampler_desc );
    }
}
```



## <a name="shader-state"></a><span data-ttu-id="7946b-123">État du nuanceur</span><span class="sxs-lookup"><span data-stu-id="7946b-123">Shader State</span></span>

<span data-ttu-id="7946b-124">L’état du nuanceur est déclaré et affecté dans une technique d’effet, au sein d’une passe.</span><span class="sxs-lookup"><span data-stu-id="7946b-124">Shader state is declared and assigned in an effect technique, within a pass.</span></span>


```
VertexShader vsRenderScene = CompileShader( vs_4_0, RenderSceneVS( 1, true, true );  
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( vsRenderScene );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}
```



<span data-ttu-id="7946b-125">Cela fonctionne comme si vous n’utilisiez pas d’effet.</span><span class="sxs-lookup"><span data-stu-id="7946b-125">This works just like it would if you were not using an effect.</span></span> <span data-ttu-id="7946b-126">Il y a trois appels, un pour chaque type de nuanceur (vertex, Geometry et pixel).</span><span class="sxs-lookup"><span data-stu-id="7946b-126">There are three calls, one for each type of shader (vertex, geometry, and pixel).</span></span> <span data-ttu-id="7946b-127">Le premier, SetVertexShader, appelle [**ID3D11DeviceContext :: VSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader).</span><span class="sxs-lookup"><span data-stu-id="7946b-127">The first one, SetVertexShader, calls [**ID3D11DeviceContext::VSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader).</span></span> <span data-ttu-id="7946b-128">CompileShader est une fonction d’effet spéciale qui prend le profil de nuanceur (vs \_ 4 \_ 0) et le nom de la fonction de nuanceur de sommets (RenderVS).</span><span class="sxs-lookup"><span data-stu-id="7946b-128">CompileShader is a special effect function that takes the shader profile(vs\_4\_0) and the name of the vertex shader function (RenderVS).</span></span> <span data-ttu-id="7946b-129">En d’autres termes, chacun de ces appels CompileShader compile la fonction de nuanceur associée et retourne un pointeur vers le nuanceur compilé.</span><span class="sxs-lookup"><span data-stu-id="7946b-129">In other words, each of these CompileShader calls compiles their associated shader function and returns a pointer to the compiled shader.</span></span>

<span data-ttu-id="7946b-130">Notez que tous les États de nuanceur ne doivent pas être définis.</span><span class="sxs-lookup"><span data-stu-id="7946b-130">Note that not all shader state must be set.</span></span> <span data-ttu-id="7946b-131">Ce test n’inclut aucun appel SetHullShader ou SetDomainShader, ce qui signifie que les nuanceurs de la coque et du domaine actuellement liés seront inchangés.</span><span class="sxs-lookup"><span data-stu-id="7946b-131">This pass does not include any SetHullShader or SetDomainShader calls, meaning that the currently bound hull and domain shaders will be unchanged.</span></span>

## <a name="texture-state"></a><span data-ttu-id="7946b-132">État de la texture</span><span class="sxs-lookup"><span data-stu-id="7946b-132">Texture State</span></span>

<span data-ttu-id="7946b-133">L’état de la texture est un peu plus complexe que la définition d’une variable, car les données de texture ne sont pas simplement lues comme une variable, elles sont échantillonnées à partir d’une texture.</span><span class="sxs-lookup"><span data-stu-id="7946b-133">Texture state is a little more complex than setting a variable, because texture data is not simply read like a variable, it is sampled from a texture.</span></span> <span data-ttu-id="7946b-134">Par conséquent, vous devez définir la variable de texture (tout comme une variable normale, sauf qu’elle utilise un type de texture) et vous devez définir les conditions d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="7946b-134">Therefore, you must define the texture variable (just like a normal variable except it uses a texture type) and you must define the sampling conditions.</span></span> <span data-ttu-id="7946b-135">Voici un exemple de déclaration de variable de texture et de déclaration d’état d’échantillonnage correspondante.</span><span class="sxs-lookup"><span data-stu-id="7946b-135">Here is an example of a texture variable declaration and the corresponding sampling state declaration.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

```



<span data-ttu-id="7946b-136">Voici un exemple de définition d’une texture à partir d’une application.</span><span class="sxs-lookup"><span data-stu-id="7946b-136">Here is an example of setting a texture from an application.</span></span> <span data-ttu-id="7946b-137">Dans cet exemple, la texture est stockée dans les données de maillage, qui ont été chargées lors de la création de l’effet.</span><span class="sxs-lookup"><span data-stu-id="7946b-137">In this example, the texture is stored in the mesh data, that was loaded when the effect was created.</span></span>

<span data-ttu-id="7946b-138">La première étape consiste à obtenir un pointeur vers la texture à partir de l’effet (à partir de la maille).</span><span class="sxs-lookup"><span data-stu-id="7946b-138">The first step is getting a pointer to the texture from the effect (from the mesh).</span></span>


```
ID3D11EffectShaderResourceVariable* g_ptxDiffuse = NULL;

// Obtain variables
g_ptxDiffuse = g_pEffect11->GetVariableByName( "g_MeshTexture" )->AsShaderResource();
```



<span data-ttu-id="7946b-139">La deuxième étape consiste à spécifier une vue pour accéder à la texture.</span><span class="sxs-lookup"><span data-stu-id="7946b-139">The second step is specifying a view for accessing the texture.</span></span> <span data-ttu-id="7946b-140">La vue définit un moyen général d’accéder aux données à partir de la ressource de texture.</span><span class="sxs-lookup"><span data-stu-id="7946b-140">The view defines a general way to access the data from the texture resource.</span></span>


```
   
OnD3D11FrameRender()
{
  ID3D11ShaderResourceView* pDiffuseRV = NULL;

  ...
  pDiffuseRV = g_Mesh11.GetMaterial(pSubset->MaterialID)->pDiffuseRV11;
  g_ptxDiffuse->SetResource( pDiffuseRV );
  ...
}   
```



<span data-ttu-id="7946b-141">Du point de vue de l’application, les vues d’accès non ordonnées sont gérées de la même façon que les vues de ressources de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="7946b-141">From the application perspective, unordered access views are handled similarly to shader resource views.</span></span> <span data-ttu-id="7946b-142">Toutefois, dans le nuanceur de pixels et les fonctions de nuanceur de calcul, les données des vues d’accès non ordonnées sont lues et écrites directement dans.</span><span class="sxs-lookup"><span data-stu-id="7946b-142">However, in the effect pixel shader and compute shader functions, unordered access view data is read from/written to directly.</span></span> <span data-ttu-id="7946b-143">Vous ne pouvez pas échantillonner à partir d’une vue d’accès non ordonnée.</span><span class="sxs-lookup"><span data-stu-id="7946b-143">You cannot sample from an unordered access view.</span></span>

<span data-ttu-id="7946b-144">Pour plus d’informations sur l’affichage des ressources, consultez [ressources](overviews-direct3d-11-resources.md).</span><span class="sxs-lookup"><span data-stu-id="7946b-144">For more information about viewing resources, see [Resources](overviews-direct3d-11-resources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7946b-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7946b-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7946b-146">Rendu d’un effet (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="7946b-146">Rendering an Effect (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




