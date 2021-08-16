---
description: Clone un maillage à l’aide d’un déclarateur.
ms.assetid: 47e0329a-ea85-478d-af8b-cf85d2a779f6
title: 'ID3DXBaseMesh :: CloneMesh, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 97fec8b0881cdef43051afcb06d63ec20284cb116299912ce0acf7ac4c54a0f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118521862"
---
# <a name="id3dxbasemeshclonemesh-method"></a>ID3DXBaseMesh :: CloneMesh, méthode

Clone un maillage à l’aide d’un déclarateur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDeclaration,
  [in]                LPDIRECT3DDEVICE9 pDevice,
  [out, retval]       LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Options* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison d’un ou de plusieurs indicateurs [**D3DXMESH**](./d3dxmesh.md) spécifiant les options de création du maillage.

</dd> <dt>

*pDeclaration* \[ dans\]
</dt> <dd>

Type : **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Tableau d’éléments [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , qui spécifie le format de vertex pour les vertex dans le maillage de sortie.

</dd> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’objet périphérique associé à la maille.

</dd> <dt>

*ppCloneMesh* \[ out, retval\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse d’un pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant le maillage cloné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

**ID3DXBaseMesh :: CloneMesh** est utilisé pour reformater et modifier la disposition des données de vertex. Pour ce faire, créez un nouvel objet de maillage. Par exemple, utilisez-le pour ajouter de l’espace pour les normales, les coordonnées de texture, les couleurs, les poids, etc. qui n’étaient pas présents avant.

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

[**ID3DXBaseMesh::CloneMeshFVF**](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
