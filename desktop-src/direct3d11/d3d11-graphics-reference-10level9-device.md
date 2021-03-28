---
title: Méthodes 10Level9 ID3D11Device
description: Cette section répertorie les différences entre chaque niveau de fonctionnalité 10Level9 et le niveau de fonctionnalité D3D \_ \_ \_ 11 \_ 0 et supérieur pour les méthodes ID3D11Device.
ms.assetid: c3bc32a9-8d97-430b-be6a-b4935d7ac56c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400c7f321981f13b3e184a25139782c8a9d9a2ba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382397"
---
# <a name="10level9-id3d11device-methods"></a><span data-ttu-id="9a6aa-103">Méthodes 10Level9 ID3D11Device</span><span class="sxs-lookup"><span data-stu-id="9a6aa-103">10Level9 ID3D11Device Methods</span></span>

<span data-ttu-id="9a6aa-104">Cette section répertorie les différences entre chaque niveau de fonctionnalité 10Level9 et le niveau de fonctionnalité D3D \_ \_ \_ 11 \_ 0 et supérieur pour les méthodes [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .</span><span class="sxs-lookup"><span data-stu-id="9a6aa-104">This section lists the differences between each 10Level9 feature level and the D3D\_FEATURE\_LEVEL\_11\_0 and higher feature level for the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) methods.</span></span>

