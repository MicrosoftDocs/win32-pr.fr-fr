---
description: Définit la transformation Sprite.
ms.assetid: 87dfc169-b647-4a96-897d-abbe765ea9e2
title: 'ID3DXSprite :: SetTransform, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 316e7e2c68dfa8f25a712c2077ece03d09455050
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211825"
---
# <a name="id3dxspritesettransform-method"></a>ID3DXSprite :: SetTransform, méthode

Définit la transformation Sprite.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetTransform(
  [in] const D3DXMATRIX *pTransform
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTransform* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Pointeur vers un [**D3DXMATRIX**](d3dxmatrix.md) qui contient une transformation du sprite à partir de l’espace universel d’origine. Utilisez cette transformation pour mettre à l’échelle, faire pivoter ou transformer le sprite.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[Transformations (Direct3D 9)](transforms.md)
</dt> </dl>

 

 




