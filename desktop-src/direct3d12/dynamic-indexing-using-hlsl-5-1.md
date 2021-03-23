---
title: Indexation dynamique à l’aide de HLSL 5.1
description: L’exemple D3D12DynamicIndexing illustre certaines des nouvelles fonctionnalités HLSL disponibles dans le modèle de nuanceur 5,1, en particulier l’indexation dynamique et les tableaux non liés, pour restituer le même maillage plusieurs fois, chaque fois que vous le rendez avec un matériau sélectionné dynamiquement. Avec l’indexation dynamique, les nuanceurs peuvent désormais indexer dans un tableau sans connaître la valeur de l’index au moment de la compilation. En cas de combinaison avec des tableaux non liés, cela ajoute un autre niveau d’indirection et de flexibilité aux auteurs de nuanceur et aux pipelines d’art.
ms.assetid: 9821AEDF-E83D-4034-863A-2B820D9B7455
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e41892e7deff23c8d11f8be1c38dac3fcba1de9
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548535"
---
# <a name="dynamic-indexing-using-hlsl-51"></a><span data-ttu-id="c9fb6-105">Indexation dynamique à l’aide de HLSL 5.1</span><span class="sxs-lookup"><span data-stu-id="c9fb6-105">Dynamic Indexing using HLSL 5.1</span></span>

<span data-ttu-id="c9fb6-106">L’exemple **D3D12DynamicIndexing** illustre certaines des nouvelles fonctionnalités HLSL disponibles dans le modèle de nuanceur 5,1, en particulier l’indexation dynamique et les tableaux non liés, pour restituer le même maillage plusieurs fois, chaque fois que vous le rendez avec un matériau sélectionné dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="c9fb6-106">The **D3D12DynamicIndexing** sample demonstrates some of the new HLSL features available in Shader Model 5.1 - particularly dynamic indexing and unbounded arrays - to render the same mesh multiple times, each time rendering it with a dynamically selected material.</span></span> <span data-ttu-id="c9fb6-107">Avec l’indexation dynamique, les nuanceurs peuvent désormais indexer dans un tableau sans connaître la valeur de l’index au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="c9fb6-107">With dynamic indexing, shaders can now index into an array without knowing the value of the index at compile time.</span></span> <span data-ttu-id="c9fb6-108">En cas de combinaison avec des tableaux non liés, cela ajoute un autre niveau d’indirection et de flexibilité aux auteurs de nuanceur et aux pipelines d’art.</span><span class="sxs-lookup"><span data-stu-id="c9fb6-108">When combined with unbounded arrays, this adds another level of indirection and flexibility for shader authors and art pipelines.</span></span>

