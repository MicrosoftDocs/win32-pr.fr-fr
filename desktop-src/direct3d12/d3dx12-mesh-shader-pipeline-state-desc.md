---
title: Structure D3DX12_MESH_SHADER_PIPELINE_STATE_DESC (D3dx12. h)
description: Pour les [nuanceurs de maillage/amplifications](https://microsoft.github.io/DirectX-Specs/d3d/MeshShader.html), vous pouvez utiliser les données d’un [EffectPipelineStateDescription](https://github.com/Microsoft/DirectXTK12/wiki/EffectPipelineStateDescription), avec **D3DX12_MESH_SHADER_PIPELINE_STATE_DESC**, pour fournir tout l’État.
keywords:
- Structure D3DX12_MESH_SHADER_PIPELINE_STATE_DESC
topic_type:
- apiref
api_name:
- D3DX12_MESH_SHADER_PIPELINE_STATE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/02/2021
ms.openlocfilehash: 99ffe747a6cd916f82e3d2ae52f9fa368203da91
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812522"
---
# <a name="d3dx12_mesh_shader_pipeline_state_desc-structure"></a>Structure D3DX12_MESH_SHADER_PIPELINE_STATE_DESC

Pour les [nuanceurs de maillage/amplifications](https://microsoft.github.io/DirectX-Specs/d3d/MeshShader.html), vous pouvez utiliser les données d’un [EffectPipelineStateDescription](https://github.com/Microsoft/DirectXTK12/wiki/EffectPipelineStateDescription), avec **D3DX12_MESH_SHADER_PIPELINE_STATE_DESC**, pour fournir tout l’État.

Voir aussi [CD3DX12_PIPELINE_STATE_STREAM2](cd3dx12-pipeline-state-stream1.md).

Pour obtenir un exemple de code, consultez [nuanceurs de maille](https://github.com/Microsoft/DirectXTK12/wiki/EffectPipelineStateDescription#mesh-shaders).

## <a name="syntax"></a>Syntaxe

```cpp
struct D3DX12_MESH_SHADER_PIPELINE_STATE_DESC
{
    ID3D12RootSignature* pRootSignature;
    D3D12_SHADER_BYTECODE         AS;
    D3D12_SHADER_BYTECODE         MS;
    D3D12_SHADER_BYTECODE         PS;
    D3D12_BLEND_DESC              BlendState;
    UINT                          SampleMask;
    D3D12_RASTERIZER_DESC         RasterizerState;
    D3D12_DEPTH_STENCIL_DESC      DepthStencilState;
    D3D12_PRIMITIVE_TOPOLOGY_TYPE PrimitiveTopologyType;
    UINT                          NumRenderTargets;
    DXGI_FORMAT                   RTVFormats[D3D12_SIMULTANEOUS_RENDER_TARGET_COUNT];
    DXGI_FORMAT                   DSVFormat;
    DXGI_SAMPLE_DESC              SampleDesc;
    UINT                          NodeMask;
    D3D12_CACHED_PIPELINE_STATE   CachedPSO;
    D3D12_PIPELINE_STATE_FLAGS    Flags;
};
```

## <a name="members"></a>Membres

`pRootSignature`

Type : **[ID3D12RootSignature](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)\***

Objet de signature racine définissant les ressources qui sont liées au pipeline.

`AS`

Type : **[D3D12_SHADER_BYTECODE](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**

Contient les données représentant le programme du nuanceur d’amplification.

`MS`

Type : **[D3D12_SHADER_BYTECODE](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**

Contient les données représentant le programme de nuanceur de maillage.

`PS`

Type : **[D3D12_SHADER_BYTECODE](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**

Contient les données représentant le programme de nuanceur de pixels.

`BlendState`

Type : **[D3D12_BLEND_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_blend_desc)**

Décrit l’état de fusion.

`SampleMask`

Type : **[uint](/windows/win32/winprog/windows-data-types)**

Exemple de masque pour l’état de fusion.

`RasterizerState`

Type : **[D3D12_RASTERIZER_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)**

Décrit l’état du rastériseur.

`DepthStencilState`

Type : **[D3D12_DEPTH_STENCIL_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)**

Décrit l’état du gabarit de profondeur.

`PrimitiveTopologyType`

Type : **[D3D12_PRIMITIVE_TOPOLOGY_TYPE](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)**

Décrit le type et l’ordre des données Primitives.

`NumRenderTargets`

Type : **[uint](/windows/win32/winprog/windows-data-types)**

Nombre de formats de cible de rendu dans le membre *RTVFormats* .

`RTVFormats`

Type : **[DXGI_FORMAT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Tableau de valeurs pour les formats de cible de rendu.

`DSVFormat`

Type : **[DXGI_FORMAT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Valeur pour le format de stencil de profondeur.

`SampleDesc`

Type : **[DXGI_SAMPLE_DESC](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Spécifie les paramètres d’échantillonnage multiple.

`CachedPSO`

Type : **[D3D12_CACHED_PIPELINE_STATE](/windows/win32/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)**

Objet d’état de pipeline mis en cache. *pCachedBlob* et *CachedBlobSizeInBytes* peuvent avoir respectivement la valeur null et la valeur 0.

`Flags`

Type : **[D3D12_PIPELINE_STATE_FLAGS](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)**

Constante d’énumération d’indicateur (par exemple, pour indiquer que l’état du pipeline doit être compilé avec des informations supplémentaires pour faciliter le débogage).

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Voir aussi

* [Structures d’assistance pour Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_PIPELINE_STATE_STREAM2](cd3dx12-pipeline-state-stream1.md)
* [nuanceurs de maille/amplifications](https://microsoft.github.io/DirectX-Specs/d3d/MeshShader.html)
* [EffectPipelineStateDescription](https://github.com/Microsoft/DirectXTK12/wiki/EffectPipelineStateDescription)
