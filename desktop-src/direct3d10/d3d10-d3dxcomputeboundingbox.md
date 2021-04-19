---
description: Calcule un cadre englobant orienté axe de coordonnées.
ms.assetid: 1b8f328c-2fe1-462e-b464-c8dd9dc03e67
title: D3DXComputeBoundingBox, fonction (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingBox
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9a93eb4a10f6c2b2fd7eda82afcc21158138a1e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531565"
---
# <a name="d3dxcomputeboundingbox-function-d3dx10mathh"></a>D3DXComputeBoundingBox, fonction (D3DX10math. h)

Calcule un cadre englobant orienté axe de coordonnées.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFirstPosition* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Pointeur vers la première position.

</dd> <dt>

*NumVertices* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Nombre de vertex.

</dd> <dt>

*dwStride* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Nombre ou nombre d’octets entre les vertex.

</dd> <dt>

*pMin* \[ à\]
</dt> <dd>

Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Pointeur vers une structure [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , décrivant l’angle inférieur gauche retourné du rectangle englobant.

</dd> <dt>

*pMax* \[ à\]
</dt> <dd>

Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Pointeur vers une structure [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , décrivant l’angle supérieur droit retourné du cadre englobant.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
