---
description: Dessinez un tableau de sprites.
ms.assetid: 3fcc7705-0d59-450e-b137-c9cb7ec6b1ea
title: ID3DX10Sprite ::D méthode rawSpritesImmediate (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesImmediate
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7fa4012f5f589c7bc0d1f789599da142194f6e08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323425"
---
# <a name="id3dx10spritedrawspritesimmediate-method"></a>ID3DX10Sprite ::D méthode rawSpritesImmediate

Dessinez un tableau de sprites. Cela envoie immédiatement les sprites à l’appareil pour le rendu, ce qui est différent de [**ID3DX10Sprite ::D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md) qui ajoute uniquement un tableau de sprites à un lot de sprites à restituer lorsque [**ID3DX10Sprite :: Flush**](id3dx10sprite-flush.md) est appelé. Cette méthode de dessin est particulièrement utile lors du dessin d’un grand nombre de sprites qui ont déjà été triés sur l’UC (ou qui n’ont pas besoin d’être triés), comme dans un système de particules. Elle doit être appelée entre les appels à [**ID3DX10Sprite :: Begin**](id3dx10sprite-begin.md) et [**ID3DX10Sprite :: end**](id3dx10sprite-end.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DrawSpritesImmediate(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites,
  [in] UINT          cbSprite,
  [in] UINT          flags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSprites* \[ dans\]
</dt> <dd>

Type : **[ **d3dx10 \_ Sprite**](d3dx10-sprite.md)\***

Tableau de sprites à dessiner. Consultez [**d3dx10 \_ Sprite**](d3dx10-sprite.md).

</dd> <dt>

*cSprites* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de sprites dans pSprites.

</dd> <dt>

*cbSprite* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Taille de la structure sprite que vous passez dans pSprites. Le passage de la valeur 0 est l’équivalent du passage de sizeof (D3DX10 \_ sprite).

</dd> <dt>

*indicateurs* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Réservé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
