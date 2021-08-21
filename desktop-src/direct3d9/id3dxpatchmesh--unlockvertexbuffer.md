---
description: Déverrouillez la mémoire tampon de vertex.
ms.assetid: 98b82fd1-56e8-45f3-bf26-a1e3b54c2979
title: 'ID3DXPatchMesh :: UnlockVertexBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.UnlockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e9f710455ae08f3548b9a778716b1d8deebad15fcf53e8c9e4ede551b3a821d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294192"
---
# <a name="id3dxpatchmeshunlockvertexbuffer-method"></a>ID3DXPatchMesh :: UnlockVertexBuffer, méthode

Déverrouillez la mémoire tampon de vertex.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UnlockVertexBuffer();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

La mémoire tampon de vertex est généralement verrouillée, écrite dans, puis déverrouillée pour la lecture.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 




