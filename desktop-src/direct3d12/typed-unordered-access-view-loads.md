---
title: Le chargement de la vue d’accès non triée (UAV) typée
description: Le chargement typé de vue d’accès non triée (UAV) est la possibilité pour un nuanceur de lire à partir d’un UAV avec un format DXGI spécifique \_ .
ms.assetid: 6106D15E-EAF6-4583-B4F2-7CC7EE30DE15
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4adfd7511590a43b7f87507c5a1e0a2a87c925b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548530"
---
# <a name="typed-unordered-access-view-uav-loads"></a><span data-ttu-id="0ae88-103">Le chargement de la vue d’accès non triée (UAV) typée</span><span class="sxs-lookup"><span data-stu-id="0ae88-103">Typed unordered access view (UAV) loads</span></span>

<span data-ttu-id="0ae88-104">Le chargement typé de vue d’accès non triée (UAV) est la possibilité pour un nuanceur de lire à partir d’un UAV avec un [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)spécifique.</span><span class="sxs-lookup"><span data-stu-id="0ae88-104">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

-   [<span data-ttu-id="0ae88-105">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="0ae88-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="0ae88-106">Formats et appels d’API pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ae88-106">Supported formats and API calls</span></span>](#supported-formats-and-api-calls)
-   [<span data-ttu-id="0ae88-107">Utilisation de chargements UAV typés à partir de HLSL</span><span class="sxs-lookup"><span data-stu-id="0ae88-107">Using typed UAV loads from HLSL</span></span>](#using-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="0ae88-108">Utilisation des charges UAV typées UNORM et RONFLEr à partir du langage HLSL</span><span class="sxs-lookup"><span data-stu-id="0ae88-108">Using UNORM and SNORM typed UAV loads from HLSL</span></span>](#using-unorm-and-snorm-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="0ae88-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0ae88-109">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="0ae88-110">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="0ae88-110">Overview</span></span>

<span data-ttu-id="0ae88-111">Une vue d’accès non triée (UAV) est une vue d’une ressource d’accès non ordonnée (qui peut inclure des mémoires tampons, des textures et des tableaux de texture, mais sans échantillonnage multiple).</span><span class="sxs-lookup"><span data-stu-id="0ae88-111">An unordered access view (UAV) is a view of an unordered access resource (which can include buffers, textures, and texture arrays, though without multi-sampling).</span></span> <span data-ttu-id="0ae88-112">Un UAV autorise l’accès en lecture/écriture non ordonné de manière temporelle à partir de plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="0ae88-112">A UAV allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="0ae88-113">Cela signifie que ce type de ressource peut être lu/écrit simultanément par plusieurs threads sans générer de conflits de mémoire.</span><span class="sxs-lookup"><span data-stu-id="0ae88-113">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span> <span data-ttu-id="0ae88-114">Cet accès simultané est géré par le biais de l’utilisation de [fonctions atomiques](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span><span class="sxs-lookup"><span data-stu-id="0ae88-114">This simultaneous access is handled through the use of [Atomic Functions](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span></span>

<span data-ttu-id="0ae88-115">D3D12 (et D3D 11.3) s’étend sur la liste des formats qui peuvent être utilisés avec les charges UAV typées.</span><span class="sxs-lookup"><span data-stu-id="0ae88-115">D3D12 (and D3D11.3) expands on the list of formats that can be used with typed UAV loads.</span></span>

## <a name="supported-formats-and-api-calls"></a><span data-ttu-id="0ae88-116">Formats et appels d’API pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ae88-116">Supported formats and API calls</span></span>

<span data-ttu-id="0ae88-117">Auparavant, les trois formats suivants prenait en charge les chargements UAV typés, et étaient requis pour le matériel D3D 11.0.</span><span class="sxs-lookup"><span data-stu-id="0ae88-117">Previously, the following three formats supported typed UAV loads, and were required for D3D11.0 hardware.</span></span> <span data-ttu-id="0ae88-118">Ils sont pris en charge pour tous les matériels D3D 11.3 et D3D12.</span><span class="sxs-lookup"><span data-stu-id="0ae88-118">They are supported for all D3D11.3 and D3D12 hardware.</span></span>

-   <span data-ttu-id="0ae88-119">R32 \_ float</span><span class="sxs-lookup"><span data-stu-id="0ae88-119">R32\_FLOAT</span></span>
-   <span data-ttu-id="0ae88-120">R32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0ae88-120">R32\_UINT</span></span>
-   <span data-ttu-id="0ae88-121">R32 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="0ae88-121">R32\_SINT</span></span>

<span data-ttu-id="0ae88-122">Les formats suivants sont pris en charge en tant qu’ensemble sur le matériel D3D12 ou D3D 11,3. si l’un d’eux est pris en charge, tous sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="0ae88-122">The following formats are supported as a set on D3D12 or D3D11.3 hardware, so if any one is supported, all are supported.</span></span>

-   <span data-ttu-id="0ae88-123">R32G32B32A32 \_ float</span><span class="sxs-lookup"><span data-stu-id="0ae88-123">R32G32B32A32\_FLOAT</span></span>
-   <span data-ttu-id="0ae88-124">R32G32B32A32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0ae88-124">R32G32B32A32\_UINT</span></span>
-   <span data-ttu-id="0ae88-125">R32G32B32A32 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="0ae88-125">R32G32B32A32\_SINT</span></span>
-   <span data-ttu-id="0ae88-126">R16G16B16A16 \_ float</span><span class="sxs-lookup"><span data-stu-id="0ae88-126">R16G16B16A16\_FLOAT</span></span>
-   <span data-ttu-id="0ae88-127">R16G16B16A16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0ae88-127">R16G16B16A16\_UINT</span></span>
-   <span data-ttu-id="0ae88-128">R16G16B16A16 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="0ae88-128">R16G16B16A16\_SINT</span></span>
-   <span data-ttu-id="0ae88-129">R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0ae88-129">R8G8B8A8\_UNORM</span></span>
-   <span data-ttu-id="0ae88-130">R8G8B8A8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0ae88-130">R8G8B8A8\_UINT</span></span>
-   <span data-ttu-id="0ae88-131">R8G8B8A8 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="0ae88-131">R8G8B8A8\_SINT</span></span>
-   <span data-ttu-id="0ae88-132">R16 \_ float</span><span class="sxs-lookup"><span data-stu-id="0ae88-132">R16\_FLOAT</span></span>
-   <span data-ttu-id="0ae88-133">R16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0ae88-133">R16\_UINT</span></span>
-   <span data-ttu-id="0ae88-134">R16 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="0ae88-134">R16\_SINT</span></span>
-   <span data-ttu-id="0ae88-135">R8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0ae88-135">R8\_UNORM</span></span>
-   <span data-ttu-id="0ae88-136">R8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0ae88-136">R8\_UINT</span></span>
-   <span data-ttu-id="0ae88-137">R8 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="0ae88-137">R8\_SINT</span></span>

<span data-ttu-id="0ae88-138">Les formats suivants sont facultatifs et individuellement pris en charge sur le matériel D3D12 et D3D 11.3. par conséquent, une seule requête doit être effectuée sur chaque format pour tester la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0ae88-138">The following formats are optionally and individually supported on D3D12 and D3D11.3 hardware, so a single query would need to be made on each format to test for support.</span></span>

-   <span data-ttu-id="0ae88-139">R16G16B16A16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0ae88-139">R16G16B16A16\_UNORM</span></span>
-   <span data-ttu-id="0ae88-140">R16G16B16A16 \_ ronfler</span><span class="sxs-lookup"><span data-stu-id="0ae88-140">R16G16B16A16\_SNORM</span></span>
-   <span data-ttu-id="0ae88-141">R32G32 \_ float</span><span class="sxs-lookup"><span data-stu-id="0ae88-141">R32G32\_FLOAT</span></span>
-   <span data-ttu-id="0ae88-142">R32G32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0ae88-142">R32G32\_UINT</span></span>
-   <span data-ttu-id="0ae88-143">R32G32 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="0ae88-143">R32G32\_SINT</span></span>
-   <span data-ttu-id="0ae88-144">R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0ae88-144">R10G10B10A2\_UNORM</span></span>
-   <span data-ttu-id="0ae88-145">R10G10B10A2 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0ae88-145">R10G10B10A2\_UINT</span></span>
-   <span data-ttu-id="0ae88-146">R11G11B10 \_ float</span><span class="sxs-lookup"><span data-stu-id="0ae88-146">R11G11B10\_FLOAT</span></span>
-   <span data-ttu-id="0ae88-147">R8G8B8A8 \_ ronfler</span><span class="sxs-lookup"><span data-stu-id="0ae88-147">R8G8B8A8\_SNORM</span></span>
-   <span data-ttu-id="0ae88-148">R16G16 \_ float</span><span class="sxs-lookup"><span data-stu-id="0ae88-148">R16G16\_FLOAT</span></span>
-   <span data-ttu-id="0ae88-149">R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0ae88-149">R16G16\_UNORM</span></span>
-   <span data-ttu-id="0ae88-150">R16G16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0ae88-150">R16G16\_UINT</span></span>
-   <span data-ttu-id="0ae88-151">R16G16 \_ ronfler</span><span class="sxs-lookup"><span data-stu-id="0ae88-151">R16G16\_SNORM</span></span>
-   <span data-ttu-id="0ae88-152">R16G16 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="0ae88-152">R16G16\_SINT</span></span>
-   <span data-ttu-id="0ae88-153">R8G8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0ae88-153">R8G8\_UNORM</span></span>
-   <span data-ttu-id="0ae88-154">R8G8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="0ae88-154">R8G8\_UINT</span></span>
-   <span data-ttu-id="0ae88-155">R8G8 \_ ronfler</span><span class="sxs-lookup"><span data-stu-id="0ae88-155">R8G8\_SNORM</span></span>
-   <span data-ttu-id="0ae88-156">R8G8 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="0ae88-156">R8G8\_SINT</span></span>
-   <span data-ttu-id="0ae88-157">R16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0ae88-157">R16\_UNORM</span></span>
-   <span data-ttu-id="0ae88-158">R16 \_ ronfler</span><span class="sxs-lookup"><span data-stu-id="0ae88-158">R16\_SNORM</span></span>
-   <span data-ttu-id="0ae88-159">R8 \_ ronfler</span><span class="sxs-lookup"><span data-stu-id="0ae88-159">R8\_SNORM</span></span>
-   <span data-ttu-id="0ae88-160">A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0ae88-160">A8\_UNORM</span></span>
-   <span data-ttu-id="0ae88-161">B5G6R5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0ae88-161">B5G6R5\_UNORM</span></span>
-   <span data-ttu-id="0ae88-162">B5G5R5A1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0ae88-162">B5G5R5A1\_UNORM</span></span>
-   <span data-ttu-id="0ae88-163">B4G4R4A4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="0ae88-163">B4G4R4A4\_UNORM</span></span>

<span data-ttu-id="0ae88-164">Pour déterminer la prise en charge de tout autre format, appelez [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) avec la structure d' [**\_ \_ \_ \_ options D3D12 des données de la fonctionnalité D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) en tant que premier paramètre (reportez-vous à [fonctionnalité interrogation](capability-querying.md)).</span><span class="sxs-lookup"><span data-stu-id="0ae88-164">To determine the support for any additional formats, call [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) with the [**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) structure as the first parameter (refer to [Capability Querying](capability-querying.md)).</span></span> <span data-ttu-id="0ae88-165">Le champ *TypedUAVLoadAdditionalFormats* est défini si la liste « pris en charge en tant que jeu » ci-dessus est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0ae88-165">The *TypedUAVLoadAdditionalFormats* field will be set if the "supported as a set" list above is supported.</span></span> <span data-ttu-id="0ae88-166">Effectuer un deuxième appel à **CheckFeatureSupport**, à l’aide d’une structure de [**\_ \_ \_ \_ prise en charge du format de données de la fonctionnalité D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) (vérification de la structure retournée par rapport à la structure D3D12 membre de \_ \_ \_ \_ chargement de type d’élément UAV \_ de l’énumération de [**\_ format \_ de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) ) pour déterminer la prise en charge dans la liste des formats éventuellement pris en charge, par exemple :</span><span class="sxs-lookup"><span data-stu-id="0ae88-166">Make a second call to **CheckFeatureSupport**, using a [**D3D12\_FEATURE\_DATA\_FORMAT\_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) structure (checking the returned structure against the D3D12\_FORMAT\_SUPPORT2\_UAV\_TYPED\_LOAD member of the [**D3D12\_FORMAT\_SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) enum) to determine support in the list of optionally supported formats listed above, for example:</span></span>

``` syntax
D3D12_FEATURE_DATA_D3D12_OPTIONS FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Cannot assume other formats are supported, so we check:
        D3D12_FEATURE_DATA_FORMAT_SUPPORT FormatSupport = {DXGI_FORMAT_R32G32_FLOAT, D3D12_FORMAT_SUPPORT1_NONE, D3D12_FORMAT_SUPPORT2_NONE};
        hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_FORMAT_SUPPORT, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.Support2 & D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
        {
            // DXGI_FORMAT_R32G32_FLOAT supports UAV Typed Load!
        }
    }
}
```

## <a name="using-typed-uav-loads-from-hlsl"></a><span data-ttu-id="0ae88-167">Utilisation de chargements UAV typés à partir de HLSL</span><span class="sxs-lookup"><span data-stu-id="0ae88-167">Using typed UAV loads from HLSL</span></span>

<span data-ttu-id="0ae88-168">Pour les UAVs typés, l’indicateur HLSL est un \_ nuanceur D3D \_ nécessitant \_ \_ \_ \_ des formats supplémentaires de chargement UAV \_ .</span><span class="sxs-lookup"><span data-stu-id="0ae88-168">For typed UAVs, the HLSL flag is D3D\_SHADER\_REQUIRES\_TYPED\_UAV\_LOAD\_ADDITIONAL\_FORMATS.</span></span>

<span data-ttu-id="0ae88-169">Voici un exemple de code de nuanceur pour traiter une charge de UAV typée :</span><span class="sxs-lookup"><span data-stu-id="0ae88-169">Here is example shader code to process a typed UAV load:</span></span>

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="using-unorm-and-snorm-typed-uav-loads-from-hlsl"></a><span data-ttu-id="0ae88-170">Utilisation des charges UAV typées UNORM et RONFLEr à partir du langage HLSL</span><span class="sxs-lookup"><span data-stu-id="0ae88-170">Using UNORM and SNORM typed UAV loads from HLSL</span></span>

<span data-ttu-id="0ae88-171">Lorsque vous utilisez des chargements UAV typés pour lire à partir d’une ressource UNORM ou RONFLEr, vous devez déclarer correctement le type d’élément de l’objet HLSL sur `unorm` ou `snorm` .</span><span class="sxs-lookup"><span data-stu-id="0ae88-171">When using typed UAV loads to read from a UNORM or SNORM resource, you must properly declare the element type of the HLSL object to be `unorm` or `snorm`.</span></span> <span data-ttu-id="0ae88-172">Elle est spécifiée comme un comportement indéfini pour incompatibilité avec le type d’élément déclaré en HLSL avec le type de données de ressource sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="0ae88-172">It is specified as undefined behavior to mismatch the element type declared in HLSL with the underlying resource data type.</span></span> <span data-ttu-id="0ae88-173">Par exemple, si vous utilisez des charges UAV typées sur une ressource de mémoire tampon avec des \_ données R8 UNORM, vous devez déclarer le type d’élément comme `unorm float` suit :</span><span class="sxs-lookup"><span data-stu-id="0ae88-173">For example, if you are using typed UAV loads on a buffer resource with R8\_UNORM data, then you must declare the element type as `unorm float`:</span></span>

``` syntax
RWBuffer<unorm float> uav;
```

## <a name="related-topics"></a><span data-ttu-id="0ae88-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0ae88-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ae88-175">Rendu</span><span class="sxs-lookup"><span data-stu-id="0ae88-175">Rendering</span></span>](rendering.md)
</dt> <dt>

[<span data-ttu-id="0ae88-176">Liaison de ressource</span><span class="sxs-lookup"><span data-stu-id="0ae88-176">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="0ae88-177">Liaison de ressources en HLSL</span><span class="sxs-lookup"><span data-stu-id="0ae88-177">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="0ae88-178">Modèle de nuanceur 5,1</span><span class="sxs-lookup"><span data-stu-id="0ae88-178">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="0ae88-179">Spécification de signatures racines en langage HLSL</span><span class="sxs-lookup"><span data-stu-id="0ae88-179">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 