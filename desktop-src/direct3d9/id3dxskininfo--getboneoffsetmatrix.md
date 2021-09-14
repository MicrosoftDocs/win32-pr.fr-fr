---
description: Obtient la matrice de décalage de l’OS.
ms.assetid: 99d47635-ffae-4668-a37c-b15442148fa1
title: 'ID3DXSkinInfo :: GetBoneOffsetMatrix, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneOffsetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fce108dc1d0eb08f198ae9375ac35ed149c5e760
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918264"
---
# <a name="id3dxskininfogetboneoffsetmatrix-method"></a>ID3DXSkinInfo :: GetBoneOffsetMatrix, méthode

Obtient la matrice de décalage de l’OS.

## <a name="syntax"></a>Syntaxe


```C++
LPD3DXMATRIX GetBoneOffsetMatrix(
  [in] DWORD Bone
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*OS* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Numéro d’os.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **LPD3DXMATRIX**](d3dxmatrix.md)**

Retourne un pointeur vers la matrice de décalage de l’OS. Ne libérez pas ce pointeur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**SetBoneOffsetMatrix**](id3dxskininfo--setboneoffsetmatrix.md)
</dt> <dt>

[**GetNumBones**](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 
