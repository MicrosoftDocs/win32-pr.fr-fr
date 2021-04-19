---
description: Ajoute un sprite à la liste des sprites regroupés par lots.
ms.assetid: 8f5c43a2-68dd-44a9-be2f-f76d9fa2d900
title: ID3DXSprite ::D méthode brute (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9cba7b12c55e7ab9f5f939347a8b500ec4965f75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537284"
---
# <a name="id3dxspritedraw-method"></a>ID3DXSprite ::D méthode brute

Ajoute un sprite à la liste des sprites regroupés par lots.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Draw(
  [in]       LPDIRECT3DTEXTURE9 pTexture,
  [in] const RECT               *pSrcRect,
  [in] const D3DXVECTOR3        *pCenter,
  [in] const D3DXVECTOR3        *pPosition,
  [in]       D3DCOLOR           Color
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTexture* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Pointeur vers une interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) qui représente la texture du sprite.

</dd> <dt>

*pSrcRect* \[ dans\]
</dt> <dd>

Type : **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui indique la partie de la texture source à utiliser pour le sprite. Si ce paramètre a la **valeur null**, la totalité de l’image source est utilisée pour le sprite.

</dd> <dt>

*pCenter* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers un vecteur [**D3DXVECTOR3**](d3dxvector3.md) qui identifie le centre du sprite. Si cet argument a la **valeur null**, le point (0, 0, 0) est utilisé, qui est l’angle supérieur gauche.

</dd> <dt>

*pPosition* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers un vecteur [**D3DXVECTOR3**](d3dxvector3.md) qui identifie la position du sprite. Si cet argument a la **valeur null**, le point (0, 0, 0) est utilisé, qui est l’angle supérieur gauche.

</dd> <dt>

*Couleur* \[ dans\]
</dt> <dd>

Type : **[ **D3DCOLOR**](d3dcolor.md)**

Type de [**D3DCOLOR**](d3dcolor.md) . La couleur et les canaux alpha sont modulés par cette valeur. La valeur 0xFFFFFFFF conserve la couleur source d’origine et les données alpha. Utilisez la macro [**D3DCOLOR \_ RVBA**](d3dcolor-rgba.md) pour aider à générer cette couleur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="remarks"></a>Notes

Pour mettre à l’échelle, faire pivoter ou traduire un sprite, appelez [**ID3DXSprite :: setTransform**](id3dxsprite--settransform.md) avec une matrice qui contient les valeurs d’échelle, de rotation et de translation (SRT), avant d’appeler ID3DXSprite ::D RAW. Pour plus d’informations sur la définition de valeurs SRT dans une matrice, consultez [transformations de matrice](transforms.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite::GetTransform**](id3dxsprite--gettransform.md)
</dt> </dl>

 

 
