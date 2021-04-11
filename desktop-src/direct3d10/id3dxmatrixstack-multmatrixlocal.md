---
description: Détermine le produit de la matrice donnée et de la matrice actuelle.
ms.assetid: 4d374a7b-99e0-4313-970d-b0e7cf3e97ce
title: 'ID3DXMATRIXStack :: MultMatrixLocal, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrixLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 095882c98169159beaca0ef6c98d13fe03b9aed2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211953"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx10h"></a>ID3DXMATRIXStack :: MultMatrixLocal, méthode (D3DX10. h)

Détermine le produit de la matrice donnée et de la matrice actuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT MultMatrixLocal(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*GCF* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Pointeur vers la structure D3DXMATRIX à multiplier avec la matrice actuelle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes

Cette méthode multiplie la matrice donnée à la matrice actuelle (la transformation concerne l’origine locale de l’objet).


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



Cette méthode n’ajoute pas d’élément à la pile, elle remplace la matrice actuelle par le produit de la matrice donnée et de la matrice actuelle.

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

 

 
