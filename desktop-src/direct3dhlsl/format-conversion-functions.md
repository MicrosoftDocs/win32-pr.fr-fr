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
# <a name="format-conversion-functions-hlsl-reference"></a>Fonctions de conversion de format (référence HLSL)

La section contient les fonctions de conversion de format utilisées dans les nuanceurs de calcul et de pixels.

-   [Fonctions de convertisseur](#converter-functions)
-   [Rubriques connexes](#related-topics)

> L’en-tête D3DX_DXGIFormatConvert. inl est fourni dans le SDK DirectX hérité et s’appuyait sur XNAMath pour la prise en charge de C++. Il est également inclus dans le package NuGet [Microsoft. DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) . La dernière version utilise DirectXMath pour la prise en charge de C++, et toutes les fonctions sont définies dans l’espace de noms **DirectX** C++.

## <a name="converter-functions"></a>Fonctions de convertisseur

### <a name="dxgi_format_r10g10b10a2_unorm"></a>DXGI \_ format \_ R10G10B10A2 \_ UNORM

<dl>

[**D3DX \_ R10G10B10A2 \_ UNORM \_ vers \_ float4**](d3dx-r10g10b10a2-unorm-to-float4.md)  
[**D3DX \_ float4 \_ vers \_ R10G10B10A2 \_ UNORM**](d3dx-float4-to-r10g10b10a2-unorm.md)  
</dl>

### <a name="dxgi_format_r10g10b10a2_uint"></a>DXGI \_ format \_ R10G10B10A2 \_ uint

<dl>

[**D3DX \_ R10G10B10A2 \_ uint \_ vers \_ UINT4**](d3dx-r10g10b10a2-uint-to-uint4.md)  
[**D3DX \_ UINT4 \_ vers \_ R10G10B10A2 \_ uint**](d3dx-uint4-to-r10g10b10a2-uint.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_unorm"></a>DXGI \_ format \_ R8G8B8A8 \_ UNORM :

<dl>

[**D3DX \_ R8G8B8A8 \_ UNORM \_ vers \_ float4**](d3dx-r8g8b8a8-unorm-to-float4.md)  
[**D3DX \_ float4 \_ vers \_ R8G8B8A8 \_ UNORM**](d3dx-float4-to-r8g8b8a8-unorm.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_unorm_srgb"></a>DXGI \_ format \_ R8G8B8A8 \_ UNORM \_ sRVB

<dl>

[**D3DX \_ R8G8B8A8 \_ UNORM \_ sRVB \_ à \_ float4 \_ inexact**](d3dx-r8g8b8a8-unorm-srgb-to-float4-inexact.md)  
[**D3DX \_ R8G8B8A8 \_ UNORM \_ sRVB \_ en \_ float4**](d3dx-r8g8b8a8-unorm-srgb-to-float4.md)  
[**D3DX \_ float4 \_ vers \_ R8G8B8A8 \_ UNORM \_ sRVB**](d3dx-float4-to-r8g8b8a8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_uint"></a>DXGI \_ format \_ R8G8B8A8 \_ uint

<dl>

[**D3DX \_ R8G8B8A8 \_ uint \_ vers \_ UINT4**](d3dx-r8g8b8a8-uint-to-uint4.md)  
[**D3DX \_ UINT4 \_ vers \_ R8G8B8A8 \_ uint**](d3dx-uint4-to-r8g8b8a8-uint.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_snorm"></a>\_Format dxgi \_ R8G8B8A8 \_ ronfler

<dl>

[**D3DX \_ R8G8B8A8 \_ ronfler \_ à \_ float4**](d3dx-r8g8b8a8-snorm-to-float4.md)  
[**D3DX \_ float4 \_ à \_ R8G8B8A8 \_ ronfler**](d3dx-float4-to-r8g8b8a8-snorm.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_sint"></a>\_Format dxgi \_ R8G8B8A8 \_ Saint-

<dl>

[**D3DX \_ R8G8B8A8 \_ Saint \_ \_ INT4**](d3dx-r8g8b8a8-sint-to-int4.md)  
[**D3DX \_ INT4 \_ à \_ R8G8B8A8 \_ Saint**](d3dx-int4-to-r8g8b8a8-sint.md)  
</dl>

### <a name="dxgi_format_b8g8r8a8_unorm"></a>DXGI \_ format \_ B8G8R8A8 \_ UNORM

<dl>

[**D3DX \_ B8G8R8A8 \_ UNORM \_ vers \_ float4**](d3dx-b8g8r8a8-unorm-to-float4.md)  
[**D3DX \_ float4 \_ vers \_ B8G8R8A8 \_ UNORM**](d3dx-float4-to-b8g8r8a8-unorm.md)  
</dl>

### <a name="dxgi_format_b8g8r8a8_unorm_srgb"></a>DXGI \_ format \_ B8G8R8A8 \_ UNORM \_ sRVB

<dl>

[**D3DX \_ B8G8R8A8 \_ UNORM \_ sRVB \_ à \_ float4 \_ inexact**](d3dx-b8g8r8a8-unorm-srgb-to-float4-inexact.md)  
[**D3DX \_ B8G8R8A8 \_ UNORM \_ sRVB \_ en \_ float4**](d3dx-b8g8r8a8-unorm-srgb-to-float4.md)  
[**D3DX \_ float4 \_ vers \_ R8G8B8A8 \_ UNORM \_ sRVB**](d3dx-float4-to-r8g8b8a8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_b8g8r8x8_unorm"></a>DXGI \_ format \_ B8G8R8X8 \_ UNORM

<dl>

[**D3DX \_ B8G8R8X8 \_ UNORM \_ vers \_ FLOAT3**](d3dx-b8g8r8x8-unorm-to-float3.md)  
[**D3DX \_ FLOAT3 \_ vers \_ B8G8R8X8 \_ UNORM**](d3dx-float3-to-b8g8r8x8-unorm.md)  
</dl>

### <a name="dxgi_format_b8g8r8x8_unorm_srgb"></a>DXGI \_ format \_ B8G8R8X8 \_ UNORM \_ sRVB

<dl>

[**D3DX \_ B8G8R8X8 \_ UNORM \_ sRVB \_ à \_ FLOAT3 \_ inexact**](d3dx-b8g8r8x8-unorm-srgb-to-float3-inexact.md)  
[**D3DX \_ B8G8R8X8 \_ UNORM \_ sRVB \_ en \_ FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md)  
[**D3DX \_ FLOAT3 \_ vers \_ B8G8R8X8 \_ UNORM \_ sRVB**](d3dx-float3-to-b8g8r8x8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_r16g16_float"></a>DXGI \_ format \_ R16G16 \_ float

<dl>

[**D3DX \_ R16G16 \_ float \_ vers \_ FLOAT2**](d3dx-r16g16-float-to-float2.md)  
[**D3DX \_ FLOAT2 \_ vers \_ R16G16 \_ float**](d3dx-float2-to-r16g16-float.md)  
</dl>

### <a name="dxgi_format_r16g16_unorm"></a>DXGI \_ format \_ R16G16 \_ UNORM

<dl>

[**D3DX \_ R16G16 \_ UNORM \_ vers \_ FLOAT2**](d3dx-r16g16-unorm-to-float2.md)  
[**D3DX \_ FLOAT2 \_ vers \_ R16G16 \_ UNORM**](d3dx-float2-to-r16g16-unorm.md)  
</dl>

### <a name="dxgi_format_r16g16_uint"></a>DXGI \_ format \_ R16G16 \_ uint

<dl>

[**D3DX \_ R16G16 \_ uint \_ vers \_ UINT2**](d3dx-r16g16-uint-to-uint2.md)  
[**D3DX \_ UINT2 \_ vers \_ R16G16 \_ uint**](d3dx-uint2-to-r16g16-uint.md)  
</dl>

### <a name="dxgi_format_r16g16_snorm"></a>\_Format dxgi \_ R16G16 \_ ronfler

<dl>

[**D3DX \_ R16G16 \_ ronfler \_ à \_ FLOAT2**](d3dx-r16g16-snorm-to-float2.md)  
[**D3DX \_ FLOAT2 \_ à \_ R16G16 \_ ronfler**](d3dx-float2-to-r16g16-snorm.md)  
</dl>

### <a name="dxgi_format_r16g16_sint"></a>\_Format dxgi \_ R16G16 \_ Saint-

<dl>

[**D3DX \_ R16G16 \_ Saint \_ \_ Int2**](d3dx-r16g16-sint-to-int2.md)  
[**D3DX \_ Int2 \_ à \_ R16G16 \_ Saint**](d3dx-int2-to-r16g16-sint.md)  
</dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de conversion de format Inline](inline-format-conversion-reference.md)
</dt> <dt>

[Décompresser et compresser le \_ format DXGI pour la modification des images In-Place](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 
