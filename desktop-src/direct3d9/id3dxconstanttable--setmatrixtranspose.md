---
description: 'ID3DXConstantTable :: SetMatrixTranspose, méthode-définit une matrice transposée.'
ms.assetid: 1c4d64ce-64bd-47d4-9912-879f4834c0e8
title: 'ID3DXConstantTable :: SetMatrixTranspose, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixTranspose
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1d2026b2bb8b3baeae778e66a0b226c63fa2aeec09cb0a5e790f989161ff7552
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118521205"
---
# <a name="id3dxconstanttablesetmatrixtranspose-method"></a>ID3DXConstantTable :: SetMatrixTranspose, méthode

Définit une matrice transposée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetMatrixTranspose(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à la table constante.

</dd> <dt>

*hConstant* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificateur unique de la matrice de constantes. Consultez [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).

</dd> <dt>

*pMatrix* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Pointeur désignant une matrice transposée. Consultez [**D3DXMATRIX**](d3dxmatrix.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 
