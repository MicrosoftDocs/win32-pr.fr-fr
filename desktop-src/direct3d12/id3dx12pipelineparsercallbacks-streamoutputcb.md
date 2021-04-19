---
title: Méthode ID3DX12PipelineParserCallbacks StreamOutputCb (D3DX12. h)
description: Appelle le rappel de sortie de flux de sous-objet d’un objet qui implémente cette interface.
ms.assetid: 93447ABE-A942-4562-A532-600EC63072DA
keywords:
- Méthode StreamOutputCb
- Méthode StreamOutputCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode StreamOutputCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.StreamOutputCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae32f084edd2b6af374aa9b1cac4e563ef8a2eb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535788"
---
# <a name="id3dx12pipelineparsercallbacksstreamoutputcb-method"></a>ID3DX12PipelineParserCallbacks :: StreamOutputCb, méthode

Appelle le rappel de sortie de flux de sous-objet d’un objet qui implémente cette interface.

## <a name="syntax"></a>Syntaxe


```C++
void StreamOutputCb(
  [ref] const D3D12_STREAM_OUTPUT_DESC &StreamOutput
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StreamOutput* \[ Réf\]
</dt> <dd>

Type : **const [**D3D12 \_ flux de \_ sortie \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)**

Détails du sous-objet de description de sortie de flux analysé à partir d’un flux d’état de pipeline.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur Nothing.

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

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[**Description de la \_ sortie du flux D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)
</dt> </dl>

 

 





