---
title: Méthodes 10Level9 ID3D11DeviceContext
description: Cette section répertorie les différences entre chaque niveau de fonctionnalité 10Level9 et le niveau de fonctionnalité D3D \_ \_ \_ 11 \_ 0 et supérieur pour les méthodes ID3D11DeviceContext.
ms.assetid: 84478b56-0306-491a-9545-0849b06d8342
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb3dc46aeeb5d629c4bf50492083d09b34de1b08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028746"
---
# <a name="10level9-id3d11devicecontext-methods"></a><span data-ttu-id="77349-103">Méthodes 10Level9 ID3D11DeviceContext</span><span class="sxs-lookup"><span data-stu-id="77349-103">10Level9 ID3D11DeviceContext Methods</span></span>

<span data-ttu-id="77349-104">Cette section répertorie les différences entre chaque niveau de fonctionnalité 10Level9 et le niveau de fonctionnalité D3D \_ \_ \_ 11 \_ 0 et supérieur pour les méthodes [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="77349-104">This section lists the differences between each 10Level9 feature level and the D3D\_FEATURE\_LEVEL\_11\_0 and higher feature level for the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods.</span></span>

-   [<span data-ttu-id="77349-105">ID3D11DeviceContext :: CopySubresourceRegion</span><span class="sxs-lookup"><span data-stu-id="77349-105">ID3D11DeviceContext::CopySubresourceRegion</span></span>](#id3d11devicecontextcopysubresourceregion)
-   [<span data-ttu-id="77349-106">ID3D11DeviceContext :: CopyResource</span><span class="sxs-lookup"><span data-stu-id="77349-106">ID3D11DeviceContext::CopyResource</span></span>](#id3d11devicecontextcopyresource)
-   [<span data-ttu-id="77349-107">ID3D11DeviceContext :: CopyStructureCount</span><span class="sxs-lookup"><span data-stu-id="77349-107">ID3D11DeviceContext::CopyStructureCount</span></span>](#id3d11devicecontextcopystructurecount)
-   [<span data-ttu-id="77349-108">ID3D11DeviceContext :: ClearUnorderedAccessViewFloat</span><span class="sxs-lookup"><span data-stu-id="77349-108">ID3D11DeviceContext::ClearUnorderedAccessViewFloat</span></span>](#id3d11devicecontextclearunorderedaccessviewfloat)
-   [<span data-ttu-id="77349-109">ID3D11DeviceContext :: ClearUnorderedAccessViewUint</span><span class="sxs-lookup"><span data-stu-id="77349-109">ID3D11DeviceContext::ClearUnorderedAccessViewUint</span></span>](#id3d11devicecontextclearunorderedaccessviewuint)
-   [<span data-ttu-id="77349-110">ID3D11DeviceContext :: ClearRenderTargetView</span><span class="sxs-lookup"><span data-stu-id="77349-110">ID3D11DeviceContext::ClearRenderTargetView</span></span>](#id3d11devicecontextclearrendertargetview)
-   [<span data-ttu-id="77349-111">ID3D11DeviceContext :: CSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="77349-111">ID3D11DeviceContext::CSSetConstantBuffers</span></span>](#id3d11devicecontextcssetconstantbuffers)
-   [<span data-ttu-id="77349-112">ID3D11DeviceContext :: CSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="77349-112">ID3D11DeviceContext::CSSetSamplers</span></span>](#id3d11devicecontextcssetsamplers)
-   [<span data-ttu-id="77349-113">ID3D11DeviceContext :: CSSetShader</span><span class="sxs-lookup"><span data-stu-id="77349-113">ID3D11DeviceContext::CSSetShader</span></span>](#id3d11devicecontextcssetshader)
-   [<span data-ttu-id="77349-114">ID3D11DeviceContext :: CSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="77349-114">ID3D11DeviceContext::CSSetShaderResources</span></span>](#id3d11devicecontextcssetshaderresources)
-   [<span data-ttu-id="77349-115">ID3D11DeviceContext :: CSSetUnorderedAccessViews</span><span class="sxs-lookup"><span data-stu-id="77349-115">ID3D11DeviceContext::CSSetUnorderedAccessViews</span></span>](#id3d11devicecontextcssetunorderedaccessviews)
-   [<span data-ttu-id="77349-116">ID3D11DeviceContext ::D ispatch</span><span class="sxs-lookup"><span data-stu-id="77349-116">ID3D11DeviceContext::Dispatch</span></span>](#id3d11devicecontextdispatch)
-   [<span data-ttu-id="77349-117">ID3D11DeviceContext ::D ispatchIndirect</span><span class="sxs-lookup"><span data-stu-id="77349-117">ID3D11DeviceContext::DispatchIndirect</span></span>](#id3d11devicecontextdispatchindirect)
-   [<span data-ttu-id="77349-118">ID3D11DeviceContext ::D RAW</span><span class="sxs-lookup"><span data-stu-id="77349-118">ID3D11DeviceContext::Draw</span></span>](#id3d11devicecontextdraw)
-   [<span data-ttu-id="77349-119">ID3D11DeviceContext ::D rawAuto</span><span class="sxs-lookup"><span data-stu-id="77349-119">ID3D11DeviceContext::DrawAuto</span></span>](#id3d11devicecontextdrawauto)
-   [<span data-ttu-id="77349-120">ID3D11DeviceContext ::D rawIndexed</span><span class="sxs-lookup"><span data-stu-id="77349-120">ID3D11DeviceContext::DrawIndexed</span></span>](#id3d11devicecontextdrawindexed)
-   [<span data-ttu-id="77349-121">ID3D11DeviceContext ::D rawIndexedInstanced</span><span class="sxs-lookup"><span data-stu-id="77349-121">ID3D11DeviceContext::DrawIndexedInstanced</span></span>](#id3d11devicecontextdrawindexedinstanced)
-   [<span data-ttu-id="77349-122">ID3D11DeviceContext ::D rawIndexedInstancedIndirect</span><span class="sxs-lookup"><span data-stu-id="77349-122">ID3D11DeviceContext::DrawIndexedInstancedIndirect</span></span>](#id3d11devicecontextdrawindexedinstancedindirect)
-   [<span data-ttu-id="77349-123">ID3D11DeviceContext ::D rawInstanced</span><span class="sxs-lookup"><span data-stu-id="77349-123">ID3D11DeviceContext::DrawInstanced</span></span>](#id3d11devicecontextdrawinstanced)
-   [<span data-ttu-id="77349-124">ID3D11DeviceContext ::D rawInstancedIndirect</span><span class="sxs-lookup"><span data-stu-id="77349-124">ID3D11DeviceContext::DrawInstancedIndirect</span></span>](#id3d11devicecontextdrawinstancedindirect)
-   [<span data-ttu-id="77349-125">ID3D11DeviceContext ::D SSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="77349-125">ID3D11DeviceContext::DSSetConstantBuffers</span></span>](#id3d11devicecontextdssetconstantbuffers)
-   [<span data-ttu-id="77349-126">ID3D11DeviceContext ::D SSetSamplers</span><span class="sxs-lookup"><span data-stu-id="77349-126">ID3D11DeviceContext::DSSetSamplers</span></span>](#id3d11devicecontextdssetsamplers)
-   [<span data-ttu-id="77349-127">ID3D11DeviceContext ::D SSetShader</span><span class="sxs-lookup"><span data-stu-id="77349-127">ID3D11DeviceContext::DSSetShader</span></span>](#id3d11devicecontextdssetshader)
-   [<span data-ttu-id="77349-128">ID3D11DeviceContext ::D SSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="77349-128">ID3D11DeviceContext::DSSetShaderResources</span></span>](#id3d11devicecontextdssetshaderresources)
-   [<span data-ttu-id="77349-129">ID3D11DeviceContext :: GSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="77349-129">ID3D11DeviceContext::GSSetConstantBuffers</span></span>](#id3d11devicecontextgssetconstantbuffers)
-   [<span data-ttu-id="77349-130">ID3D11DeviceContext :: GSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="77349-130">ID3D11DeviceContext::GSSetSamplers</span></span>](#id3d11devicecontextgssetsamplers)
-   [<span data-ttu-id="77349-131">ID3D11DeviceContext :: GSSetShader</span><span class="sxs-lookup"><span data-stu-id="77349-131">ID3D11DeviceContext::GSSetShader</span></span>](#id3d11devicecontextgssetshader)
-   [<span data-ttu-id="77349-132">ID3D11DeviceContext :: GSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="77349-132">ID3D11DeviceContext::GSSetShaderResources</span></span>](#id3d11devicecontextgssetshaderresources)
-   [<span data-ttu-id="77349-133">ID3D11DeviceContext :: HSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="77349-133">ID3D11DeviceContext::HSSetConstantBuffers</span></span>](#id3d11devicecontexthssetconstantbuffers)
-   [<span data-ttu-id="77349-134">ID3D11DeviceContext :: HSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="77349-134">ID3D11DeviceContext::HSSetSamplers</span></span>](#id3d11devicecontexthssetsamplers)
-   [<span data-ttu-id="77349-135">ID3D11DeviceContext :: HSSetShader</span><span class="sxs-lookup"><span data-stu-id="77349-135">ID3D11DeviceContext::HSSetShader</span></span>](#id3d11devicecontexthssetshader)
-   [<span data-ttu-id="77349-136">ID3D11DeviceContext :: HSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="77349-136">ID3D11DeviceContext::HSSetShaderResources</span></span>](#id3d11devicecontexthssetshaderresources)
-   [<span data-ttu-id="77349-137">ID3D11DeviceContext::IASetIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="77349-137">ID3D11DeviceContext::IASetIndexBuffer</span></span>](#id3d11devicecontextiasetindexbuffer)
-   [<span data-ttu-id="77349-138">ID3D11DeviceContext :: IASetPrimitiveTopology</span><span class="sxs-lookup"><span data-stu-id="77349-138">ID3D11DeviceContext::IASetPrimitiveTopology</span></span>](#id3d11devicecontextiasetprimitivetopology)
-   [<span data-ttu-id="77349-139">ID3D11DeviceContext :: OMSetBlendState</span><span class="sxs-lookup"><span data-stu-id="77349-139">ID3D11DeviceContext::OMSetBlendState</span></span>](#id3d11devicecontextomsetblendstate)
-   [<span data-ttu-id="77349-140">ID3D11DeviceContext :: OMSetRenderTargets</span><span class="sxs-lookup"><span data-stu-id="77349-140">ID3D11DeviceContext::OMSetRenderTargets</span></span>](#id3d11devicecontextomsetrendertargets)
-   [<span data-ttu-id="77349-141">ID3D11DeviceContext :: OMSetRenderTargetsAndUnorderedAccessViews</span><span class="sxs-lookup"><span data-stu-id="77349-141">ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews</span></span>](#id3d11devicecontextomsetrendertargetsandunorderedaccessviews)
-   [<span data-ttu-id="77349-142">ID3D11DeviceContext ::P SSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="77349-142">ID3D11DeviceContext::PSSetConstantBuffers</span></span>](#id3d11devicecontextpssetconstantbuffers)
-   [<span data-ttu-id="77349-143">ID3D11DeviceContext ::P SSetSamplers</span><span class="sxs-lookup"><span data-stu-id="77349-143">ID3D11DeviceContext::PSSetSamplers</span></span>](#id3d11devicecontextpssetsamplers)
-   [<span data-ttu-id="77349-144">ID3D11DeviceContext ::P SSetShader</span><span class="sxs-lookup"><span data-stu-id="77349-144">ID3D11DeviceContext::PSSetShader</span></span>](#id3d11devicecontextpssetshader)
-   [<span data-ttu-id="77349-145">ID3D11DeviceContext ::P SSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="77349-145">ID3D11DeviceContext::PSSetShaderResources</span></span>](#id3d11devicecontextpssetshaderresources)
-   [<span data-ttu-id="77349-146">ID3D11DeviceContext :: RSSetScissorRects</span><span class="sxs-lookup"><span data-stu-id="77349-146">ID3D11DeviceContext::RSSetScissorRects</span></span>](#id3d11devicecontextrssetscissorrects)
-   [<span data-ttu-id="77349-147">ID3D11DeviceContext :: RSSetViewports</span><span class="sxs-lookup"><span data-stu-id="77349-147">ID3D11DeviceContext::RSSetViewports</span></span>](#id3d11devicecontextrssetviewports)
-   [<span data-ttu-id="77349-148">ID3D11DeviceContext :: SetPredication</span><span class="sxs-lookup"><span data-stu-id="77349-148">ID3D11DeviceContext::SetPredication</span></span>](#id3d11devicecontextsetpredication)
-   [<span data-ttu-id="77349-149">ID3D11DeviceContext :: SOSetTargets</span><span class="sxs-lookup"><span data-stu-id="77349-149">ID3D11DeviceContext::SOSetTargets</span></span>](#id3d11devicecontextsosettargets)
-   [<span data-ttu-id="77349-150">ID3D11DeviceContext :: VSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="77349-150">ID3D11DeviceContext::VSSetConstantBuffers</span></span>](#id3d11devicecontextvssetconstantbuffers)
-   [<span data-ttu-id="77349-151">ID3D11DeviceContext :: VSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="77349-151">ID3D11DeviceContext::VSSetSamplers</span></span>](#id3d11devicecontextvssetsamplers)
-   [<span data-ttu-id="77349-152">ID3D11DeviceContext :: VSSetShader</span><span class="sxs-lookup"><span data-stu-id="77349-152">ID3D11DeviceContext::VSSetShader</span></span>](#id3d11devicecontextvssetshader)
-   [<span data-ttu-id="77349-153">ID3D11DeviceContext :: VSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="77349-153">ID3D11DeviceContext::VSSetShaderResources</span></span>](#id3d11devicecontextvssetshaderresources)
-   [<span data-ttu-id="77349-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="77349-154">Related topics</span></span>](#related-topics)

## <a name="id3d11devicecontextcopysubresourceregion"></a><span data-ttu-id="77349-155">ID3D11DeviceContext :: CopySubresourceRegion</span><span class="sxs-lookup"><span data-stu-id="77349-155">ID3D11DeviceContext::CopySubresourceRegion</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-156">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-156">Feature Level</span></span></th>
<th><span data-ttu-id="77349-157">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-157">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-158">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-158">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"> <span data-ttu-id="77349-159">Seuls les Texture2D et les tampons peuvent être copiés dans la mémoire accessible par le GPU.</span><span class="sxs-lookup"><span data-stu-id="77349-159">Only Texture2D and buffers may be copied within GPU-accessible memory.</span></span><br/> <span data-ttu-id="77349-160">Les Texture3D ne peuvent pas être copiés de la mémoire accessible par le GPU vers la mémoire accessible par le processeur.</span><span class="sxs-lookup"><span data-stu-id="77349-160">Texture3D cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="77349-161">Toutes les ressources qui ont uniquement des D3D10_BIND_SHADER_RESOURCE ne peuvent pas être copiées de la mémoire accessible par le GPU vers la mémoire accessible par le processeur.</span><span class="sxs-lookup"><span data-stu-id="77349-161">Any resource that has only D3D10_BIND_SHADER_RESOURCE cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="77349-162">Vous ne pouvez pas copier les textures de volume mipmapped.</span><span class="sxs-lookup"><span data-stu-id="77349-162">You can't copy mipmapped volume textures.</span></span> <br/> <span data-ttu-id="77349-163">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-163">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-164">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-164">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-165">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-165">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopyresource"></a><span data-ttu-id="77349-166">ID3D11DeviceContext :: CopyResource</span><span class="sxs-lookup"><span data-stu-id="77349-166">ID3D11DeviceContext::CopyResource</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-167">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-167">Feature Level</span></span></th>
<th><span data-ttu-id="77349-168">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-168">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-169">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-169">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"> <span data-ttu-id="77349-170">Seuls les Texture2D et les tampons peuvent être copiés dans la mémoire accessible par le GPU.</span><span class="sxs-lookup"><span data-stu-id="77349-170">Only Texture2D and buffers may be copied within GPU-accessible memory.</span></span><br/> <span data-ttu-id="77349-171">Les Texture3D ne peuvent pas être copiés de la mémoire accessible par le GPU vers la mémoire accessible par le processeur.</span><span class="sxs-lookup"><span data-stu-id="77349-171">Texture3D cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="77349-172">Toutes les ressources qui ont uniquement des D3D10_BIND_SHADER_RESOURCE ne peuvent pas être copiées de la mémoire accessible par le GPU vers la mémoire accessible par le processeur.</span><span class="sxs-lookup"><span data-stu-id="77349-172">Any resource that has only D3D10_BIND_SHADER_RESOURCE cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="77349-173">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-173">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-174">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-174">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-175">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-175">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopystructurecount"></a><span data-ttu-id="77349-176">ID3D11DeviceContext :: CopyStructureCount</span><span class="sxs-lookup"><span data-stu-id="77349-176">ID3D11DeviceContext::CopyStructureCount</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-177">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-177">Feature Level</span></span></th>
<th><span data-ttu-id="77349-178">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-178">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-179">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-179">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-180">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-180">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-181">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-181">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-182">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-182">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewfloat"></a><span data-ttu-id="77349-183">ID3D11DeviceContext :: ClearUnorderedAccessViewFloat</span><span class="sxs-lookup"><span data-stu-id="77349-183">ID3D11DeviceContext::ClearUnorderedAccessViewFloat</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-184">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-184">Feature Level</span></span></th>
<th><span data-ttu-id="77349-185">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-185">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-186">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-186">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-187">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-187">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-188">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-188">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-189">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-189">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewuint"></a><span data-ttu-id="77349-190">ID3D11DeviceContext :: ClearUnorderedAccessViewUint</span><span class="sxs-lookup"><span data-stu-id="77349-190">ID3D11DeviceContext::ClearUnorderedAccessViewUint</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-191">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-191">Feature Level</span></span></th>
<th><span data-ttu-id="77349-192">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-192">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-193">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-193">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-194">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-194">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-195">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-195">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-196">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-196">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearrendertargetview"></a><span data-ttu-id="77349-197">ID3D11DeviceContext :: ClearRenderTargetView</span><span class="sxs-lookup"><span data-stu-id="77349-197">ID3D11DeviceContext::ClearRenderTargetView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-198">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-198">Feature Level</span></span></th>
<th><span data-ttu-id="77349-199">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-199">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-200">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-200">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-201">Seule la première tranche du tableau sera effacée.</span><span class="sxs-lookup"><span data-stu-id="77349-201">Only the first array slice will be cleared.</span></span> <span data-ttu-id="77349-202">Les applications doivent créer une vue de la cible de rendu pour chaque face ou tranche de tableau, puis effacer chaque vue individuellement. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-202">Applications should create a render target view for each face or array slice, then clear each view individually.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-203">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-203">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-204">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-204">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetconstantbuffers"></a><span data-ttu-id="77349-205">ID3D11DeviceContext :: CSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="77349-205">ID3D11DeviceContext::CSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-206">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-206">Feature Level</span></span></th>
<th><span data-ttu-id="77349-207">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-207">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-208">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-208">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-209">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-209">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-210">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-210">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-211">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-211">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetsamplers"></a><span data-ttu-id="77349-212">ID3D11DeviceContext :: CSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="77349-212">ID3D11DeviceContext::CSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-213">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-213">Feature Level</span></span></th>
<th><span data-ttu-id="77349-214">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-214">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-215">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-215">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-216">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-216">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-217">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-217">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-218">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-218">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshader"></a><span data-ttu-id="77349-219">ID3D11DeviceContext :: CSSetShader</span><span class="sxs-lookup"><span data-stu-id="77349-219">ID3D11DeviceContext::CSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-220">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-220">Feature Level</span></span></th>
<th><span data-ttu-id="77349-221">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-221">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-222">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-222">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-223">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-223">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-224">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-224">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-225">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-225">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshaderresources"></a><span data-ttu-id="77349-226">ID3D11DeviceContext :: CSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="77349-226">ID3D11DeviceContext::CSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-227">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-227">Feature Level</span></span></th>
<th><span data-ttu-id="77349-228">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-228">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-229">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-229">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-230">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-230">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-231">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-231">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-232">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-232">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetunorderedaccessviews"></a><span data-ttu-id="77349-233">ID3D11DeviceContext :: CSSetUnorderedAccessViews</span><span class="sxs-lookup"><span data-stu-id="77349-233">ID3D11DeviceContext::CSSetUnorderedAccessViews</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-234">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-234">Feature Level</span></span></th>
<th><span data-ttu-id="77349-235">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-235">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-236">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-236">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-237">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-237">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-238">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-238">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-239">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-239">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatch"></a><span data-ttu-id="77349-240">ID3D11DeviceContext ::D ispatch</span><span class="sxs-lookup"><span data-stu-id="77349-240">ID3D11DeviceContext::Dispatch</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-241">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-241">Feature Level</span></span></th>
<th><span data-ttu-id="77349-242">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-242">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-243">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-243">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-244">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-244">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-245">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-245">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-246">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-246">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatchindirect"></a><span data-ttu-id="77349-247">ID3D11DeviceContext ::D ispatchIndirect</span><span class="sxs-lookup"><span data-stu-id="77349-247">ID3D11DeviceContext::DispatchIndirect</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-248">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-248">Feature Level</span></span></th>
<th><span data-ttu-id="77349-249">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-249">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-250">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-250">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-251">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-251">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-252">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-252">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-253">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-253">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdraw"></a><span data-ttu-id="77349-254">ID3D11DeviceContext ::D RAW</span><span class="sxs-lookup"><span data-stu-id="77349-254">ID3D11DeviceContext::Draw</span></span>



| <span data-ttu-id="77349-255">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-255">Feature Level</span></span>             | <span data-ttu-id="77349-256">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-256">Behavior Differences</span></span>                                                                                                               |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77349-257">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="77349-257">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="77349-258">Le nombre de primitives ne peut pas dépasser 65535.</span><span class="sxs-lookup"><span data-stu-id="77349-258">Number of primitives may not exceed 65535.</span></span><br/> <span data-ttu-id="77349-259">Les textures ne peuvent pas se répéter sur une primitive plus de 128 fois.</span><span class="sxs-lookup"><span data-stu-id="77349-259">Textures cannot repeat over one primitive more than 128 times.</span></span><br/>    |
| <span data-ttu-id="77349-260">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="77349-260">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="77349-261">Le nombre de primitives ne peut pas dépasser 1048575.</span><span class="sxs-lookup"><span data-stu-id="77349-261">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="77349-262">Les textures ne peuvent pas se répéter sur une primitive plus de 2048 fois.</span><span class="sxs-lookup"><span data-stu-id="77349-262">Textures cannot repeat over one primitive more than 2048 times.</span></span><br/> |
| <span data-ttu-id="77349-263">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="77349-263">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="77349-264">Le nombre de primitives ne peut pas dépasser 1048575.</span><span class="sxs-lookup"><span data-stu-id="77349-264">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="77349-265">Les textures ne peuvent pas se répéter sur une primitive plus de 8192 fois.</span><span class="sxs-lookup"><span data-stu-id="77349-265">Textures cannot repeat over one primitive more than 8192 times.</span></span><br/> |



 

## <a name="id3d11devicecontextdrawauto"></a><span data-ttu-id="77349-266">ID3D11DeviceContext ::D rawAuto</span><span class="sxs-lookup"><span data-stu-id="77349-266">ID3D11DeviceContext::DrawAuto</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-267">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-267">Feature Level</span></span></th>
<th><span data-ttu-id="77349-268">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-268">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-269">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-269">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-270">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-270">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-271">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-271">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-272">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-272">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexed"></a><span data-ttu-id="77349-273">ID3D11DeviceContext ::D rawIndexed</span><span class="sxs-lookup"><span data-stu-id="77349-273">ID3D11DeviceContext::DrawIndexed</span></span>



| <span data-ttu-id="77349-274">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-274">Feature Level</span></span>             | <span data-ttu-id="77349-275">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-275">Behavior Differences</span></span>                                                                                                                                                                                                            |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77349-276">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="77349-276">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="77349-277">Le nombre de primitives ne peut pas dépasser 65535.</span><span class="sxs-lookup"><span data-stu-id="77349-277">Number of primitives may not exceed 65535.</span></span><br/> <span data-ttu-id="77349-278">Les textures ne peuvent pas se répéter sur une primitive plus de 128 fois.</span><span class="sxs-lookup"><span data-stu-id="77349-278">Textures cannot repeat over one primitive more than 128 times.</span></span><br/> <span data-ttu-id="77349-279">Les valeurs d’index ne peuvent pas dépasser 65534.</span><span class="sxs-lookup"><span data-stu-id="77349-279">Index values cannot exceed 65534.</span></span><br/> <span data-ttu-id="77349-280">Listes de points indexées non prises en charge.</span><span class="sxs-lookup"><span data-stu-id="77349-280">Indexed point lists not supported.</span></span><br/>      |
| <span data-ttu-id="77349-281">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="77349-281">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="77349-282">Le nombre de primitives ne peut pas dépasser 1048575.</span><span class="sxs-lookup"><span data-stu-id="77349-282">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="77349-283">Les textures ne peuvent pas se répéter sur une primitive plus de 2048 fois.</span><span class="sxs-lookup"><span data-stu-id="77349-283">Textures cannot repeat over one primitive more than 2048 times.</span></span><br/> <span data-ttu-id="77349-284">Les valeurs d’index ne peuvent pas dépasser 1048575.</span><span class="sxs-lookup"><span data-stu-id="77349-284">Index values cannot exceed 1048575.</span></span><br/> <span data-ttu-id="77349-285">Listes de points indexées non prises en charge.</span><span class="sxs-lookup"><span data-stu-id="77349-285">Indexed point lists not supported.</span></span><br/> |
| <span data-ttu-id="77349-286">\_Niveau de fonctionnalité D3D \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="77349-286">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="77349-287">Le nombre de primitives ne peut pas dépasser 1048575.</span><span class="sxs-lookup"><span data-stu-id="77349-287">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="77349-288">Les textures ne peuvent pas se répéter sur une primitive plus de 8192 fois.</span><span class="sxs-lookup"><span data-stu-id="77349-288">Textures cannot repeat over one primitive more than 8192 times.</span></span><br/> <span data-ttu-id="77349-289">Les valeurs d’index ne peuvent pas dépasser 1048575.</span><span class="sxs-lookup"><span data-stu-id="77349-289">Index values cannot exceed 1048575.</span></span><br/> <span data-ttu-id="77349-290">Listes de points indexées non prises en charge.</span><span class="sxs-lookup"><span data-stu-id="77349-290">Indexed point lists not supported.</span></span><br/> |



 

## <a name="id3d11devicecontextdrawindexedinstanced"></a><span data-ttu-id="77349-291">ID3D11DeviceContext ::D rawIndexedInstanced</span><span class="sxs-lookup"><span data-stu-id="77349-291">ID3D11DeviceContext::DrawIndexedInstanced</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-292">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-292">Feature Level</span></span></th>
<th><span data-ttu-id="77349-293">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-293">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-294">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-294">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="77349-295">Non pris en charge $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-295">Not supported${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-296">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-296">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-297">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-297">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="77349-298">Le nombre de primitives ne peut pas dépasser 1048575.</span><span class="sxs-lookup"><span data-stu-id="77349-298">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="77349-299">Les textures ne peuvent pas se répéter sur une primitive plus de 8192 fois.</span><span class="sxs-lookup"><span data-stu-id="77349-299">Textures cannot repeat over one primitive more than 8192 times.</span></span><br/> <span data-ttu-id="77349-300">Les valeurs d’index ne peuvent pas dépasser 1048575.</span><span class="sxs-lookup"><span data-stu-id="77349-300">Index values cannot exceed 1048575.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="77349-301">Quand vous appelez la méthode <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced"><strong>DrawIndexedInstanced</strong></a> avec un nuanceur de sommets qui est lié au pipeline et qui n’importe pas de données par instance, certains matériels graphiques Direct3D 9 peuvent ne rien dessiner.</span><span class="sxs-lookup"><span data-stu-id="77349-301">When you call the <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced"><strong>DrawIndexedInstanced</strong></a> method with a vertex shader that is bound to the pipeline and that doesn't import any per-instance data, some Direct3D 9 graphics hardware might not draw anything.</span></span> <span data-ttu-id="77349-302">En particulier, si le nuanceur vertex n’utilise pas de données par instance, l’appel de <strong>DrawIndexedInstanced</strong> avec 1 instance n’est pas équivalent à l’appel de <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw"><strong>Draw</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="77349-302">In particular, if the vertex shader does not use any per-instance data, calling <strong>DrawIndexedInstanced</strong> with 1 instance is not equivalent to calling <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw"><strong>Draw</strong></a>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexedinstancedindirect"></a><span data-ttu-id="77349-303">ID3D11DeviceContext ::D rawIndexedInstancedIndirect</span><span class="sxs-lookup"><span data-stu-id="77349-303">ID3D11DeviceContext::DrawIndexedInstancedIndirect</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-304">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-304">Feature Level</span></span></th>
<th><span data-ttu-id="77349-305">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-305">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-306">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-306">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="77349-307">Non pris en charge sur les 9. \* ou 10. \* niveau de fonctionnalité. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-307">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-308">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-308">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-309">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-309">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="77349-310">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="77349-310">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-311">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="77349-311">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstanced"></a><span data-ttu-id="77349-312">ID3D11DeviceContext ::D rawInstanced</span><span class="sxs-lookup"><span data-stu-id="77349-312">ID3D11DeviceContext::DrawInstanced</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-313">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-313">Feature Level</span></span></th>
<th><span data-ttu-id="77349-314">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-314">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-315">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-315">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-316">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-316">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-317">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-317">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-318">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-318">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstancedindirect"></a><span data-ttu-id="77349-319">ID3D11DeviceContext ::D rawInstancedIndirect</span><span class="sxs-lookup"><span data-stu-id="77349-319">ID3D11DeviceContext::DrawInstancedIndirect</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-320">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-320">Feature Level</span></span></th>
<th><span data-ttu-id="77349-321">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-321">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-322">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-322">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="77349-323">Non pris en charge sur les 9. \* ou 10. \* niveau de fonctionnalité. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-323">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-324">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-324">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-325">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-325">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="77349-326">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="77349-326">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-327">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="77349-327">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetconstantbuffers"></a><span data-ttu-id="77349-328">ID3D11DeviceContext ::D SSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="77349-328">ID3D11DeviceContext::DSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-329">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-329">Feature Level</span></span></th>
<th><span data-ttu-id="77349-330">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-330">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-331">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-331">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="77349-332">Non pris en charge sur les 9. \* ou 10. \* niveau de fonctionnalité. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-332">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-333">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-333">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-334">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-334">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="77349-335">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="77349-335">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-336">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="77349-336">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetsamplers"></a><span data-ttu-id="77349-337">ID3D11DeviceContext ::D SSetSamplers</span><span class="sxs-lookup"><span data-stu-id="77349-337">ID3D11DeviceContext::DSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-338">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-338">Feature Level</span></span></th>
<th><span data-ttu-id="77349-339">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-339">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-340">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-340">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="77349-341">Non pris en charge sur les 9. \* ou 10. \* niveau de fonctionnalité. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-341">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-342">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-342">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-343">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-343">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="77349-344">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="77349-344">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-345">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="77349-345">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshader"></a><span data-ttu-id="77349-346">ID3D11DeviceContext ::D SSetShader</span><span class="sxs-lookup"><span data-stu-id="77349-346">ID3D11DeviceContext::DSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-347">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-347">Feature Level</span></span></th>
<th><span data-ttu-id="77349-348">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-348">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-349">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-349">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="77349-350">Non pris en charge sur les 9. \* ou 10. \* niveau de fonctionnalité. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-350">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-351">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-351">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-352">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-352">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="77349-353">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="77349-353">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-354">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="77349-354">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshaderresources"></a><span data-ttu-id="77349-355">ID3D11DeviceContext ::D SSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="77349-355">ID3D11DeviceContext::DSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-356">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-356">Feature Level</span></span></th>
<th><span data-ttu-id="77349-357">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-357">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-358">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-358">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="77349-359">Non pris en charge sur les 9. \* ou 10. \* niveau de fonctionnalité. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-359">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-360">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-360">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-361">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-361">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="77349-362">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="77349-362">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-363">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="77349-363">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetconstantbuffers"></a><span data-ttu-id="77349-364">ID3D11DeviceContext :: GSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="77349-364">ID3D11DeviceContext::GSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-365">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-365">Feature Level</span></span></th>
<th><span data-ttu-id="77349-366">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-366">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-367">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-367">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-368">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-368">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-369">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-369">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-370">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-370">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetsamplers"></a><span data-ttu-id="77349-371">ID3D11DeviceContext :: GSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="77349-371">ID3D11DeviceContext::GSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-372">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-372">Feature Level</span></span></th>
<th><span data-ttu-id="77349-373">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-373">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-374">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-374">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-375">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-375">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-376">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-376">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-377">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-377">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshader"></a><span data-ttu-id="77349-378">ID3D11DeviceContext :: GSSetShader</span><span class="sxs-lookup"><span data-stu-id="77349-378">ID3D11DeviceContext::GSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-379">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-379">Feature Level</span></span></th>
<th><span data-ttu-id="77349-380">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-380">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-381">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-381">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-382">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-382">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-383">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-383">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-384">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-384">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshaderresources"></a><span data-ttu-id="77349-385">ID3D11DeviceContext :: GSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="77349-385">ID3D11DeviceContext::GSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-386">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-386">Feature Level</span></span></th>
<th><span data-ttu-id="77349-387">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-387">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-388">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-388">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-389">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-389">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-390">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-390">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-391">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-391">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetconstantbuffers"></a><span data-ttu-id="77349-392">ID3D11DeviceContext :: HSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="77349-392">ID3D11DeviceContext::HSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-393">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-393">Feature Level</span></span></th>
<th><span data-ttu-id="77349-394">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-394">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-395">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-395">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="77349-396">Non pris en charge sur les 9. \* ou 10. \* niveau de fonctionnalité. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-396">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-397">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-397">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-398">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-398">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="77349-399">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="77349-399">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-400">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="77349-400">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetsamplers"></a><span data-ttu-id="77349-401">ID3D11DeviceContext :: HSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="77349-401">ID3D11DeviceContext::HSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-402">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-402">Feature Level</span></span></th>
<th><span data-ttu-id="77349-403">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-403">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-404">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-404">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="77349-405">Non pris en charge sur les 9. \* ou 10. \* niveau de fonctionnalité. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-405">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-406">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-406">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-407">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-407">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="77349-408">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="77349-408">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-409">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="77349-409">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshader"></a><span data-ttu-id="77349-410">ID3D11DeviceContext :: HSSetShader</span><span class="sxs-lookup"><span data-stu-id="77349-410">ID3D11DeviceContext::HSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-411">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-411">Feature Level</span></span></th>
<th><span data-ttu-id="77349-412">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-412">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-413">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-413">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="77349-414">Non pris en charge sur les 9. \* ou 10. \* niveau de fonctionnalité. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-414">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-415">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-415">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-416">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-416">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="77349-417">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="77349-417">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-418">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="77349-418">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshaderresources"></a><span data-ttu-id="77349-419">ID3D11DeviceContext :: HSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="77349-419">ID3D11DeviceContext::HSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-420">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-420">Feature Level</span></span></th>
<th><span data-ttu-id="77349-421">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-421">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-422">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-422">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="77349-423">Non pris en charge sur les 9. \* ou 10. \* niveau de fonctionnalité. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-423">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-424">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-424">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-425">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-425">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="77349-426">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="77349-426">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-427">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="77349-427">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetindexbuffer"></a><span data-ttu-id="77349-428">ID3D11DeviceContext::IASetIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="77349-428">ID3D11DeviceContext::IASetIndexBuffer</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-429">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-429">Feature Level</span></span></th>
<th><span data-ttu-id="77349-430">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-430">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-431">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-431">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td><span data-ttu-id="77349-432">Le format peut être différent de celui spécifié lors de la création de la mémoire tampon, mais une traduction coûteuse sera encourue.</span><span class="sxs-lookup"><span data-stu-id="77349-432">Format is allowed to be different from that specified at buffer creation, but an expensive translation will be incurred.</span></span><br/> <span data-ttu-id="77349-433">Autorise uniquement les mémoires tampons d’index avec le format DXGI_FORMAT_R16_UINT.</span><span class="sxs-lookup"><span data-stu-id="77349-433">Only allows index buffers with the DXGI_FORMAT_R16_UINT format.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-434">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-434">D3D_FEATURE_LEVEL_9_2</span></span></td>
<td rowspan="2"> <span data-ttu-id="77349-435">Le format peut être différent de celui spécifié lors de la création de la mémoire tampon, mais une traduction coûteuse sera encourue.</span><span class="sxs-lookup"><span data-stu-id="77349-435">Format is allowed to be different from that specified at buffer creation, but an expensive translation will be incurred.</span></span><br/> <span data-ttu-id="77349-436">Permet aux mémoires tampons d’index avec les formats DXGI_FORMAT_R16_UINT et DXGI_FORMAT_R32_UINT comme D3D_FEATURE_LEVEL_10_0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="77349-436">Allows index buffers with the DXGI_FORMAT_R16_UINT and DXGI_FORMAT_R32_UINT formats like D3D_FEATURE_LEVEL_10_0 and higher.</span></span> <br/> <span data-ttu-id="77349-437">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-437">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="77349-438">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-438">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetprimitivetopology"></a><span data-ttu-id="77349-439">ID3D11DeviceContext :: IASetPrimitiveTopology</span><span class="sxs-lookup"><span data-stu-id="77349-439">ID3D11DeviceContext::IASetPrimitiveTopology</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-440">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-440">Feature Level</span></span></th>
<th><span data-ttu-id="77349-441">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-441">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-442">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-442">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-443">Les topologies de primitives avec contiguïté ne sont pas prises en charge $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-443">Primitive topologies with adjacency are not supported${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-444">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-444">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-445">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-445">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetblendstate"></a><span data-ttu-id="77349-446">ID3D11DeviceContext :: OMSetBlendState</span><span class="sxs-lookup"><span data-stu-id="77349-446">ID3D11DeviceContext::OMSetBlendState</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-447">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-447">Feature Level</span></span></th>
<th><span data-ttu-id="77349-448">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-448">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-449">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-449">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-450">SampleMask ne peut pas être égal à zéro $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-450">SampleMask cannot be zero${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-451">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-451">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-452">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-452">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargets"></a><span data-ttu-id="77349-453">ID3D11DeviceContext :: OMSetRenderTargets</span><span class="sxs-lookup"><span data-stu-id="77349-453">ID3D11DeviceContext::OMSetRenderTargets</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-454">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-454">Feature Level</span></span></th>
<th><span data-ttu-id="77349-455">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-455">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-456">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-456">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="77349-457">Une seule cible de rendu prise en charge $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-457">Only one render target supported${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-458">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-458">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-459">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-459">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="77349-460">Seules quatre cibles de rendu sont prises en charge, et toutes les ressources liées doivent avoir la même profondeur de bits.</span><span class="sxs-lookup"><span data-stu-id="77349-460">Only four render targets supported, and all bound resources must have same bit depth.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargetsandunorderedaccessviews"></a><span data-ttu-id="77349-461">ID3D11DeviceContext :: OMSetRenderTargetsAndUnorderedAccessViews</span><span class="sxs-lookup"><span data-stu-id="77349-461">ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-462">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-462">Feature Level</span></span></th>
<th><span data-ttu-id="77349-463">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-463">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-464">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-464">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-465">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-465">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-466">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-466">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-467">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-467">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetconstantbuffers"></a><span data-ttu-id="77349-468">ID3D11DeviceContext ::P SSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="77349-468">ID3D11DeviceContext::PSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-469">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-469">Feature Level</span></span></th>
<th><span data-ttu-id="77349-470">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-470">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-471">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-471">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-472">Consultez le niveau de fonctionnalité 10,0, mais le nombre total de constantes utilisées par le nuanceur ne peut pas dépasser 32 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-472">See feature level 10.0, but total number of constants used by shader cannot exceed 32${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-473">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-473">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-474">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-474">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetsamplers"></a><span data-ttu-id="77349-475">ID3D11DeviceContext ::P SSetSamplers</span><span class="sxs-lookup"><span data-stu-id="77349-475">ID3D11DeviceContext::PSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-476">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-476">Feature Level</span></span></th>
<th><span data-ttu-id="77349-477">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-477">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-478">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-478">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-479">Vous ne pouvez pas lier plus de 16 échantillonneurs $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-479">No more than 16 samplers can be bound${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-480">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-480">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-481">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-481">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshader"></a><span data-ttu-id="77349-482">ID3D11DeviceContext ::P SSetShader</span><span class="sxs-lookup"><span data-stu-id="77349-482">ID3D11DeviceContext::PSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-483">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-483">Feature Level</span></span></th>
<th><span data-ttu-id="77349-484">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-484">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-485">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-485">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="77349-486">Uniquement ps_4_0_level_9_1 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-486">Only ps_4_0_level_9_1${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-487">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-487">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-488">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-488">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="77349-489">Ps_4_0_level_9_3 ou ps_4_0_level_9_1 uniquement</span><span class="sxs-lookup"><span data-stu-id="77349-489">Only ps_4_0_level_9_3 or ps_4_0_level_9_1</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshaderresources"></a><span data-ttu-id="77349-490">ID3D11DeviceContext ::P SSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="77349-490">ID3D11DeviceContext::PSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-491">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-491">Feature Level</span></span></th>
<th><span data-ttu-id="77349-492">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-492">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-493">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-493">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-494">Pas plus de 8 ressources de nuanceur liées simultanément $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-494">No more than 8 simultaneously bound shader resources${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-495">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-495">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-496">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-496">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetscissorrects"></a><span data-ttu-id="77349-497">ID3D11DeviceContext :: RSSetScissorRects</span><span class="sxs-lookup"><span data-stu-id="77349-497">ID3D11DeviceContext::RSSetScissorRects</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-498">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-498">Feature Level</span></span></th>
<th><span data-ttu-id="77349-499">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-499">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-500">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-500">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-501">Seul le rectangle avant toute chose ciseaux est disponible $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-501">Only the zeroth scissor rect is available${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-502">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-502">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-503">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-503">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetviewports"></a><span data-ttu-id="77349-504">ID3D11DeviceContext :: RSSetViewports</span><span class="sxs-lookup"><span data-stu-id="77349-504">ID3D11DeviceContext::RSSetViewports</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-505">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-505">Feature Level</span></span></th>
<th><span data-ttu-id="77349-506">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-506">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-507">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-507">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-508">Seule la fenêtre d’affichage avant toute chose est disponible $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-508">Only the zeroth viewport is available${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-509">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-509">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-510">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-510">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="77349-511">Même si vous spécifiez des valeurs float pour les membres de la structure de la [**\_ fenêtre d’affichage d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) pour le tableau *pViewports* dans un appel à [**ID3D11DeviceContext :: RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) pour les [niveaux de fonctionnalité](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x, **RSSetViewports** utilise des DWORD en interne.</span><span class="sxs-lookup"><span data-stu-id="77349-511">Even though you specify float values to the members of the [**D3D11\_VIEWPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) structure for the *pViewports* array in a call to [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) for [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 9\_x, **RSSetViewports** uses DWORDs internally.</span></span> <span data-ttu-id="77349-512">En raison de ce comportement, lorsque vous utilisez un coin supérieur gauche négatif pour la fenêtre d’affichage, l’appel à **RSSetViewports** pour les niveaux de fonctionnalité 9 \_ x échoue.</span><span class="sxs-lookup"><span data-stu-id="77349-512">Because of this behavior, when you use a negative top left corner for the viewport, the call to **RSSetViewports** for feature levels 9\_x fails.</span></span> <span data-ttu-id="77349-513">Cet échec se produit parce que **RSSetViewports** pour 9 \_ x convertit les valeurs à virgule flottante en entiers non signés sans validation, ce qui entraîne un dépassement sur les entiers.</span><span class="sxs-lookup"><span data-stu-id="77349-513">This failure occurs because **RSSetViewports** for 9\_x casts the floating point values into unsigned integers without validation, which results in integer overflow.</span></span>

<span data-ttu-id="77349-514">L’appel à [**ID3D11DeviceContext :: RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) pour les [niveaux de fonctionnalité](overviews-direct3d-11-devices-downlevel-intro.md) 10 \_ x et 11 \_ x fonctionne comme prévu, même quand vous utilisez un coin supérieur gauche négatif pour la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="77349-514">The call to [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) for [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 10\_x and 11\_x works as you expect even when you use a negative top left corner for the viewport.</span></span>

## <a name="id3d11devicecontextsetpredication"></a><span data-ttu-id="77349-515">ID3D11DeviceContext :: SetPredication</span><span class="sxs-lookup"><span data-stu-id="77349-515">ID3D11DeviceContext::SetPredication</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-516">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-516">Feature Level</span></span></th>
<th><span data-ttu-id="77349-517">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-517">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-518">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-518">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-519">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-519">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-520">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-520">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-521">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-521">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextsosettargets"></a><span data-ttu-id="77349-522">ID3D11DeviceContext :: SOSetTargets</span><span class="sxs-lookup"><span data-stu-id="77349-522">ID3D11DeviceContext::SOSetTargets</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-523">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-523">Feature Level</span></span></th>
<th><span data-ttu-id="77349-524">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-524">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-525">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-525">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-526">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-526">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-527">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-527">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-528">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-528">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetconstantbuffers"></a><span data-ttu-id="77349-529">ID3D11DeviceContext :: VSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="77349-529">ID3D11DeviceContext::VSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-530">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-530">Feature Level</span></span></th>
<th><span data-ttu-id="77349-531">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-531">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-532">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-532">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-533">Consultez le niveau de fonctionnalité 10,0, mais le nombre total de constantes utilisées par le nuanceur ne peut pas dépasser 255 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-533">See feature level 10.0, but total number of constants used by shader cannot exceed 255${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-534">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-534">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-535">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-535">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetsamplers"></a><span data-ttu-id="77349-536">ID3D11DeviceContext :: VSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="77349-536">ID3D11DeviceContext::VSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-537">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-537">Feature Level</span></span></th>
<th><span data-ttu-id="77349-538">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-538">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-539">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-539">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-540">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-540">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-541">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-541">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-542">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-542">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshader"></a><span data-ttu-id="77349-543">ID3D11DeviceContext :: VSSetShader</span><span class="sxs-lookup"><span data-stu-id="77349-543">ID3D11DeviceContext::VSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-544">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-544">Feature Level</span></span></th>
<th><span data-ttu-id="77349-545">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-545">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-546">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-546">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="77349-547">Uniquement vs_4_0_level_9_1 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-547">Only vs_4_0_level_9_1${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-548">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-548">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-549">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-549">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="77349-550">Vs_4_0_level_9_3 ou vs_4_0_level_9_1 uniquement</span><span class="sxs-lookup"><span data-stu-id="77349-550">Only vs_4_0_level_9_3 or vs_4_0_level_9_1</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshaderresources"></a><span data-ttu-id="77349-551">ID3D11DeviceContext :: VSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="77349-551">ID3D11DeviceContext::VSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="77349-552">Niveau de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="77349-552">Feature Level</span></span></th>
<th><span data-ttu-id="77349-553">Différences de comportement</span><span class="sxs-lookup"><span data-stu-id="77349-553">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77349-554">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="77349-554">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="77349-555">Non pris en charge sur un niveau de fonctionnalité 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77349-555">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="77349-556">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="77349-556">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="77349-557">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="77349-557">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="77349-558">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="77349-558">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77349-559">Référence 10Level9</span><span class="sxs-lookup"><span data-stu-id="77349-559">10Level9 Reference</span></span>](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

 





