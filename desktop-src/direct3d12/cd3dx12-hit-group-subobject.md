---
title: CD3DX12_HIT_GROUP_SUBOBJECT, classe (D3dx12. h)
description: Classe d’assistance pour la création d’un sous-objet d’état de groupe d’accès.
keywords:
- Classe CD3DX12_HIT_GROUP_SUBOBJECT
topic_type:
- apiref
api_name:
- CD3DX12_HIT_GROUP_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: dd2b396e1305d2cf21cb2121aaa6a186c47d7677
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813098"
---
# <a name="cd3dx12_hit_group_subobject-class"></a>Classe CD3DX12_HIT_GROUP_SUBOBJECT

Classe d’assistance pour la création d’un sous-objet d’état de groupe d’accès.

Pour plus d’informations sur les applications d’assistance pour la création d’objets d’État D3DX12, consultez [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Syntaxe

```cpp
class CD3DX12_HIT_GROUP_SUBOBJECT
{
    CD3DX12_HIT_GROUP_SUBOBJECT() noexcept;
    CD3DX12_HIT_GROUP_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetHitGroupExport(LPCWSTR exportName);
    void SetHitGroupType(D3D12_HIT_GROUP_TYPE Type) noexcept;
    void SetAnyHitShaderImport(LPCWSTR importName);
    void SetClosestHitShaderImport(LPCWSTR importName);
    void SetIntersectionShaderImport(LPCWSTR importName);
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept { return *m_pSubobject; }
    operator const D3D12_HIT_GROUP_DESC& () const noexcept { return m_Desc; }
};
```

## <a name="members"></a>Membres

`CD3DX12_HIT_GROUP_SUBOBJECT`

Constructeur par défaut. Crée une nouvelle instance, initialisée par défaut, d’un **CD3DX12_HIT_GROUP_SUBOBJECT**.

`CD3DX12_HIT_GROUP_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Constructeur qui crée une nouvelle instance d’un **CD3DX12_HIT_GROUP_SUBOBJECT** initialisé avec le contenu d’un objet [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) .

`SetHitGroupExport(LPCWSTR)`

Fonction permettant de définir le nom du groupe d’accès.

`SetHitGroupType(D3D12_HIT_GROUP_TYPE)`

Fonction permettant de définir une valeur à partir de l’énumération [D3D12_HIT_GROUP_TYPE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type) en spécifiant le type du groupe d’accès.

`SetAnyHitShaderImport(LPCWSTR)`

Fonction permettant de définir éventuellement le nom du nuanceur d’accès en tout cas associé au groupe d’accès.

`SetClosestHitShaderImport(LPCWSTR)`

Fonction permettant de définir éventuellement le nom du nuanceur le plus proche associé au groupe d’accès.

`SetIntersectionShaderImport(LPCWSTR)`

Fonction permettant de définir éventuellement le nom du nom facultatif du nuanceur d’intersection associé au groupe d’accès.

`Type`

Récupère le type du sous-objet, représenté par la constante [D3D12_STATE_SUBOBJECT_TYPE_HIT_GROUP](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) .

`operator const D3D12_STATE_SUBOBJECT&`

Opérateur de conversion qui retourne une référence à une constante [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) objet décrivant l’objet d’État.

`operator const D3D12_HIT_GROUP_DESC&`

Opérateur de conversion qui retourne une référence à une constante [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) objet décrivant l’objet d’État.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Voir aussi

* [Structures d’assistance pour Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
