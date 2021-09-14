---
description: Clone un objet d’informations d’apparence.
ms.assetid: 82d0a78a-95f3-4b09-bc1a-b4bc663e0850
title: 'ID3DXSkinInfo :: Clone, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Clone
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: edd9776b75d027a32b32b58c59fc82daaebfa3ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918279"
---
# <a name="id3dxskininfoclone-method"></a>ID3DXSkinInfo :: Clone, méthode

Clone un objet d’informations d’apparence.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Clone(
  [in, out] LPD3DXSKININFO *ppSkinInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppSkinInfo* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Adresse d’un pointeur vers un objet [**ID3DXSkinInfo**](id3dxskininfo.md) , qui contient l’objet cloné si la méthode réussit.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 




