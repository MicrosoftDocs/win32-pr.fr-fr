---
description: Clone un maillage à l’aide d’un code de format de vertex flexible.
ms.assetid: b7d23ea9-1a2f-46e3-bcb5-82040d2a1e12
title: 'ID3DXBaseMesh :: CloneMeshFVF, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMeshFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4cb3b0ad33e54e79464949f441842173fb48a180
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542154"
---
# <a name="id3dxbasemeshclonemeshfvf-method"></a>ID3DXBaseMesh :: CloneMeshFVF, méthode

Clone un maillage à l’aide d’un code de format de vertex flexible.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CloneMeshFVF(
  [in]          DWORD             Options,
  [in]          DWORD             FVF,
  [in]          LPDIRECT3DDEVICE9 pDevice,
  [out, retval] LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Options* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison d’un ou de plusieurs indicateurs [**D3DXMESH**](./d3dxmesh.md) spécifiant les options de création du maillage.

</dd> <dt>

*Commission* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison de codes de la Commission, qui spécifie le format de vertex pour les vertex dans le maillage de sortie. Pour obtenir les valeurs des codes, consultez [D3DFVF](d3dfvf.md).

</dd> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) représentant l’objet périphérique associé à la maille.

</dd> <dt>

*ppCloneMesh* \[ out, retval\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse d’un pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant le maillage cloné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

**ID3DXBaseMesh :: CloneMeshFVF** est utilisé pour reformater et modifier la disposition des données de vertex. Pour ce faire, créez un nouvel objet de maillage. Par exemple, utilisez-le pour ajouter de l’espace pour les normales, les coordonnées de texture, les couleurs, les pondérations, etc. qui n’étaient pas déjà présentes.

[**ID3DXBaseMesh :: UpdateSemantics**](id3dxbasemesh--updatesemantics.md) met à jour la déclaration de vertex avec des informations sémantiques différentes sans modifier la disposition de la mémoire tampon de vertex. Cette méthode ne modifie pas le contenu de la mémoire tampon de vertex. Par exemple, utilisez-le pour réétiqueter une coordonnée de texture 3D en tant que biperpendiculaire ou tangente, ou vice versa.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**D3DXFVFFromDeclarator**](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
