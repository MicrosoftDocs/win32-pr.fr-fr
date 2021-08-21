---
description: Crée un maillage de correctifs avec la déclaration de vertex spécifiée.
ms.assetid: cc488cd3-fb38-468f-8aec-17c6ed842582
title: 'ID3DXPatchMesh :: CloneMesh, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1418bf890ae0ba10adec9e0c7de74eb5f118f91566554eb325cc2badaedfc613
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294380"
---
# <a name="id3dxpatchmeshclonemesh-method"></a>ID3DXPatchMesh :: CloneMesh, méthode

Crée un maillage de correctifs avec la déclaration de vertex spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDecl,
  [out, retval]       LPD3DXPATCHMESH   *pMesh
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Options* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison d’un ou de plusieurs indicateurs [**D3DXMESH**](./d3dxmesh.md) qui spécifient des options de création pour le maillage.

</dd> <dt>

*pDecl* \[ dans\]
</dt> <dd>

Type : **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Tableau d’éléments [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) qui spécifient le format de vertex pour les vertex dans le maillage de sortie.

</dd> <dt>

*pMesh* \[ out, retval\]
</dt> <dd>

Type : **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***

Adresse d’un pointeur vers une interface [**ID3DXPatchMesh**](id3dxpatchmesh.md) qui représente le maillage cloné.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

**CloneMesh** convertit la mémoire tampon de vertex en la nouvelle déclaration de vertex. Les entrées de la déclaration de vertex qui sont nouvelles dans le maillage d’origine ont la valeur 0. Si le maillage actuel a une contiguïté, le nouveau maillage aura également une contiguïté.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
