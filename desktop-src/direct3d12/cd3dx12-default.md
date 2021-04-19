---
title: Structure CD3DX12_DEFAULT (D3dx12. h)
description: Passe D3D12 \_ par défaut dans un constructeur pour chaque structure d’assistance. Cette structure est simplement utilisée comme un mécanisme pour définir des paramètres par défaut sur les autres structures d’assistance.
ms.assetid: AD41FD7B-9172-400E-9292-374FFAEDE145
keywords:
- Structure CD3DX12_DEFAULT
topic_type:
- apiref
api_name:
- CD3DX12_DEFAULT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b010e8f0fdce67f16750d0f66d1cf272c8ddb849
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538741"
---
# <a name="cd3dx12_default-structure"></a>CD3DX12, \_ structure par défaut

Passe D3D12 \_ par défaut dans un constructeur pour chaque structure d’assistance. Cette structure est simplement utilisée comme un mécanisme pour définir des paramètres par défaut sur les autres structures d’assistance.

## <a name="remarks"></a>Notes

Ce struct est déclaré comme suit :

``` syntax
struct CD3DX12_DEFAULT {};
extern const DECLSPEC_SELECTANY CD3DX12_DEFAULT D3D12_DEFAULT;
```

Passe D3D12 \_ par défaut dans un constructeur pour chaque struct d’assistance. Par exemple, le constructeur suivant est déclaré dans d3dx12. h :

\_ \_ Handle de descripteur de processeur CD3DX12 \_ ( \_ valeur par défaut CD3DX12) {PTR = 0 ;}

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





