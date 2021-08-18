---
title: Structure CD3DX12_PIPELINE_STATE_STREAM (D3dx12. h)
description: Structure d’assistance pour la création et l’utilisation des graphiques et des États de pipeline de calcul via une interface combinée. Consultez D3D12 \_ Graphics \_ pipeline \_ State \_ DESC et D3D12 \_ Compute \_ pipeline \_ State \_ desc. | Structure CD3DX12_PIPELINE_STATE_STREAM (D3dx12. h)
ms.assetid: C0CEFC67-72B3-4A8D-9C88-381990FC9898
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95e45c46c39a21aaeb53a2980fa3c082947e92cd5bb4ab3eccbbb225001a6504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733981"
---
# <a name="cd3dx12_pipeline_state_stream-structure"></a>\_Structure du \_ flux d’État du PIPELINe CD3DX12 \_

Structure d’assistance pour la création et l’utilisation des graphiques et des États de pipeline de calcul via une interface combinée. Consultez [**D3D12 \_ Graphics \_ pipeline \_ State \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) et [**D3D12 \_ Compute \_ pipeline \_ State \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

\_ \_ le flux d’état du pipeline CD3DX12 \_ prend en charge Windows 10 Creators Update et versions ultérieures, mais ne prend pas en charge les nouvelles fonctionnalités de la mise à jour des créateurs de automne, comme l’instanciation Pour prendre en charge les fonctionnalités de la mise à jour des créateurs de automne, utilisez à la place [**CD3DX12 \_ pipeline \_ State \_ STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM {
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM();
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc);
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc);
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

**\_Flux d’État du pipeline CD3DX12 \_ \_ ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ flux d’état de pipeline CD3DX12 \_ \_ .

</dd> <dt>

**\_Flux d’État du pipeline CD3DX12 \_ \_ (const D3D12 \_ Graphics \_ pipeline \_ State \_ desc& DESC)**
</dt> <dd>

Crée une nouvelle instance d’un \_ flux d’état de pipeline CD3DX12 \_ \_ , initialisée avec les valeurs copiées à partir d’une structure de flux d' **\_ \_ état \_ de pipeline CD3DX12** .

</dd> <dt>

**\_Flux d’État du pipeline CD3DX12 \_ \_ (const D3D12 \_ Compute \_ pipeline \_ State \_ desc& DESC)**
</dt> <dd>

Crée une nouvelle instance d’un \_ flux d’état de pipeline CD3DX12 \_ \_ , initialisée avec les valeurs copiées à partir d’une structure de flux d' **\_ \_ état \_ de pipeline CD3DX12** .

</dd> <dt>

**GraphicsDescV0()**
</dt> <dd>

retourne le contenu de l' \_ objet de flux d’état de pipeline CD3DX12 \_ \_ en tant que \_ structure DESC d’état de pipeline D3D12 Graphics \_ \_ \_ par valeur. Notez que la \_ \_ Description de l’état du pipeline Graphics D3D12 \_ \_ n’inclut pas le membre **CS** , donc cette valeur est perdue lors de la conversion.

</dd> <dt>

**ComputeDescV0()**
</dt> <dd>

retourne le contenu de l' \_ objet de flux d’État du pipeline CD3DX12 \_ \_ en tant que \_ structure DESC de l’état du pipeline de calcul D3D12 \_ \_ \_ par valeur. Notez que la \_ Description de \_ l’état du pipeline de calcul D3D12 \_ \_ n’inclut pas les membres **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **vs**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc** ou **SampleMask** . par conséquent, ces valeurs sont perdues lors de la conversion.

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

**SH**
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

le \_ flux d’état du pipeline CD3DX12 \_ \_ prend en charge Windows 10 Creators Update et versions ultérieures, mais ne prend pas en charge les types de sous-objets ajoutés dans Windows 10 mise à jour des créateurs de automne, par exemple pour l’instanciation de vues. Pour prendre en charge les types de sous-objets ajoutés à la mise à jour des créateurs de automne, utilisez à la place [**CD3DX12 \_ pipeline \_ State \_ STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) .

Les variables membres accessibles de cette structure sont tous les typedefs du \_ modèle de sous-objet de flux d’État du pipeline CD3DX12 \_ \_ \_ , qui combine le marqueur de type de sous-objet et les données de sous-objet dans un objet unique approprié pour une description de flux.

Ces typedefs sont les suivants :

<dl> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**\_État du pipeline CD3DX12 \_ \_ STREAM1**](cd3dx12-pipeline-state-stream1.md)
</dt> <dt>

[**Description de l' \_ \_ État du pipeline GRAPHICs D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[**\_Description de l' \_ État du pipeline de calcul D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 





