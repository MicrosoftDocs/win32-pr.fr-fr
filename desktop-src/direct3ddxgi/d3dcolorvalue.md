---
description: 'D3DCOLORVALUE structure (Dxgitype. h) : représente une valeur de couleur avec alpha, qui est utilisée pour la transparence.'
ms.assetid: 27A86A10-FC0E-421E-BEA7-2DEB539849BB
title: D3DCOLORVALUE, structure (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLORVALUE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: ba2e4731e1fd308c3b87cb5d1856020e5471f5fe0eac8f8cc99de3e3f32ded5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117910035"
---
# <a name="d3dcolorvalue-structure-dxgitypeh"></a>D3DCOLORVALUE, structure (Dxgitype. h)

Représente une valeur de couleur avec alpha, qui est utilisé pour la transparence.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
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

Le type d’en-tête DXGItype. h-définit [**dxgi \_ RVBA**](dxgi-rgba.md) comme un alias de **D3DCOLORVALUE**, comme suit :


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



Vous pouvez utiliser D3DCOLORVALUE ou [**dxgi \_ RVBA**](dxgi-rgba.md) avec [**IDXGISwapChain1 :: SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1 :: GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)et le [**\_ \_ mode Alpha dxgi**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Dxgitype. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures DXGI](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[**DXGI \_ RVBA**](dxgi-rgba.md)
</dt> </dl>

 

 




