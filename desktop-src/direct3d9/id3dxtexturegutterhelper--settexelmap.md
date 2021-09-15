---
description: Définit les coordonnées de texture (u, v) de chaque Texel.
ms.assetid: b1f8f5d6-568f-4868-87c9-9d6b1034d898
title: 'ID3DXTextureGutterHelper :: SetTexelMap, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetTexelMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ee00394e81dadf147d54dffe0dc02199b2274e9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403527"
---
# <a name="id3dxtexturegutterhelpersettexelmap-method"></a>ID3DXTextureGutterHelper :: SetTexelMap, méthode

Définit les coordonnées de texture (u, v) de chaque Texel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetTexelMap(
  [in] D3DXVECTOR2 *pTexelData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTexelData* \[ dans\]
</dt> <dd>

Type : **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Pointeur vers l’emplacement, en pixels (u, v), coordonnées de texture où chaque Texel se trouve.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




