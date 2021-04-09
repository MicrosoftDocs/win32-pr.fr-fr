---
description: Définit un tableau de matrices transposées.
ms.assetid: 100288f2-44f0-4e75-bffb-78732c50a55c
title: 'ID3DXTextureShader :: SetMatrixTransposeArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixTransposeArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c9efd0c81cef8a72880a9755ca40e4dd8b4950ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953828"
---
# <a name="id3dxtextureshadersetmatrixtransposearray-method"></a>ID3DXTextureShader :: SetMatrixTransposeArray, méthode

Définit un tableau de matrices transposées.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetMatrixTransposeArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hConstant* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificateur unique du tableau de constantes de matrice. Consultez [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*pMatrix* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Tableau de matrices transposées. Consultez [**D3DXMATRIX**](d3dxmatrix.md).

</dd> <dt>

*Nombre* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de matrices dans le tableau.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes

Une matrice transposée contient des données de colonne principales ; autrement dit, chaque vecteur est contenu dans une colonne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
