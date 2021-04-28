---
description: 'ID3DXMATRIXStack :: RotateAxisLocal, méthode (D3dx9math. h) : pivote (par rapport à l’espace de coordonnées local de l’objet) autour d’un axe arbitraire.'
ms.assetid: c7ef11e9-f4c4-4801-8f25-190066baeb52
title: 'ID3DXMATRIXStack :: RotateAxisLocal, méthode (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateAxisLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0bfcfd7301f90dcf49b03e7bbb3fd7e3b0de6c3e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093467"
---
# <a name="id3dxmatrixstackrotateaxislocal-method-d3dx9mathh"></a>ID3DXMATRIXStack :: RotateAxisLocal, méthode (D3dx9math. h)

Pivote (par rapport à l’espace de coordonnées local de l’objet) autour d’un axe arbitraire.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RotateAxisLocal(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PV* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers l’axe arbitraire de la rotation. Consultez [**D3DXVECTOR3**](d3dxvector3.md).

</dd> <dt>

*Angle* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Angle de rotation autour de l’axe arbitraire, en radians. Les angles sont mesurés dans le sens inverse des aiguilles d’une consiste à Rechercher l’origine dans l’axe arbitraire.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes 

Cette méthode ajoute la rotation à la pile de matrice avec la matrice de rotation calculée similaire à ce qui suit :


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



Étant donné que la rotation est multipliée à gauche à la pile de matrices, la rotation est relative à l’espace de coordonnées local de l’objet.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**D3DXMatrixRotationAxis**](d3dxmatrixrotationaxis.md)
</dt> <dt>

[**ID3DXMATRIXStack::RotateAxis**](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[**ID3DXMATRIXStack::RotateYawPitchRoll**](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> <dt>

[**ID3DXMATRIXStack::RotateYawPitchRollLocal**](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
