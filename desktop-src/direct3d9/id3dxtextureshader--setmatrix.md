---
description: 'ID3DXTextureShader :: SetMatrix, méthode-définit une matrice non transposée.'
ms.assetid: 891441ea-09d5-43b6-a080-578d7f8e4586
title: 'ID3DXTextureShader :: SetMatrix, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e0d905a3d73bb357e7988f4cc5a749740b796c1793ca912a2f3af471893d65f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729012"
---
# <a name="id3dxtextureshadersetmatrix-method"></a>ID3DXTextureShader :: SetMatrix, méthode

Définit une matrice non transposée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hConstant* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificateur unique de la matrice de constantes. Consultez [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*pMatrix* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Pointeur désignant une matrice non transposée. Consultez [**D3DXMATRIX**](d3dxmatrix.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Remarques

Une matrice non transposée contient des données de lignes principales ; autrement dit, chaque vecteur est contenu dans une ligne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 




