---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING (D3dx12. h)
description: Structure d’assistance utilisée pour encapsuler une structure [CD3DX12_VIEW_INSTANCING_DESC](cd3dx12-view-instancing-desc.md) . Permet aux nuanceurs de s’afficher dans plusieurs vues avec un seul appel de dessin ; utile pour la vision stéréo ou la génération de carte cubique.
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/05/2021
ms.openlocfilehash: b693130bab6d090379d253d07ce4bbaa5c88b150
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520828"
---
# <a name="cd3dx12_pipeline_state_stream_view_instancing-structure"></a>Structure CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING

Structure d’assistance utilisée pour encapsuler une structure [CD3DX12_VIEW_INSTANCING_DESC](cd3dx12-view-instancing-desc.md) . Permet aux nuanceurs de s’afficher dans plusieurs vues avec un seul appel de dessin ; utile pour la vision stéréo ou la génération de carte cubique.

## <a name="syntax"></a>Syntaxe

```cpp
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_VIEW_INSTANCING_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_VIEW_INSTANCING, CD3DX12_DEFAULT> CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING;
```

**CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING** est une `typedef` spécialisation du modèle de [CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT](cd3dx12-pipeline-state-stream-subobject.md) .

## <a name="members"></a>Membres

Consultez [CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT](cd3dx12-pipeline-state-stream-subobject.md) et [CD3DX12_VIEW_INSTANCING_DESC](cd3dx12-view-instancing-desc.md).

## <a name="requirements"></a>Spécifications

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Voir aussi

* [Structures d’assistance pour Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT](cd3dx12-pipeline-state-stream-subobject.md)
* [D3D12_PIPELINE_STATE_SUBOBJECT_TYPE](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
* [D3DX12_VIEW_INSTANCING_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
