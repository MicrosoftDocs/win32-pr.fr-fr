---
title: Structure CD3DX12_PIPELINE_STATE_STREAM1 (D3dx12. h)
description: Structure d’assistance pour la création et l’utilisation des graphiques et des États de pipeline de calcul via une interface combinée. Consultez [D3D12_GRAPHICS_PIPELINE_STATE_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) et [D3D12_COMPUTE_PIPELINE_STATE_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).
ms.assetid: 4D3E4D99-E820-4220-92F3-4924791E780F
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM1
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e56422aeb9b6f1c0bb87b31960b21068e75bd70d
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520448"
---
# <a name="cd3dx12_pipeline_state_stream1-structure"></a>Structure CD3DX12_PIPELINE_STATE_STREAM1

Structure d’assistance pour la création et l’utilisation des graphiques et des États de pipeline de calcul via une interface combinée. Consultez [D3D12_GRAPHICS_PIPELINE_STATE_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) et [D3D12_COMPUTE_PIPELINE_STATE_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

CD3DX12_PIPELINE_STATE_STREAM1 prend en charge la Windows 10 Fall Creators Update avec de nouvelles fonctionnalités telles que l’instanciation de vues.

Consultez [CD3DX12_PIPELINE_STATE_STREAM2](cd3dx12-pipeline-state-stream2.md) pour la prise en charge de la version de système d’exploitation 19041 + (où se trouve un pipeline de nuanceur de maille).

## <a name="syntax"></a>Syntaxe

```C++
struct CD3DX12_PIPELINE_STATE_STREAM1 {
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1();
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc);
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc);
  D3D12_GRAPHICS_PIPELINE_STATE_DESC                  GraphicsDescV0();
  D3D12_COMPUTE_PIPELINE_STATE_DESC                   ComputeDescV0();
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS                 Flags;
  CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK             NodeMask;
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE        pRootSignature;
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT          InputLayout;
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE    IBStripCutValue;
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY    PrimitiveTopologyType;
  CD3DX12_PIPELINE_STATE_STREAM_VS                    VS;
  CD3DX12_PIPELINE_STATE_STREAM_GS                    GS;
  CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT         StreamOutput;
  CD3DX12_PIPELINE_STATE_STREAM_HS                    HS;
  CD3DX12_PIPELINE_STATE_STREAM_DS                    DS;
  CD3DX12_PIPELINE_STATE_STREAM_PS                    PS;
  CD3DX12_PIPELINE_STATE_STREAM_CS                    CS;
  CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC            BlendState;
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1        DepthStencilState;
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT  DSVFormat;
  CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER            RasterizerState;
  CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS RTVFormats;
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC           SampleDesc;
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK           SampleMask;
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO            CachedPSO;
};
```

## <a name="members"></a>Membres

<dl> <dt>

**CD3DX12_PIPELINE_STATE_STREAM1 ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un CD3DX12_PIPELINE_STATE_STREAM1.

</dd> <dt>

**CD3DX12_PIPELINE_STATE_STREAM1 (const D3D12_GRAPHICS_PIPELINE_STATE_DESC& DESC)**
</dt> <dd>

Crée une nouvelle instance d’un CD3DX12_PIPELINE_STATE_STREAM1, initialisée avec les valeurs copiées à partir d’une structure **CD3DX12_PIPELINE_STATE_STREAM1** .

</dd> <dt>

**CD3DX12_PIPELINE_STATE_STREAM1 (const D3D12_COMPUTE_PIPELINE_STATE_DESC& DESC)**
</dt> <dd>

Crée une nouvelle instance d’un CD3DX12_PIPELINE_STATE_STREAM1, initialisée avec les valeurs copiées à partir d’une structure **CD3DX12_PIPELINE_STATE_STREAM1** .

</dd> <dt>

**GraphicsDescV0()**
</dt> <dd>

retourne le contenu de l’objet CD3DX12_PIPELINE_STATE_STREAM1 sous forme de D3D12_GRAPHICS_PIPELINE_STATE_DESC structure par valeur. Notez que D3D12_GRAPHICS_PIPELINE_STATE_DESC n’inclut pas le membre **CS** , donc cette valeur est perdue lors de la conversion.

</dd> <dt>

**ComputeDescV0()**
</dt> <dd>

retourne le contenu de l’objet CD3DX12_PIPELINE_STATE_STREAM1 sous forme de D3D12_COMPUTE_PIPELINE_STATE_DESC structure par valeur. Notez que D3D12_COMPUTE_PIPELINE_STATE_DESC n’inclut pas les membres **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **vs**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc** ou **SampleMask** , afin que ces valeurs soient perdues dans le convertisseur.

</dd> <dt>

**Indicateurs**
</dt> <dd>

Décrit les indicateurs d’État du pipeline, qui contrôlent les fonctionnalités telles que « outil de débogage ».

</dd> <dt>

**NodeMask**
</dt> <dd>

Décrit le masque de nœud d’état de pipeline, qui est utilisé pour identifier les nœuds (adaptateurs physiques du périphérique) auxquels le PSO s’applique dans les scénarios à plusieurs adaptateurs ; chaque bit du masque correspond à un nœud unique. Pour les scénarios à un seul adaptateur, définissez cette valeur sur 0.

</dd> <dt>

**pRootSignature**
</dt> <dd>

Décrit la signature racine.

</dd> <dt>

**InputLayout**
</dt> <dd>

Décrit le format de mémoire tampon d’entrée pour l’étape assembleur d’entrée

</dd> <dt>

**IBStripCutValue**
</dt> <dd>

Décrit la valeur d’index spéciale de la mémoire tampon d’entrée qui indique une coupure (discontinuation) lors de l’utilisation de la topologie de la bande triangulaire.

</dd> <dt>

**PrimitiveTopologyType**
</dt> <dd>

Décrit la topologie primitive et son ordre.

</dd> <dt>

**COMPARATIF**
</dt> <dd>

Décrit le nuanceur de sommets.

</dd> <dt>

**GS**
</dt> <dd>

Décrit le nuanceur Geometry.

</dd> <dt>

**StreamOutput**
</dt> <dd>

Décrit la mémoire tampon de sortie de diffusion en continu.

</dd> <dt>

**HS**
</dt> <dd>

Décrit le nuanceur de coque.

</dd> <dt>

**Source de données**
</dt> <dd>

Décrit le nuanceur de domaine.

</dd> <dt>

**ALIMENTATION**
</dt> <dd>

Décrit le nuanceur de pixels.

</dd> <dt>

**CS**
</dt> <dd>

Décrit le nuanceur de calcul.

</dd> <dt>

**BlendState**
</dt> <dd>

Décrit l’état de fusion.

</dd> <dt>

**DepthStencilState**
</dt> <dd>

Décrit l’état du gabarit de profondeur.

</dd> <dt>

**DSVFormat**
</dt> <dd>

Décrit le format de stencil de profondeur.

</dd> <dt>

**RasterizerState**
</dt> <dd>

Décrit l’état du rastériseur.

</dd> <dt>

**RTVFormats**
</dt> <dd>

Décrit les formats de la cible de rendu.

</dd> <dt>

**SampleDesc**
</dt> <dd>

Décrit le nombre d’échantillons et la qualité.

</dd> <dt>

**SampleMask**
</dt> <dd>

Décrit l’exemple de masque utilisé avec l’état de fusion.

</dd> <dt>

**CachedPSO**
</dt> <dd>

Décrit un PSO mis en cache.

</dd> </dl>

## <a name="remarks"></a>Remarques

[CD3DX12_PIPELINE_STATE_STREAM](cd3dx12-pipeline-state-stream.md) prend en charge le Windows 10 Fall Creators Update, mais ne prend pas en charge les types de sous-objets ajoutés dans Windows 10 mise à jour des créateurs de automne, par exemple pour l’instanciation de vues. Pour prendre en charge les nouveaux types de sous-objet, utilisez **CD3DX12_PIPELINE_STATE_STREAM1** à la place.

Les variables membres accessibles de cette structure sont tous les typedefs du modèle [**CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT**](./cd3dx12-pipeline-state-stream-subobject.md) , qui combine le marqueur de type de sous-objet et les données de sous-objet dans un objet unique approprié pour une description de flux.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Voir aussi

* [Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
* [**CD3DX12_PIPELINE_STATE_STREAM**](cd3dx12-pipeline-state-stream.md)
* [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
* [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
