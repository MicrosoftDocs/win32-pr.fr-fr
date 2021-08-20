---
title: Structure CD3DX12_PIPELINE_STATE_STREAM2 (D3dx12. h)
description: Structure d’assistance pour la création et l’utilisation des graphiques et des États de pipeline de calcul via une interface combinée.
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM2
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM2
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/03/2021
ms.openlocfilehash: 18b662217f5e2a59c7925e0f401a9288ea710e8a
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812333"
---
# <a name="cd3dx12_pipeline_state_stream2-structure"></a>Structure CD3DX12_PIPELINE_STATE_STREAM2

Structure d’assistance pour la création et l’utilisation des graphiques et des États de pipeline de calcul via une interface combinée. Consultez [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) et [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

**CD3DX12_PIPELINE_STATE_STREAM2** prend en charge la version du système d’exploitation 19041 + (où il y a un pipeline de nuanceur de maille).

## <a name="syntax"></a>Syntaxe

```cpp
struct CD3DX12_PIPELINE_STATE_STREAM2
{
    CD3DX12_PIPELINE_STATE_STREAM2();
    CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc) noexcept;
    CD3DX12_PIPELINE_STATE_STREAM2(const D3DX12_MESH_SHADER_PIPELINE_STATE_DESC& Desc) noexcept;
    CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc) noexcept;
    CD3DX12_PIPELINE_STATE_STREAM_FLAGS Flags;
    CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK NodeMask;
    CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE pRootSignature;
    CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT InputLayout;
    CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE IBStripCutValue;
    CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY PrimitiveTopologyType;
    CD3DX12_PIPELINE_STATE_STREAM_VS VS;
    CD3DX12_PIPELINE_STATE_STREAM_GS GS;
    CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT StreamOutput;
    CD3DX12_PIPELINE_STATE_STREAM_HS HS;
    CD3DX12_PIPELINE_STATE_STREAM_DS DS;
    CD3DX12_PIPELINE_STATE_STREAM_PS PS;
    CD3DX12_PIPELINE_STATE_STREAM_AS AS;
    CD3DX12_PIPELINE_STATE_STREAM_MS MS;
    CD3DX12_PIPELINE_STATE_STREAM_CS CS;
    CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC BlendState;
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 DepthStencilState;
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT DSVFormat;
    CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER RasterizerState;
    CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS RTVFormats;
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC SampleDesc;
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK SampleMask;
    CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO CachedPSO;
    CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING ViewInstancingDesc;
    D3D12_GRAPHICS_PIPELINE_STATE_DESC GraphicsDescV0() const noexcept;
    D3D12_COMPUTE_PIPELINE_STATE_DESC ComputeDescV0() const noexcept;
};
```

## <a name="members"></a>Membres

`CD3DX12_PIPELINE_STATE_STREAM2`

Constructeur par défaut. Crée une nouvelle instance non initialisée d’un **CD3DX12_PIPELINE_STATE_STREAM2**.

`CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_GRAPHICS_PIPELINE_STATE_DESC&)`

Constructeur qui crée une nouvelle instance d’un **CD3DX12_PIPELINE_STATE_STREAM2** initialisé avec le contenu d’une structure [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) .

Vous devez ensuite définir les nuanceurs de maillage et d’amplification manuellement, car ils n’ont pas de représentation dans **D3D12_GRAPHICS_PIPELINE_STATE_DESC**.

`CD3DX12_PIPELINE_STATE_STREAM2(const D3DX12_MESH_SHADER_PIPELINE_STATE_DESC&)`

Constructeur qui crée une nouvelle instance d’un **CD3DX12_PIPELINE_STATE_STREAM2** initialisé avec le contenu d’une structure [**D3DX12_MESH_SHADER_PIPELINE_STATE_DESC**](d3dx12-mesh-shader-pipeline-state-desc.md) .

`CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_COMPUTE_PIPELINE_STATE_DESC&)`

Constructeur qui crée une nouvelle instance d’un **CD3DX12_PIPELINE_STATE_STREAM2** initialisé avec le contenu d’une structure [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc) .

`Flags`

Type : **[CD3DX12_PIPELINE_STATE_STREAM_FLAGS](cd3dx12-pipeline-state-stream-flags.md)**

Indicateurs (par exemple, pour indiquer que l’état du pipeline doit être compilé avec des informations supplémentaires pour faciliter le débogage).

`NodeMask`

Type : **[CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK](cd3dx12-pipeline-state-stream-node-mask.md)**

Décrit le masque de nœud d’état de pipeline, qui est utilisé pour identifier les nœuds (adaptateurs physiques du périphérique) auxquels le PSO s’applique dans les scénarios à plusieurs adaptateurs ; chaque bit du masque correspond à un nœud unique. Pour les scénarios à un seul adaptateur, utilisez 0.

`pRootSignature`

Type : **[CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE](cd3dx12-pipeline-state-stream-root-signature.md)**

Décrit la signature racine.

`InputLayout`

Type : **[CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT](cd3dx12-pipeline-state-stream-input-layout.md)**

Décrit le format de mémoire tampon d’entrée pour l’étape assembleur d’entrée

`IBStripCutValue`

Type : **[CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md)**

Décrit la valeur d’index spéciale de la mémoire tampon d’entrée qui indique une coupure (discontinuation) lors de l’utilisation de la topologie de la bande triangulaire.

`PrimitiveTopologyType`

Type : **[CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY](cd3dx12-pipeline-state-stream-primitive-topology.md)**

Décrit la topologie primitive et son ordre.

`VS`

Type : **[CD3DX12_PIPELINE_STATE_STREAM_VS](cd3dx12-pipeline-state-stream-vs.md)**

Décrit le nuanceur de sommets.

`GS`

Type : **[CD3DX12_PIPELINE_STATE_STREAM_GS](cd3dx12-pipeline-state-stream-gs.md)**

Décrit le nuanceur Geometry.

`StreamOutput`

Type : **[CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT](cd3dx12-pipeline-state-stream-stream-output.md)**

Décrit la mémoire tampon de sortie de diffusion en continu.

`HS`

Type : **[CD3DX12_PIPELINE_STATE_STREAM_HS](cd3dx12-pipeline-state-stream-hs.md)**

Décrit le nuanceur de coque.

`DS`

Type : **[CD3DX12_PIPELINE_STATE_STREAM_DS](cd3dx12-pipeline-state-stream-ds.md)**

Décrit le nuanceur de domaine.

`PS`

Type : **[CD3DX12_PIPELINE_STATE_STREAM_PS](cd3dx12-pipeline-state-stream-ps.md)**

Décrit le nuanceur de pixels.

`AS`

Type : **CD3DX12_PIPELINE_STATE_STREAM_AS**

Décrit le nuanceur d’amplification.

`MS`

Type : **CD3DX12_PIPELINE_STATE_STREAM_MS**

Décrit le nuanceur de maille.

`CS`

Type : **[CD3DX12_PIPELINE_STATE_STREAM_CS](cd3dx12-pipeline-state-stream-cs.md)**

Décrit le nuanceur de calcul.

`BlendState`

Type : **[CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC](cd3dx12-pipeline-state-stream-blend-desc.md)**

Décrit l’état de fusion.

`DepthStencilState`

Type : **[CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1](cd3dx12-pipeline-state-stream-depth-stencil1.md)**

Décrit l’état du gabarit de profondeur.

`DSVFormat`

Type : **[CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT](cd3dx12-pipeline-state-stream-depth-stencil-format.md)**

Décrit le format de stencil de profondeur.

`RasterizerState`

Type : **[CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER](cd3dx12-pipeline-state-stream-rasterizer.md)**

Décrit l’état du rastériseur.

`RTVFormats`

Type : **[CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS](cd3dx12-pipeline-state-stream-render-target-formats.md)**

Décrit les formats de la cible de rendu.

`SampleDesc`

Type : **[CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC](cd3dx12-pipeline-state-stream-sample-desc.md)**

Décrit le nombre d’échantillons et la qualité.

`SampleMask`

Type : **[CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK](cd3dx12-pipeline-state-stream-sample-mask.md)**

Décrit l’exemple de masque utilisé avec l’état de fusion.

`CachedPSO`

Type : **[CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO](cd3dx12-pipeline-state-stream-cached-pso.md)**

Décrit un PSO mis en cache.

`ViewInstancingDesc`

Type : **[CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING](cd3dx12-pipeline-state-stream-view-instancing.md)**

Décrit une configuration d’instanciation de vues.

`GraphicsDescV0`

Retourne [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc).

retourne le contenu de l’objet **CD3DX12_PIPELINE_STATE_STREAM2** sous forme de **D3D12_GRAPHICS_PIPELINE_STATE_DESC** structure par valeur. **D3D12_GRAPHICS_PIPELINE_STATE_DESC** n’inclut pas le membre *CS* , de sorte que la valeur est perdue lors de la conversion.

`ComputeDescV0`

Retourne [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

retourne le contenu de l’objet **CD3DX12_PIPELINE_STATE_STREAM2** sous forme de **D3D12_COMPUTE_PIPELINE_STATE_DESC** structure par valeur. **D3D12_COMPUTE_PIPELINE_STATE_DESC** n’inclut pas les membres *InputLayout*, *IBStripCutValue*, *PrimitiveTopologyType*, *vs*, *GS*, *StreamOutput*, *HS*, *DS*, *PS*, *BlendState*, *DepthStencilState*, *DSVFormat*, *RasterizerState*, *NumRootSignature*, *RTVFormats*, *SampleDesc* et *SampleMask*, par conséquent, ces valeurs sont perdues lors de la conversion.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Voir aussi

* [Structures d’assistance pour Direct3D 12](helper-structures-for-d3d12.md)
