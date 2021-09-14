---
title: Méthode ID3DX12PipelineParserCallbacks CSCb (D3DX12. h)
description: Appelle le rappel du sous-objet de nuanceur de calcul d’un objet qui implémente cette interface.
ms.assetid: DE1ABA3D-D372-4D7F-9DB6-4E3360EAFAC2
keywords:
- Méthode CSCb
- Méthode CSCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode CSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.CSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27dcf175d153211e06864cb73139b03f868d15db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918468"
---
# <a name="id3dx12pipelineparsercallbackscscb-method"></a>ID3DX12PipelineParserCallbacks :: CSCb, méthode

Appelle le rappel du sous-objet de nuanceur de calcul d’un objet qui implémente cette interface.

## <a name="syntax"></a>Syntaxe


```C++
void CSCb(
  [ref] const D3D12_SHADER_BYTECODE &CS
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CS* \[ Réf\]
</dt> <dd>

Type : **const [**D3D12 \_ Shader \_ bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**

Détails du sous-objet de nuanceur de calcul analysé à partir d’un flux d’état de pipeline.

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

 

 





