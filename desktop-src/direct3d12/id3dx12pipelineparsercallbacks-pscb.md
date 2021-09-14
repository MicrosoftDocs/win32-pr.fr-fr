---
title: Méthode ID3DX12PipelineParserCallbacks PSCb (D3DX12. h)
description: Appelle le rappel de sous-objet de nuanceur de pixels d’un objet qui implémente cette interface.
ms.assetid: 3397B018-C26A-426F-88BB-89013BACBEEA
keywords:
- Méthode PSCb
- Méthode PSCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode PSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.PSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c972702c215556b953797a6e332f8e86c480b094
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918436"
---
# <a name="id3dx12pipelineparsercallbackspscb-method"></a>ID3DX12PipelineParserCallbacks ::P méthode SCb

Appelle le rappel de sous-objet de nuanceur de pixels d’un objet qui implémente cette interface.

## <a name="syntax"></a>Syntaxe


```C++
void PSCb(
  [ref] const D3D12_SHADER_BYTECODE &PS
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PS* \[ Réf\]
</dt> <dd>

Type : **const [**D3D12 \_ Shader \_ bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**

Détails du sous-objet de nuanceur de pixels analysé à partir d’un flux d’état de pipeline.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la valeur Nothing.

## <a name="requirements"></a>Spécifications



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

 

 





