---
description: Obtient une matrice nontransposed.
ms.assetid: d507c82c-b1a5-4e83-8921-5d45f52faba0
title: 'ID3DXBaseEffect :: GetMatrix, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrix
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 17d59700d8752526f3f4c48efeaf7f3e6bd985bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525096"
---
# <a name="id3dxbaseeffectgetmatrix-method"></a>ID3DXBaseEffect :: GetMatrix, méthode

Obtient une matrice nontransposed.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetMatrix(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hParameter* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificateur unique. Consultez [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pMatrix* \[ à\]
</dt> <dd>

Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Retourne une matrice nontransposed. Consultez [**D3DXMATRIX**](d3dxmatrix.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes

Une matrice nontransposed contient des données de lignes principales ; autrement dit, chaque vecteur est contenu dans une ligne.

Si la matrice de destination est plus grande que la matrice source, seuls les composants supérieurs gauches de la matrice de destination seront remplis et les composants restants seront définis sur zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetMatrix**](id3dxbaseeffect--setmatrix.md)
</dt> </dl>

 

 




