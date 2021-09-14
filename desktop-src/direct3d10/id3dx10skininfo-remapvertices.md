---
description: Modifiez les vertex qui sont influencés par les segments.
ms.assetid: b0d71f3e-9a2d-469d-808b-2fa768cf14b0
title: 'ID3DX10SkinInfo :: RemapVertices, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapVertices
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cc51c912794135b456542bb9a8a779601681f393
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916708"
---
# <a name="id3dx10skininforemapvertices-method"></a>ID3DX10SkinInfo :: RemapVertices, méthode

Modifiez les vertex qui sont influencés par les segments.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RemapVertices(
  [in] UINT NewVertexCount,
  [in] UINT *pVertexRemap
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NewVertexCount* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nouveau nombre de vertex.

</dd> <dt>

*pVertexRemap* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Pointeur vers un tableau d’index de vertex qui décrivent le remappage. Par exemple, disons SkinInfo contient des vertex tels que bone0 est mappé à v0, bone1 à v1 et bone2 à v2, et Array avec 2, 1, 0 est spécifié pour pBoneRemap. Bone0 sera alors mappé à v2, bone1 à v1 et bone2 à v0.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être : E \_ OUTOFMEMORY ou e \_ INVALIDARG.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
