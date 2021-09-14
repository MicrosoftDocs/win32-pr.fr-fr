---
title: Méthode ID3DX12PipelineParserCallbacks SampleDescCb (D3DX12. h)
description: Appelle l’exemple de rappel de sous-objet de description d’un objet qui implémente cette interface.
ms.assetid: 32F112D3-97B1-45C2-8744-9F27DC95C249
keywords:
- Méthode SampleDescCb
- Méthode SampleDescCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode SampleDescCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleDescCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0644837720dd8c81dc1c7577a1d6506ebdf61c24
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918447"
---
# <a name="id3dx12pipelineparsercallbackssampledesccb-method"></a>ID3DX12PipelineParserCallbacks :: SampleDescCb, méthode

Appelle l’exemple de rappel de sous-objet de description d’un objet qui implémente cette interface.

## <a name="syntax"></a>Syntaxe


```C++
void SampleDescCb(
  [ref] const DXGI_SAMPLE_DESC &SampleDesc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SampleDesc* \[ Réf\]
</dt> <dd>

Type : **const [**dxgi \_ exemple \_ desc**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)**

Détails de l’exemple de sous-objet Description analysé à partir d’un flux d’État du pipeline.

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

[**\_exemple dxgi \_ desc**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)
</dt> </dl>

 

