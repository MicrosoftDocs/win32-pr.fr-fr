---
description: Applique les enveloppes logicielles aux vertex cibles en fonction des matrices actuelles.
ms.assetid: 4858dfd4-dc0d-4852-9165-8ae1b40386d4
title: 'ID3DXSkinInfo :: UpdateSkinnedMesh, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.UpdateSkinnedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 645e6ae1e1cb84991b352c250b137cd3ae2491f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519257"
---
# <a name="id3dxskininfoupdateskinnedmesh-method"></a>ID3DXSkinInfo :: UpdateSkinnedMesh, méthode

Applique les enveloppes logicielles aux vertex cibles en fonction des matrices actuelles.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UpdateSkinnedMesh(
  [in] const D3DXMATRIX *pBoneTransforms,
  [in] const D3DXMATRIX *pBoneInvTransposeTransforms,
  [in]       LPCVOID    pVerticesSrc,
  [in]       PVOID      pVerticesDst
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pBoneTransforms* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Matrice de transformation osseuse.

</dd> <dt>

*pBoneInvTransposeTransforms* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Transposer l’inverse de la matrice de transformation osseuse.

</dd> <dt>

*pVerticesSrc* \[ dans\]
</dt> <dd>

Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**

Pointeur vers la mémoire tampon qui contient les vertex sources.

</dd> <dt>

*pVerticesDst* \[ dans\]
</dt> <dd>

Type : **[ **pVoid**](../winprog/windows-data-types.md)**

Pointeur vers la mémoire tampon qui contient les sommets de destination.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes

Lorsqu’elle est utilisée pour l’apparence des vertex avec deux éléments de position, cette méthode enveloppe le deuxième élément de position avec l’inverse du segment au lieu du segment lui-même.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
