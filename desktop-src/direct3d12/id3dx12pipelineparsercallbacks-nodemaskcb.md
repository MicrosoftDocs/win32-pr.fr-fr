---
title: Méthode ID3DX12PipelineParserCallbacks NodemaskCb (D3DX12. h)
description: Appelle le rappel de sous-objet nodemask d’un objet qui implémente cette interface.
ms.assetid: F5A408B7-A777-4BBC-A2A3-1BC3551E65ED
keywords:
- Méthode NodemaskCb
- Méthode NodemaskCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode NodemaskCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.NodemaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 356ddf6ea86980ee882ad7544096811db420ae0cf8224f315801b708b95ae98d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045447"
---
# <a name="id3dx12pipelineparsercallbacksnodemaskcb-method"></a>ID3DX12PipelineParserCallbacks :: NodemaskCb, méthode

Appelle le rappel de sous-objet nodemask d’un objet qui implémente cette interface.

## <a name="syntax"></a>Syntaxe


```C++
void NodemaskCb(
   
        UINT
       Nodemask
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nodemask* 
</dt> <dd>

Type : **uint**

Détails du sous-objet nodemask analysé à partir d’un flux d’État du pipeline.

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
</dt> </dl>

 

 





