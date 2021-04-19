---
title: Méthode ID3DX12PipelineParserCallbacks HSCb (D3DX12. h)
description: Appelle le rappel de sous-objet de nuanceur de coque d’un objet qui implémente cette interface.
ms.assetid: B2967E7F-391F-4A76-A087-E0B925018EE3
keywords:
- Méthode HSCb
- Méthode HSCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode HSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.HSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7d351e0b3827087cb51c38af173badd28d698c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539167"
---
# <a name="id3dx12pipelineparsercallbackshscb-method"></a>ID3DX12PipelineParserCallbacks :: HSCb, méthode

Appelle le rappel de sous-objet de nuanceur de coque d’un objet qui implémente cette interface.

## <a name="syntax"></a>Syntaxe


```C++
void HSCb(
  [ref] const D3D12_SHADER_BYTECODE &HS
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HS* \[ Réf\]
</dt> <dd>

Type : **const [**D3D12 \_ Shader \_ bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**

Détails du sous-objet de nuanceur de coque analysé à partir d’un flux d’état de pipeline.

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

[**\_Bytecode de nuanceur D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





