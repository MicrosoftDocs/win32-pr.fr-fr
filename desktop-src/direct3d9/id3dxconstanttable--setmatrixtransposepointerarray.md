---
description: 'ID3DXConstantTable :: SetMatrixTransposePointerArray, méthode-définit un tableau de pointeurs vers des matrices transposées.'
ms.assetid: f2db10cb-a146-412d-8de8-f093253470fd
title: 'ID3DXConstantTable :: SetMatrixTransposePointerArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixTransposePointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aa21e6a19fe3ebb8ea1ee9dfecaa9e7370c5dd412d9dea8599987a55dc1858d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951849"
---
# <a name="id3dxconstanttablesetmatrixtransposepointerarray-method"></a>ID3DXConstantTable :: SetMatrixTransposePointerArray, méthode

Définit un tableau de pointeurs vers des matrices transposées.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        **ppMatrix,
  [in]       UINT              Count
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

Identificateur unique du tableau de constantes de matrice. Consultez [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).

</dd> <dt>

*ppMatrix* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***

Tableau de pointeurs vers les matrices transposées. Consultez [**D3DXMATRIX**](d3dxmatrix.md).

</dd> <dt>

*Nombre* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de matrices dans le tableau.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Remarques

Une matrice transposée contient des données de colonne principales ; autrement dit, chaque vecteur est contenu dans une colonne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 
