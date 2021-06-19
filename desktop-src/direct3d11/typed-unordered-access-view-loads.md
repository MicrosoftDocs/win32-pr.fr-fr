---
title: Chargements de vues d’accès non ordonnées typées
description: En savoir plus sur la charge typée de la vue d’accès non triée (UAV) dans Direct3D 11. La charge typée UAV est la capacité d’un nuanceur à lire à partir d’un UAV avec un DXGI_FORMAT spécifique.
ms.assetid: BA72BF21-8621-461D-8677-9DFB7D5BC6AA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c6d2cbfa51c8473dc3da51c5844c63bef944b50
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396284"
---
# <a name="typed-unordered-access-view-loads"></a><span data-ttu-id="282c5-104">Chargements de vues d’accès non ordonnées typées</span><span class="sxs-lookup"><span data-stu-id="282c5-104">Typed Unordered Access View Loads</span></span>

<span data-ttu-id="282c5-105">Le chargement typé de vue d’accès non triée (UAV) est la possibilité pour un nuanceur de lire à partir d’un UAV avec un format DXGI spécifique \_ .</span><span class="sxs-lookup"><span data-stu-id="282c5-105">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific DXGI\_FORMAT.</span></span>

-   [<span data-ttu-id="282c5-106">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="282c5-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="282c5-107">Formats et appels d’API pris en charge</span><span class="sxs-lookup"><span data-stu-id="282c5-107">Supported formats and API calls</span></span>](#supported-formats-and-api-calls)
-   [<span data-ttu-id="282c5-108">Utilisation de chargements UAV typés à partir de HLSL</span><span class="sxs-lookup"><span data-stu-id="282c5-108">Using typed UAV loads from HLSL</span></span>](#using-typed-uav-loads-from-hlsl)
-   [<span data-ttu-id="282c5-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="282c5-109">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="282c5-110">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="282c5-110">Overview</span></span>

<span data-ttu-id="282c5-111">Une vue d’accès non triée (UAV) est une vue d’une ressource d’accès non ordonnée (qui peut inclure des mémoires tampons, des textures et des tableaux de texture, mais sans échantillonnage multiple).</span><span class="sxs-lookup"><span data-stu-id="282c5-111">An unordered access view (UAV) is a view of an unordered access resource (which can include buffers, textures, and texture arrays, though without multi-sampling).</span></span> <span data-ttu-id="282c5-112">Un UAV autorise l’accès en lecture/écriture non ordonné de manière temporelle à partir de plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="282c5-112">A UAV allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="282c5-113">Cela signifie que ce type de ressource peut être lu/écrit simultanément par plusieurs threads sans générer de conflits de mémoire.</span><span class="sxs-lookup"><span data-stu-id="282c5-113">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span> <span data-ttu-id="282c5-114">Cet accès simultané est géré par le biais de l’utilisation de [fonctions atomiques](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span><span class="sxs-lookup"><span data-stu-id="282c5-114">This simultaneous access is handled through the use of [Atomic Functions](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).</span></span>

<span data-ttu-id="282c5-115">D3D12 et D3D 11.3 se développent dans la liste des formats qui peuvent être utilisés avec les charges UAV typées.</span><span class="sxs-lookup"><span data-stu-id="282c5-115">D3D12 and D3D11.3 expands on the list of formats that can be used with typed UAV loads.</span></span>

## <a name="supported-formats-and-api-calls"></a><span data-ttu-id="282c5-116">Formats et appels d’API pris en charge</span><span class="sxs-lookup"><span data-stu-id="282c5-116">Supported formats and API calls</span></span>

<span data-ttu-id="282c5-117">Auparavant, les trois formats suivants prenait en charge les chargements UAV typés, et étaient requis pour le matériel D3D 11.0.</span><span class="sxs-lookup"><span data-stu-id="282c5-117">Previously, the following three formats supported typed UAV loads, and were required for D3D11.0 hardware.</span></span> <span data-ttu-id="282c5-118">Ils sont pris en charge pour tous les matériels D3D 11.3 et D3D12.</span><span class="sxs-lookup"><span data-stu-id="282c5-118">They are supported for all D3D11.3 and D3D12 hardware.</span></span>

-   <span data-ttu-id="282c5-119">R32 \_ float</span><span class="sxs-lookup"><span data-stu-id="282c5-119">R32\_FLOAT</span></span>
-   <span data-ttu-id="282c5-120">R32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="282c5-120">R32\_UINT</span></span>
-   <span data-ttu-id="282c5-121">R32 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="282c5-121">R32\_SINT</span></span>

<span data-ttu-id="282c5-122">Les formats suivants sont pris en charge en tant qu’ensemble sur le matériel D3D12 ou D3D 11,3. si l’un d’eux est pris en charge, tous sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="282c5-122">The following formats are supported as a set on D3D12 or D3D11.3 hardware, so if any one is supported, all are supported.</span></span>

-   <span data-ttu-id="282c5-123">R32G32B32A32 \_ float</span><span class="sxs-lookup"><span data-stu-id="282c5-123">R32G32B32A32\_FLOAT</span></span>
-   <span data-ttu-id="282c5-124">R32G32B32A32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="282c5-124">R32G32B32A32\_UINT</span></span>
-   <span data-ttu-id="282c5-125">R32G32B32A32 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="282c5-125">R32G32B32A32\_SINT</span></span>
-   <span data-ttu-id="282c5-126">R16G16B16A16 \_ float</span><span class="sxs-lookup"><span data-stu-id="282c5-126">R16G16B16A16\_FLOAT</span></span>
-   <span data-ttu-id="282c5-127">R16G16B16A16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="282c5-127">R16G16B16A16\_UINT</span></span>
-   <span data-ttu-id="282c5-128">R16G16B16A16 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="282c5-128">R16G16B16A16\_SINT</span></span>
-   <span data-ttu-id="282c5-129">R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="282c5-129">R8G8B8A8\_UNORM</span></span>
-   <span data-ttu-id="282c5-130">R8G8B8A8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="282c5-130">R8G8B8A8\_UINT</span></span>
-   <span data-ttu-id="282c5-131">R8G8B8A8 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="282c5-131">R8G8B8A8\_SINT</span></span>
-   <span data-ttu-id="282c5-132">R16 \_ float</span><span class="sxs-lookup"><span data-stu-id="282c5-132">R16\_FLOAT</span></span>
-   <span data-ttu-id="282c5-133">R16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="282c5-133">R16\_UINT</span></span>
-   <span data-ttu-id="282c5-134">R16 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="282c5-134">R16\_SINT</span></span>
-   <span data-ttu-id="282c5-135">R8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="282c5-135">R8\_UNORM</span></span>
-   <span data-ttu-id="282c5-136">R8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="282c5-136">R8\_UINT</span></span>
-   <span data-ttu-id="282c5-137">R8 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="282c5-137">R8\_SINT</span></span>

<span data-ttu-id="282c5-138">Les formats suivants sont facultatifs et individuellement pris en charge sur le matériel D3D12 et D3D 11.3. par conséquent, une seule requête doit être effectuée sur chaque format pour tester la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="282c5-138">The following formats are optionally and individually supported on D3D12 and D3D11.3 hardware, so a single query would need to be made on each format to test for support.</span></span>

-   <span data-ttu-id="282c5-139">R16G16B16A16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="282c5-139">R16G16B16A16\_UNORM</span></span>
-   <span data-ttu-id="282c5-140">R16G16B16A16 \_ ronfler</span><span class="sxs-lookup"><span data-stu-id="282c5-140">R16G16B16A16\_SNORM</span></span>
-   <span data-ttu-id="282c5-141">R32G32 \_ float</span><span class="sxs-lookup"><span data-stu-id="282c5-141">R32G32\_FLOAT</span></span>
-   <span data-ttu-id="282c5-142">R32G32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="282c5-142">R32G32\_UINT</span></span>
-   <span data-ttu-id="282c5-143">R32G32 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="282c5-143">R32G32\_SINT</span></span>
-   <span data-ttu-id="282c5-144">R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="282c5-144">R10G10B10A2\_UNORM</span></span>
-   <span data-ttu-id="282c5-145">R10G10B10A2 \_ uint</span><span class="sxs-lookup"><span data-stu-id="282c5-145">R10G10B10A2\_UINT</span></span>
-   <span data-ttu-id="282c5-146">R11G11B10 \_ float</span><span class="sxs-lookup"><span data-stu-id="282c5-146">R11G11B10\_FLOAT</span></span>
-   <span data-ttu-id="282c5-147">R8G8B8A8 \_ ronfler</span><span class="sxs-lookup"><span data-stu-id="282c5-147">R8G8B8A8\_SNORM</span></span>
-   <span data-ttu-id="282c5-148">R16G16 \_ float</span><span class="sxs-lookup"><span data-stu-id="282c5-148">R16G16\_FLOAT</span></span>
-   <span data-ttu-id="282c5-149">R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="282c5-149">R16G16\_UNORM</span></span>
-   <span data-ttu-id="282c5-150">R16G16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="282c5-150">R16G16\_UINT</span></span>
-   <span data-ttu-id="282c5-151">R16G16 \_ ronfler</span><span class="sxs-lookup"><span data-stu-id="282c5-151">R16G16\_SNORM</span></span>
-   <span data-ttu-id="282c5-152">R16G16 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="282c5-152">R16G16\_SINT</span></span>
-   <span data-ttu-id="282c5-153">R8G8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="282c5-153">R8G8\_UNORM</span></span>
-   <span data-ttu-id="282c5-154">R8G8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="282c5-154">R8G8\_UINT</span></span>
-   <span data-ttu-id="282c5-155">R8G8 \_ ronfler</span><span class="sxs-lookup"><span data-stu-id="282c5-155">R8G8\_SNORM</span></span>
-   <span data-ttu-id="282c5-156">8G8 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="282c5-156">8G8\_SINT</span></span>
-   <span data-ttu-id="282c5-157">R16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="282c5-157">R16\_UNORM</span></span>
-   <span data-ttu-id="282c5-158">R16 \_ ronfler</span><span class="sxs-lookup"><span data-stu-id="282c5-158">R16\_SNORM</span></span>
-   <span data-ttu-id="282c5-159">R8 \_ ronfler</span><span class="sxs-lookup"><span data-stu-id="282c5-159">R8\_SNORM</span></span>
-   <span data-ttu-id="282c5-160">A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="282c5-160">A8\_UNORM</span></span>
-   <span data-ttu-id="282c5-161">B5G6R5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="282c5-161">B5G6R5\_UNORM</span></span>
-   <span data-ttu-id="282c5-162">B5G5R5A1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="282c5-162">B5G5R5A1\_UNORM</span></span>
-   <span data-ttu-id="282c5-163">B4G4R4A4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="282c5-163">B4G4R4A4\_UNORM</span></span>

<span data-ttu-id="282c5-164">Pour déterminer la prise en charge de tout autre format, appelez [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) avec la structure [**\_ \_ \_ d3d11 \_ OPTIONS2 des données de la fonctionnalité d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) en tant que premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="282c5-164">To determine the support for any additional formats, call [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) with the [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) structure as the first parameter.</span></span> <span data-ttu-id="282c5-165">Le `TypedUAVLoadAdditionalFormats` bit est défini si la liste « pris en charge en tant que jeu » ci-dessus est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="282c5-165">The `TypedUAVLoadAdditionalFormats` bit will be set if the "supported as a set" list above is supported.</span></span> <span data-ttu-id="282c5-166">Effectuez un deuxième appel à **CheckFeatureSupport**, à l’aide de la structure de données de la [**fonctionnalité d3d11, (vérification \_ \_ \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) de la structure retournée par rapport au D3D12 \_ format \_ de chargement de type d’élément \_ UAV \_ \_ de l’énumération de format d3d11) pour déterminer la prise en charge dans la liste des formats éventuellement pris en charge ci-dessus, par exemple : [**\_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2)</span><span class="sxs-lookup"><span data-stu-id="282c5-166">Make a second call to **CheckFeatureSupport**, using a [**D3D11\_FEATURE\_DATA\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) structure (checking the returned structure against the D3D12\_FORMAT\_SUPPORT2\_UAV\_TYPED\_LOAD member of the [**D3D11\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) enum) to determine support in the list of optionally supported formats above, for example:</span></span>

``` syntax
D3D11_FEATURE_DATA_D3D11_OPTIONS2 FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_D3D11_OPTIONS2, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Can not assume other formats are supported, so we check:
        D3D11_FEATURE_DATA_FORMAT_SUPPORT2 FormatSupport;
        ZeroMemory(&FormatSupport, sizeof(FormatSupport));
        FormatSupport.InFormat = DXGI_FORMAT_R32G32_FLOAT;
        hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_FORMAT_SUPPORT2, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.OutFormatSupport2 & D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
        {
            // DXGI_FORMAT_R32G32_FLOAT supports UAV Typed Load!
        }
    }
}
```

## <a name="using-typed-uav-loads-from-hlsl"></a><span data-ttu-id="282c5-167">Utilisation de chargements UAV typés à partir de HLSL</span><span class="sxs-lookup"><span data-stu-id="282c5-167">Using typed UAV loads from HLSL</span></span>

<span data-ttu-id="282c5-168">Pour les UAVs typés, l’indicateur HLSL est un \_ nuanceur D3D \_ nécessitant \_ \_ \_ \_ des formats supplémentaires de chargement UAV \_ .</span><span class="sxs-lookup"><span data-stu-id="282c5-168">For typed UAVs, the HLSL flag is D3D\_SHADER\_REQUIRES\_TYPED\_UAV\_LOAD\_ADDITIONAL\_FORMATS.</span></span>

<span data-ttu-id="282c5-169">Voici un exemple de code de nuanceur pour traiter une charge de UAV typée :</span><span class="sxs-lookup"><span data-stu-id="282c5-169">Here is example shader code to process a typed UAV load:</span></span>

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="related-topics"></a><span data-ttu-id="282c5-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="282c5-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="282c5-171">Fonctionnalités Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="282c5-171">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="282c5-172">Modèle de nuanceur 5,1</span><span class="sxs-lookup"><span data-stu-id="282c5-172">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 