---
description: Crée une maille à partir d’un maillage de contrôle-correctif.
ms.assetid: 50e4f7aa-a6b8-4a2b-9813-a9448f408d06
title: D3DXCreatePatchMesh, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aa4e1292f4b5c42515351d89dc7fc039f1f6f29201da72a78e07f447818e0f91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988639"
---
# <a name="d3dxcreatepatchmesh-function"></a>D3DXCreatePatchMesh fonction)

Crée une maille à partir d’un maillage de contrôle-correctif.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreatePatchMesh(
  _In_  const D3DXPATCHINFO     *pInfo,
  _In_        DWORD             dwNumPatches,
  _In_        DWORD             dwNumVertices,
  _In_        DWORD             dwOptions,
  _In_  const D3DVERTEXELEMENT9 *pDecl,
  _In_        LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_       LPD3DXPATCHMESH   *pPatchMesh
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pinfo* \[ dans\]
</dt> <dd>

Type : **const [**D3DXPATCHINFO**](d3dxpatchinfo.md) \***

Structure des informations sur les correctifs. Pour plus d’informations, consultez [**D3DXPATCHINFO**](d3dxpatchinfo.md).

</dd> <dt>

*dwNumPatches* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Nombre de correctifs.

</dd> <dt>

*dwNumVertices* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Nombre de vertex de contrôle dans le correctif.

</dd> <dt>

*dwOptions* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Inutilisé. Réservé pour une utilisation ultérieure.

</dd> <dt>

*pDecl* \[ dans\]
</dt> <dd>

Type : **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Tableau d’éléments [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , décrivant le format de vertex pour le maillage retourné.

</dd> <dt>

*pD3DDevice* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Pointeur l’appareil qui crée la maille de correctifs. Consultez [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).

</dd> <dt>

*pPatchMesh* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***

Pointeur vers l’objet [**ID3DXPatchMesh**](id3dxpatchmesh.md) créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Cette méthode prend une maille de correction d’entrée et la convertit en maillage fractionné. Les maillages de correctifs utilisent des mémoires tampons d’index 16 bits. Par conséquent, les index de [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md) sont de 16 bits.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXPATCHINFO**](d3dxpatchinfo.md)
</dt> </dl>

 

 
