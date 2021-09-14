---
title: Méthode ID3DX12PipelineParserCallbacks PrimitiveTopologyTypeCb (D3DX12. h)
description: Appelle le rappel de sous-objet de type de topologie primitif d’un objet qui implémente cette interface.
ms.assetid: FF9D8D5C-3A6A-40D8-8EA4-3EA305EB4568
keywords:
- Méthode PrimitiveTopologyTypeCb
- Méthode PrimitiveTopologyTypeCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode PrimitiveTopologyTypeCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.PrimitiveTopologyTypeCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01a2d73edd6ac94719905757d75a756c905c832
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918444"
---
# <a name="id3dx12pipelineparsercallbacksprimitivetopologytypecb-method"></a>ID3DX12PipelineParserCallbacks ::P méthode rimitiveTopologyTypeCb

Appelle le rappel de sous-objet de type de topologie primitif d’un objet qui implémente cette interface.

## <a name="syntax"></a>Syntaxe


```C++
void PrimitiveTopologyTypeCb(
   D3D12_PRIMITIVE_TOPOLOGY_TYPE PrimitiveTopologyType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PrimitiveTopologyType* 
</dt> <dd>

Type : **[ **\_ \_ \_ type de topologie primitive D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)**

Détails du sous-objet de type de topologie primitif analysé à partir d’un flux d’état de pipeline.

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

[**\_Type de \_ topologie primitive \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)
</dt> </dl>

 

 





