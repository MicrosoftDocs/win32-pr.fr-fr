---
description: 'Fonction D3DXComputeBoundingSphere (D3DX10math. h) : calcule une sphère englobante pour la maille.'
ms.assetid: 54f486d2-45e9-4fc1-90a3-97488ed4d900
title: D3DXComputeBoundingSphere, fonction (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingSphere
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0041d775b21d1af37bc51d6ec2f432e616b2abd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113297"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx10mathh"></a>D3DXComputeBoundingSphere, fonction (D3DX10math. h)

Calcule une sphère englobante pour la maille.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_ const D3DXVECTOR3 *pFirstPosition,
  _In_       DWORD       NumVertices,
  _In_       DWORD       dwStride,
  _In_       D3DXVECTOR3 *pCenter,
  _In_       FLOAT       *pRadius
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

Nombre d’octets entre les vecteurs de position.

</dd> <dt>

*pCenter* \[ dans\]
</dt> <dd>

Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Structure [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , qui définit le centre de coordonnées de la sphère englobante retournée.

</dd> <dt>

*pRadius* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Rayon de la sphère englobante retournée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

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

 

 