-   [<span data-ttu-id="9a6aa-105">ID3D11Device :: CheckCounter</span><span class="sxs-lookup"><span data-stu-id="9a6aa-105">ID3D11Device::CheckCounter</span></span>](#id3d11devicecheckcounter)
-   [<span data-ttu-id="9a6aa-106">ID3D11Device :: CheckFormatSupport</span><span class="sxs-lookup"><span data-stu-id="9a6aa-106">ID3D11Device::CheckFormatSupport</span></span>](#id3d11devicecheckformatsupport)
-   [<span data-ttu-id="9a6aa-107">ID3D11Device :: CheckMultisampleQualityLevels</span><span class="sxs-lookup"><span data-stu-id="9a6aa-107">ID3D11Device::CheckMultisampleQualityLevels</span></span>](#id3d11devicecheckmultisamplequalitylevels)
-   [<span data-ttu-id="9a6aa-108">ID3D11Device :: CreateBlendState</span><span class="sxs-lookup"><span data-stu-id="9a6aa-108">ID3D11Device::CreateBlendState</span></span>](#id3d11devicecreateblendstate)
-   [<span data-ttu-id="9a6aa-109">ID3D11Device :: CreateBlendState1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-109">ID3D11Device::CreateBlendState1</span></span>](#id3d11devicecreateblendstate1)
-   [<span data-ttu-id="9a6aa-110">ID3D11Device :: CreateBuffer</span><span class="sxs-lookup"><span data-stu-id="9a6aa-110">ID3D11Device::CreateBuffer</span></span>](#id3d11devicecreatebuffer)
-   [<span data-ttu-id="9a6aa-111">ID3D11Device :: CreateCounter</span><span class="sxs-lookup"><span data-stu-id="9a6aa-111">ID3D11Device::CreateCounter</span></span>](#id3d11devicecreatecounter)
-   [<span data-ttu-id="9a6aa-112">ID3D11Device :: CreateDepthStencilView</span><span class="sxs-lookup"><span data-stu-id="9a6aa-112">ID3D11Device::CreateDepthStencilView</span></span>](#id3d11devicecreatedepthstencilview)
-   [<span data-ttu-id="9a6aa-113">ID3D11Device :: CreateDomainShader</span><span class="sxs-lookup"><span data-stu-id="9a6aa-113">ID3D11Device::CreateDomainShader</span></span>](#id3d11devicecreatedomainshader)
-   [<span data-ttu-id="9a6aa-114">ID3D11Device :: CreateGeometryShader</span><span class="sxs-lookup"><span data-stu-id="9a6aa-114">ID3D11Device::CreateGeometryShader</span></span>](#id3d11devicecreategeometryshader)
-   [<span data-ttu-id="9a6aa-115">ID3D11Device :: CreateGeometryShaderWithStreamOutput</span><span class="sxs-lookup"><span data-stu-id="9a6aa-115">ID3D11Device::CreateGeometryShaderWithStreamOutput</span></span>](#id3d11devicecreategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="9a6aa-116">ID3D11Device :: CreateHullShader</span><span class="sxs-lookup"><span data-stu-id="9a6aa-116">ID3D11Device::CreateHullShader</span></span>](#id3d11devicecreatehullshader)
-   [<span data-ttu-id="9a6aa-117">ID3D11Device :: CreateInputLayout</span><span class="sxs-lookup"><span data-stu-id="9a6aa-117">ID3D11Device::CreateInputLayout</span></span>](#id3d11devicecreateinputlayout)
-   [<span data-ttu-id="9a6aa-118">ID3D11Device :: CreatePixelShader</span><span class="sxs-lookup"><span data-stu-id="9a6aa-118">ID3D11Device::CreatePixelShader</span></span>](#id3d11devicecreatepixelshader)
-   [<span data-ttu-id="9a6aa-119">ID3D11Device :: CreatePredicate</span><span class="sxs-lookup"><span data-stu-id="9a6aa-119">ID3D11Device::CreatePredicate</span></span>](#id3d11devicecreatepredicate)
-   [<span data-ttu-id="9a6aa-120">ID3D11Device :: CreateQuery</span><span class="sxs-lookup"><span data-stu-id="9a6aa-120">ID3D11Device::CreateQuery</span></span>](#id3d11devicecreatequery)
-   [<span data-ttu-id="9a6aa-121">ID3D11Device :: CreateRasterizerState</span><span class="sxs-lookup"><span data-stu-id="9a6aa-121">ID3D11Device::CreateRasterizerState</span></span>](#id3d11devicecreaterasterizerstate)
-   [<span data-ttu-id="9a6aa-122">ID3D11Device :: CreateRenderTargetView</span><span class="sxs-lookup"><span data-stu-id="9a6aa-122">ID3D11Device::CreateRenderTargetView</span></span>](#id3d11devicecreaterendertargetview)
-   [<span data-ttu-id="9a6aa-123">ID3D11Device :: CreateSamplerState</span><span class="sxs-lookup"><span data-stu-id="9a6aa-123">ID3D11Device::CreateSamplerState</span></span>](#id3d11devicecreatesamplerstate)
-   [<span data-ttu-id="9a6aa-124">ID3D11Device :: CreateShaderResourceView</span><span class="sxs-lookup"><span data-stu-id="9a6aa-124">ID3D11Device::CreateShaderResourceView</span></span>](#id3d11devicecreateshaderresourceview)
-   [<span data-ttu-id="9a6aa-125">ID3D11Device :: CreateTexture1D</span><span class="sxs-lookup"><span data-stu-id="9a6aa-125">ID3D11Device::CreateTexture1D</span></span>](#id3d11devicecreatetexture1d)
-   [<span data-ttu-id="9a6aa-126">ID3D11Device :: CreateTexture2D</span><span class="sxs-lookup"><span data-stu-id="9a6aa-126">ID3D11Device::CreateTexture2D</span></span>](#id3d11devicecreatetexture2d)
-   [<span data-ttu-id="9a6aa-127">ID3D11Device :: CreateTexture3D</span><span class="sxs-lookup"><span data-stu-id="9a6aa-127">ID3D11Device::CreateTexture3D</span></span>](#id3d11devicecreatetexture3d)
-   [<span data-ttu-id="9a6aa-128">ID3D11Device :: CreateUnorderedAccessView</span><span class="sxs-lookup"><span data-stu-id="9a6aa-128">ID3D11Device::CreateUnorderedAccessView</span></span>](#id3d11devicecreateunorderedaccessview)
-   [<span data-ttu-id="9a6aa-129">ID3D11Device :: CreateVertexShader</span><span class="sxs-lookup"><span data-stu-id="9a6aa-129">ID3D11Device::CreateVertexShader</span></span>](#id3d11devicecreatevertexshader)
-   [<span data-ttu-id="9a6aa-130">ID3D11Device :: OpenSharedResource</span><span class="sxs-lookup"><span data-stu-id="9a6aa-130">ID3D11Device::OpenSharedResource</span></span>](#id3d11deviceopensharedresource)
-   [<span data-ttu-id="9a6aa-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9a6aa-131">Related topics</span></span>](#related-topics)

## <a name="id3d11devicecheckcounter"></a><span data-ttu-id="9a6aa-132">ID3D11Device :: CheckCounter</span><span class="sxs-lookup"><span data-stu-id="9a6aa-132">ID3D11Device::CheckCounter</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9a6aa-133">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-133">Feature Level</span></span></th>
<th><span data-ttu-id="9a6aa-134">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="9a6aa-134">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a6aa-135">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-135">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="9a6aa-136">Les compteurs dépendants de l’appareil sont éventuellement pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-136">Device-dependent counters are optionally supported.</span></span> <span data-ttu-id="9a6aa-137">Utilisez <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkcounterinfo"><strong>ID3D11Device :: CheckCounterInfo</strong></a> pour déterminer la prise en charge. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="9a6aa-137">Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkcounterinfo"><strong>ID3D11Device::CheckCounterInfo</strong></a> to determine support.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a6aa-138">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-138">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="9a6aa-139">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-139">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecheckformatsupport"></a><span data-ttu-id="9a6aa-140">ID3D11Device :: CheckFormatSupport</span><span class="sxs-lookup"><span data-stu-id="9a6aa-140">ID3D11Device::CheckFormatSupport</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9a6aa-141">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-141">Feature Level</span></span></th>
<th><span data-ttu-id="9a6aa-142">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="9a6aa-142">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a6aa-143">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-143">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="9a6aa-144">Consultez formater la prise en charge par <a href="overviews-direct3d-11-devices-downlevel-intro.md">niveau de fonctionnalité</a>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="9a6aa-144">See format support by <a href="overviews-direct3d-11-devices-downlevel-intro.md">feature level</a>${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a6aa-145">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-145">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="9a6aa-146">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-146">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecheckmultisamplequalitylevels"></a><span data-ttu-id="9a6aa-147">ID3D11Device :: CheckMultisampleQualityLevels</span><span class="sxs-lookup"><span data-stu-id="9a6aa-147">ID3D11Device::CheckMultisampleQualityLevels</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9a6aa-148">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-148">Feature Level</span></span></th>
<th><span data-ttu-id="9a6aa-149">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="9a6aa-149">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a6aa-150">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-150">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="9a6aa-151">Les niveaux de fonctionnalité n’assurent aucune garantie quant à la prise en charge MSAA. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="9a6aa-151">Feature levels make no guarantees concerning MSAA support.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a6aa-152">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-152">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="9a6aa-153">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-153">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateblendstate"></a><span data-ttu-id="9a6aa-154">ID3D11Device :: CreateBlendState</span><span class="sxs-lookup"><span data-stu-id="9a6aa-154">ID3D11Device::CreateBlendState</span></span>



| <span data-ttu-id="9a6aa-155">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-155">Feature Level</span></span>              | <span data-ttu-id="9a6aa-156">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="9a6aa-156">Behavior Differences</span></span>                                                                                                                                                                                                                                                                                                                                             |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a6aa-157">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-157">D3D\_FEATURE\_LEVEL\_9\_1</span></span>  | <span data-ttu-id="9a6aa-158">AlphaToCoverageEnable doit avoir la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-158">AlphaToCoverageEnable must be **FALSE**.</span></span><br/> <span data-ttu-id="9a6aa-159">Les quatre premiers BlendEnables doivent tous avoir la même valeur.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-159">The first four BlendEnables must all have the same value.</span></span><br/> <span data-ttu-id="9a6aa-160">D3D11 \_ Blend \_ src \_ ALPHASAT non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-160">D3D11\_BLEND\_SRC\_ALPHASAT not supported.</span></span><br/> <span data-ttu-id="9a6aa-161">Mélange de couleurs à double source non pris en charge (SrcBlend ou DestBlend avec SRC1 dans le nom)</span><span class="sxs-lookup"><span data-stu-id="9a6aa-161">Dual-source color blend not supported (any SrcBlend or DestBlend with SRC1 in the name)</span></span><br/>                                                                                |
| <span data-ttu-id="9a6aa-162">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-162">D3D\_FEATURE\_LEVEL\_9\_2</span></span>  | <span data-ttu-id="9a6aa-163">AlphaToCoverageEnable doit avoir la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-163">AlphaToCoverageEnable must be **FALSE**.</span></span><br/> <span data-ttu-id="9a6aa-164">Les quatre premiers BlendEnables doivent tous avoir la même valeur.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-164">The first four BlendEnables must all have the same value.</span></span><br/> <span data-ttu-id="9a6aa-165">Les quatre premiers RenderTargetWriteMasks doivent tous avoir la même valeur.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-165">The first four RenderTargetWriteMasks must all have the same value.</span></span><br/> <span data-ttu-id="9a6aa-166">D3D11 \_ Blend \_ src \_ ALPHASAT non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-166">D3D11\_BLEND\_SRC\_ALPHASAT not supported.</span></span><br/> <span data-ttu-id="9a6aa-167">Mélange de couleurs à double source non pris en charge (SrcBlend ou DestBlend avec SRC1 dans le nom)</span><span class="sxs-lookup"><span data-stu-id="9a6aa-167">Dual-source color blend not supported (any SrcBlend or DestBlend with SRC1 in the name)</span></span><br/> |
| <span data-ttu-id="9a6aa-168">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-168">D3D\_FEATURE\_LEVEL\_9\_3</span></span>  | <span data-ttu-id="9a6aa-169">AlphaToCoverageEnable doit avoir la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-169">AlphaToCoverageEnable must be **FALSE**.</span></span><br/> <span data-ttu-id="9a6aa-170">Les quatre premiers BlendEnables doivent tous avoir la même valeur.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-170">The first four BlendEnables must all have the same value.</span></span><br/> <span data-ttu-id="9a6aa-171">D3D11 \_ Blend \_ src \_ ALPHASAT non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-171">D3D11\_BLEND\_SRC\_ALPHASAT not supported.</span></span><br/> <span data-ttu-id="9a6aa-172">Mélange de couleurs à double source non pris en charge (SrcBlend ou DestBlend avec SRC1 dans le nom)</span><span class="sxs-lookup"><span data-stu-id="9a6aa-172">Dual-source color blend not supported (any SrcBlend or DestBlend with SRC1 in the name)</span></span><br/>                                                                                |
| <span data-ttu-id="9a6aa-173">\_Niveau de fonctionnalité D3D \_ \_ 10 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9a6aa-173">D3D\_FEATURE\_LEVEL\_10\_0</span></span> | <span data-ttu-id="9a6aa-174">Ajoute alpha-to-coverage</span><span class="sxs-lookup"><span data-stu-id="9a6aa-174">Adds alpha-to-coverage</span></span>                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="id3d11devicecreateblendstate1"></a><span data-ttu-id="9a6aa-175">ID3D11Device :: CreateBlendState1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-175">ID3D11Device::CreateBlendState1</span></span>



| <span data-ttu-id="9a6aa-176">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-176">Feature Level</span></span>              | <span data-ttu-id="9a6aa-177">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="9a6aa-177">Behavior Differences</span></span>                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a6aa-178">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-178">D3D\_FEATURE\_LEVEL\_9\_1</span></span>  | <span data-ttu-id="9a6aa-179">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a6aa-179">Unsupported</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="9a6aa-180">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-180">D3D\_FEATURE\_LEVEL\_9\_2</span></span>  | <span data-ttu-id="9a6aa-181">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a6aa-181">Unsupported</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="9a6aa-182">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-182">D3D\_FEATURE\_LEVEL\_9\_3</span></span>  | <span data-ttu-id="9a6aa-183">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a6aa-183">Unsupported</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="9a6aa-184">\_Niveau de fonctionnalité D3D \_ \_ 10 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9a6aa-184">D3D\_FEATURE\_LEVEL\_10\_0</span></span> | <span data-ttu-id="9a6aa-185">Le membre *OutputMergerLogicOp* a été ajouté aux [**\_ \_ \_ \_ options d3d11 des données de la fonctionnalité d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options)pour déterminer la prise en charge des opérations logiques (opérations de logique au niveau du bit entre la sortie du nuanceur de pixels et le contenu de la cible de rendu, reportez-vous à [**d3d11 \_ Render \_ target \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1)).</span><span class="sxs-lookup"><span data-stu-id="9a6aa-185">The *OutputMergerLogicOp* member has been added to [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options), to determine support for logical operations (bitwise logic operations between pixel shader output and render target contents, refer to [**D3D11\_RENDER\_TARGET\_BLEND\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1)).</span></span> |



 

## <a name="id3d11devicecreatebuffer"></a><span data-ttu-id="9a6aa-186">ID3D11Device :: CreateBuffer</span><span class="sxs-lookup"><span data-stu-id="9a6aa-186">ID3D11Device::CreateBuffer</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9a6aa-187">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-187">Feature Level</span></span></th>
<th><span data-ttu-id="9a6aa-188">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="9a6aa-188">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a6aa-189">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-189">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td><span data-ttu-id="9a6aa-190">Les mémoires tampons ne peuvent pas avoir de vues de cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-190">Buffers can't have render target views.</span></span><br/> <span data-ttu-id="9a6aa-191">Les mémoires tampons doivent avoir une seule des D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER ou D3D11_BIND_CONSTANT_BUFFER.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-191">Buffers must have exactly one of D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER, or D3D11_BIND_CONSTANT_BUFFER.</span></span><br/> <span data-ttu-id="9a6aa-192">Autorise uniquement les mémoires tampons d’index avec le format DXGI_FORMAT_R16_UINT.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-192">Only allows index buffers with the DXGI_FORMAT_R16_UINT format.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a6aa-193">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-193">D3D_FEATURE_LEVEL_9_2</span></span></td>
<td rowspan="2"> <span data-ttu-id="9a6aa-194">Les mémoires tampons ne peuvent pas avoir de vues de cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-194">Buffers can't have render target views.</span></span><br/> <span data-ttu-id="9a6aa-195">Les mémoires tampons doivent avoir une seule des D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER ou D3D11_BIND_CONSTANT_BUFFER.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-195">Buffers must have exactly one of D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER, or D3D11_BIND_CONSTANT_BUFFER.</span></span><br/> <span data-ttu-id="9a6aa-196">Permet aux mémoires tampons d’index avec les formats DXGI_FORMAT_R16_UINT et DXGI_FORMAT_R32_UINT comme D3D_FEATURE_LEVEL_10_0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-196">Allows index buffers with the DXGI_FORMAT_R16_UINT and DXGI_FORMAT_R32_UINT formats like D3D_FEATURE_LEVEL_10_0 and higher.</span></span> <br/> <span data-ttu-id="9a6aa-197">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="9a6aa-197">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a6aa-198">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-198">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatecounter"></a><span data-ttu-id="9a6aa-199">ID3D11Device :: CreateCounter</span><span class="sxs-lookup"><span data-stu-id="9a6aa-199">ID3D11Device::CreateCounter</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9a6aa-200">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-200">Feature Level</span></span></th>
<th><span data-ttu-id="9a6aa-201">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="9a6aa-201">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a6aa-202">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-202">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="9a6aa-203">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="9a6aa-203">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a6aa-204">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-204">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="9a6aa-205">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-205">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatedepthstencilview"></a><span data-ttu-id="9a6aa-206">ID3D11Device :: CreateDepthStencilView</span><span class="sxs-lookup"><span data-stu-id="9a6aa-206">ID3D11Device::CreateDepthStencilView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9a6aa-207">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-207">Feature Level</span></span></th>
<th><span data-ttu-id="9a6aa-208">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="9a6aa-208">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a6aa-209">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-209">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="9a6aa-210">Ne prend pas en charge le stencil à deux côtés. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="9a6aa-210">Does not support two-sided stencil.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a6aa-211">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-211">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="9a6aa-212">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-212">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatedomainshader"></a><span data-ttu-id="9a6aa-213">ID3D11Device :: CreateDomainShader</span><span class="sxs-lookup"><span data-stu-id="9a6aa-213">ID3D11Device::CreateDomainShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9a6aa-214">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-214">Feature Level</span></span></th>
<th><span data-ttu-id="9a6aa-215">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="9a6aa-215">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a6aa-216">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-216">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="9a6aa-217">Non pris en charge sur les fonctionnalités 9. \* ou 10. \*.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-217">Not supported on any 9.\* or 10.\* feature level.</span></span> <span data-ttu-id="9a6aa-218">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="9a6aa-218">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a6aa-219">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-219">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="9a6aa-220">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-220">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="9a6aa-221">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="9a6aa-221">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="9a6aa-222">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-222">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreategeometryshader"></a><span data-ttu-id="9a6aa-223">ID3D11Device :: CreateGeometryShader</span><span class="sxs-lookup"><span data-stu-id="9a6aa-223">ID3D11Device::CreateGeometryShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9a6aa-224">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-224">Feature Level</span></span></th>
<th><span data-ttu-id="9a6aa-225">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="9a6aa-225">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a6aa-226">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-226">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="9a6aa-227">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="9a6aa-227">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a6aa-228">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-228">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="9a6aa-229">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-229">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreategeometryshaderwithstreamoutput"></a><span data-ttu-id="9a6aa-230">ID3D11Device :: CreateGeometryShaderWithStreamOutput</span><span class="sxs-lookup"><span data-stu-id="9a6aa-230">ID3D11Device::CreateGeometryShaderWithStreamOutput</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9a6aa-231">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-231">Feature Level</span></span></th>
<th><span data-ttu-id="9a6aa-232">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="9a6aa-232">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a6aa-233">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-233">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="9a6aa-234">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="9a6aa-234">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a6aa-235">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-235">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="9a6aa-236">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-236">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatehullshader"></a><span data-ttu-id="9a6aa-237">ID3D11Device :: CreateHullShader</span><span class="sxs-lookup"><span data-stu-id="9a6aa-237">ID3D11Device::CreateHullShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9a6aa-238">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-238">Feature Level</span></span></th>
<th><span data-ttu-id="9a6aa-239">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="9a6aa-239">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a6aa-240">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-240">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="9a6aa-241">Non pris en charge sur les 9. \* ou 10. \* niveau de fonctionnalité. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="9a6aa-241">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a6aa-242">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-242">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="9a6aa-243">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-243">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="9a6aa-244">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="9a6aa-244">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="9a6aa-245">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-245">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateinputlayout"></a><span data-ttu-id="9a6aa-246">ID3D11Device :: CreateInputLayout</span><span class="sxs-lookup"><span data-stu-id="9a6aa-246">ID3D11Device::CreateInputLayout</span></span>



| <span data-ttu-id="9a6aa-247">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-247">Feature Level</span></span>             | <span data-ttu-id="9a6aa-248">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="9a6aa-248">Behavior Differences</span></span>                                                                                              |
|---------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a6aa-249">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-249">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="9a6aa-250">Ne prend pas en charge les \_ données d’entrée d3d11 \_ par \_ instance \_</span><span class="sxs-lookup"><span data-stu-id="9a6aa-250">Does not support D3D11\_INPUT\_PER\_INSTANCE\_DATA</span></span>                                                                |
| <span data-ttu-id="9a6aa-251">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-251">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="9a6aa-252">Ne prend pas en charge les \_ données d’entrée d3d11 \_ par \_ instance \_</span><span class="sxs-lookup"><span data-stu-id="9a6aa-252">Does not support D3D11\_INPUT\_PER\_INSTANCE\_DATA</span></span>                                                                |
| <span data-ttu-id="9a6aa-253">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-253">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="9a6aa-254">Le flux de vertex zéro doit \_ avoir \_ une entrée d3d11 par \_ \_ données de vertex, si des flux ont une \_ entrée d3d11 \_ par \_ vertex \_</span><span class="sxs-lookup"><span data-stu-id="9a6aa-254">Vertex stream zero must have D3D11\_INPUT\_PER\_VERTEX\_DATA, if any streams have D3D11\_INPUT\_PER\_VERTEX\_DATA</span></span> |



 

<span data-ttu-id="9a6aa-255">Pour plus d’informations sur les formats pouvant être utilisés pour les données de vertex à chaque niveau de fonctionnalité, consultez la page formater la prise en charge par le [graphique au](overviews-direct3d-11-devices-downlevel-intro.md) niveau des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-255">See the format support by [feature level chart](overviews-direct3d-11-devices-downlevel-intro.md) for details on what formats can be used for vertex data at each feature level.</span></span>

## <a name="id3d11devicecreatepixelshader"></a><span data-ttu-id="9a6aa-256">ID3D11Device :: CreatePixelShader</span><span class="sxs-lookup"><span data-stu-id="9a6aa-256">ID3D11Device::CreatePixelShader</span></span>



| <span data-ttu-id="9a6aa-257">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-257">Feature Level</span></span>             | <span data-ttu-id="9a6aa-258">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="9a6aa-258">Behavior Differences</span></span>                                    |
|---------------------------|---------------------------------------------------------|
| <span data-ttu-id="9a6aa-259">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-259">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="9a6aa-260">Doit utiliser PS \_ 4 \_ 0 \_ niveau \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-260">Must use ps\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="9a6aa-261">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-261">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="9a6aa-262">Doit utiliser PS \_ 4 \_ 0 \_ niveau \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-262">Must use ps\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="9a6aa-263">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-263">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="9a6aa-264">Doit utiliser PS \_ 4 \_ 0 \_ niveau \_ 9 \_ 3 ou PS \_ 4 \_ 0 \_ niveau \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-264">Must use ps\_4\_0\_level\_9\_3 or ps\_4\_0\_level\_9\_1</span></span> |



 

## <a name="id3d11devicecreatepredicate"></a><span data-ttu-id="9a6aa-265">ID3D11Device :: CreatePredicate</span><span class="sxs-lookup"><span data-stu-id="9a6aa-265">ID3D11Device::CreatePredicate</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9a6aa-266">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-266">Feature Level</span></span></th>
<th><span data-ttu-id="9a6aa-267">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="9a6aa-267">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a6aa-268">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-268">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="9a6aa-269">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="9a6aa-269">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a6aa-270">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-270">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="9a6aa-271">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-271">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatequery"></a><span data-ttu-id="9a6aa-272">ID3D11Device :: CreateQuery</span><span class="sxs-lookup"><span data-stu-id="9a6aa-272">ID3D11Device::CreateQuery</span></span>



| <span data-ttu-id="9a6aa-273">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-273">Feature Level</span></span>             | <span data-ttu-id="9a6aa-274">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="9a6aa-274">Behavior Differences</span></span>                                                                                                                                  |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a6aa-275">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-275">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="9a6aa-276">Les requêtes d’événements sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-276">Event queries are supported.</span></span> <span data-ttu-id="9a6aa-277">Les requêtes d’horodatage sont facultatives : appelez [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) pour déterminer la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-277">Timestamp queries are optional: call [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) to determine support.</span></span>               |
| <span data-ttu-id="9a6aa-278">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-278">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="9a6aa-279">Les requêtes d’événement et d’occlusion sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-279">Event and occlusion queries are supported.</span></span> <span data-ttu-id="9a6aa-280">Les requêtes d’horodatage sont facultatives : appelez [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) pour déterminer la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-280">Timestamp queries are optional: call [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) to determine support.</span></span> |
| <span data-ttu-id="9a6aa-281">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-281">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="9a6aa-282">Les requêtes d’événement et d’occlusion sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-282">Event and occlusion queries are supported.</span></span> <span data-ttu-id="9a6aa-283">Les requêtes d’horodatage sont facultatives : appelez [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) pour déterminer la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-283">Timestamp queries are optional: call [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) to determine support.</span></span> |



 

## <a name="id3d11devicecreaterasterizerstate"></a><span data-ttu-id="9a6aa-284">ID3D11Device :: CreateRasterizerState</span><span class="sxs-lookup"><span data-stu-id="9a6aa-284">ID3D11Device::CreateRasterizerState</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9a6aa-285">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-285">Feature Level</span></span></th>
<th><span data-ttu-id="9a6aa-286">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="9a6aa-286">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a6aa-287">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-287">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="9a6aa-288">DepthClipEnable doit avoir la <strong>valeur true</strong>.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-288">DepthClipEnable must be <strong>TRUE</strong>.</span></span> <span data-ttu-id="9a6aa-289">DepthBiasClamp doit avoir la valeur 0. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="9a6aa-289">DepthBiasClamp must be set to 0.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a6aa-290">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-290">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="9a6aa-291">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-291">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreaterendertargetview"></a><span data-ttu-id="9a6aa-292">ID3D11Device :: CreateRenderTargetView</span><span class="sxs-lookup"><span data-stu-id="9a6aa-292">ID3D11Device::CreateRenderTargetView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9a6aa-293">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-293">Feature Level</span></span></th>
<th><span data-ttu-id="9a6aa-294">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="9a6aa-294">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a6aa-295">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-295">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="9a6aa-296">Peut uniquement prendre en charge les affichages de cible de rendu des objets Texture2D. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="9a6aa-296">Can only support render target views of Texture2D objects.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a6aa-297">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-297">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="9a6aa-298">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-298">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatesamplerstate"></a><span data-ttu-id="9a6aa-299">ID3D11Device :: CreateSamplerState</span><span class="sxs-lookup"><span data-stu-id="9a6aa-299">ID3D11Device::CreateSamplerState</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9a6aa-300">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-300">Feature Level</span></span></th>
<th><span data-ttu-id="9a6aa-301">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="9a6aa-301">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a6aa-302">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-302">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td><span data-ttu-id="9a6aa-303">Le filtre de comparaison n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-303">Comparison filter is not supported.</span></span><br/> <span data-ttu-id="9a6aa-304">La couleur de la bordure doit être comprise entre [0, 1]</span><span class="sxs-lookup"><span data-stu-id="9a6aa-304">Border color must be within [0,1]</span></span><br/> <span data-ttu-id="9a6aa-305">Le LOD minimal ne peut pas être fractionnaire</span><span class="sxs-lookup"><span data-stu-id="9a6aa-305">Min LOD cannot be fractional</span></span><br/> <span data-ttu-id="9a6aa-306">Le LOD maximal doit être FLT_MAX</span><span class="sxs-lookup"><span data-stu-id="9a6aa-306">Max LOD must be FLT_MAX</span></span><br/> <span data-ttu-id="9a6aa-307">L’anisotropie maximale est 2.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-307">Maximum anisotropy is 2.</span></span><br/> <span data-ttu-id="9a6aa-308">D3D11_TEXTURE_ADDRESS_MIRRORONCE pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-308">D3D11_TEXTURE_ADDRESS_MIRRORONCE not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a6aa-309">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-309">D3D_FEATURE_LEVEL_9_2</span></span></td>
<td rowspan="2"> <span data-ttu-id="9a6aa-310">Le filtre de comparaison n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-310">Comparison filter is not supported.</span></span><br/> <span data-ttu-id="9a6aa-311">La couleur de la bordure doit être comprise entre [0, 1]</span><span class="sxs-lookup"><span data-stu-id="9a6aa-311">Border color must be within [0,1]</span></span><br/> <span data-ttu-id="9a6aa-312">Le LOD minimal ne peut pas être fractionnaire</span><span class="sxs-lookup"><span data-stu-id="9a6aa-312">Min LOD cannot be fractional</span></span><br/> <span data-ttu-id="9a6aa-313">Le LOD maximal doit être FLT_MAX</span><span class="sxs-lookup"><span data-stu-id="9a6aa-313">Max LOD must be FLT_MAX</span></span><br/> <span data-ttu-id="9a6aa-314">L’anisotropie maximale est 16.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-314">Maximum anisotropy is 16.</span></span><br/> <span data-ttu-id="9a6aa-315">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="9a6aa-315">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a6aa-316">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-316">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateshaderresourceview"></a><span data-ttu-id="9a6aa-317">ID3D11Device :: CreateShaderResourceView</span><span class="sxs-lookup"><span data-stu-id="9a6aa-317">ID3D11Device::CreateShaderResourceView</span></span>



| <span data-ttu-id="9a6aa-318">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-318">Feature Level</span></span>             | <span data-ttu-id="9a6aa-319">MostDetailedMip plus Miplevels a doit inclure LOD (plus petite sous-ressource</span><span class="sxs-lookup"><span data-stu-id="9a6aa-319">MostDetailedMip plus MipLevels must include lowest LOD (smallest subresource</span></span> | <span data-ttu-id="9a6aa-320">La vue doit inclure tous les éléments du tableau de ressources</span><span class="sxs-lookup"><span data-stu-id="9a6aa-320">View must include all resource array elements</span></span> |
|---------------------------|------------------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="9a6aa-321">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-321">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="9a6aa-322">Oui</span><span class="sxs-lookup"><span data-stu-id="9a6aa-322">Yes</span></span>                                                                          | <span data-ttu-id="9a6aa-323">Oui</span><span class="sxs-lookup"><span data-stu-id="9a6aa-323">yes</span></span>                                           |
| <span data-ttu-id="9a6aa-324">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-324">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="9a6aa-325">Oui</span><span class="sxs-lookup"><span data-stu-id="9a6aa-325">Yes</span></span>                                                                          | <span data-ttu-id="9a6aa-326">Oui</span><span class="sxs-lookup"><span data-stu-id="9a6aa-326">Yes</span></span>                                           |
| <span data-ttu-id="9a6aa-327">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-327">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="9a6aa-328">Oui</span><span class="sxs-lookup"><span data-stu-id="9a6aa-328">Yes</span></span>                                                                          | <span data-ttu-id="9a6aa-329">Oui</span><span class="sxs-lookup"><span data-stu-id="9a6aa-329">Yes</span></span>                                           |



 

## <a name="id3d11devicecreatetexture1d"></a><span data-ttu-id="9a6aa-330">ID3D11Device :: CreateTexture1D</span><span class="sxs-lookup"><span data-stu-id="9a6aa-330">ID3D11Device::CreateTexture1D</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9a6aa-331">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-331">Feature Level</span></span></th>
<th><span data-ttu-id="9a6aa-332">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="9a6aa-332">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a6aa-333">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-333">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="9a6aa-334">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="9a6aa-334">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a6aa-335">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-335">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="9a6aa-336">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-336">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatetexture2d"></a><span data-ttu-id="9a6aa-337">ID3D11Device :: CreateTexture2D</span><span class="sxs-lookup"><span data-stu-id="9a6aa-337">ID3D11Device::CreateTexture2D</span></span>

<span data-ttu-id="9a6aa-338">Les ressources Texture2D ont des limites de largeur et de hauteur qui diffèrent selon les [niveaux de fonctionnalité](overviews-direct3d-11-devices-downlevel-intro.md).</span><span class="sxs-lookup"><span data-stu-id="9a6aa-338">Texture2D resources have limits on their width and height that differ across [feature levels](overviews-direct3d-11-devices-downlevel-intro.md).</span></span> <span data-ttu-id="9a6aa-339">Dans les niveaux de fonctionnalité 9 \_ 3, les éléments suivants sont des minima garantis et les implémentations individuelles peuvent dépasser les exigences.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-339">In feature levels 9\_3, the following are guaranteed minima, and individual implementations may exceed the requirements.</span></span>



| <span data-ttu-id="9a6aa-340">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-340">Feature Level</span></span>             | <span data-ttu-id="9a6aa-341">Si MipCount > 1, les dimensions doivent être une puissance intégrale de deux</span><span class="sxs-lookup"><span data-stu-id="9a6aa-341">If MipCount > 1, Dimensions must be integral power of two</span></span> | <span data-ttu-id="9a6aa-342">Dimension de texture minimale prise en charge</span><span class="sxs-lookup"><span data-stu-id="9a6aa-342">Minimum supported texture dimension</span></span> | <span data-ttu-id="9a6aa-343">Les dimensions des textures de cube doivent être une puissance de deux</span><span class="sxs-lookup"><span data-stu-id="9a6aa-343">Cube textures dimensions must be power of two</span></span> | <span data-ttu-id="9a6aa-344">Si MISC \_ TEXTURECUBE est défini, arraySize est :</span><span class="sxs-lookup"><span data-stu-id="9a6aa-344">If MISC\_TEXTURECUBE is set, the ArraySize is:</span></span> | <span data-ttu-id="9a6aa-345">Si MISC \_ TEXTURECUBE n’est pas défini, arraySize a la valeur.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-345">If MISC\_TEXTURECUBE is not set, the ArraySize is.</span></span> |
|---------------------------|--------------------------------------------------------------|-------------------------------------|-----------------------------------------------|------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="9a6aa-346">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-346">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="9a6aa-347">Oui</span><span class="sxs-lookup"><span data-stu-id="9a6aa-347">Yes</span></span>                                                          | <span data-ttu-id="9a6aa-348">2 048</span><span class="sxs-lookup"><span data-stu-id="9a6aa-348">2048</span></span>                                | <span data-ttu-id="9a6aa-349">Oui</span><span class="sxs-lookup"><span data-stu-id="9a6aa-349">Yes</span></span>                                           | <span data-ttu-id="9a6aa-350">6</span><span class="sxs-lookup"><span data-stu-id="9a6aa-350">6</span></span>                                              | <span data-ttu-id="9a6aa-351">1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-351">1</span></span>                                                  |
| <span data-ttu-id="9a6aa-352">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-352">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="9a6aa-353">Oui</span><span class="sxs-lookup"><span data-stu-id="9a6aa-353">Yes</span></span>                                                          | <span data-ttu-id="9a6aa-354">2 048</span><span class="sxs-lookup"><span data-stu-id="9a6aa-354">2048</span></span>                                | <span data-ttu-id="9a6aa-355">Oui</span><span class="sxs-lookup"><span data-stu-id="9a6aa-355">Yes</span></span>                                           | <span data-ttu-id="9a6aa-356">6</span><span class="sxs-lookup"><span data-stu-id="9a6aa-356">6</span></span>                                              | <span data-ttu-id="9a6aa-357">1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-357">1</span></span>                                                  |
| <span data-ttu-id="9a6aa-358">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-358">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="9a6aa-359">Oui</span><span class="sxs-lookup"><span data-stu-id="9a6aa-359">Yes</span></span>                                                          | <span data-ttu-id="9a6aa-360">4096</span><span class="sxs-lookup"><span data-stu-id="9a6aa-360">4096</span></span>                                | <span data-ttu-id="9a6aa-361">Oui</span><span class="sxs-lookup"><span data-stu-id="9a6aa-361">Yes</span></span>                                           | <span data-ttu-id="9a6aa-362">6</span><span class="sxs-lookup"><span data-stu-id="9a6aa-362">6</span></span>                                              | <span data-ttu-id="9a6aa-363">1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-363">1</span></span>                                                  |



 

<span data-ttu-id="9a6aa-364">Dans le tableau précédent, le nom complet de **\_ TEXTURECUBE divers** est [**d3d11 \_ Resource \_ misc \_ TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag).</span><span class="sxs-lookup"><span data-stu-id="9a6aa-364">In the previous table, the full name of **MISC\_TEXTURECUBE** is [**D3D11\_RESOURCE\_MISC\_TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag).</span></span>

<span data-ttu-id="9a6aa-365">Les éléments suivants sont vrais pour les 9 \_ \* [niveaux de fonctionnalité](overviews-direct3d-11-devices-downlevel-intro.md):</span><span class="sxs-lookup"><span data-stu-id="9a6aa-365">The following are true for all 9\_\* [feature levels](overviews-direct3d-11-devices-downlevel-intro.md):</span></span>

-   <span data-ttu-id="9a6aa-366">Lors de l’utilisation de D3D11 \_ \_ par défaut ou de l’utilisation de d3d11 \_ \_ immuable, BindFlags ne peut pas être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-366">When using D3D11\_USAGE\_DEFAULT or D3D11\_USAGE\_IMMUTABLE, BindFlags cannot be zero.</span></span>
-   <span data-ttu-id="9a6aa-367">Lors de l’utilisation du \_ \_ \_ stencil de profondeur de liaison d3d11, miplevels a doit être 1.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-367">When using D3D11\_BIND\_DEPTH\_STENCIL, MipLevels must be 1.</span></span>
-   <span data-ttu-id="9a6aa-368">Lors de l' \_ utilisation \_ de la ressource de nuanceur de liaison d3d11 \_ , SampleDesc. Count doit avoir la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-368">When using D3D11\_BIND\_SHADER\_RESOURCE, SampleDesc.Count must be 1.</span></span>
-   <span data-ttu-id="9a6aa-369">Lors de l’utilisation d’une \_ liaison d3d11 \_ présente, la ressource ne peut pas avoir de \_ ressource de nuanceur de liaison d3d11 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9a6aa-369">When using D3D11\_BIND\_PRESENT, resource cannot have D3D11\_BIND\_SHADER\_RESOURCE.</span></span>
-   <span data-ttu-id="9a6aa-370">Lors de l’utilisation \_ de la ressource D3D10 DDI \_ \_ misc \_ Shared, le format ne peut pas être dxgi \_ format \_ R8G8B8A8 \_ UNORM ou dxgi \_ format R8G8B8A8 \_ \_ UNORM \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-370">When using D3D10\_DDI\_RESOURCE\_MISC\_SHARED, Format cannot be DXGI\_FORMAT\_R8G8B8A8\_UNORM or DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB.</span></span>

## <a name="id3d11devicecreatetexture3d"></a><span data-ttu-id="9a6aa-371">ID3D11Device :: CreateTexture3D</span><span class="sxs-lookup"><span data-stu-id="9a6aa-371">ID3D11Device::CreateTexture3D</span></span>



| <span data-ttu-id="9a6aa-372">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-372">Feature Level</span></span>             | <span data-ttu-id="9a6aa-373">Dimension maximum (tout axe)</span><span class="sxs-lookup"><span data-stu-id="9a6aa-373">Maximum Dimension (any axis)</span></span> | <span data-ttu-id="9a6aa-374">Les dimensions doivent être une puissance de deux</span><span class="sxs-lookup"><span data-stu-id="9a6aa-374">Dimensions must be power of two</span></span> |
|---------------------------|------------------------------|---------------------------------|
| <span data-ttu-id="9a6aa-375">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-375">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="9a6aa-376">256</span><span class="sxs-lookup"><span data-stu-id="9a6aa-376">256</span></span>                          | <span data-ttu-id="9a6aa-377">Oui</span><span class="sxs-lookup"><span data-stu-id="9a6aa-377">Yes</span></span>                             |
| <span data-ttu-id="9a6aa-378">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-378">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="9a6aa-379">512</span><span class="sxs-lookup"><span data-stu-id="9a6aa-379">512</span></span>                          | <span data-ttu-id="9a6aa-380">Oui</span><span class="sxs-lookup"><span data-stu-id="9a6aa-380">Yes</span></span>                             |
| <span data-ttu-id="9a6aa-381">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-381">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="9a6aa-382">512</span><span class="sxs-lookup"><span data-stu-id="9a6aa-382">512</span></span>                          | <span data-ttu-id="9a6aa-383">Oui</span><span class="sxs-lookup"><span data-stu-id="9a6aa-383">Yes</span></span>                             |



 

<span data-ttu-id="9a6aa-384">Si la ressource est une \_ utilisation d3d11 \_ par défaut ou \_ une utilisation d3d11 \_ immuable, BindFlags ne peut pas être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-384">If resource is D3D11\_USAGE\_DEFAULT or D3D11\_USAGE\_IMMUTABLE, BindFlags cannot be zero.</span></span>

## <a name="id3d11devicecreateunorderedaccessview"></a><span data-ttu-id="9a6aa-385">ID3D11Device :: CreateUnorderedAccessView</span><span class="sxs-lookup"><span data-stu-id="9a6aa-385">ID3D11Device::CreateUnorderedAccessView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9a6aa-386">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-386">Feature Level</span></span></th>
<th><span data-ttu-id="9a6aa-387">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="9a6aa-387">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a6aa-388">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-388">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="9a6aa-389">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="9a6aa-389">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a6aa-390">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-390">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="9a6aa-391">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-391">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatevertexshader"></a><span data-ttu-id="9a6aa-392">ID3D11Device :: CreateVertexShader</span><span class="sxs-lookup"><span data-stu-id="9a6aa-392">ID3D11Device::CreateVertexShader</span></span>



| <span data-ttu-id="9a6aa-393">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-393">Feature Level</span></span>             | <span data-ttu-id="9a6aa-394">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="9a6aa-394">Behavior Differences</span></span>                                    |
|---------------------------|---------------------------------------------------------|
| <span data-ttu-id="9a6aa-395">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-395">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="9a6aa-396">Doit utiliser vs \_ 4 \_ 0 \_ niveau \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-396">Must use vs\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="9a6aa-397">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-397">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="9a6aa-398">Doit utiliser vs \_ 4 \_ 0 \_ niveau \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-398">Must use vs\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="9a6aa-399">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-399">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="9a6aa-400">Doit utiliser vs \_ 4 \_ 0 \_ niveau \_ 9 \_ 3 ou vs \_ 4 \_ 0 \_ niveau \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-400">Must use vs\_4\_0\_level\_9\_3 or vs\_4\_0\_level\_9\_1</span></span> |



 

## <a name="id3d11deviceopensharedresource"></a><span data-ttu-id="9a6aa-401">ID3D11Device :: OpenSharedResource</span><span class="sxs-lookup"><span data-stu-id="9a6aa-401">ID3D11Device::OpenSharedResource</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9a6aa-402">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9a6aa-402">Feature Level</span></span></th>
<th><span data-ttu-id="9a6aa-403">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="9a6aa-403">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a6aa-404">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="9a6aa-404">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"> <span data-ttu-id="9a6aa-405">Utilisez <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device :: CheckFeatureSupport</strong></a> avec la valeur <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE_FORMAT_SUPPORT2</strong></a> et la structure <a href="/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a> pour déterminer si un format peut être partagé.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-405">Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device::CheckFeatureSupport</strong></a> with the <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE_FORMAT_SUPPORT2</strong></a> value and the <a href="/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a> structure to determine if a format can be shared.</span></span> <span data-ttu-id="9a6aa-406">Si le format peut être partagé, <strong>CheckFeatureSupport</strong> retourne l’indicateur <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2_SHAREABLE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9a6aa-406">If the format can be shared, <strong>CheckFeatureSupport</strong> returns the <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2_SHAREABLE</strong></a> flag.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9a6aa-407">[<strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong>] (/Windows/Desktop/API/dxgiformat/ne-dxgiformat-dxgi_format) et <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> ne peuvent jamais être partagés lors de l’utilisation du niveau de fonctionnalité 9, même si l’appareil indique une prise en charge facultative des fonctionnalités pour <strong>D3D11_FORMAT_SUPPORT_SHAREABLE</strong>.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-407">[<strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) and <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> are never shareable when using feature level 9, even if the device indicates optional feature support for <strong>D3D11_FORMAT_SUPPORT_SHAREABLE</strong>.</span></span> <span data-ttu-id="9a6aa-408">La tentative de création de ressources partagées avec des formats DXGI <strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong> et <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> échouera toujours, à moins que le niveau de fonctionnalité soit 10_0 ou supérieur.</span><span class="sxs-lookup"><span data-stu-id="9a6aa-408">Attempting to create shared resources with DXGI formats <strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong> and <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> will always fail unless the feature level is 10_0 or higher.</span></span>
</blockquote>
<br/> <span data-ttu-id="9a6aa-409">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="9a6aa-409">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a6aa-410">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="9a6aa-410">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="9a6aa-411">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="9a6aa-411">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="9a6aa-412">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9a6aa-412">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a6aa-413">Référence 10Level9</span><span class="sxs-lookup"><span data-stu-id="9a6aa-413">10Level9 Reference</span></span>](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

