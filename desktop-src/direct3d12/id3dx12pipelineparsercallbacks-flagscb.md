---
title: Méthode ID3DX12PipelineParserCallbacks FlagsCb (D3DX12. h)
description: Appelle le rappel de sous-objet d’indicateurs d’un objet qui implémente cette interface.
ms.assetid: 81DD8CF3-87BA-4380-BECD-70A80580048A
keywords:
- Méthode FlagsCb
- Méthode FlagsCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode FlagsCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.FlagsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d14e8b507ae04a5f35b2786ca4ba7ab6ec19bb449492aa2c40f32510cd3ecb57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528781"
---
# <a name="id3dx12pipelineparsercallbacksflagscb-method"></a>ID3DX12PipelineParserCallbacks :: FlagsCb, méthode

Appelle le rappel de sous-objet d’indicateurs d’un objet qui implémente cette interface.

## <a name="syntax"></a>Syntaxe


```C++
void FlagsCb(
   D3D12_PIPELINE_STATE_FLAGS Flags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Indicateurs* 
</dt> <dd>

Type : **[ **\_ indicateurs d' \_ état \_ du pipeline D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)**

Détails du sous-objet Flags analysé à partir d’un flux d’État du pipeline.

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

[**\_Indicateurs d’État du pipeline D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)
</dt> </dl>

 

 





