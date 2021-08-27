---
title: CD3DX12_EXISTING_COLLECTION_SUBOBJECT, classe (D3dx12. h)
description: Classe d’assistance pour la création d’un sous-objet d’état de collection existant.
keywords:
- Classe CD3DX12_EXISTING_COLLECTION_SUBOBJECT
topic_type:
- apiref
api_name:
- CD3DX12_EXISTING_COLLECTION_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: 2059bca83236ae51cbd69a9480624c3e540f18d6
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813286"
---
# <a name="cd3dx12_existing_collection_subobject-class"></a>Classe CD3DX12_EXISTING_COLLECTION_SUBOBJECT

Classe d’assistance pour la création d’un sous-objet d’état de collection existant.

Pour plus d’informations sur les applications d’assistance pour la création d’objets d’État D3DX12, consultez [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Syntaxe

```cpp
class CD3DX12_EXISTING_COLLECTION_SUBOBJECT
{
    CD3DX12_EXISTING_COLLECTION_SUBOBJECT() noexcept;
    CD3DX12_EXISTING_COLLECTION_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&);
    SetExistingCollection(ID3D12StateObject* pExistingCollection) noexcept;
    void DefineExport(
        LPCWSTR Name,
        LPCWSTR ExportToRename = nullptr,
        D3D12_EXPORT_FLAGS Flags = D3D12_EXPORT_FLAG_NONE);
    template<size_t N> void DefineExports(LPCWSTR(&Exports)[N]);
    void DefineExports(const LPCWSTR* Exports, UINT N);
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_EXISTING_COLLECTION_DESC& () const noexcept;
};
```

## <a name="members"></a>Membres

`CD3DX12_EXISTING_COLLECTION_SUBOBJECT`

Constructeur par défaut. Crée une nouvelle instance, initialisée par défaut, d’un **CD3DX12_EXISTING_COLLECTION_SUBOBJECT**.

`CD3DX12_EXISTING_COLLECTION_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Constructeur qui crée une nouvelle instance d’un **CD3DX12_EXISTING_COLLECTION_SUBOBJECT** initialisé avec le contenu d’un objet [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) .

`SetExistingCollection(ID3D12StateObject*)`

Fonction permettant de définir la collection existante sous la forme du pointeur sur un [ID3D12StateObject](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobject) passé comme paramètre.

`DefineExport(LPCWSTR, LPCWSTR = nullptr, D3D12_EXPORT_FLAGS)`

Définit un symbole exporté à partir du sous-objet. Prend un [D3D12_EXPORT_FLAGS](/windows/win32/api/d3d12/ne-d3d12-d3d12_export_flags) comme paramètre facultatif.

`DefineExports(LPCWSTR(&)[N]);`

Définit un tableau de symboles exportés à partir du sous-objet. Le paramètre de modèle *N* spécifie le nombre d’éléments dans le tableau.

`DefineExports(const LPCWSTR*, UINT)`

Définit un tableau de *N* symboles exportés à partir du sous-objet.

`Type`

Récupère le type du sous-objet, représenté par la constante [D3D12_STATE_SUBOBJECT_TYPE_EXISTING_COLLECTION](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) .

`operator const D3D12_STATE_SUBOBJECT&`

Opérateur de conversion qui retourne une référence à une constante [**D3D12_STATE_SUBOBJECT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) objet décrivant l’objet d’État.

`operator const D3D12_EXISTING_COLLECTION_DESC&`

Opérateur de conversion qui retourne une référence à une constante [**D3D12_EXISTING_COLLECTION_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_existing_collection_desc) objet décrivant l’objet d’État.

## <a name="remarks"></a>Notes

## <a name="requirements"></a>Spécifications

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Voir aussi

* [Structures d’assistance pour Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
