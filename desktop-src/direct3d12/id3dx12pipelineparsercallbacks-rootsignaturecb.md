---
title: Méthode ID3DX12PipelineParserCallbacks RootSignatureCb (D3DX12. h)
description: Appelle le rappel de sous-objet de signature racine d’un objet qui implémente cette interface.
ms.assetid: FD467001-41B1-4A73-8E54-12C6B5EEAC3E
keywords:
- Méthode RootSignatureCb
- Méthode RootSignatureCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode RootSignatureCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RootSignatureCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78160ff1e61432a0711876934215ff15afb918de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545262"
---
# <a name="id3dx12pipelineparsercallbacksrootsignaturecb-method"></a>ID3DX12PipelineParserCallbacks :: RootSignatureCb, méthode

Appelle le rappel de sous-objet de signature racine d’un objet qui implémente cette interface.

## <a name="syntax"></a>Syntaxe


```C++
void RootSignatureCb(
   ID3D12RootSignature *RootSignature
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RootSignature* 
</dt> <dd>

Type : **[ **ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)\***

Détails du sous-objet de signature racine analysé à partir d’un flux d’État du pipeline.

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

[**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)
</dt> </dl>

 

