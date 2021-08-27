---
title: Structure CD3DX12_VIEW_INSTANCING_DESC (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une structure [**D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc) .
keywords:
- Structure CD3DX12_VIEW_INSTANCING_DESC
topic_type:
- apiref
api_name:
- CD3DX12_VIEW_INSTANCING_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2021
ms.openlocfilehash: 51c9f5caf5bedf9712001420993393a2dcfa6870
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813259"
---
# <a name="cd3dx12_view_instancing_desc-structure"></a>Structure CD3DX12_VIEW_INSTANCING_DESC

Structure d’assistance pour faciliter l’initialisation d’une structure [**D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .

## <a name="syntax"></a>Syntaxe

```cpp
struct CD3DX12_VIEW_INSTANCING_DESC : public D3D12_VIEW_INSTANCING_DESC
{
    CD3DX12_VIEW_INSTANCING_DESC();
    explicit CD3DX12_VIEW_INSTANCING_DESC(const D3D12_VIEW_INSTANCING_DESC& o) noexcept;
    explicit CD3DX12_VIEW_INSTANCING_DESC(CD3DX12_DEFAULT) noexcept;
    explicit CD3DX12_VIEW_INSTANCING_DESC(
        UINT InViewInstanceCount,
        const D3D12_VIEW_INSTANCE_LOCATION* InViewInstanceLocations,
        D3D12_VIEW_INSTANCING_FLAGS InFlags) noexcept;
};
```

## <a name="members"></a>Membres

`CD3DX12_VIEW_INSTANCING_DESC`

Constructeur par défaut. Crée une nouvelle instance non initialisée d’un **CD3DX12_VIEW_INSTANCING_DESC**.

`CD3DX12_VIEW_INSTANCING_DESC(const D3D12_VIEW_INSTANCING_DESC&)`

Constructeur qui crée une nouvelle instance d’un **CD3DX12_VIEW_INSTANCING_DESC** initialisé avec le contenu d’une structure [**D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .

`CD3DX12_VIEW_INSTANCING_DESC(CD3DX12_DEFAULT)`

Constructeur qui crée une nouvelle instance d’un **CD3DX12_VIEW_INSTANCING_DESC** initialisé avec ces valeurs.

|Membre de données|valeur|
|-|-|
|ViewInstanceCount|0|
|pViewInstanceLocations|nullptr|
|Indicateurs|D3D12_VIEW_INSTANCING_FLAG_NONE|

`CD3DX12_VIEW_INSTANCING_DESC(UINT, const D3D12_VIEW_INSTANCE_LOCATION*, D3D12_VIEW_INSTANCING_FLAGS)`

Constructeur qui crée une nouvelle instance d’un **CD3DX12_VIEW_INSTANCING_DESC** initialisé avec les paramètres qui lui sont passés.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Voir aussi

* [D3DX12_VIEW_INSTANCING_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
* [Structures d’assistance pour Direct3D 12](helper-structures-for-d3d12.md)
