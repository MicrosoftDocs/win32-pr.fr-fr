---
description: 'ID3DXMATRIXStack :: MultMatrix, méthode (D3dx9math. h)-détermine le produit de la matrice actuelle et la matrice donnée.'
ms.assetid: a673ce82-6fed-4a3f-8c37-d0db11195f06
title: 'ID3DXMATRIXStack :: MultMatrix, méthode (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d9d0808f1b23475b823ea43f55d93f8dacb01e4e491957fa34100110946fa72e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856459"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx9mathh"></a>ID3DXMATRIXStack :: MultMatrix, méthode (D3dx9math. h)

Détermine le produit de la matrice actuelle et de la matrice donnée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMat* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) à multiplier avec la matrice actuelle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Remarques

Cette méthode multiplie la matrice donnée à la matrice actuelle (la transformation concerne l’origine mondiale active).


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



Cette méthode n’ajoute pas d’élément à la pile, elle remplace la matrice actuelle par le produit de la matrice actuelle et la matrice donnée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md)
</dt> </dl>

 

 




