---
title: Méthode ID3DX12PipelineParserCallbacks RasterizerStateCb (D3DX12. h)
description: Appelle le rappel de sous-objet de description de l’état de rastériseur d’un objet qui implémente cette interface.
ms.assetid: 125FC6EC-B749-4EE2-9D34-14BD12993BDC
keywords:
- Méthode RasterizerStateCb
- Méthode RasterizerStateCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode RasterizerStateCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RasterizerStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39a179f26d88f25027eb9ffc2b4b3712ac963b65179334fff1bfa4d6103ef76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528619"
---
# <a name="id3dx12pipelineparsercallbacksrasterizerstatecb-method"></a>ID3DX12PipelineParserCallbacks :: RasterizerStateCb, méthode

Appelle le rappel de sous-objet de description de l’état de rastériseur d’un objet qui implémente cette interface.

## <a name="syntax"></a>Syntaxe


```C++
void RasterizerStateCb(
  [ref] const D3D12_RASTERIZER_DESC &RasterizerState
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RasterizerState* \[ Réf\]
</dt> <dd>

Type : **const [**D3D12 \_ rastériseur \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)**

Détails du sous-objet de description de l’état du rastériseur analysé à partir d’un flux d’État du pipeline.

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

[**D3D12 \_ rastériseur \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> </dl>

 

 





