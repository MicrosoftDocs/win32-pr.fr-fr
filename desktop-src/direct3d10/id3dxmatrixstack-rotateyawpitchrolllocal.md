---
description: 'ID3DXMATRIXStack :: RotateYawPitchRollLocal, méthode (D3DX10. h) : pivote (par rapport à l’espace de coordonnées local de l’objet) autour d’un axe arbitraire.'
ms.assetid: da023816-5176-460d-ab6b-909b89cc46cd
title: 'ID3DXMATRIXStack :: RotateYawPitchRollLocal, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateYawPitchRollLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 840e51c420d3c5241edc410233b03dd948c408dda7e81a1aba6d104066cd6fe8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118301692"
---
# <a name="id3dxmatrixstackrotateyawpitchrolllocal-method-d3dx10h"></a>ID3DXMATRIXStack :: RotateYawPitchRollLocal, méthode (D3DX10. h)

Pivote (par rapport à l’espace de coordonnées local de l’objet) autour d’un axe arbitraire.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RotateYawPitchRollLocal(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Lacet* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Lacet autour de l’axe y en radians.

</dd> <dt>

*Espacement* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

La hauteur autour de l’axe x en radians.

</dd> <dt>

*Roll* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Roulement autour de l’axe z en radians.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK.

## <a name="remarks"></a>Notes

Cette méthode ajoute la rotation à la pile de matrice avec la matrice de rotation calculée similaire à ce qui suit :


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



Étant donné que la rotation est multipliée à gauche à la pile de matrices, la rotation est relative à l’espace de coordonnées local de l’objet.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
