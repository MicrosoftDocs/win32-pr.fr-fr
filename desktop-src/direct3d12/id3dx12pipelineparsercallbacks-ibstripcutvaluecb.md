---
title: Méthode ID3DX12PipelineParserCallbacks IBStripCutValueCb (D3DX12. h)
description: Appelle le rappel de sous-objet de valeur de coupe de la mémoire tampon d’index d’un objet qui implémente cette interface.
ms.assetid: 702CA90A-FF20-4554-9469-C86428C203BC
keywords:
- Méthode IBStripCutValueCb
- Méthode IBStripCutValueCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode IBStripCutValueCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.IBStripCutValueCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f79fca93e76f43b97ffc8e133594805214fe84cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106544404"
---
# <a name="id3dx12pipelineparsercallbacksibstripcutvaluecb-method"></a>ID3DX12PipelineParserCallbacks :: IBStripCutValueCb, méthode

Appelle le rappel de sous-objet de valeur de coupe de la mémoire tampon d’index d’un objet qui implémente cette interface.

## <a name="syntax"></a>Syntaxe


```C++
void IBStripCutValueCb(
   D3D12_INDEX_BUFFER_STRIP_CUT_VALUE IBStripCutValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IBStripCutValue* 
</dt> <dd>

Type : valeur de coupe de la **[ **\_ \_ bande de mémoire tampon \_ \_ \_ d’index D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)**

Détails du sous-objet de valeur coupe-bande de la mémoire tampon d’index analysé à partir d’un flux d’État du pipeline.

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

[**Valeur de coupe de la \_ \_ bande de mémoire tampon d’index \_ D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)
</dt> </dl>

 

 





