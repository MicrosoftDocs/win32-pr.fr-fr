---
title: Fonctions de conversion de format (référence HLSL)
description: La section contient les fonctions de conversion de format utilisées dans les nuanceurs de calcul et de pixels.
ms.assetid: 05575ee8-4428-437f-bfb6-e5c676405d65
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 355fb59aa6a94e144daf05942b40d3f685daff51
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222877"
---
# <a name="format-conversion-functions-hlsl-reference"></a><span data-ttu-id="68997-103">Fonctions de conversion de format (référence HLSL)</span><span class="sxs-lookup"><span data-stu-id="68997-103">Format conversion functions (HLSL reference)</span></span>

<span data-ttu-id="68997-104">La section contient les fonctions de conversion de format utilisées dans les nuanceurs de calcul et de pixels.</span><span class="sxs-lookup"><span data-stu-id="68997-104">The section contains the format conversion functions used in Compute and Pixel Shaders.</span></span>

-   [<span data-ttu-id="68997-105">Fonctions de convertisseur</span><span class="sxs-lookup"><span data-stu-id="68997-105">Converter Functions</span></span>](#converter-functions)
-   [<span data-ttu-id="68997-106">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="68997-106">Related topics</span></span>](#related-topics)

> <span data-ttu-id="68997-107">L’en-tête D3DX_DXGIFormatConvert. inl est fourni dans le SDK DirectX hérité et s’appuyait sur XNAMath pour la prise en charge de C++.</span><span class="sxs-lookup"><span data-stu-id="68997-107">The D3DX_DXGIFormatConvert.inl header ships in the legacy DirectX SDK and relied on XNAMath for C++ support.</span></span> <span data-ttu-id="68997-108">Il est également inclus dans le package NuGet [Microsoft. DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) .</span><span class="sxs-lookup"><span data-stu-id="68997-108">It is also included in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet package.</span></span> <span data-ttu-id="68997-109">La dernière version utilise DirectXMath pour la prise en charge de C++, et toutes les fonctions sont définies dans l’espace de noms **DirectX** C++.</span><span class="sxs-lookup"><span data-stu-id="68997-109">The latest version uses DirectXMath for C++ support, and all functions are defined in the **DirectX** C++ namespace.</span></span>

## <a name="converter-functions"></a><span data-ttu-id="68997-110">Fonctions de convertisseur</span><span class="sxs-lookup"><span data-stu-id="68997-110">Converter Functions</span></span>

### <a name="dxgi_format_r10g10b10a2_unorm"></a><span data-ttu-id="68997-111">DXGI \_ format \_ R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="68997-111">DXGI\_FORMAT\_R10G10B10A2\_UNORM</span></span>

<dl>

[<span data-ttu-id="68997-112">**D3DX \_ R10G10B10A2 \_ UNORM \_ vers \_ float4**</span><span class="sxs-lookup"><span data-stu-id="68997-112">**D3DX\_R10G10B10A2\_UNORM\_to\_FLOAT4**</span></span>](d3dx-r10g10b10a2-unorm-to-float4.md)  
[<span data-ttu-id="68997-113">**D3DX \_ float4 \_ vers \_ R10G10B10A2 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="68997-113">**D3DX\_FLOAT4\_to\_R10G10B10A2\_UNORM**</span></span>](d3dx-float4-to-r10g10b10a2-unorm.md)  
</dl>

### <a name="dxgi_format_r10g10b10a2_uint"></a><span data-ttu-id="68997-114">DXGI \_ format \_ R10G10B10A2 \_ uint</span><span class="sxs-lookup"><span data-stu-id="68997-114">DXGI\_FORMAT\_R10G10B10A2\_UINT</span></span>

<dl>

[<span data-ttu-id="68997-115">**D3DX \_ R10G10B10A2 \_ uint \_ vers \_ UINT4**</span><span class="sxs-lookup"><span data-stu-id="68997-115">**D3DX\_R10G10B10A2\_UINT\_to\_UINT4**</span></span>](d3dx-r10g10b10a2-uint-to-uint4.md)  
[<span data-ttu-id="68997-116">**D3DX \_ UINT4 \_ vers \_ R10G10B10A2 \_ uint**</span><span class="sxs-lookup"><span data-stu-id="68997-116">**D3DX\_UINT4\_to\_R10G10B10A2\_UINT**</span></span>](d3dx-uint4-to-r10g10b10a2-uint.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_unorm"></a><span data-ttu-id="68997-117">DXGI \_ format \_ R8G8B8A8 \_ UNORM :</span><span class="sxs-lookup"><span data-stu-id="68997-117">DXGI\_FORMAT\_R8G8B8A8\_UNORM:</span></span>

<dl>

[<span data-ttu-id="68997-118">**D3DX \_ R8G8B8A8 \_ UNORM \_ vers \_ float4**</span><span class="sxs-lookup"><span data-stu-id="68997-118">**D3DX\_R8G8B8A8\_UNORM\_to\_FLOAT4**</span></span>](d3dx-r8g8b8a8-unorm-to-float4.md)  
[<span data-ttu-id="68997-119">**D3DX \_ float4 \_ vers \_ R8G8B8A8 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="68997-119">**D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM**</span></span>](d3dx-float4-to-r8g8b8a8-unorm.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_unorm_srgb"></a><span data-ttu-id="68997-120">DXGI \_ format \_ R8G8B8A8 \_ UNORM \_ sRVB</span><span class="sxs-lookup"><span data-stu-id="68997-120">DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB</span></span>

<dl>

[<span data-ttu-id="68997-121">**D3DX \_ R8G8B8A8 \_ UNORM \_ sRVB \_ à \_ float4 \_ inexact**</span><span class="sxs-lookup"><span data-stu-id="68997-121">**D3DX\_R8G8B8A8\_UNORM\_SRGB\_to\_FLOAT4\_inexact**</span></span>](d3dx-r8g8b8a8-unorm-srgb-to-float4-inexact.md)  
[<span data-ttu-id="68997-122">**D3DX \_ R8G8B8A8 \_ UNORM \_ sRVB \_ en \_ float4**</span><span class="sxs-lookup"><span data-stu-id="68997-122">**D3DX\_R8G8B8A8\_UNORM\_SRGB\_to\_FLOAT4**</span></span>](d3dx-r8g8b8a8-unorm-srgb-to-float4.md)  
[<span data-ttu-id="68997-123">**D3DX \_ float4 \_ vers \_ R8G8B8A8 \_ UNORM \_ sRVB**</span><span class="sxs-lookup"><span data-stu-id="68997-123">**D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM\_SRGB**</span></span>](d3dx-float4-to-r8g8b8a8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_uint"></a><span data-ttu-id="68997-124">DXGI \_ format \_ R8G8B8A8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="68997-124">DXGI\_FORMAT\_R8G8B8A8\_UINT</span></span>

<dl>

[<span data-ttu-id="68997-125">**D3DX \_ R8G8B8A8 \_ uint \_ vers \_ UINT4**</span><span class="sxs-lookup"><span data-stu-id="68997-125">**D3DX\_R8G8B8A8\_UINT\_to\_UINT4**</span></span>](d3dx-r8g8b8a8-uint-to-uint4.md)  
[<span data-ttu-id="68997-126">**D3DX \_ UINT4 \_ vers \_ R8G8B8A8 \_ uint**</span><span class="sxs-lookup"><span data-stu-id="68997-126">**D3DX\_UINT4\_to\_R8G8B8A8\_UINT**</span></span>](d3dx-uint4-to-r8g8b8a8-uint.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_snorm"></a><span data-ttu-id="68997-127">\_Format dxgi \_ R8G8B8A8 \_ ronfler</span><span class="sxs-lookup"><span data-stu-id="68997-127">DXGI\_FORMAT\_R8G8B8A8\_SNORM</span></span>

<dl>

[<span data-ttu-id="68997-128">**D3DX \_ R8G8B8A8 \_ ronfler \_ à \_ float4**</span><span class="sxs-lookup"><span data-stu-id="68997-128">**D3DX\_R8G8B8A8\_SNORM\_to\_FLOAT4**</span></span>](d3dx-r8g8b8a8-snorm-to-float4.md)  
[<span data-ttu-id="68997-129">**D3DX \_ float4 \_ à \_ R8G8B8A8 \_ ronfler**</span><span class="sxs-lookup"><span data-stu-id="68997-129">**D3DX\_FLOAT4\_to\_R8G8B8A8\_SNORM**</span></span>](d3dx-float4-to-r8g8b8a8-snorm.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_sint"></a><span data-ttu-id="68997-130">\_Format dxgi \_ R8G8B8A8 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="68997-130">DXGI\_FORMAT\_R8G8B8A8\_SINT</span></span>

<dl>

[<span data-ttu-id="68997-131">**D3DX \_ R8G8B8A8 \_ Saint \_ \_ INT4**</span><span class="sxs-lookup"><span data-stu-id="68997-131">**D3DX\_R8G8B8A8\_SINT\_to\_INT4**</span></span>](d3dx-r8g8b8a8-sint-to-int4.md)  
[<span data-ttu-id="68997-132">**D3DX \_ INT4 \_ à \_ R8G8B8A8 \_ Saint**</span><span class="sxs-lookup"><span data-stu-id="68997-132">**D3DX\_INT4\_to\_R8G8B8A8\_SINT**</span></span>](d3dx-int4-to-r8g8b8a8-sint.md)  
</dl>

### <a name="dxgi_format_b8g8r8a8_unorm"></a><span data-ttu-id="68997-133">DXGI \_ format \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="68997-133">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span>

<dl>

[<span data-ttu-id="68997-134">**D3DX \_ B8G8R8A8 \_ UNORM \_ vers \_ float4**</span><span class="sxs-lookup"><span data-stu-id="68997-134">**D3DX\_B8G8R8A8\_UNORM\_to\_FLOAT4**</span></span>](d3dx-b8g8r8a8-unorm-to-float4.md)  
[<span data-ttu-id="68997-135">**D3DX \_ float4 \_ vers \_ B8G8R8A8 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="68997-135">**D3DX\_FLOAT4\_to\_B8G8R8A8\_UNORM**</span></span>](d3dx-float4-to-b8g8r8a8-unorm.md)  
</dl>

### <a name="dxgi_format_b8g8r8a8_unorm_srgb"></a><span data-ttu-id="68997-136">DXGI \_ format \_ B8G8R8A8 \_ UNORM \_ sRVB</span><span class="sxs-lookup"><span data-stu-id="68997-136">DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB</span></span>

<dl>

[<span data-ttu-id="68997-137">**D3DX \_ B8G8R8A8 \_ UNORM \_ sRVB \_ à \_ float4 \_ inexact**</span><span class="sxs-lookup"><span data-stu-id="68997-137">**D3DX\_B8G8R8A8\_UNORM\_SRGB\_to\_FLOAT4\_inexact**</span></span>](d3dx-b8g8r8a8-unorm-srgb-to-float4-inexact.md)  
[<span data-ttu-id="68997-138">**D3DX \_ B8G8R8A8 \_ UNORM \_ sRVB \_ en \_ float4**</span><span class="sxs-lookup"><span data-stu-id="68997-138">**D3DX\_B8G8R8A8\_UNORM\_SRGB\_to\_FLOAT4**</span></span>](d3dx-b8g8r8a8-unorm-srgb-to-float4.md)  
[<span data-ttu-id="68997-139">**D3DX \_ float4 \_ vers \_ R8G8B8A8 \_ UNORM \_ sRVB**</span><span class="sxs-lookup"><span data-stu-id="68997-139">**D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM\_SRGB**</span></span>](d3dx-float4-to-r8g8b8a8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_b8g8r8x8_unorm"></a><span data-ttu-id="68997-140">DXGI \_ format \_ B8G8R8X8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="68997-140">DXGI\_FORMAT\_B8G8R8X8\_UNORM</span></span>

<dl>

[<span data-ttu-id="68997-141">**D3DX \_ B8G8R8X8 \_ UNORM \_ vers \_ FLOAT3**</span><span class="sxs-lookup"><span data-stu-id="68997-141">**D3DX\_B8G8R8X8\_UNORM\_to\_FLOAT3**</span></span>](d3dx-b8g8r8x8-unorm-to-float3.md)  
[<span data-ttu-id="68997-142">**D3DX \_ FLOAT3 \_ vers \_ B8G8R8X8 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="68997-142">**D3DX\_FLOAT3\_to\_B8G8R8X8\_UNORM**</span></span>](d3dx-float3-to-b8g8r8x8-unorm.md)  
</dl>

### <a name="dxgi_format_b8g8r8x8_unorm_srgb"></a><span data-ttu-id="68997-143">DXGI \_ format \_ B8G8R8X8 \_ UNORM \_ sRVB</span><span class="sxs-lookup"><span data-stu-id="68997-143">DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB</span></span>

<dl>

[<span data-ttu-id="68997-144">**D3DX \_ B8G8R8X8 \_ UNORM \_ sRVB \_ à \_ FLOAT3 \_ inexact**</span><span class="sxs-lookup"><span data-stu-id="68997-144">**D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3\_inexact**</span></span>](d3dx-b8g8r8x8-unorm-srgb-to-float3-inexact.md)  
[<span data-ttu-id="68997-145">**D3DX \_ B8G8R8X8 \_ UNORM \_ sRVB \_ en \_ FLOAT3**</span><span class="sxs-lookup"><span data-stu-id="68997-145">**D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3**</span></span>](d3dx-b8g8r8x8-unorm-srgb-to-float3.md)  
[<span data-ttu-id="68997-146">**D3DX \_ FLOAT3 \_ vers \_ B8G8R8X8 \_ UNORM \_ sRVB**</span><span class="sxs-lookup"><span data-stu-id="68997-146">**D3DX\_FLOAT3\_to\_B8G8R8X8\_UNORM\_SRGB**</span></span>](d3dx-float3-to-b8g8r8x8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_r16g16_float"></a><span data-ttu-id="68997-147">DXGI \_ format \_ R16G16 \_ float</span><span class="sxs-lookup"><span data-stu-id="68997-147">DXGI\_FORMAT\_R16G16\_FLOAT</span></span>

<dl>

[<span data-ttu-id="68997-148">**D3DX \_ R16G16 \_ float \_ vers \_ FLOAT2**</span><span class="sxs-lookup"><span data-stu-id="68997-148">**D3DX\_R16G16\_FLOAT\_to\_FLOAT2**</span></span>](d3dx-r16g16-float-to-float2.md)  
[<span data-ttu-id="68997-149">**D3DX \_ FLOAT2 \_ vers \_ R16G16 \_ float**</span><span class="sxs-lookup"><span data-stu-id="68997-149">**D3DX\_FLOAT2\_to\_R16G16\_FLOAT**</span></span>](d3dx-float2-to-r16g16-float.md)  
</dl>

### <a name="dxgi_format_r16g16_unorm"></a><span data-ttu-id="68997-150">DXGI \_ format \_ R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="68997-150">DXGI\_FORMAT\_R16G16\_UNORM</span></span>

<dl>

[<span data-ttu-id="68997-151">**D3DX \_ R16G16 \_ UNORM \_ vers \_ FLOAT2**</span><span class="sxs-lookup"><span data-stu-id="68997-151">**D3DX\_R16G16\_UNORM\_to\_FLOAT2**</span></span>](d3dx-r16g16-unorm-to-float2.md)  
[<span data-ttu-id="68997-152">**D3DX \_ FLOAT2 \_ vers \_ R16G16 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="68997-152">**D3DX\_FLOAT2\_to\_R16G16\_UNORM**</span></span>](d3dx-float2-to-r16g16-unorm.md)  
</dl>

### <a name="dxgi_format_r16g16_uint"></a><span data-ttu-id="68997-153">DXGI \_ format \_ R16G16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="68997-153">DXGI\_FORMAT\_R16G16\_UINT</span></span>

<dl>

[<span data-ttu-id="68997-154">**D3DX \_ R16G16 \_ uint \_ vers \_ UINT2**</span><span class="sxs-lookup"><span data-stu-id="68997-154">**D3DX\_R16G16\_UINT\_to\_UINT2**</span></span>](d3dx-r16g16-uint-to-uint2.md)  
[<span data-ttu-id="68997-155">**D3DX \_ UINT2 \_ vers \_ R16G16 \_ uint**</span><span class="sxs-lookup"><span data-stu-id="68997-155">**D3DX\_UINT2\_to\_R16G16\_UINT**</span></span>](d3dx-uint2-to-r16g16-uint.md)  
</dl>

### <a name="dxgi_format_r16g16_snorm"></a><span data-ttu-id="68997-156">\_Format dxgi \_ R16G16 \_ ronfler</span><span class="sxs-lookup"><span data-stu-id="68997-156">DXGI\_FORMAT\_R16G16\_SNORM</span></span>

<dl>

[<span data-ttu-id="68997-157">**D3DX \_ R16G16 \_ ronfler \_ à \_ FLOAT2**</span><span class="sxs-lookup"><span data-stu-id="68997-157">**D3DX\_R16G16\_SNORM\_to\_FLOAT2**</span></span>](d3dx-r16g16-snorm-to-float2.md)  
[<span data-ttu-id="68997-158">**D3DX \_ FLOAT2 \_ à \_ R16G16 \_ ronfler**</span><span class="sxs-lookup"><span data-stu-id="68997-158">**D3DX\_FLOAT2\_to\_R16G16\_SNORM**</span></span>](d3dx-float2-to-r16g16-snorm.md)  
</dl>

### <a name="dxgi_format_r16g16_sint"></a><span data-ttu-id="68997-159">\_Format dxgi \_ R16G16 \_ Saint-</span><span class="sxs-lookup"><span data-stu-id="68997-159">DXGI\_FORMAT\_R16G16\_SINT</span></span>

<dl>

[<span data-ttu-id="68997-160">**D3DX \_ R16G16 \_ Saint \_ \_ Int2**</span><span class="sxs-lookup"><span data-stu-id="68997-160">**D3DX\_R16G16\_SINT\_to\_INT2**</span></span>](d3dx-r16g16-sint-to-int2.md)  
[<span data-ttu-id="68997-161">**D3DX \_ Int2 \_ à \_ R16G16 \_ Saint**</span><span class="sxs-lookup"><span data-stu-id="68997-161">**D3DX\_INT2\_to\_R16G16\_SINT**</span></span>](d3dx-int2-to-r16g16-sint.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="68997-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="68997-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68997-163">Référence de conversion de format Inline</span><span class="sxs-lookup"><span data-stu-id="68997-163">Inline Format Conversion Reference</span></span>](inline-format-conversion-reference.md)
</dt> <dt>

[<span data-ttu-id="68997-164">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="68997-164">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 
