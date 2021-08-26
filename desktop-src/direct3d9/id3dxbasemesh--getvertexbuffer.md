---
description: 'ID3DXBaseMesh :: GetVertexBuffer, méthode-récupère la mémoire tampon de vertex associée à la maille.'
ms.assetid: 5caa6ce1-feab-4919-944e-f92fad3ad443
title: 'ID3DXBaseMesh :: GetVertexBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bc0fc1f47ba3ed27af8f06d1a1f5ea83b884cdbe645d8597cd9513e7ad5c0387
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118849"
---
# <a name="id3dxbasemeshgetvertexbuffer-method"></a>ID3DXBaseMesh :: GetVertexBuffer, méthode

Récupère la mémoire tampon de vertex associée à la maille.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetVertexBuffer(
  [out, retval] LPDIRECT3DVERTEXBUFFER9 *ppVB
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppVB* \[ out, retval\]
</dt> <dd>

Type : **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***

Adresse d’un pointeur vers une interface [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) , représentant l’objet de mémoire tampon de vertex associé à la maille.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
