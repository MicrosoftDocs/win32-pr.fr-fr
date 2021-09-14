---
description: Crée un objet de maillage à l’aide d’un code de format de vertex flexible.
ms.assetid: 4681f181-8a16-42d4-bbfa-bdee5ed69fd3
title: D3DXCreateMeshFVF, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMeshFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9d5589b0f02bfcb85f9c0f0dc4dc5de69e2fb23
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127236988"
---
# <a name="d3dxcreatemeshfvf-function"></a>D3DXCreateMeshFVF fonction)

Crée un objet de maillage à l’aide d’un code de format de vertex flexible.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreateMeshFVF(
  _In_  DWORD             NumFaces,
  _In_  DWORD             NumVertices,
  _In_  DWORD             Options,
  _In_  DWORD             FVF,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NumFaces* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Nombre de faces de la maille. La plage valide pour ce nombre est supérieure à 0, et une valeur inférieure à la valeur DWORD Max, généralement 2 ³ ²-1, car le dernier index est réservé.

</dd> <dt>

*NumVertices* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Nombre de vertex pour le maillage. Ce paramètre doit être supérieur à 0.

</dd> <dt>

*Options* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison d’un ou de plusieurs indicateurs de l’énumération [**D3DXMESH**](./d3dxmesh.md) , en spécifiant les options de création du maillage.

</dd> <dt>

*Commission* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison de [D3DFVF](d3dfvf.md) qui décrit le format de vertex pour le maillage retourné. Cette fonction ne prend pas en charge D3DFVF \_ XYZRHW.

</dd> <dt>

*pD3DDevice* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l’objet appareil à associer à la maille.

</dd> <dt>

*ppMesh* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse d’un pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant l’objet de maillage créé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXFVFFromDeclarator**](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
