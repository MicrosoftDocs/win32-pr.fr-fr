---
title: CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT, classe (D3dx12. h)
description: Classe d’assistance pour la création d’un sous-objet d’état de configuration du pipeline Raytracing.
keywords:
- Classe CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT
topic_type:
- apiref
api_name:
- CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/05/2021
ms.openlocfilehash: 153d7f777909cf3622f6c0ededeea79b9d6a27072da35d06f9fe7dce4347b357
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132275"
---
# <a name="cd3dx12_raytracing_pipeline_config_subobject-class"></a>Classe CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT

Classe d’assistance pour la création d’un sous-objet d’état de configuration du pipeline Raytracing. Voir aussi [CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT](cd3dx12-raytracing-pipeline-config1-subobject.md).

Pour plus d’informations sur les applications d’assistance pour la création d’objets d’État D3DX12, consultez [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Syntaxe

```cpp
class CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT
{
    CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT() noexcept;
    CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void Config(UINT MaxTraceRecursionDepth) noexcept;
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_RAYTRACING_PIPELINE_CONFIG& () const noexcept;
};
```

## <a name="members"></a>Membres

`CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT`

Constructeur par défaut. Crée une nouvelle instance, initialisée par défaut, d’un **CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT**.

`CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Constructeur qui crée une nouvelle instance d’un **CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT** initialisé avec le contenu d’un objet [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) .

`Config(UINT)`

Fonction permettant de configurer la limite de récurrence de rayon pour le pipeline Raytracing.

`Type`

Récupère le type du sous-objet, représenté par la constante [D3D12_STATE_SUBOBJECT_TYPE_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) .

`operator const D3D12_STATE_SUBOBJECT&`

Opérateur de conversion qui retourne une référence à une constante [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) objet décrivant l’objet d’État.

`operator const D3D12_RAYTRACING_PIPELINE_CONFIG&`

Opérateur de conversion qui retourne une référence à une constante [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) objet décrivant l’objet d’État.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Voir aussi

* [Structures d’assistance pour Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
* [CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT](cd3dx12-raytracing-pipeline-config1-subobject.md)
