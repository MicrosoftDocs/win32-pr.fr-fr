---
title: D3D12DecomposeSubresource, fonction (D3dx12.h)
description: Affiche la tranche MIP, le segment de tableau et la tranche de plan correspondant à l’index de sous-ressource spécifié.
ms.assetid: 89FAD7C5-E732-4E74-AC2F-DEECD6ADDA7D
keywords:
- D3D12DecomposeSubresource fonction)
topic_type:
- apiref
api_name:
- D3D12DecomposeSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c27089fb09c2408917be06b2f74e6d32f3e2f5aa9b96924de1ab92de190efb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045637"
---
# <a name="d3d12decomposesubresource-function"></a>D3D12DecomposeSubresource fonction)

Affiche la tranche MIP, le segment de tableau et la tranche de plan correspondant à l’index de sous-ressource spécifié.

## <a name="syntax"></a>Syntaxe


```C++
void inline D3D12DecomposeSubresource(
        UINT Subresource,
        UINT MipLevels,
        UINT ArraySize,
  _Out_ T    &MipSlice,
  _Out_ U    &ArraySlice,
  _Out_ V    &PlaneSlice
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Sous-ressource* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Index de la sous-ressource.

</dd> <dt>

*Miplevels a* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Nombre maximal de niveaux de mipmap dans la sous-ressource.

</dd> <dt>

*ArraySize* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Nombre d’éléments dans le tableau.

</dd> <dt>

*MipSlice* \[ out, Ref\]
</dt> <dd>

Type : **T**

Génère une sortie de la tranche MIP qui correspond à l’index de sous-ressource donné.

</dd> <dt>

*ArraySlice* \[ out, Ref\]
</dt> <dd>

Type : **U**

Génère la sortie de la tranche de tableau qui correspond à l’index de sous-ressource donné.

</dd> <dt>

*PlaneSlice* \[ out, Ref\]
</dt> <dd>

Type : **V**

Génère la sortie de la tranche de plan qui correspond à l’index de sous-ressource donné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette fonction détermine quelle tranche MIP, tranche de tableau et tranche de plan correspondent à un index de sous-ressources donné. Il s’agit d’un utilitaire utile, bien qu’il soit spécifique à C++.

Cette fonction est déclarée comme suit, avec des paramètres de type C++ pour les types **T**, **U** et **V**:


```c++
template <typename T, typename U, typename V>
inline void D3D12DecomposeSubresource( UINT Subresource, UINT MipLevels, UINT ArraySize, _Out_ T& MipSlice, _Out_ U& ArraySlice, _Out_ V& PlaneSlice )
{
    MipSlice = static_cast<T>(Subresource % MipLevels);
    ArraySlice = static_cast<U>((Subresource / MipLevels) % ArraySize);
    PlaneSlice = static_cast<V>(Subresource / (MipLevels * ArraySize));
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Bibliothèque<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

[Fonctions d’assistance pour D3D12](helper-functions-for-d3d12.md)

[Sous-ressources](subresources.md)
