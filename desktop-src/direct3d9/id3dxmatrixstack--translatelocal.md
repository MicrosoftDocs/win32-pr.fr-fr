---
description: Détermine le produit de la matrice de traduction calculée, déterminé par les facteurs donnés (x, y et z) et la matrice actuelle.
ms.assetid: d4752a6c-2114-4016-a69f-dcc561d2c76b
title: 'ID3DXMATRIXStack :: TranslateLocal, méthode (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.TranslateLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 784e623ae47dfece9b395d423437fb6ce661b223
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211842"
---
# <a name="id3dxmatrixstacktranslatelocal-method-d3dx9mathh"></a>ID3DXMATRIXStack :: TranslateLocal, méthode (D3dx9math. h)

Détermine le produit de la matrice de traduction calculée, déterminé par les facteurs donnés (x, y et z) et la matrice actuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT TranslateLocal(
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

Facteur de translation sur l’axe x.

</dd> <dt>

*y* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Facteur de translation sur l’axe y.

</dd> <dt>

*z* \[\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Facteur de translation dans l’axe z.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK.

## <a name="remarks"></a>Notes

Cette méthode multiplie la matrice actuelle par la matrice de traduction calculée (la transformation concerne l’origine locale de l’objet).


```
    
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
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

[**ID3DXMATRIXStack :: translate**](id3dxmatrixstack--translate.md)
</dt> </dl>

 

 
