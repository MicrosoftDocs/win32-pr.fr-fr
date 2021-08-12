---
description: Obtient la mémoire tampon d’index de maillage.
ms.assetid: d9152f3b-c8e6-4def-8cf1-a517ca4d34e7
title: 'ID3DXPatchMesh :: GetIndexBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c7b32c5414f72b1dd16a6c309294056e81468f8e039e73d1d43c05d5ac3dd0f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294352"
---
# <a name="id3dxpatchmeshgetindexbuffer-method"></a>ID3DXPatchMesh :: GetIndexBuffer, méthode

Obtient la mémoire tampon d’index de maillage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetIndexBuffer(
  [out, retval] LPDIRECT3DINDEXBUFFER9 *ppIB
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppIB* \[ out, retval\]
</dt> <dd>

Type : **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***

Pointeur vers la mémoire tampon d’index.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Le tampon d’index contient l’ordonnancement des vertex dans la mémoire tampon de vertex. Le tampon d’index est utilisé pour accéder à la mémoire tampon de vertex lorsque le maillage est rendu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
