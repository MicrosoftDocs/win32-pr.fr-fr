---
title: Méthode ID3DX12PipelineParserCallbacks InputLayoutCb (D3DX12. h)
description: Appelle le rappel de sous-objet de la disposition d’entrée d’un objet qui implémente cette interface.
ms.assetid: A21AB7A1-6E51-42CB-BA98-C0BD08D43009
keywords:
- Méthode InputLayoutCb
- Méthode InputLayoutCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode InputLayoutCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.InputLayoutCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0f7012686c85b38e94f8f3d2400cf406d614fc83ff0ba25e746ac0433b2e167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528771"
---
# <a name="id3dx12pipelineparsercallbacksinputlayoutcb-method"></a>ID3DX12PipelineParserCallbacks :: InputLayoutCb, méthode

Appelle le rappel de sous-objet de la disposition d’entrée d’un objet qui implémente cette interface.

## <a name="syntax"></a>Syntaxe


```C++
void InputLayoutCb(
  [ref] const D3D12_INPUT_LAYOUT_DESC &InputLayout
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*InputLayout* \[ Réf\]
</dt> <dd>

Type : **const [**D3D12 \_ disposition d’entrée \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)**

Détails du sous-objet de disposition d’entrée analysé à partir d’un flux d’état de pipeline.

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

[**Description de la \_ disposition d’entrée D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)
</dt> </dl>

 

 





