---
title: Méthode ID3DX12PipelineParserCallbacks ErrorDuplicateSubobject (D3DX12. h)
description: Appelle le rappel d’erreur de sous-objet dupliqué d’un objet qui implémente cette interface.
ms.assetid: 625C72C4-7BFB-4DAD-8D39-EDDBC7189499
keywords:
- Méthode ErrorDuplicateSubobject
- Méthode ErrorDuplicateSubobject, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode ErrorDuplicateSubobject
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorDuplicateSubobject
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33724b1fdfec4951ce2efb31d4916ce210dc2b73858a5ef250c14a8744646bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045467"
---
# <a name="id3dx12pipelineparsercallbackserrorduplicatesubobject-method"></a>ID3DX12PipelineParserCallbacks :: ErrorDuplicateSubobject, méthode

Appelle le rappel d’erreur de sous-objet dupliqué d’un objet qui implémente cette interface.

## <a name="syntax"></a>Syntaxe


```C++
void ErrorDuplicateSubobject(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE DuplicateType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DuplicateType* 
</dt> <dd>

Type : **[ **\_ type de \_ \_ \_ sous-objet état du pipeline D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)**

Type de sous-objet qui a été dupliqué.

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

[**\_Type de \_ \_ sous-objet état \_ du pipeline D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

