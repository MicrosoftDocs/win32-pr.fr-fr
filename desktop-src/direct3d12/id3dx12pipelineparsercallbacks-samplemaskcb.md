---
title: Méthode ID3DX12PipelineParserCallbacks SampleMaskCb (D3DX12. h)
description: Appelle l’exemple de rappel de sous-objet de masque d’un objet qui implémente cette interface.
ms.assetid: 4D729414-1E04-407B-B32F-ECE1EA9FF414
keywords:
- Méthode SampleMaskCb
- Méthode SampleMaskCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode SampleMaskCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleMaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0124b228056089e21c078ffce25ce59eef0e3dee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922667"
---
# <a name="id3dx12pipelineparsercallbackssamplemaskcb-method"></a>ID3DX12PipelineParserCallbacks :: SampleMaskCb, méthode

Appelle l’exemple de rappel de sous-objet de masque d’un objet qui implémente cette interface.

## <a name="syntax"></a>Syntaxe


```C++
void SampleMaskCb(
   
        UINT
           SampleMask
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SampleMask* 
</dt> <dd>

Type : **uint**

Détails de l’exemple de sous-objet de masque analysé à partir d’un flux d’état de pipeline.

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
</dt> </dl>

 

 