-   [<span data-ttu-id="c9fb6-109">Configurer le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="c9fb6-109">Set up the pixel shader</span></span>](#set-up-the-pixel-shader)
-   [<span data-ttu-id="c9fb6-110">Configurer la signature racine</span><span class="sxs-lookup"><span data-stu-id="c9fb6-110">Set up the root signature</span></span>](#set-up-the-root-signature)
-   [<span data-ttu-id="c9fb6-111">Créer les textures</span><span class="sxs-lookup"><span data-stu-id="c9fb6-111">Create the textures</span></span>](#create-the-textures)
-   [<span data-ttu-id="c9fb6-112">Charger les données de texture</span><span class="sxs-lookup"><span data-stu-id="c9fb6-112">Upload the texture data</span></span>](#upload-the-texture-data)
-   [<span data-ttu-id="c9fb6-113">Charger la texture diffuse</span><span class="sxs-lookup"><span data-stu-id="c9fb6-113">Load the diffuse texture</span></span>](#load-the-diffuse-texture)
-   [<span data-ttu-id="c9fb6-114">Créer un échantillonneur</span><span class="sxs-lookup"><span data-stu-id="c9fb6-114">Create a sampler</span></span>](#create-a-sampler)
-   [<span data-ttu-id="c9fb6-115">Modifier dynamiquement l’index du paramètre racine</span><span class="sxs-lookup"><span data-stu-id="c9fb6-115">Dynamically change the root parameter index</span></span>](#dynamically-change-the-root-parameter-index)
-   [<span data-ttu-id="c9fb6-116">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="c9fb6-116">Run the sample</span></span>](#run-the-sample)
-   [<span data-ttu-id="c9fb6-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c9fb6-117">Related topics</span></span>](#related-topics)

## <a name="set-up-the-pixel-shader"></a><span data-ttu-id="c9fb6-118">Configurer le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="c9fb6-118">Set up the pixel shader</span></span>

<span data-ttu-id="c9fb6-119">Examinons tout d’abord le nuanceur lui-même, qui est un nuanceur de pixels pour cet exemple.</span><span class="sxs-lookup"><span data-stu-id="c9fb6-119">Let's first look at the shader itself, which for this sample is a pixel shader.</span></span>

``` syntax
Texture2D        g_txDiffuse : register(t0);
Texture2D        g_txMats[]  : register(t1);
SamplerState     g_sampler   : register(s0);

struct PSSceneIn
{
    float4 pos : SV_Position;
    float2 tex : TEXCOORD0;
};

struct MaterialConstants
{
    uint matIndex;  // Dynamically set index for looking up from g_txMats[].
};
ConstantBuffer<MaterialConstants> materialConstants : register(b0, space0);

float4 PSSceneMain(PSSceneIn input) : SV_Target
{
    float3 diffuse = g_txDiffuse.Sample(g_sampler, input.tex).rgb;
    float3 mat = g_txMats[materialConstants.matIndex].Sample(g_sampler, input.tex).rgb;
    return float4(diffuse * mat, 1.0f);
}
```

<span data-ttu-id="c9fb6-120">La fonctionnalité de tableau indépendant est illustrée par le `g_txMats[]` tableau, car elle ne spécifie pas de taille de tableau.</span><span class="sxs-lookup"><span data-stu-id="c9fb6-120">The unbounded array feature is illustrated by the `g_txMats[]` array as it does not specify an array size.</span></span> <span data-ttu-id="c9fb6-121">L’indexation dynamique est utilisée pour l’indexation dans `g_txMats[]` avec `matIndex` , qui est défini en tant que constante racine.</span><span class="sxs-lookup"><span data-stu-id="c9fb6-121">Dynamic indexing is used to index into `g_txMats[]` with `matIndex`, which is defined as a root constant.</span></span> <span data-ttu-id="c9fb6-122">Le nuanceur n’a aucune connaissance de la taille ou du tableau ou de la valeur de l’index au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="c9fb6-122">The shader has no knowledge of the size or the array or the value of the index at compile-time.</span></span> <span data-ttu-id="c9fb6-123">Les deux attributs sont définis dans la signature racine de l’objet d’état de pipeline utilisé avec le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="c9fb6-123">Both attributes are defined in the root signature of the pipeline state object used with the shader.</span></span>

<span data-ttu-id="c9fb6-124">Pour tirer parti des fonctionnalités d’indexation dynamique en langage HLSL, le nuanceur doit être compilé avec le SM 5,1.</span><span class="sxs-lookup"><span data-stu-id="c9fb6-124">To take advantage of the dynamic indexing features in HLSL requires that the shader be compiled with SM 5.1.</span></span> <span data-ttu-id="c9fb6-125">En outre, pour utiliser des tableaux indépendants, l’indicateur de **\_ \_ \_ tables de descripteurs non délimités/Enable** doit également être utilisé.</span><span class="sxs-lookup"><span data-stu-id="c9fb6-125">Additionally, to make use of unbounded arrays, the **/enable\_unbounded\_descriptor\_tables** flag must also be used.</span></span> <span data-ttu-id="c9fb6-126">Les options de ligne de commande suivantes sont utilisées pour compiler ce nuanceur avec l' [outil Effect-compiler Tool](/windows/desktop/direct3dtools/fxc) (fxc) :</span><span class="sxs-lookup"><span data-stu-id="c9fb6-126">The following command line options are used to compile this shader with the [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) (FXC):</span></span>

``` syntax
fxc /Zi /E"PSSceneMain" /Od /Fo"dynamic_indexing_pixel.cso" /ps"_5_1" /nologo /enable_unbounded_descriptor_tables
```

## <a name="set-up-the-root-signature"></a><span data-ttu-id="c9fb6-127">Configurer la signature racine</span><span class="sxs-lookup"><span data-stu-id="c9fb6-127">Set up the root signature</span></span>

<span data-ttu-id="c9fb6-128">À présent, examinons la définition de signature racine, en particulier la façon dont nous définissons la taille du tableau indépendant et liez une constante racine à `matIndex` .</span><span class="sxs-lookup"><span data-stu-id="c9fb6-128">Now, let's look at the root signature definition, particularly, how we define the size of the unbounded array and link a root constant to `matIndex`.</span></span> <span data-ttu-id="c9fb6-129">Pour le nuanceur de pixels, nous définissons trois éléments : une table de descripteurs pour SRVs (notre Texture2Ds), une table de descripteurs pour les échantillonneurs et une constante racine unique.</span><span class="sxs-lookup"><span data-stu-id="c9fb6-129">For the pixel shader, we define three things: a descriptor table for SRVs (our Texture2Ds), a descriptor table for Samplers and a single root constant.</span></span> <span data-ttu-id="c9fb6-130">La table descripteur de notre SRVs contient des `CityMaterialCount + 1` entrées.</span><span class="sxs-lookup"><span data-stu-id="c9fb6-130">The descriptor table for our SRVs contains `CityMaterialCount + 1` entries.</span></span> <span data-ttu-id="c9fb6-131">`CityMaterialCount` constante qui définit la longueur de `g_txMats[]` et + 1 pour `g_txDiffuse` .</span><span class="sxs-lookup"><span data-stu-id="c9fb6-131">`CityMaterialCount` is a constant that defines the length of `g_txMats[]` and the + 1 is for `g_txDiffuse`.</span></span> <span data-ttu-id="c9fb6-132">La table de descripteurs de nos exemples contient une seule entrée et nous définissons uniquement la valeur de constante racine 1 32 bits via **InitAsConstants**(...)., dans la méthode **LoadAssets** .</span><span class="sxs-lookup"><span data-stu-id="c9fb6-132">The descriptor table for our Samplers contains only one entry and we only define one 32-bit root constant value via **InitAsConstants**(…)., in the **LoadAssets** method.</span></span>

``` syntax
 // Create the root signature.
    {
        CD3DX12_DESCRIPTOR_RANGE ranges[3];
        ranges[0].Init(D3D12_DESCRIPTOR_RANGE_TYPE_SRV, 1 + CityMaterialCount, 0);  // Diffuse texture + array of materials.
        ranges[1].Init(D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER, 1, 0);
        ranges[2].Init(D3D12_DESCRIPTOR_RANGE_TYPE_CBV, 1, 0);

        CD3DX12_ROOT_PARAMETER rootParameters[4];
        rootParameters[0].InitAsDescriptorTable(1, &ranges[0], D3D12_SHADER_VISIBILITY_PIXEL);
        rootParameters[1].InitAsDescriptorTable(1, &ranges[1], D3D12_SHADER_VISIBILITY_PIXEL);
        rootParameters[2].InitAsDescriptorTable(1, &ranges[2], D3D12_SHADER_VISIBILITY_VERTEX);
        rootParameters[3].InitAsConstants(1, 0, 0, D3D12_SHADER_VISIBILITY_PIXEL);

        CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
        rootSignatureDesc.Init(_countof(rootParameters), rootParameters, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

        ComPtr<ID3DBlob> signature;
        ComPtr<ID3DBlob> error;
        ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
        ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));
    }
```



| <span data-ttu-id="c9fb6-133">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="c9fb6-133">Call flow</span></span>                                                             | <span data-ttu-id="c9fb6-134">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9fb6-134">Parameters</span></span>                                                            |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="c9fb6-135">**\_Plage du descripteur CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="c9fb6-135">**CD3DX12\_DESCRIPTOR\_RANGE**</span></span>](cd3dx12-descriptor-range.md)        | [<span data-ttu-id="c9fb6-136">**\_Type de plage du descripteur D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c9fb6-136">**D3D12\_DESCRIPTOR\_RANGE\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) |
| [<span data-ttu-id="c9fb6-137">**\_Paramètre racine \_ CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="c9fb6-137">**CD3DX12\_ROOT\_PARAMETER**</span></span>](cd3dx12-root-parameter.md)            | [<span data-ttu-id="c9fb6-138">**\_Visibilité du nuanceur D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="c9fb6-138">**D3D12\_SHADER\_VISIBILITY**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [<span data-ttu-id="c9fb6-139">**Description de la \_ signature racine CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c9fb6-139">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) | [<span data-ttu-id="c9fb6-140">**\_Indicateurs de \_ signature \_ racine D3D12**</span><span class="sxs-lookup"><span data-stu-id="c9fb6-140">**D3D12\_ROOT\_SIGNATURE\_FLAGS**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| <span data-ttu-id="c9fb6-141">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c9fb6-141">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span>                                   |                                                                       |
| [<span data-ttu-id="c9fb6-142">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="c9fb6-142">**D3D12SerializeRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="c9fb6-143">**\_Version de \_ signature \_ racine D3D**</span><span class="sxs-lookup"><span data-stu-id="c9fb6-143">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="c9fb6-144">**CreateRootSignature**</span><span class="sxs-lookup"><span data-stu-id="c9fb6-144">**CreateRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |



 

## <a name="create-the-textures"></a><span data-ttu-id="c9fb6-145">Créer les textures</span><span class="sxs-lookup"><span data-stu-id="c9fb6-145">Create the textures</span></span>

<span data-ttu-id="c9fb6-146">Le contenu de `g_txMats[]` sont des textures générées par des procédures créées dans **LoadAssets**.</span><span class="sxs-lookup"><span data-stu-id="c9fb6-146">The contents of `g_txMats[]` are procedurally generated textures created in **LoadAssets**.</span></span> <span data-ttu-id="c9fb6-147">Chaque ville rendue dans la scène partage la même texture diffuse, mais chacune a également sa propre texture générée de manière procédurale.</span><span class="sxs-lookup"><span data-stu-id="c9fb6-147">Each city rendered in the scene shares the same diffuse texture but each also has its own procedurally generated texture.</span></span> <span data-ttu-id="c9fb6-148">Le tableau de textures couvre le spectre arc-en-ciel pour visualiser facilement la technique d’indexation.</span><span class="sxs-lookup"><span data-stu-id="c9fb6-148">The array of textures span the rainbow spectrum to easily visualize the indexing technique.</span></span>

``` syntax
 // Create the textures and sampler.
    {
        // Procedurally generate an array of textures to use as city materials.
        {
            // All of these materials use the same texture desc.
            D3D12_RESOURCE_DESC textureDesc = {};
            textureDesc.MipLevels = 1;
            textureDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
            textureDesc.Width = CityMaterialTextureWidth;
            textureDesc.Height = CityMaterialTextureHeight;
            textureDesc.Flags = D3D12_RESOURCE_FLAG_NONE;
            textureDesc.DepthOrArraySize = 1;
            textureDesc.SampleDesc.Count = 1;
            textureDesc.SampleDesc.Quality = 0;
            textureDesc.Dimension = D3D12_RESOURCE_DIMENSION_TEXTURE2D;

            // The textures evenly span the color rainbow so that each city gets
            // a different material.
            float materialGradStep = (1.0f / static_cast<float>(CityMaterialCount));

            // Generate texture data.
            vector<vector<unsigned char>> cityTextureData;
            cityTextureData.resize(CityMaterialCount);
            for (int i = 0; i < CityMaterialCount; ++i)
            {
                CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_DEFAULT);
                ThrowIfFailed(m_device->CreateCommittedResource(
                    &heapProps,
                    D3D12_HEAP_FLAG_NONE,
                    &textureDesc,
                    D3D12_RESOURCE_STATE_COPY_DEST,
                    nullptr,
                    IID_PPV_ARGS(&m_cityMaterialTextures[i])));

                // Fill the texture.
                float t = i * materialGradStep;
                cityTextureData[i].resize(CityMaterialTextureWidth * CityMaterialTextureHeight * CityMaterialTextureChannelCount);
                for (int x = 0; x < CityMaterialTextureWidth; ++x)
                {
                    for (int y = 0; y < CityMaterialTextureHeight; ++y)
                    {
                        // Compute the appropriate index into the buffer based on the x/y coordinates.
                        int pixelIndex = (y * CityMaterialTextureChannelCount * CityMaterialTextureWidth) + (x * CityMaterialTextureChannelCount);

                        // Determine this row's position along the rainbow gradient.
                        float tPrime = t + ((static_cast<float>(y) / static_cast<float>(CityMaterialTextureHeight)) * materialGradStep);

                        // Compute the RGB value for this position along the rainbow
                        // and pack the pixel value.
                        XMVECTOR hsl = XMVectorSet(tPrime, 0.5f, 0.5f, 1.0f);
                        XMVECTOR rgb = XMColorHSLToRGB(hsl);
                        cityTextureData[i][pixelIndex + 0] = static_cast<unsigned char>((255 * XMVectorGetX(rgb)));
                        cityTextureData[i][pixelIndex + 1] = static_cast<unsigned char>((255 * XMVectorGetY(rgb)));
                        cityTextureData[i][pixelIndex + 2] = static_cast<unsigned char>((255 * XMVectorGetZ(rgb)));
                        cityTextureData[i][pixelIndex + 3] = 255;
                    }
                }
            }
        }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c9fb6-149">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="c9fb6-149">Call flow</span></span></th>
<th><span data-ttu-id="c9fb6-150">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9fb6-150">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9fb6-151"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc"><strong>D3D12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-151"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc"><strong>D3D12_RESOURCE_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="c9fb6-152"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-152"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span></span><br /><span data-ttu-id="c9fb6-153">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-153">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></span></span><br /><span data-ttu-id="c9fb6-154">
<a href=""></a>[<strong>D3D12_RESOURCE_DIMENSION</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_dimension)</span><span class="sxs-lookup"><span data-stu-id="c9fb6-154">
<a href=""></a>[<strong>D3D12_RESOURCE_DIMENSION</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9fb6-155"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-155"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="c9fb6-156"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-156"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br /><span data-ttu-id="c9fb6-157">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-157">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span></span><br /><span data-ttu-id="c9fb6-158">
<a href=""></a>[<strong>D3D12_HEAP_FLAG</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_heap_flags)</span><span class="sxs-lookup"><span data-stu-id="c9fb6-158">
<a href=""></a>[<strong>D3D12_HEAP_FLAG</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags)</span></span><br /><span data-ttu-id="c9fb6-159">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-159">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span></span><br /><span data-ttu-id="c9fb6-160">
<a href=""></a>[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="c9fb6-160">
<a href=""></a>[<strong>D3D12_RESOURCE_STATES</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9fb6-161"><a href="/windows/desktop/dxmath/xmvector-data-type"><strong>XMVECTOR</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-161"><a href="/windows/desktop/dxmath/xmvector-data-type"><strong>XMVECTOR</strong></a></span></span></td>
<td><dl><span data-ttu-id="c9fb6-162"><a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorset"><strong>XMVectorSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-162"><a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorset"><strong>XMVectorSet</strong></a></span></span><br /><span data-ttu-id="c9fb6-163">
<a href=""></a>[<strong>XMColorHSLToRGB</strong>] (/windows/desktop/api/directxmath/nf-directxmath-xmcolorhsltorgb)</span><span class="sxs-lookup"><span data-stu-id="c9fb6-163">
<a href=""></a>[<strong>XMColorHSLToRGB</strong>](/windows/desktop/api/directxmath/nf-directxmath-xmcolorhsltorgb)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="upload-the-texture-data"></a><span data-ttu-id="c9fb6-164">Charger les données de texture</span><span class="sxs-lookup"><span data-stu-id="c9fb6-164">Upload the texture data</span></span>

<span data-ttu-id="c9fb6-165">Les données de texture sont téléchargées vers le GPU via un tas de chargement et les SRVs sont créés pour chaque et stockés dans un tas de descripteur SRV.</span><span class="sxs-lookup"><span data-stu-id="c9fb6-165">Texture data is uploaded to the GPU via an upload heap and SRVs are created for each and stored in an SRV descriptor heap.</span></span>

``` syntax
         // Upload texture data to the default heap resources.
            {
                const UINT subresourceCount = textureDesc.DepthOrArraySize * textureDesc.MipLevels;
                const UINT64 uploadBufferStep = GetRequiredIntermediateSize(m_cityMaterialTextures[0].Get(), 0, subresourceCount); // All of our textures are the same size in this case.
                const UINT64 uploadBufferSize = uploadBufferStep * CityMaterialCount;
                CD3DX12_HEAP_PROPERTIES uploadHeap(D3D12_HEAP_TYPE_UPLOAD);
                auto uploadDesc = CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize);
                ThrowIfFailed(m_device->CreateCommittedResource(
                    &uploadHeap,
                    D3D12_HEAP_FLAG_NONE,
                    &uploadDesc,
                    D3D12_RESOURCE_STATE_GENERIC_READ,
                    nullptr,
                    IID_PPV_ARGS(&materialsUploadHeap)));

                for (int i = 0; i < CityMaterialCount; ++i)
                {
                    // Copy data to the intermediate upload heap and then schedule 
                    // a copy from the upload heap to the appropriate texture.
                    D3D12_SUBRESOURCE_DATA textureData = {};
                    textureData.pData = &cityTextureData[i][0];
                    textureData.RowPitch = static_cast<LONG_PTR>((CityMaterialTextureChannelCount * textureDesc.Width));
                    textureData.SlicePitch = textureData.RowPitch * textureDesc.Height;

                    UpdateSubresources(m_commandList.Get(), m_cityMaterialTextures[i].Get(), materialsUploadHeap.Get(), i * uploadBufferStep, 0, subresourceCount, &textureData);
                    auto barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_cityMaterialTextures[i].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE);
                    m_commandList->ResourceBarrier(1, &barrier);
                }
            }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c9fb6-166">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="c9fb6-166">Call flow</span></span></th>
<th><span data-ttu-id="c9fb6-167">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9fb6-167">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9fb6-168"><a href="getrequiredintermediatesize.md"><strong>GetRequiredIntermediateSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-168"><a href="getrequiredintermediatesize.md"><strong>GetRequiredIntermediateSize</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="c9fb6-169"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-169"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="c9fb6-170"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-170"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br /><span data-ttu-id="c9fb6-171">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-171">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span></span><br /><span data-ttu-id="c9fb6-172">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-172">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span></span><br /><span data-ttu-id="c9fb6-173">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-173">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span></span><br /><span data-ttu-id="c9fb6-174">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-174">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9fb6-175"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data"><strong>D3D12_SUBRESOURCE_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-175"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data"><strong>D3D12_SUBRESOURCE_DATA</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="c9fb6-176"><a href="updatesubresources1.md"><strong>Updatesubresources par</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-176"><a href="updatesubresources1.md"><strong>UpdateSubresources</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c9fb6-177"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-177"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>
<td><dl><span data-ttu-id="c9fb6-178"><a href="/windows/desktop/direct3d12/cd3dx12-resource-barrier"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-178"><a href="/windows/desktop/direct3d12/cd3dx12-resource-barrier"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br /><span data-ttu-id="c9fb6-179">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-179">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="load-the-diffuse-texture"></a><span data-ttu-id="c9fb6-180">Charger la texture diffuse</span><span class="sxs-lookup"><span data-stu-id="c9fb6-180">Load the diffuse texture</span></span>

<span data-ttu-id="c9fb6-181">La texture diffuse, g \_ `txDiffuse` , est téléchargée de la même manière et obtient également son propre SRV, mais les données de texture sont déjà définies dans occcity. bin.</span><span class="sxs-lookup"><span data-stu-id="c9fb6-181">The diffuse texture, g\_`txDiffuse`, is uploaded in a similar manner and also gets its own SRV, but the texture data is already defined in occcity.bin.</span></span>

``` syntax
// Load the occcity diffuse texture with baked-in ambient lighting.
        // This texture will be blended with a texture from the materials
        // array in the pixel shader.
        {
            D3D12_RESOURCE_DESC textureDesc = {};
            textureDesc.MipLevels = SampleAssets::Textures[0].MipLevels;
            textureDesc.Format = SampleAssets::Textures[0].Format;
            textureDesc.Width = SampleAssets::Textures[0].Width;
            textureDesc.Height = SampleAssets::Textures[0].Height;
            textureDesc.Flags = D3D12_RESOURCE_FLAG_NONE;
            textureDesc.DepthOrArraySize = 1;
            textureDesc.SampleDesc.Count = 1;
            textureDesc.SampleDesc.Quality = 0;
            textureDesc.Dimension = D3D12_RESOURCE_DIMENSION_TEXTURE2D;

            CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_DEFAULT);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &heapProps,
                D3D12_HEAP_FLAG_NONE,
                &textureDesc,
                D3D12_RESOURCE_STATE_COPY_DEST,
                nullptr,
                IID_PPV_ARGS(&m_cityDiffuseTexture)));

            const UINT subresourceCount = textureDesc.DepthOrArraySize * textureDesc.MipLevels;
            const UINT64 uploadBufferSize = GetRequiredIntermediateSize(m_cityDiffuseTexture.Get(), 0, subresourceCount);
            CD3DX12_HEAP_PROPERTIES uploadHeap(D3D12_HEAP_TYPE_UPLOAD);
            auto uploadDesc = CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &uploadHeap,
                D3D12_HEAP_FLAG_NONE,
                &uploadDesc,
                D3D12_RESOURCE_STATE_GENERIC_READ,
                nullptr,
                IID_PPV_ARGS(&textureUploadHeap)));

            // Copy data to the intermediate upload heap and then schedule 
            // a copy from the upload heap to the diffuse texture.
            D3D12_SUBRESOURCE_DATA textureData = {};
            textureData.pData = pMeshData + SampleAssets::Textures[0].Data[0].Offset;
            textureData.RowPitch = SampleAssets::Textures[0].Data[0].Pitch;
            textureData.SlicePitch = SampleAssets::Textures[0].Data[0].Size;

            UpdateSubresources(m_commandList.Get(), m_cityDiffuseTexture.Get(), textureUploadHeap.Get(), 0, 0, subresourceCount, &textureData);
            auto barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_cityDiffuseTexture.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE);
            m_commandList->ResourceBarrier(1, &barrier);
        }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c9fb6-182">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="c9fb6-182">Call flow</span></span></th>
<th><span data-ttu-id="c9fb6-183">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9fb6-183">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9fb6-184"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc"><strong>D3D12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-184"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc"><strong>D3D12_RESOURCE_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="c9fb6-185"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-185"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></span></span><br /><span data-ttu-id="c9fb6-186">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension"><strong>D3D12_RESOURCE_DIMENSION</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-186">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension"><strong>D3D12_RESOURCE_DIMENSION</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9fb6-187"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-187"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="c9fb6-188"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-188"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br /><span data-ttu-id="c9fb6-189">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-189">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span></span><br /><span data-ttu-id="c9fb6-190">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-190">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span></span><br /><span data-ttu-id="c9fb6-191">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-191">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span></span><br /><span data-ttu-id="c9fb6-192">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-192">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9fb6-193"><a href="getrequiredintermediatesize.md"><strong>GetRequiredIntermediateSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-193"><a href="getrequiredintermediatesize.md"><strong>GetRequiredIntermediateSize</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="c9fb6-194"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-194"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="c9fb6-195"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-195"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br /><span data-ttu-id="c9fb6-196">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-196">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span></span><br /><span data-ttu-id="c9fb6-197">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-197">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span></span><br /><span data-ttu-id="c9fb6-198">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-198">
<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc"><strong>CD3DX12_RESOURCE_DESC</strong></a></span></span><br /><span data-ttu-id="c9fb6-199">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-199">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9fb6-200"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data"><strong>D3D12_SUBRESOURCE_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-200"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data"><strong>D3D12_SUBRESOURCE_DATA</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="c9fb6-201"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-201"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>
<td><dl><span data-ttu-id="c9fb6-202"><a href="/windows/desktop/direct3d12/cd3dx12-resource-barrier"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-202"><a href="/windows/desktop/direct3d12/cd3dx12-resource-barrier"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br /><span data-ttu-id="c9fb6-203">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-203">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="create-a-sampler"></a><span data-ttu-id="c9fb6-204">Créer un échantillonneur</span><span class="sxs-lookup"><span data-stu-id="c9fb6-204">Create a sampler</span></span>

<span data-ttu-id="c9fb6-205">Enfin, pour **LoadAssets**, un échantillonneur unique est créé pour échantillonner à partir de la texture diffuse ou du tableau de texture.</span><span class="sxs-lookup"><span data-stu-id="c9fb6-205">Finally for **LoadAssets**, a single sampler is created to sample from either the diffuse texture or the texture array.</span></span>

``` syntax
 // Describe and create a sampler.
        D3D12_SAMPLER_DESC samplerDesc = {};
        samplerDesc.Filter = D3D12_FILTER_MIN_MAG_MIP_LINEAR;
        samplerDesc.AddressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
        samplerDesc.AddressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
        samplerDesc.AddressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
        samplerDesc.MinLOD = 0;
        samplerDesc.MaxLOD = D3D12_FLOAT32_MAX;
        samplerDesc.MipLODBias = 0.0f;
        samplerDesc.MaxAnisotropy = 1;
        samplerDesc.ComparisonFunc = D3D12_COMPARISON_FUNC_ALWAYS;
        m_device->CreateSampler(&samplerDesc, m_samplerHeap->GetCPUDescriptorHandleForHeapStart());

        // Create SRV for the city's diffuse texture.
        CD3DX12_CPU_DESCRIPTOR_HANDLE srvHandle(m_cbvSrvHeap->GetCPUDescriptorHandleForHeapStart(), 0, m_cbvSrvDescriptorSize);
        D3D12_SHADER_RESOURCE_VIEW_DESC diffuseSrvDesc = {};
        diffuseSrvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
        diffuseSrvDesc.Format = SampleAssets::Textures->Format;
        diffuseSrvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
        diffuseSrvDesc.Texture2D.MipLevels = 1;
        m_device->CreateShaderResourceView(m_cityDiffuseTexture.Get(), &diffuseSrvDesc, srvHandle);
        srvHandle.Offset(m_cbvSrvDescriptorSize);

        // Create SRVs for each city material.
        for (int i = 0; i < CityMaterialCount; ++i)
        {
            D3D12_SHADER_RESOURCE_VIEW_DESC materialSrvDesc = {};
            materialSrvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
            materialSrvDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
            materialSrvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
            materialSrvDesc.Texture2D.MipLevels = 1;
            m_device->CreateShaderResourceView(m_cityMaterialTextures[i].Get(), &materialSrvDesc, srvHandle);

            srvHandle.Offset(m_cbvSrvDescriptorSize);
        }   
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c9fb6-206">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="c9fb6-206">Call flow</span></span></th>
<th><span data-ttu-id="c9fb6-207">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9fb6-207">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9fb6-208"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc"><strong>D3D12_SAMPLER_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-208"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc"><strong>D3D12_SAMPLER_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="c9fb6-209"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter"><strong>D3D12_FILTER</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-209"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter"><strong>D3D12_FILTER</strong></a></span></span><br />
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode"></a><br />
<span data-ttu-id="c9fb6-210">D3D12_FLOAT32_MAX (<a href="constants.md"><strong>constantes</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c9fb6-210">D3D12_FLOAT32_MAX (<a href="constants.md"><strong>Constants</strong></a>)</span></span><br /><span data-ttu-id="c9fb6-211">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func"><strong>D3D12_COMPARISON_FUNC</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-211">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func"><strong>D3D12_COMPARISON_FUNC</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9fb6-212"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createsampler"><strong>CreateSampler</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-212"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createsampler"><strong>CreateSampler</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="c9fb6-213"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-213"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="c9fb6-214"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-214"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9fb6-215"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-215"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="c9fb6-216"><a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-216"><a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span></span><br /><span data-ttu-id="c9fb6-217">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-217">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9fb6-218"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-218"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="c9fb6-219"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-219"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="c9fb6-220"><a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-220"><a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span></span><br /><span data-ttu-id="c9fb6-221">
<a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-221">
<a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span></span><br /><span data-ttu-id="c9fb6-222">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-222">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9fb6-223"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9fb6-223"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

## <a name="dynamically-change-the-root-parameter-index"></a><span data-ttu-id="c9fb6-224">Modifier dynamiquement l’index du paramètre racine</span><span class="sxs-lookup"><span data-stu-id="c9fb6-224">Dynamically change the root parameter index</span></span>

<span data-ttu-id="c9fb6-225">Si nous devions restituer la scène maintenant, toutes les villes apparaîtraient le même, car nous n’avons pas défini la valeur de notre constante racine, `matIndex` .</span><span class="sxs-lookup"><span data-stu-id="c9fb6-225">If we were to render the scene now, all of the cities would appear the same, because we have not set the value of our root constant, `matIndex`.</span></span> <span data-ttu-id="c9fb6-226">Chaque nuanceur de pixels est indexé dans l’emplacement 0 de `g_txMats` et la scène ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="c9fb6-226">Each pixel shader would index into the 0th slot of `g_txMats` and the scene would look like this:</span></span>

![toutes les villes affichent la même couleur](images/dynamicindexing-image1.png)

<span data-ttu-id="c9fb6-228">La valeur de la constante racine est définie dans **FrameResource ::P opulatecommandlists**.</span><span class="sxs-lookup"><span data-stu-id="c9fb6-228">The value of the root constant is set in **FrameResource::PopulateCommandLists**.</span></span> <span data-ttu-id="c9fb6-229">Dans la boucle double **for** où une commande Draw est enregistrée pour chaque ville, nous enregistrons un appel à [**SetGraphicsRoot32BitConstants**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstants) en spécifiant notre index de paramètre racine en ce qui concerne la signature racine, dans ce cas 3, la valeur de l’index dynamique et un décalage, dans ce cas 0.</span><span class="sxs-lookup"><span data-stu-id="c9fb6-229">In the double **for** loop where a draw command is recorded for each city, we record a call to [**SetGraphicsRoot32BitConstants**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstants) specifying our root parameter index in regards to the root signature – in this case 3 – the value of the dynamic index and an offset – in this case 0.</span></span> <span data-ttu-id="c9fb6-230">Étant donné que la longueur de `g_txMats` est égale au nombre de villes que nous rendons, la valeur de l’index est définie de façon incrémentielle pour chaque ville.</span><span class="sxs-lookup"><span data-stu-id="c9fb6-230">Since the length of `g_txMats` is equal to the number of cities we render, the value of the index is incrementally set for each city.</span></span>

``` syntax
 for (UINT i = 0; i < m_cityRowCount; i++)
    {
        for (UINT j = 0; j < m_cityColumnCount; j++)
        {
            pCommandList->SetPipelineState(pPso);

            // Set the city's root constant for dynamically indexing into the material array.
            pCommandList->SetGraphicsRoot32BitConstant(3, (i * m_cityColumnCount) + j, 0);

            // Set this city's CBV table and move to the next descriptor.
            pCommandList->SetGraphicsRootDescriptorTable(2, cbvSrvHandle);
            cbvSrvHandle.Offset(cbvSrvDescriptorSize);

            pCommandList->DrawIndexedInstanced(numIndices, 1, 0, 0, 0);
        }
    }
```



| <span data-ttu-id="c9fb6-231">Workflow d’appel</span><span class="sxs-lookup"><span data-stu-id="c9fb6-231">Call flow</span></span>                                                                                          | <span data-ttu-id="c9fb6-232">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9fb6-232">Parameters</span></span> |
|----------------------------------------------------------------------------------------------------|------------|
| [<span data-ttu-id="c9fb6-233">**SetPipelineState**</span><span class="sxs-lookup"><span data-stu-id="c9fb6-233">**SetPipelineState**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)                             |            |
| [<span data-ttu-id="c9fb6-234">**SetGraphicsRoot32BitConstant**</span><span class="sxs-lookup"><span data-stu-id="c9fb6-234">**SetGraphicsRoot32BitConstant**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstant)     |            |
| [<span data-ttu-id="c9fb6-235">**SetGraphicsRootDescriptorTable**</span><span class="sxs-lookup"><span data-stu-id="c9fb6-235">**SetGraphicsRootDescriptorTable**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable) |            |
| [<span data-ttu-id="c9fb6-236">**DrawIndexedInstanced**</span><span class="sxs-lookup"><span data-stu-id="c9fb6-236">**DrawIndexedInstanced**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)                     |            |

## <a name="run-the-sample"></a><span data-ttu-id="c9fb6-237">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="c9fb6-237">Run the sample</span></span>

<span data-ttu-id="c9fb6-238">À présent, lorsque nous rendons la scène, chaque ville aura une valeur différente pour `matIndex` et, par conséquent, recherchera une texture différente de celle qui ressemble à `g_txMats[]` ceci :</span><span class="sxs-lookup"><span data-stu-id="c9fb6-238">Now when we render the scene, each city will have a different value for `matIndex` and will thus look up a different texture from `g_txMats[]` making the scene look like this:</span></span>

![toutes les villes apparaissent dans des couleurs différentes](images/dynamicindexing-image2.png)

## <a name="related-topics"></a><span data-ttu-id="c9fb6-240">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c9fb6-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9fb6-241">Guide pas à pas du code D3D12</span><span class="sxs-lookup"><span data-stu-id="c9fb6-241">D3D12 Code Walk-Throughs</span></span>](d3d12-code-walk-throughs.md)
</dt> <dt>

[<span data-ttu-id="c9fb6-242">Effect-Tool du compilateur</span><span class="sxs-lookup"><span data-stu-id="c9fb6-242">Effect-Compiler Tool</span></span>](/windows/desktop/direct3dtools/fxc)
</dt> <dt>

[<span data-ttu-id="c9fb6-243">Caractéristiques du modèle de nuanceur HLSL 5,1 pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="c9fb6-243">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[<span data-ttu-id="c9fb6-244">Liaison de ressources en HLSL</span><span class="sxs-lookup"><span data-stu-id="c9fb6-244">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="c9fb6-245">Modèle de nuanceur 5,1</span><span class="sxs-lookup"><span data-stu-id="c9fb6-245">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="c9fb6-246">Spécification de signatures racines en langage HLSL</span><span class="sxs-lookup"><span data-stu-id="c9fb6-246">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>
