---
title: Méthode ID3DX12PipelineParserCallbacks DSCb (D3DX12. h)
description: Appelle le rappel de sous-objet de nuanceur de domaine d’un objet qui implémente cette interface.
ms.assetid: F4877211-4122-4418-9323-3F68B0BB3363
keywords:
- Méthode DSCb
- Méthode DSCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode DSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63c4cee98bf617fb02cb5c543050f51c56a733d56964e2139e5b7357c7a88034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528987"
---
# <a name="id3dx12pipelineparsercallbacksdscb-method"></a>ID3DX12PipelineParserCallbacks ::D méthode SCb

Appelle le rappel de sous-objet de nuanceur de domaine d’un objet qui implémente cette interface.

## <a name="syntax"></a>Syntaxe


```C++
void DSCb(
  [ref] const D3D12_SHADER_BYTECODE &DS
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Service d’annuaire* \[ Réf\]
</dt> <dd>

Type : **const [**D3D12 \_ Shader \_ bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**

Détails du sous-objet du nuanceur de domaine analysé à partir d’un flux d’État du pipeline.

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

 

 





