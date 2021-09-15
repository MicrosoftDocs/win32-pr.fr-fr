---
title: CD3DX12_STATE_OBJECT_DESC, classe (D3dx12. h)
description: Classe centrale des applications auxiliaires de création d’objets d’État D3DX12, qui sont des classes d’assistance pour la création d’objets d’État à partir d’un ensemble arbitraire de sous-objets.
keywords:
- Classe CD3DX12_STATE_OBJECT_DESC
topic_type:
- apiref
api_name:
- CD3DX12_STATE_OBJECT_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/03/2021
ms.openlocfilehash: cc3d65a9779c379debd94e7872717e4449a71ac8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517021"
---
# <a name="cd3dx12_state_object_desc-class"></a>Classe CD3DX12_STATE_OBJECT_DESC

Classe centrale des applications auxiliaires de création d’objets d’État D3DX12, qui sont des classes d’assistance pour la création d’objets d’État à partir d’un ensemble arbitraire de sous-objets.

## <a name="syntax"></a>Syntaxe

```cpp
class CD3DX12_STATE_OBJECT_DESC
{
    CD3DX12_STATE_OBJECT_DESC() noexcept;
    CD3DX12_STATE_OBJECT_DESC(D3D12_STATE_OBJECT_TYPE) noexcept;
    void SetStateObjectType(D3D12_STATE_OBJECT_TYPE) noexcept;
    operator const D3D12_STATE_OBJECT_DESC& ();
    operator const D3D12_STATE_OBJECT_DESC* ();
    template<typename T> T* CreateSubobject();
};
```

## <a name="members"></a>Membres

`CD3DX12_STATE_OBJECT_DESC`

Constructeur par défaut. Crée une nouvelle instance, initialisée par défaut, d’un **CD3DX12_STATE_OBJECT_DESC**.

`CD3DX12_STATE_OBJECT_DESC(D3D12_STATE_OBJECT_TYPE)`

Constructeur qui crée une nouvelle instance d’une **CD3DX12_STATE_OBJECT_DESC** initialisée avec un type subjobject correspondant à la valeur de l' [**D3D12_STATE_OBJECT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_object_type) passé.

`SetStateObjectType(D3D12_STATE_OBJECT_TYPE)`

Méthode qui définit le type subjobject sur la valeur de la [**D3D12_STATE_OBJECT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_object_type) qui lui est passée.

`operator const D3D12_STATE_OBJECT_DESC&`

Opérateur de conversion qui retourne une référence à une constante [**D3D12_STATE_OBJECT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_desc) objet décrivant l’objet d’État.

`operator const D3D12_STATE_OBJECT_DESC*`

Opérateur de conversion qui retourne un pointeur vers une constante [**D3D12_STATE_OBJECT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_desc) objet décrivant l’objet d’État.

`CreateSubobject`

Modèle de fonction qui crée une application d’assistance sububject dont la durée de vie est la propriété de cette classe.

Le paramètre de modèle *T* spécifie le type d’assistance subjobject, par exemple, [CD3DX12_HIT_GROUP_SUBOBJECT](cd3dx12-hit-group-subobject.md).

## <a name="remarks"></a>Notes

Pour utiliser les applications d’assistance pour la création d’objets d’État D3DX12, commencez par instancier un objet **CD3DX12_STATE_OBJECT_DESC** et appelez sa fonction **CreateSubobject** pour créer des sous-objets. Les applications auxiliaires de sous-objet possèdent chacune des méthodes spécifiques à ce sous-objet pour la configuration de son contenu.

```cpp
CD3DX12_STATE_OBJECT_DESC Collection1(D3D12_STATE_OBJECT_TYPE_COLLECTION);
auto Lib0 = Collection1.CreateSubobject<CD3DX12_DXIL_LIBRARY_SUBOBJECT>();
Lib0->SetDXILLibrary(&pMyAppDxilLibs[0]);
Lib0->DefineExport(L"rayGenShader0");
// In practice, these export listings might be data/engine-driven.
...
```

Vous pouvez également instancier explicitement des applications auxiliaires de sous-objet, comme par exemple via des variables locales, en passant la description de l’objet d’État (qui doit pointer vers celle-ci) dans le constructeur d’assistance (ou l’appel `mySubobjectHelper.AddToStateObject(Collection1)` ).

Dans ce scénario alternatif, vous devez conserver le sous-objet actif tant que l’objet d’État auquel il est associé est actif, sinon ses références de pointeur seront obsolètes.

```cpp
CD3DX12_STATE_OBJECT_DESC RaytracingState2(D3D12_STATE_OBJECT_TYPE_RAYTRACING_PIPELINE);
CD3DX12_DXIL_LIBRARY_SUBOBJECT LibA(RaytracingState2);
LibA.SetDXILLibrary(&pMyAppDxilLibs[4]);
// Not manually specifying exports; meaning that all exports in the libraries are exported.
...
```

## <a name="requirements"></a>Spécifications

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Voir aussi

* [Structures d’assistance pour Direct3D 12](helper-structures-for-d3d12.md)
