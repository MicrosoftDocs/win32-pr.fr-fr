---
description: Obtient le nom du segment à partir de l’index de l’OS.
ms.assetid: f56faf41-c119-4cdd-bb8a-86fc99ff5893
title: 'ID3DXSkinInfo :: GetBoneName, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fa56b175d9047935b9f92829823ba2608536ddabb90cb0ad674b86b73cc17475
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674729"
---
# <a name="id3dxskininfogetbonename-method"></a>ID3DXSkinInfo :: GetBoneName, méthode

Obtient le nom du segment à partir de l’index de l’OS.

## <a name="syntax"></a>Syntaxe


```C++
LPCSTR GetBoneName(
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

## <a name="return-value"></a>Valeur retournée

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Retourne le nom du segment. Ne libérez pas cette chaîne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetBoneName**](id3dxskininfo--setbonename.md)
</dt> <dt>

[**ID3DXSkinInfo::GetNumBones**](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 
