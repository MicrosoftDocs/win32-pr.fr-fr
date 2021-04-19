---
title: Méthode ID3DX12PipelineParserCallbacks ErrorBadInputParameter (D3DX12. h)
description: Appelle le rappel d’erreur de paramètre d’entrée incorrect d’un objet qui implémente cette interface.
ms.assetid: CB1F9A77-B120-4D72-99D3-16594E668520
keywords:
- Méthode ErrorBadInputParameter
- Méthode ErrorBadInputParameter, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, méthode ErrorBadInputParameter
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorBadInputParameter
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5181e8d9fb83b7338adc3af5c0ce44aec1b447d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531351"
---
# <a name="id3dx12pipelineparsercallbackserrorbadinputparameter-method"></a>ID3DX12PipelineParserCallbacks :: ErrorBadInputParameter, méthode

Appelle le rappel d’erreur de paramètre d’entrée incorrect d’un objet qui implémente cette interface.

## <a name="syntax"></a>Syntaxe


```C++
void ErrorBadInputParameter(
   
        UINT
           ParameterIndex
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ParameterIndex* 
</dt> <dd>

Type : **uint**

Position du paramètre qui contient une entrée incorrecte. Le paramètre le plus à gauche se trouve à la position 1, et non à la position 0.

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
</dt> </dl>

 

 





