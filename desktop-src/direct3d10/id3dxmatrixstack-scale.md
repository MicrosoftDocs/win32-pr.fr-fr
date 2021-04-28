---
description: 'ID3DXMATRIXStack :: Scale, méthode (D3DX10. h)-mettre à l’échelle la matrice actuelle à propos de l’origine de la coordonnée universelle.'
ms.assetid: d0f4b341-b3b6-42e4-84df-78f203c3728e
title: 'ID3DXMATRIXStack :: Scale, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Scale
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a7b4aceb53659fc2b1a4a95f964d068e6d7d2554
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107787"
---
# <a name="id3dxmatrixstackscale-method-d3dx10h"></a>ID3DXMATRIXStack :: Scale, méthode (D3DX10. h)

Mettre à l’échelle la matrice actuelle sur l’origine de la coordonnée universelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Scale(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*x* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Composant de mise à l’échelle sur l’axe x.

</dd> <dt>

*y* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Composant de mise à l’échelle sur l’axe y.

</dd> <dt>

*z* \[\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Composant de mise à l’échelle dans l’axe z.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK.

## <a name="remarks"></a>Notes 

Cette méthode multiplie la matrice actuelle par la matrice de mise à l’échelle calculée. La transformation concerne l’origine du monde actuel.


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



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

 

 
