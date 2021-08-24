---
description: Définit la matrice de décalage de l’OS.
ms.assetid: f8ac1117-510d-42af-a6bf-422cbaaf6b74
title: 'ID3DXSkinInfo :: SetBoneOffsetMatrix, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneOffsetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d5daf20697777cfbf1b72d4ab18936f81c262ba9b23379d6089bffca8b9a516
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674709"
---
# <a name="id3dxskininfosetboneoffsetmatrix-method"></a>ID3DXSkinInfo :: SetBoneOffsetMatrix, méthode

Définit la matrice de décalage de l’OS.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetBoneOffsetMatrix(
  [in]       DWORD      Bone,
  [in] const D3DXMATRIX *pBoneTransform
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*OS* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Numéro d’os.

</dd> <dt>

*pBoneTransform* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Pointeur vers la matrice de décalage de l’OS.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Remarques

Les noms osseux sont retournés par [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::GetBoneOffsetMatrix**](id3dxskininfo--getboneoffsetmatrix.md)
</dt> </dl>

 

 
