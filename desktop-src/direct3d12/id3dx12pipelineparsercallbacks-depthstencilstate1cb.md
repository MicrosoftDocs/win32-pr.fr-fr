---
title: Méthode ID3DX12PipelineParserCallbacks DepthStencilState1Cb (D3DX12. h)
description: Appelle l’état du stencil de profondeur (D3D12 \_ Depth \_ stencil \_ DESC1) rappel de sous-objet d’un objet qui implémente cette interface.
ms.assetid: C1AE06E5-B1FF-44C2-9C56-1540B97AD883
keywords:
- Méthode DepthStencilState1Cb
- Méthode DepthStencilState1Cb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode DepthStencilState1Cb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilState1Cb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a42cf85f60dcf27a5751f77a346931bfad6b03e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918459"
---
# <a name="id3dx12pipelineparsercallbacksdepthstencilstate1cb-method"></a>ID3DX12PipelineParserCallbacks ::D méthode epthStencilState1Cb

Appelle l’état du stencil de profondeur ([**D3D12 \_ Depth \_ stencil \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) rappel de sous-objet d’un objet qui implémente cette interface.

## <a name="syntax"></a>Syntaxe


```C++
void DepthStencilState1Cb(
  [ref] const D3D12_DEPTH_STENCIL_DESC1 &DepthStencilState
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DepthStencilState* \[ Réf\]
</dt> <dd>

Type : **const [**D3D12 de \_ profondeur du \_ stencil \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)**

Détails du sous-objet état du stencil de profondeur analysé à partir d’un flux d’État du pipeline.

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

[**D3D12 \_ du \_ stencil de profondeur \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> </dl>

 

 





