---
description: Décompose une matrice de transformation 3D générale en ses composants scalaires, de rotation et de translation.
ms.assetid: 3694769f-56e7-4983-924e-021c129462a2
title: D3DXMatrixDecompose, fonction (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDecompose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 507c8f177db0f71b3d333a8343e4166e649f424a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211913"
---
# <a name="d3dxmatrixdecompose-function-d3dx10mathh"></a>D3DXMatrixDecompose, fonction (D3DX10Math. h)

Décompose une matrice de transformation 3D générale en ses composants scalaires, de rotation et de translation.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXMatrixDecompose(
  _In_       D3DXVECTOR3    *pOutScale,
  _In_       D3DXQUATERNION *pOutRotation,
  _In_       D3DXVECTOR3    *pOutTranslation,
  _In_ const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pOutScale* \[ dans\]
</dt> <dd>

Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Pointeur vers le [**D3DXVECTOR3**](d3d10-d3dxvector3.md) de sortie qui contient les facteurs d’échelle appliqués le long des axes x, y et z.

</dd> <dt>

*pOutRotation* \[ dans\]
</dt> <dd>

Type : **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Pointeur vers le [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) qui décrit la rotation.

</dd> <dt>

*pOutTranslation* \[ dans\]
</dt> <dd>

Type : **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Pointeur vers le vecteur D3DXVECTOR3 qui décrit la traduction.

</dd> <dt>

*GCF* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Pointeur vers une matrice d’entrée [**D3DXMATRIX**](d3d10-d3dxmatrix.md) à décomposer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est S \_ OK. Si la fonction échoue, la valeur de retour peut être la suivante : D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions mathématiques](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
