---
description: Récupère l’index de l’influence osseuse affectant un seul vertex.
ms.assetid: vs|directx_sdk|~\id3dxskininfo__findbonevertexinfluenceindex.htm
title: 'ID3DXSkinInfo :: FindBoneVertexInfluenceIndex, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.FindBoneVertexInfluenceIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 05a86e98e5001092700fdec12f2a7afc33ddf082
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106543020"
---
# <a name="id3dxskininfofindbonevertexinfluenceindex-method"></a>ID3DXSkinInfo :: FindBoneVertexInfluenceIndex, méthode

Récupère l’index de l’influence osseuse affectant un seul vertex.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT FindBoneVertexInfluenceIndex(
  [in]      DWORD boneNum,
  [in]      DWORD vertexNum,
  [in, out] DWORD *pInfluenceIndex
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*boneNum* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Index du segment. Doit être compris entre 0 et le nombre d’os.

</dd> <dt>

*vertexNum* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Index du vertex pour lequel l’influence du segment est recherchée. Doit être compris entre 0 et le nombre de vertex dans le maillage.

</dd> <dt>

*pInfluenceIndex* \[ in, out\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur vers l’index de l’influence du segment qui affecte vertexNum.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si le segment spécifié n’influence pas le vertex donné, S \_ false est retourné. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::GetBoneVertexInfluence**](id3dxskininfo--getbonevertexinfluence.md)
</dt> <dt>

[**ID3DXSkinInfo::SetBoneVertexInfluence**](id3dxskininfo--setbonevertexinfluence.md)
</dt> <dt>

[**ID3DXSkinInfo::GetBoneInfluence**](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
