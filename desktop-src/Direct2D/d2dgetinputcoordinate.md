---
title: D2DGetInputCoordinate, fonction (D2d1effecthelpers. h)
description: Retourne la valeur de l’TEXCOORDN d’entrée. Disponible uniquement pour les entrées complexes.
ms.assetid: 60125E23-53B3-45ED-89FE-684E79004F6B
keywords:
- D2DGetInputCoordinate fonction Direct2D
topic_type:
- apiref
api_name:
- D2DGetInputCoordinate
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3fe0d825dea70c8e5211b8c13f1e850fa513670bbc93de98f1f8e2b87ef046
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075293"
---
# <a name="d2dgetinputcoordinate-function"></a>D2DGetInputCoordinate fonction)

Retourne la valeur de l’TEXCOORDN d’entrée. Disponible uniquement pour les entrées complexes.

## <a name="syntax"></a>Syntaxe

``` syntax
float4 WINAPI D2DGetInputCoordinate(
  in uint N
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*N* \[ dans\]
</dt> <dd>

Numéro d’entrée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne un **float4**, au format TEXCOORDN.

## <a name="remarks"></a>Remarques

La coordonnée retournée par cette fonction se trouve dans l’espace Texel. Un nuanceur ne doit pas prendre de dépendances quant à la façon dont cette valeur est calculée. Il doit l’utiliser uniquement pour échantillonner l’entrée du nuanceur de pixels. Pour plus d’informations, consultez [Ajout d’un nuanceur de pixels à une transformation personnalisée](./custom-effects.md#adding-a-pixel-shader-to-a-custom-transform).

L’exemple suivant illustre la fonction utilisée pour un effet de mappage de déplacement.

``` syntax
float2 GetDisplacementOffset(float4 uv0, float4 uv1)  
{  
    // TODO: return the displacement offset 
}  
  
D2D_PS_ENTRY(DisplacementMapBilinear)  
{  
    const float4 coord0 = D2DGetInputCoordinate(0);  
    const float4 coord1 = D2DGetInputCoordinate(1);  
    return D2DSampleInput(0, GetDisplacementOffset(coord0, coord1) * coord0.zw + coord0.xy);  
}  
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D2d1effecthelpers. hlsli</dt> </dl> |
| DLL<br/>    | <dl> <dt>D2d1.dll</dt> </dl>                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liaison de nuanceurs d’effet](effect-shader-linking.md)
</dt> <dt>

[Applications auxiliaires HLSL](hlsl-helpers.md)
</dt> </dl>

 

