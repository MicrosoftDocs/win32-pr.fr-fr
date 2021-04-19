---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER (D3dx12. h)
description: Génère un \_ \_ \_ objet de flux d’état de pipeline CD3DX12 interne à partir des détails de sous-objet passés dans les fonctions membres correspondantes. Ce struct implémente l’interface ID3DX12PipelineParserCallbacks.
ms.assetid: 7D4FFD1D-9FA3-4482-A67B-E742611030BC
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44cc6228f690abd677e1adc8552293e440452ec5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529595"
---
# <a name="cd3dx12_pipeline_state_stream_parse_helper-structure"></a>\_ \_ \_ \_ \_ Structure d’assistance d’analyse du flux d’État du pipeline CD3DX12

Génère un \_ \_ \_ objet de flux d’état de pipeline CD3DX12 interne à partir des détails de sous-objet passés dans les fonctions membres correspondantes. Ce struct implémente l’interface [**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER  : public ID3DX12PipelineParserCallbacks{
  CD3DX12_PIPELINE_STATE_STREAM1 PipelineStream;
  void                           FlagsCb(D3D12_PIPELINE_STATE_FLAGS Flags);
  void                           NodeMaskCb(UINT NodeMask);
  void                           RootSignatureCb(ID3D12RootSignature* pRootSignature);
  void                           InputLayoutCb(const D3D12_INPUT_LAYOUT_DESC& InputLayout);
  void                           IBStripCutValueCb(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE IBStripCutValue);
  void                           PrimitiveTopologyTypeCb(D3D12_PRIMITIVE_TOPOLOGY_TYPE PrimitiveTopologyType);
  void                           VSCb(const D3D12_SHADER_BYTECODE& VS);
  void                           GSCb(const D3D12_SHADER_BYTECODE& GS);
  void                           StreamOutputCb(const D3D12_STREAM_OUTPUT_DESC& StreamOutput);
  void                           HSCb(const D3D12_SHADER_BYTECODE& HS);
  void                           DSCb(const D3D12_SHADER_BYTECODE& DS);
  void                           PSCb(const D3D12_SHADER_BYTECODE& PS);
  void                           CSCb(const D3D12_SHADER_BYTECODE& CS);
  void                           BlendStateCb(const D3D12_BLEND_DESC& BlendState);
  void                           DepthStencilStateCb(const D3D12_DEPTH_STENCIL_DESC& DepthStencilState);
  void                           DepthStencilState1Cb(const D3D12_DEPTH_STENCIL_DESC1& DepthStencilState);
  void                           DSVFormatCb(DXGI_FORMAT DSVFormat);
  void                           RasterizerStateCb(const D3D12_RASTERIZER_DESC& RasterizerState);
  void                           RTVFormatsCb(const D3D12_RT_FORMAT_ARRAY& RTVFormats);
  void                           SampleDescCb(const DXGI_SAMPLE_DESC& SampleDesc);
  void                           SampleMaskCb(UINT SampleMask);
  void                           ViewInstancingCb(const D3D12_VIEW_INSTANCING_DESC& ViewInstancingDesc);
  void                           CachedPSOCb(const D3D12_CACHED_PIPELINE_STATE& CachedPSO);
  void                           ErrorBadInputParameter(UINT);
  void                           ErrorDuplicateSubobject(D3D12_PIPELINE_STATE_SUBOBJECT_TYPE);
  void                           ErrorUnknownSubobject(UINT);
};
```



## <a name="members"></a>Membres

<dl> <dt>

**PipelineStream**
</dt> <dd>

L’état interne du [**\_ pipeline CD3DX12 \_ \_ STREAM1**](cd3dx12-pipeline-state-stream1.md). Son état actuel représente l’effet cumulatif des méthodes de rappel qui ont été appelées sur cet objet.

</dd> <dt>

**FlagsCb ( \_ indicateurs d’indicateurs d’état de pipeline D3D12 \_ \_ )**
</dt> <dd>

Initialise le membre **Flags** de **PipelineStream** à l’aide de la valeur du paramètre *Flags* .

</dd> <dt>

**NodeMaskCb (UINT NodeMask)**
</dt> <dd>

Initialise le membre **NodeMask** de **PipelineStream** à l’aide de la valeur du paramètre *NodeMask* .

</dd> <dt>

**RootSignatureCb (ID3D12RootSignature \* pRootSignature)**
</dt> <dd>

Initialise le membre **pRootSignature** de **PipelineStream** à l’aide de la valeur du paramètre *pRootSignature* .

</dd> <dt>

**InputLayoutCb (const D3D12 \_ disposition d’entrée \_ \_ desc& InputLayout)**
</dt> <dd>

Initialise le membre **InputLayout** de **PipelineStream** à l’aide de la valeur du paramètre *InputLayout* .

</dd> <dt>

**IBStripCutValueCb (valeur de coupe de la bande de la \_ mémoire tampon d’index D3D12 \_ \_ \_ \_ IBStripCutValue)**
</dt> <dd>

Initialise le membre **IBStripCutValue** de **PipelineStream** à l’aide de la valeur du paramètre *IBStripCutValue* .

</dd> <dt>

**PrimitiveTopologyTypeCb ( \_ type de topologie D3D12 primitif \_ \_ PrimitiveTopologyType)**
</dt> <dd>

Initialise le membre **PrimitiveTopologyType** de **PipelineStream** à l’aide de la valeur du paramètre *PrimitiveTopologyType* .

</dd> <dt>

**VSCb (pseudo-code de nuanceur const D3D12 \_ \_& vs)**
</dt> <dd>

Initialise le membre **vs** (vertex shader) de **PipelineStream** à l’aide de la valeur du paramètre *vs* .

</dd> <dt>

**GSCb (code de nuanceur const D3D12 \_ \_& GS)**
</dt> <dd>

Initialise le membre **GS** (Geometry Shader) de **PipelineStream** à l’aide de la valeur du paramètre *GS* .

</dd> <dt>

**StreamOutputCb (const D3D12 \_ flux de \_ sortie \_ desc& StreamOutput)**
</dt> <dd>

Initialise le membre **StreamOutput** de **PipelineStream** à l’aide de la valeur du paramètre *StreamOutput* .

</dd> <dt>

**HSCb (code de nuanceur const D3D12 \_ \_& HS)**
</dt> <dd>

Initialise le membre **HS** (coque Shader) de **PipelineStream** à l’aide de la valeur du paramètre *HS* .

</dd> <dt>

**DSCb (code de nuanceur const D3D12 \_ \_& DS)**
</dt> <dd>

Initialise le membre **DS** (Domain Shader) de **PipelineStream** à l’aide de la valeur du paramètre *DS* .

</dd> <dt>

**PSCb (code de nuanceur const D3D12 \_ \_& PS)**
</dt> <dd>

Initialise le membre **PS** (Pixel Shader) de **PipelineStream** à l’aide de la valeur du paramètre *PS* .

</dd> <dt>

**CSCb (code de nuanceur const D3D12 \_ \_& CS)**
</dt> <dd>

Initialise le membre **CS** de **PipelineStream** à l’aide de la valeur du paramètre *CS* .

</dd> <dt>

**BlendStateCb (const D3D12 \_ Blend \_ desc& BlendState)**
</dt> <dd>

Initialise le membre **BlendState** de **PipelineStream** à l’aide de la valeur du paramètre *BlendState* .

</dd> <dt>

**DepthStencilStateCb (const D3D12 \_ \_ Description du stencil \_& DepthStencilState)**
</dt> <dd>

Initialise le membre **DepthStencilState** de **PipelineStream** à l’aide de la valeur du paramètre *DepthStencilState* , [**une \_ \_ \_ Description du stencil de profondeur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc).

</dd> <dt>

**DepthStencilState1Cb (const D3D12 \_ Depth \_ STENCIL \_ DESC1& DepthStencilState)**
</dt> <dd>

Initialise le membre **DepthStencilState** de **PipelineStream** à l’aide de la valeur du paramètre *DepthStencilState* , un [**stencil de profondeur D3D12 \_ \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1).

</dd> <dt>

**DSVFormatCb (DXGI \_ format DSVFormat)**
</dt> <dd>

Initialise le membre **DSVFormat** de **PipelineStream** à l’aide de la valeur du paramètre *DSVFormat* .

</dd> <dt>

**RasterizerStateCb (const D3D12 \_ rastériseur \_ desc& RasterizerState)**
</dt> <dd>

Initialise le membre **RasterizerState** de **PipelineStream** à l’aide de la valeur du paramètre *RasterizerState* .

</dd> <dt>

**RTVFormatsCb (const D3D12 \_ RT \_ FORMAT \_ tableau& RTVFormats)**
</dt> <dd>

Initialise le membre **RTVFormats** de **PipelineStream** à l’aide de la valeur du paramètre *RTVFormats* .

</dd> <dt>

**SampleDescCb (const DXGI \_ \_ , exemple DESC& SampleDesc)**
</dt> <dd>

Initialise le membre **SampleDesc** de **PipelineStream** à l’aide de la valeur du paramètre *SampleDesc* .

</dd> <dt>

**SampleMaskCb (UINT SampleMask)**
</dt> <dd>

Initialise le membre **SampleMask** de **PipelineStream** à l’aide de la valeur du paramètre *SampleMask* .

</dd> <dt>

**ViewInstancingCb (const D3D12 \_ View \_ INSTANCING \_ desc& ViewInstancingDesc)**
</dt> <dd>

Initialise le membre **ViewInstancingDesc** de **PipelineStream** à l’aide de la valeur du paramètre *ViewInstancingDesc* .

</dd> <dt>

**CachedPSOCb (const D3D12 \_ État du \_ pipeline mis en cache \_& CachedPSO)**
</dt> <dd>

Initialise le membre **CachedPSO** de **PipelineStream** à l’aide de la valeur du paramètre *CachedPSO* .

</dd> <dt>

**ErrorBadInputParameter (UINT)**
</dt> <dd>

Ne fait rien.

</dd> <dt>

**ErrorDuplicateSubobject ( \_ type de \_ sous-objet état du pipeline D3D12 \_ \_ )**
</dt> <dd>

Ne fait rien.

</dd> <dt>

**ErrorUnknownSubobject (UINT)**
</dt> <dd>

Ne fait rien.

</dd> </dl>

## <a name="remarks"></a>Notes

Lorsqu’il est passé en tant que deuxième paramètre à la fonction [**D3DX12ParsePipelineStream**](d3dx12parsepipelinestream.md) , les détails de l’objet STREAM1 interne de l' [**\_ \_ état \_ du pipeline CD3DX12**](cd3dx12-pipeline-state-stream1.md) sont clonés à partir du flux de données d' [**\_ État du pipeline \_ \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) passé comme premier paramètre. Ce processus valide la description du flux source. Si D3DX12ParsePipelineStream retourne la valeur **\_ OK**, la description du flux source et les **STREAM1PipelineStream d' \_ \_ État de \_ pipeline CD3DX12** résultants sont valides ; sinon, les deux ne sont pas valides. Les flux non valides et les autres erreurs sont signalés uniquement via la valeur de retour de D3DX12ParsePipelineStream ; Cette structure implémente les rappels d’erreur pour ne rien faire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’assistance pour Direct3D 12](helper-structures-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





