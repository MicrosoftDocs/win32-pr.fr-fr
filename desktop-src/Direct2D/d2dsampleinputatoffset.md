---
title: D2DSampleInputAtOffset, fonction (D2d1effecthelpers. h)
description: Échantillonne l’entrée N à un offset de décalage par rapport à la coordonnée d’entrée. Disponible uniquement pour les entrées complexes.
ms.assetid: 4A01264E-04E3-49BD-9EF8-7834D9B8B0B8
keywords:
- D2DSampleInputAtOffset fonction Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInputAtOffset
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e316e4daf533f66bba9d34a6ac89c61094db536e19e710d1c5c235edb7d250c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075303"
---
# <a name="d2dsampleinputatoffset-function"></a>D2DSampleInputAtOffset fonction)

Échantillonne l’entrée N à un offset de décalage par rapport à la coordonnée d’entrée. Disponible uniquement pour les entrées complexes.

## <a name="syntax"></a>Syntaxe

``` syntax
float4 WINAPI D2DSampleInputAtOffset(
  in uint N,
  in float2 offset
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*N* \[ dans\]
</dt> <dd>

Numéro d’entrée.

</dd> <dt>

*décalage* \[ dans\]
</dt> <dd>

Décalage UV.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne un **float4**, au format TEXCOORDN.

## <a name="remarks"></a>Remarques

L’exemple suivant illustre la fonction utilisée dans le cadre d’un masque de dégradé de mise en surbrillance et d’ombres.

``` syntax
  
D2D_PS_ENTRY(HighlightsAndShadowsGradientMask)  
{  
    MIN_TYPE(float4) blurred = D2DGetInput(0);  
  
    // Compute X and Y gradients 
    MIN_TYPE(float) dX1 = D2DSampleInputAtOffset(0, float2(1, 0));
    MIN_TYPE(float) dX2 = D2DSampleInputAtOffset(0, float2(-1, 0));
    MIN_TYPE(float) dY1 = D2DSampleInputAtOffset(0, float2(0, 1));
    MIN_TYPE(float) dY2 = D2DSampleInputAtOffset(0, float2(0, -1));
    
    // TODO: math to calculate shadow gradients

    // Return the value in the alpha channel.  
    blurred.a = // TODO: math to calculate blurred value
  
    return blurred;  
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

 

 





