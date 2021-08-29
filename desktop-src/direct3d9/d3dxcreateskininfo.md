---
description: D3DXCreateSkinInfo fonction-crée un objet de maillage d’apparence vide à l’aide d’un déclarateur.
ms.assetid: c98da2e5-a9eb-4070-8846-b346b5c57fb3
title: D3DXCreateSkinInfo, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfo
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5d1539e0bf7a552fdb44bb1c2f323af387797a660d4e1bade312000652fb5bbf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676139"
---
# <a name="d3dxcreateskininfo-function"></a>D3DXCreateSkinInfo fonction)

Crée un objet de maillage d’apparence vide à l’aide d’un déclarateur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreateSkinInfo(
  _In_        DWORD             NumVertices,
  _In_  const D3DVERTEXELEMENT9 *pDeclaration,
  _In_        DWORD             NumBones,
  _Out_       LPD3DXSKININFO    *ppSkinInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NumVertices* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Nombre de vertex pour le maillage de l’apparence.

</dd> <dt>

*pDeclaration* \[ dans\]
</dt> <dd>

Type : **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Tableau d’éléments [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , décrivant le format de vertex pour le maillage retourné.

</dd> <dt>

*NumBones* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Nombre d’OS pour le maillage de l’apparence.

</dd> <dt>

*ppSkinInfo* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Adresse d’un pointeur vers une interface [**ID3DXSkinInfo**](id3dxskininfo.md) représentant l’objet de maillage d’apparence créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être : E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Utilisez [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) pour remplir l’objet de maillage d’apparence vide retourné par cette méthode.

## <a name="requirements"></a>Configuration requise



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

 

 
