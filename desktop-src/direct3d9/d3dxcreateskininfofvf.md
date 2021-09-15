---
description: Crée un objet de maillage d’apparence vide à l’aide d’un code de format de vertex flexible.
ms.assetid: 72e27850-0102-4121-a397-16f2e0220b93
title: D3DXCreateSkinInfoFVF, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfoFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 907ab874b8cd8b766e6f9413212ba8771df9b25c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127526069"
---
# <a name="d3dxcreateskininfofvf-function"></a>D3DXCreateSkinInfoFVF fonction)

Crée un objet de maillage d’apparence vide à l’aide d’un code de format de vertex flexible.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreateSkinInfoFVF(
  _In_  DWORD          NumVertices,
  _In_  DWORD          FVF,
  _In_  DWORD          NumBones,
  _Out_ LPD3DXSKININFO *ppSkinInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NumVertices* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Nombre de vertex pour le maillage de l’apparence.

</dd> <dt>

*Commission* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison de [D3DFVF](d3dfvf.md) qui décrit le format de vertex pour le maillage d’apparence retourné.

</dd> <dt>

*NumBones* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Nombre d’OS pour le maillage de l’apparence.

</dd> <dt>

*ppSkinInfo* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Adresse d’un pointeur vers une interface [**ID3DXSkinInfo**](id3dxskininfo.md) , représentant l’objet d’informations d’apparence créé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Utilisez [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) pour remplir l’objet de maillage d’apparence vide retourné par cette méthode.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
