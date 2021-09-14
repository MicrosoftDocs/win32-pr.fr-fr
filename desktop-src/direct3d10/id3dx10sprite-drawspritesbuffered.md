---
description: Ajoutez un tableau de sprites au lot de sprites à restituer.
ms.assetid: e6a9f806-7244-4139-b47e-c46dfab38a31
title: ID3DX10Sprite ::D méthode rawSpritesBuffered (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesBuffered
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72893f6a8c3cf82c67f014b4bdbb9a92453de319
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915571"
---
# <a name="id3dx10spritedrawspritesbuffered-method"></a>ID3DX10Sprite ::D méthode rawSpritesBuffered

Ajoutez un tableau de sprites au lot de sprites à restituer. Elle doit être appelée entre les appels à [**ID3DX10Sprite :: Begin**](id3dx10sprite-begin.md) et [**ID3DX10Sprite :: end**](id3dx10sprite-end.md), et [**ID3DX10Sprite :: Flush**](id3dx10sprite-flush.md) doit être appelé avant end pour envoyer tous les sprites traités par lot à l’appareil pour le rendu. Cette méthode de dessin est particulièrement utile lorsque vous dessinez un petit nombre de sprites que vous souhaitez mettre en mémoire tampon dans un grand lot, tel que des polices.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DrawSpritesBuffered(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites
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

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="requirements"></a>Spécifications



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

 

 
