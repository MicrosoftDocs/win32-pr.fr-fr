---
title: CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT, classe (D3dx12. h)
description: Classe d’assistance pour la création d’un sous-objet qui définit les propriétés générales d’un objet d’État.
keywords:
- Classe CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT
topic_type:
- apiref
api_name:
- CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/05/2021
ms.openlocfilehash: 952bf1cd1b2833a4e4a2bf0a91892fbb1d6f797c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918507"
---
# <a name="cd3dx12_state_object_config_subobject-class"></a>Classe CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT

Classe d’assistance pour la création d’un sous-objet qui définit les propriétés générales d’un objet d’État.

Pour plus d’informations sur les applications d’assistance pour la création d’objets d’État D3DX12, consultez [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Syntaxe

```cpp
class CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT
{
public:
    CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT() noexcept;
    CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetFlags(D3D12_STATE_OBJECT_FLAGS Flags) noexcept;
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_STATE_OBJECT_CONFIG& () const noexcept;
};
```

## <a name="members"></a>Membres

`CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT`

Constructeur par défaut. Crée une nouvelle instance, initialisée par défaut, d’un **CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT**.

`CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Constructeur qui crée une nouvelle instance d’un **CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT** initialisé avec le contenu d’un objet [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) .

`SetFlags(D3D12_STATE_OBJECT_FLAGS)`

Fonction permettant de spécifier la configuration requise pour l’objet d’état via un objet [D3D12_STATE_OBJECT_FLAGS](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_object_flags) .

`Type`

Récupère le type du sous-objet, représenté par la constante [D3D12_STATE_SUBOBJECT_TYPE_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) .

`operator const D3D12_STATE_SUBOBJECT&`

Opérateur de conversion qui retourne une référence à une constante [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) objet décrivant l’objet d’État.

`operator const D3D12_STATE_OBJECT_CONFIG&`

Opérateur de conversion qui retourne une référence à une constante [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) objet décrivant l’objet d’État.

## <a name="requirements"></a>Spécifications

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Voir aussi

* [Structures d’assistance pour Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
