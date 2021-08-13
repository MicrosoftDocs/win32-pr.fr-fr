---
description: Créer un sprite pour dessiner une texture 2D. Remarque au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser Direct2D et la bibliothèque DirectXTK, la classe SpriteBatch.
ms.assetid: 64efb8e4-da0b-4e67-874a-e0bb0083961c
title: D3DX10CreateSprite, fonction (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSprite
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6f67a0a6e0be8a3ea71ff1eef46d72b6cf080d028e7cc32f72a52db6a209cea4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118541057"
---
# <a name="d3dx10createsprite-function"></a>D3DX10CreateSprite fonction)

Créer un sprite pour dessiner une texture 2D.

> [!Note]  
> Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser [Direct2D](../direct2d/direct2d-portal.md) et la bibliothèque [DirectXTK](https://github.com/Microsoft/DirectXTK) , la classe **SpriteBatch** .

 

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX10CreateSprite(
  _In_  ID3D10Device   *pDevice,
  _In_  UINT           cDeviceBufferSize,
  _Out_ LPD3DX10SPRITE *ppSprite
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Pointeur vers l’appareil (voir [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) qui dessinera le sprite.

</dd> <dt>

*cDeviceBufferSize* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Taille de la mémoire tampon de vertex, en nombre de sprites, qui sera envoyée à l’appareil lorsque [**ID3DX10Sprite :: Flush**](id3dx10sprite-flush.md) ou [**ID3DX10Sprite ::D rawspritesimmediate**](id3dx10sprite-drawspritesimmediate.md) est appelée. Ce nombre doit être faible si vous savez que vous allez afficher un petit nombre de sprites à la fois (pour économiser la mémoire) et un grand nombre si vous savez que vous allez afficher un grand nombre de sprites à la fois. La valeur maximale est 4096. Si la valeur 0 est spécifiée, la taille de la mémoire tampon du vertex sera automatiquement définie sur 4096.

</dd> <dt>

*ppSprite* \[ à\]
</dt> <dd>

Type : **[ **LPD3DX10SPRITE**](id3dx10sprite.md)\***

Adresse d’un pointeur vers une interface Sprite (voir [**interface ID3DX10Sprite**](id3dx10sprite.md)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est S \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions usage général](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
