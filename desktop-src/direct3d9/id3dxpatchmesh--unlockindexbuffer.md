---
description: Déverrouillez la mémoire tampon d’index.
ms.assetid: de3d0893-1596-42df-b049-6574c58ffa8d
title: 'ID3DXPatchMesh :: UnlockIndexBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.UnlockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 995a9ff69c4b1404035e323f85540f232ad01aa7dc46efaa5e42acd79429052d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120643"
---
# <a name="id3dxpatchmeshunlockindexbuffer-method"></a>ID3DXPatchMesh :: UnlockIndexBuffer, méthode

Déverrouillez la mémoire tampon d’index.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UnlockIndexBuffer();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

La mémoire tampon d’index est généralement verrouillée, écrite dans, puis déverrouillée pour la lecture.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 




