---
title: Interface ID3DX12PipelineParserCallbacks (D3DX12. h)
description: Interface qui représente une collection d’analyseurs et les rappels d’erreur utilisés par la fonction d’assistance D3DX12parsePipelineStream.
ms.assetid: CBC04D17-2E19-4755-B1CB-FC42BF5083E5
keywords:
- Interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, Description
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f83e0987009e60d5e207a9531cc4809f6cfcfbd5b50360a583df8cb0c01898f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733742"
---
# <a name="id3dx12pipelineparsercallbacks-interface"></a>Interface ID3DX12PipelineParserCallbacks

Interface qui représente une collection d’analyseurs et les rappels d’erreur utilisés par la fonction d’assistance [**D3DX12parsePipelineStream**](d3dx12parsepipelinestream.md) .

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX12PipelineParserCallbacks** possède ces méthodes.



| Méthode                                                                                    | Description                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BlendStateCb**](id3dx12pipelineparsercallbacks-blendstatecb.md)                       | Appelle le rappel de sous-objet de description de l’état de fusion d’un objet qui implémente cette interface.<br/>                                                                 |
| [**CachedPSOCb**](id3dx12pipelineparsercallbacks-cachedpsocb.md)                         | Appelle le rappel d’objet de sous-objet PSO mis en cache (objet d’état de pipeline) d’un objet qui implémente cette interface.<br/>                                                      |
| [**CSCb**](id3dx12pipelineparsercallbacks-cscb.md)                                       | Appelle le rappel du sous-objet de nuanceur de calcul d’un objet qui implémente cette interface.<br/>                                                                          |
| [**DepthStencilState1Cb**](id3dx12pipelineparsercallbacks-depthstencilstate1cb.md)       | Appelle l’état du stencil de profondeur ([**D3D12 \_ Depth \_ stencil \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) rappel de sous-objet d’un objet qui implémente cette interface.<br/> |
| [**DepthStencilStateCb**](id3dx12pipelineparsercallbacks-dsvformatcb.md)                 | Appelle le rappel de format de valeur de stencil de profondeur d’un objet qui implémente cette interface.<br/>                                                              |
| [**DepthStencilStateCb**](id3dx12pipelineparsercallbacks-depthstencilstatecb.md)         | Appelle le rappel de sous-objet d’État du stencil de profondeur d’un objet qui implémente cette interface.<br/>                                                                     |
| [**DSCb**](id3dx12pipelineparsercallbacks-dscb.md)                                       | Appelle le rappel de sous-objet de nuanceur de domaine d’un objet qui implémente cette interface.<br/>                                                                           |
| [**ErrorBadInputParameter**](id3dx12pipelineparsercallbacks-errorbadinputparameter.md)   | Appelle le rappel d’erreur de paramètre d’entrée incorrect d’un objet qui implémente cette interface.<br/>                                                                         |
| [**ErrorDuplicateSubobject**](id3dx12pipelineparsercallbacks-errorduplicatesubobject.md) | Appelle le rappel d’erreur de sous-objet dupliqué d’un objet qui implémente cette interface.<br/>                                                                         |
| [**ErrorUnknownSubobject**](id3dx12pipelineparsercallbacks-errorunknownsubobject.md)     | Appelle le rappel d’erreur de sous-objet inconnu d’un objet qui implémente cette interface.<br/>                                                                           |
| [**FlagsCb**](id3dx12pipelineparsercallbacks-flagscb.md)                                 | Appelle le rappel de sous-objet d’indicateurs d’un objet qui implémente cette interface.<br/>                                                                                   |
| [**GSCb**](id3dx12pipelineparsercallbacks-gscb.md)                                       | Appelle le rappel de sous-objet de nuanceur Geometry d’un objet qui implémente cette interface.<br/>                                                                         |
| [**HSCb**](id3dx12pipelineparsercallbacks-hscb.md)                                       | Appelle le rappel de sous-objet de nuanceur de coque d’un objet qui implémente cette interface.<br/>                                                                             |
| [**IBStripCutValueCb**](id3dx12pipelineparsercallbacks-ibstripcutvaluecb.md)             | Appelle le rappel de sous-objet de valeur de coupe de la mémoire tampon d’index d’un objet qui implémente cette interface.<br/>                                                            |
| [**InputLayoutCb**](id3dx12pipelineparsercallbacks-inputlayoutcb.md)                     | Appelle le rappel de sous-objet de la disposition d’entrée d’un objet qui implémente cette interface.<br/>                                                                            |
| [**NodemaskCb**](id3dx12pipelineparsercallbacks-nodemaskcb.md)                           | Appelle le rappel de sous-objet nodemask d’un objet qui implémente cette interface.<br/>                                                                                |
| [**PrimitiveTopologyTypeCb**](id3dx12pipelineparsercallbacks-primitivetopologytypecb.md) | Appelle le rappel de sous-objet de type de topologie primitif d’un objet qui implémente cette interface.<br/>                                                                 |
| [**PSCb**](id3dx12pipelineparsercallbacks-pscb.md)                                       | Appelle le rappel de sous-objet de nuanceur de pixels d’un objet qui implémente cette interface.<br/>                                                                            |
| [**RasterizerStateCb**](id3dx12pipelineparsercallbacks-rasterizerstatecb.md)             | Appelle le rappel de sous-objet de description de l’état de rastériseur d’un objet qui implémente cette interface.<br/>                                                            |
| [**RootSignatureCB**](id3dx12pipelineparsercallbacks-rootsignaturecb.md)                 | Appelle le rappel de sous-objet de signature racine d’un objet qui implémente cette interface.<br/>                                                                          |
| [**RTVFormatsCb**](id3dx12pipelineparsercallbacks-rtvformatscb.md)                       | Appelle le rappel de sous-objet du tableau de format de la cible de rendu d’un objet qui implémente cette interface.<br/>                                                              |
| [**SampleDescCb**](id3dx12pipelineparsercallbacks-sampledesccb.md)                       | Appelle l’exemple de rappel de sous-objet de description d’un objet qui implémente cette interface.<br/>                                                                      |
| [**SampleMaskCb**](id3dx12pipelineparsercallbacks-samplemaskcb.md)                       | Appelle l’exemple de rappel de sous-objet de masque d’un objet qui implémente cette interface.<br/>                                                                             |
| [**StreamOutputCb**](id3dx12pipelineparsercallbacks-streamoutputcb.md)                   | Appelle le rappel de sortie de flux de sous-objet d’un objet qui implémente cette interface.<br/>                                                               |
| [**VSCb**](id3dx12pipelineparsercallbacks-vscb.md)                                       | Appelle le rappel de sous-objet de nuanceur vertex d’un objet qui implémente cette interface.<br/>                                                                           |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX12. h</dt> </dl>  |
| Bibliothèque<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces d’assistance pour Direct3D 12](helper-interfaces-for-d3d12.md)
</dt> <dt>

[**D3DX12parsePipelineStream**](d3dx12parsepipelinestream.md)
</dt> </dl>

 

 





