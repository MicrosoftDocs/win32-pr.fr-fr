---
title: Méthode ID3DX12PipelineParserCallbacks RTVFormatsCb (D3DX12. h)
description: Appelle le rappel de sous-objet du tableau de format de la cible de rendu d’un objet qui implémente cette interface.
ms.assetid: 0D5F0BC4-D9E2-4B16-99B5-509454AF8C02
keywords:
- Méthode RTVFormatsCb
- Méthode RTVFormatsCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode RTVFormatsCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RTVFormatsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caaa1df508e1a448de3851d408f9aad5ac94d957
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922675"
---
# <a name="id3dx12pipelineparsercallbacksrtvformatscb-method"></a>ID3DX12PipelineParserCallbacks :: RTVFormatsCb, méthode

Appelle le rappel de sous-objet du tableau de format de la cible de rendu d’un objet qui implémente cette interface.

## <a name="syntax"></a>Syntaxe


```C++
void RTVFormatsCb(
  [ref] const D3D12_RT_FORMAT_ARRAY &RTVFormats
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RTVFormats* \[ Réf\]
</dt> <dd>

Type : **const [**D3D12 \_ RT \_ , \_ tableau**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)**

Détails du sous-objet du tableau de format de la cible de rendu analysé à partir d’un flux d’État du pipeline.

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

[**\_Tableau de \_ format D3D12 RT \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





