---
description: 'DXGI_RGBA structure : représente une valeur de couleur avec alpha, qui est utilisée pour la transparence.'
ms.assetid: 5F9DDDC1-644E-4DA2-8E3D-F157789809E7
title: Structure DXGI_RGBA (DXGItype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_RGBA
api_type:
- HeaderDef
api_location:
- DXGItype.h
ms.openlocfilehash: 2c1ef7bd65645fa68e699b6f70894e72452a707eac29ab0d35e56364a66604bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627419"
---
# <a name="dxgi_rgba-structure"></a>DXGI \_ RVBA, structure

Représente une valeur de couleur avec alpha, qui est utilisé pour la transparence.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _DXGI_RGBA {
  float r;
  float g;
  float b;
  float a;
} DXGI_RGBA;
```



## <a name="members"></a>Membres

<dl> <dt>

**r**
</dt> <dd>

Valeur à virgule flottante qui spécifie le composant rouge d’une couleur. Cette valeur est généralement comprise entre 0,0 et 1,0. La valeur 0,0 indique l’absence totale du composant rouge, tandis que la valeur 1,0 indique que le rouge est entièrement présent.

</dd> <dt>

**activée**
</dt> <dd>

Valeur à virgule flottante qui spécifie le composant vert d’une couleur. Cette valeur est généralement comprise entre 0,0 et 1,0. La valeur 0,0 indique l’absence totale du composant vert, tandis que la valeur 1,0 indique que le vert est entièrement présent.

</dd> <dt>

**b**
</dt> <dd>

Valeur à virgule flottante qui spécifie le composant bleu d’une couleur. Cette valeur est généralement comprise entre 0,0 et 1,0. La valeur 0,0 indique l’absence totale du composant bleu, tandis que la valeur 1,0 indique que le bleu est entièrement présent.

</dd> <dt>

**un**
</dt> <dd>

Valeur à virgule flottante qui spécifie le composant alpha d’une couleur. Cette valeur est généralement comprise entre 0,0 et 1,0. Une valeur de 0,0 indique une transparence complète, tandis que la valeur 1,0 indique une opacité totale.

</dd> </dl>

## <a name="remarks"></a>Remarques

Vous pouvez définir les membres de cette structure sur des valeurs situées en dehors de la plage comprise entre 0 et 1 pour implémenter des effets inhabituels. Les valeurs supérieures à 1 produisent des lumières fortes qui ont tendance à nettoyer une scène. Les valeurs négatives produisent des lumières sombres qui suppriment en fait la lumière d’une scène.

Le type d’en-tête DXGItype. h-définit **dxgi \_ RVBA** comme un alias de [**D3DCOLORVALUE**](d3dcolorvalue.md), comme suit :


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



Vous pouvez utiliser **dxgi \_ RVBA** avec [**IDXGISwapChain1 :: SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1 :: GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)et le [**\_ \_ mode Alpha dxgi**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | mise à jour Windows 8 et de plateforme pour les applications de bureau Windows 7 \[ \|\]<br/>                        |
| Serveur minimal pris en charge<br/> | mise à jour Windows Server 2012 et de plateforme pour les applications de bureau Windows Server 2008 R2 \[ \|\]<br/> |
| En-tête<br/>                   | <dl> <dt>DXGItype. h</dt> </dl>                      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures DXGI](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[**D3DCOLORVALUE**](d3dcolorvalue.md)
</dt> <dt>

[**D3DCOLORVALUE (dans Direct3D 9)**](../direct3d9/d3dcolorvalue.md)
</dt> </dl>

 

 
