---
title: Méthode ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12. h)
description: Appelle le rappel de sous-objet d’État du stencil de profondeur d’un objet qui implémente cette interface.
ms.assetid: 6E77A3B7-20D8-4D31-9D31-515CF4618157
keywords:
- Méthode DepthStencilStateCb
- Méthode DepthStencilStateCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode DepthStencilStateCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1086156fcaa6b8736c049c93bacc5dfd1f5e915ba8a7006b3c71e654ba65f52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894579"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h"></a>Méthode ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12. h)

Appelle le rappel de sous-objet d’État du stencil de profondeur d’un objet qui implémente cette interface.

## <a name="syntax"></a>Syntaxe


```C++
void DepthStencilStateCb(
  [ref] const D3D12_DEPTH_STENCIL_DESC &DepthStencilState
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DepthStencilState* \[ Réf\]
</dt> <dd>

Type : **const [**D3D12 de \_ profondeur du \_ stencil \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)**

Détails du sous-objet état du stencil de profondeur analysé à partir d’un flux d’État du pipeline.

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

[**\_Description du \_ stencil de profondeur D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





