---
description: Crée un maillage N-patch à partir d’un maillage de triangles.
ms.assetid: f565ed0b-72fc-4184-b423-f68b0acfafb0
title: D3DXCreateNPatchMesh, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateNPatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fb23022bfa79ba9bc429bc76a5c42892403b783b4ed634e9b7887b74db126b87
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119241369"
---
# <a name="d3dxcreatenpatchmesh-function"></a>D3DXCreateNPatchMesh fonction)

Crée un maillage N-patch à partir d’un maillage de triangles.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreateNPatchMesh(
  _In_    LPD3DXMESH      pMeshSysMem,
  _Inout_ LPD3DXPATCHMESH *pPatchMesh
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMeshSysMem* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

Adresse d’un pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) qui représente l’objet de maillage de triangle.

</dd> <dt>

*pPatchMesh* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***

Adresse d’un pointeur vers une interface [**ID3DXPatchMesh**](id3dxpatchmesh.md) qui représente l’objet de maillage de correctif créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




