---
description: Définit l’influence minimale du segment. Les valeurs d’influence inférieures à cette valeur sont ignorées.
ms.assetid: 9af19c9e-bb6e-4f93-973f-5c38f88eea3d
title: 'ID3DXSkinInfo :: SetMinBoneInfluence, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetMinBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: abe9f1d7f9c54b9c3086160b974e2bc7dc659eb6dae3ff647f059627ff3ef145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747479"
---
# <a name="id3dxskininfosetminboneinfluence-method"></a>ID3DXSkinInfo :: SetMinBoneInfluence, méthode

Définit l’influence minimale du segment. Les valeurs d’influence inférieures à cette valeur sont ignorées.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetMinBoneInfluence(
  [in] FLOAT MinInfl
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*MinInfl* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Valeur d’influence minimale. Les valeurs d’influence inférieures à cette valeur sont ignorées.

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

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::GetMinBoneInfluence**](id3dxskininfo--getminboneinfluence.md)
</dt> </dl>

 

 
