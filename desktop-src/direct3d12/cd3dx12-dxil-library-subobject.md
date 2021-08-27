---
title: CD3DX12_DXIL_LIBRARY_SUBOBJECT, classe (D3dx12. h)
description: Classe d’assistance pour la création d’un sous-objet d’état de la bibliothèque DXIL.
keywords:
- Classe CD3DX12_DXIL_LIBRARY_SUBOBJECT
topic_type:
- apiref
api_name:
- CD3DX12_DXIL_LIBRARY_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: 33ec22dd722469ce131bc58d5aca83f0aed4edf0
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812544"
---
# <a name="cd3dx12_dxil_library_subobject-class"></a>Classe CD3DX12_DXIL_LIBRARY_SUBOBJECT

Classe d’assistance pour la création d’un sous-objet d’état de la bibliothèque DXIL.

Pour plus d’informations sur les applications d’assistance pour la création d’objets d’État D3DX12, consultez [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Syntaxe

```cpp
class CD3DX12_DXIL_LIBRARY_SUBOBJECT
{
    CD3DX12_DXIL_LIBRARY_SUBOBJECT() noexcept;
    CD3DX12_DXIL_LIBRARY_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&);
    void SetDXILLibrary(const D3D12_SHADER_BYTECODE* pCode) noexcept;
    void DefineExport(
        LPCWSTR Name,
        LPCWSTR ExportToRename = nullptr,
        D3D12_EXPORT_FLAGS Flags = D3D12_EXPORT_FLAG_NONE);
    template<size_t N> void DefineExports(LPCWSTR(&Exports)[N]);
    void DefineExports(const LPCWSTR* Exports, UINT N);
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_DXIL_LIBRARY_DESC& () const noexcept;
};
```

## <a name="members"></a>Membres

`CD3DX12_DXIL_LIBRARY_SUBOBJECT`

Constructeur par défaut. Crée une nouvelle instance, initialisée par défaut, d’un **CD3DX12_DXIL_LIBRARY_SUBOBJECT**.

`CD3DX12_DXIL_LIBRARY_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Constructeur qui crée une nouvelle instance d’un **CD3DX12_DXIL_LIBRARY_SUBOBJECT** initialisé avec le contenu d’un objet [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) .

`SetDXILLibrary(const D3D12_SHADER_BYTECODE*)`

Fonction permettant de définir la bibliothèque DXIL sous la forme du pointeur sur un [D3D12_SHADER_BYTECODE](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode) passé comme paramètre.

`DefineExport(LPCWSTR, LPCWSTR = nullptr, D3D12_EXPORT_FLAGS)`

Définit un symbole exporté à partir du sous-objet. Prend un [D3D12_EXPORT_FLAGS](/windows/win32/api/d3d12/ne-d3d12-d3d12_export_flags) comme paramètre facultatif.

`DefineExports(LPCWSTR(&)[N]);`

Définit un tableau de *N* symboles exportés à partir du sous-objet. Le paramètre de modèle *N* spécifie le nombre d’éléments dans le tableau.

`DefineExports(const LPCWSTR*, UINT)`

Définit un tableau de symboles exportés à partir du sous-objet.

`Type`

Récupère le type du sous-objet, représenté par la constante [D3D12_STATE_SUBOBJECT_TYPE_DXIL_LIBRARY](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) .

`operator const D3D12_STATE_SUBOBJECT&`

Opérateur de conversion qui retourne une référence à une constante [**D3D12_STATE_SUBOBJECT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) objet décrivant l’objet d’État.

`operator const D3D12_DXIL_LIBRARY_DESC&`

Opérateur de conversion qui retourne une référence à une constante [**D3D12_DXIL_LIBRARY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_library_desc) objet décrivant l’objet d’État.

## <a name="remarks"></a>Notes

## <a name="requirements"></a>Spécifications

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Voir aussi

* [Structures d’assistance pour Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
