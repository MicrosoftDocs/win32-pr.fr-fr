---
title: Méthode ID3DX12PipelineParserCallbacks CachedPSOCb (D3DX12. h)
description: Appelle le rappel d’objet de sous-objet PSO mis en cache (objet d’état de pipeline) d’un objet qui implémente cette interface.
ms.assetid: 9EF8C468-1D86-4F49-9091-36B6125F1B68
keywords:
- Méthode CachedPSOCb
- Méthode CachedPSOCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode CachedPSOCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.CachedPSOCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c168635a66eff012768a1eabbc803c6986a2c43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525895"
---
# <a name="id3dx12pipelineparsercallbackscachedpsocb-method"></a>ID3DX12PipelineParserCallbacks :: CachedPSOCb, méthode

Appelle le rappel d’objet de sous-objet PSO mis en cache (objet d’état de pipeline) d’un objet qui implémente cette interface.

## <a name="syntax"></a>Syntaxe


```C++
void CachedPSOCb(
  [ref] const D3D12_CACHED_PIPELINE_STATE &CachedPSO
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CachedPSO* \[ Réf\]
</dt> <dd>

Type : **const [**D3D12 \_ \_ \_ État du pipeline mis en cache**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)**

Détails du sous-objet PSO mis en cache (objet d’État du pipeline) analysé à partir d’un flux d’État du pipeline.

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

[**\_ \_ État du pipeline mis en cache D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)
</dt> </dl>

 

 





