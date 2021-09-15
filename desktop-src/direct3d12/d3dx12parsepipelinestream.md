---
title: D3DX12ParsePipelineStream, fonction (D3dx12. h)
description: Analyse une description du flux d’État du pipeline, en appelant un rappel défini par l’utilisateur pour chaque instance de sous-objet analysée.
ms.assetid: BE4E8CC4-1E1F-4FE8-B109-05FAF93EB620
keywords:
- D3DX12ParsePipelineStream fonction)
topic_type:
- apiref
api_name:
- D3DX12ParsePipelineStream
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6778c29793f01ff7f1e5fd6424fb6795a29e64c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521729"
---
# <a name="d3dx12parsepipelinestream-function"></a>D3DX12ParsePipelineStream fonction)

Analyse une description du flux d’État du pipeline, en appelant un rappel défini par l’utilisateur pour chaque instance de sous-objet analysée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT inline D3DX12ParsePipelineStream(
   const D3D12_PIPELINE_STATE_STREAM_DESC &Desc,
         ID3DX12PipelineParserCallbacks   *pCallbacks
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Description* \[ Réf\]
</dt> <dd>

Type : **const [**D3D12 \_ pipeline d’état de pipeline \_ \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)**

Description du flux d’état de pipeline à analyser.

</dd> <dt>

*pCallbacks* 
</dt> <dd>

Type : **[ **ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)\***

Structure qui spécifie les rappels à appeler pour chaque type de sous-objet et les rappels supplémentaires à appeler en cas d’erreur d’analyse.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Cette méthode retourne une erreur HRESULT réussie (**S \_ OK** ou **E \_ INVALIDARG** si un type de sous-objet inconnu est rencontré, si la description du flux est vide, null ou contient des sous-objets en double (y compris des sous-objets dérivés) ou si *pCallbacks* a la valeur null. Dans chaque cas où E \_ INVALIDARG est retourné, un rappel correspondant est d’abord appelé.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Bibliothèque<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions d’assistance pour D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





