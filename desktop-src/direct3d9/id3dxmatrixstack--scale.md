---
description: 'ID3DXMATRIXStack :: Scale, méthode (D3dx9math. h)-mettre à l’échelle la matrice actuelle à propos de l’origine de la coordonnée universelle.'
ms.assetid: 6c4ef625-736e-41a0-8a79-4d71e8685754
title: 'ID3DXMATRIXStack :: Scale, méthode (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c140e1a4b39d79c3d28b13fa8ad3bf357b3beb903132d16f7221d52e8ed11eb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847539"
---
# <a name="id3dxmatrixstackscale-method-d3dx9mathh"></a>ID3DXMATRIXStack :: Scale, méthode (D3dx9math. h)

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

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK.

## <a name="remarks"></a>Remarques

Cette méthode multiplie la matrice actuelle par la matrice de mise à l’échelle calculée. La transformation concerne l’origine du monde actuel.


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::ScaleLocal**](id3dxmatrixstack--scalelocal.md)
</dt> </dl>

 

 
