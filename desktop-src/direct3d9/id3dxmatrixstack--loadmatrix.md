---
description: 'ID3DXMATRIXStack :: LoadMatrix, méthode (D3dx9math. h)-charge la matrice donnée dans la matrice actuelle.'
ms.assetid: c4c5ac50-238f-4b41-8ea9-7e48ffd03fc5
title: 'ID3DXMATRIXStack :: LoadMatrix, méthode (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2ee7e5cae4d28b81b805faa4f113d0819f1eae9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127516765"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx9mathh"></a>ID3DXMATRIXStack :: LoadMatrix, méthode (D3dx9math. h)

Charge la matrice donnée dans la matrice actuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMat* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Pointeur vers la structure [**D3DXMATRIX**](d3dxmatrix.md) chargée dans la matrice actuelle.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes

Notez que cette méthode n’ajoute pas d’élément à la pile ; au lieu de cela, elle remplace la matrice actuelle par la matrice fournie.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::LoadIdentity**](id3dxmatrixstack--loadidentity.md)
</dt> </dl>

 

 




