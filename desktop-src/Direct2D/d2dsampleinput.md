---
title: D2DSampleInput, fonction (D2d1effecthelpers. h)
description: Échantillonne l’entrée N à la position UV. Disponible uniquement pour les entrées complexes.
ms.assetid: 8C1E3B23-D05B-4FCC-B32F-A5870A7C3FEF
keywords:
- D2DSampleInput fonction Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c887221ade413b63456ecb3c4a91c7a5b480858b04e1f34e89506fdcf071dfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075273"
---
# <a name="d2dsampleinput-function"></a>D2DSampleInput fonction)

Échantillonne l’entrée N à la position UV. Disponible uniquement pour les entrées complexes.

## <a name="syntax"></a>Syntaxe

``` syntax
float4 WINAPI D2DSampleInput(
  in uint N,
  in float2 uv
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*N* \[ dans\]
</dt> <dd>

Numéro d’entrée.

</dd> <dt>

*UV* \[ dans\]
</dt> <dd>

Position UV.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne un **float4**, au format TEXCOORDN.

## <a name="remarks"></a>Remarques

L’exemple suivant illustre la fonction utilisée pour calculer les normales des surfaces.

``` syntax
   
float3 CalculateSurfaceNormal(TAPARGS)  
{  
    float3 normal = float3(0, 0, 1.0);  
  
    // unrolled loop  
    normal.xy += tap1.zw * D2DSampleInput(0, tap1.xy).a;  
    normal.xy += tap2.zw * D2DSampleInput(0, tap2.xy).a;  
    normal.xy += tap3.zw * D2DSampleInput(0, tap3.xy).a;  
    normal.xy += tap4.zw * D2DSampleInput(0, tap4.xy).a;  
    normal.xy += tap5.zw * D2DSampleInput(0, tap5.xy).a;  
    normal.xy += tap6.zw * D2DSampleInput(0, tap6.xy).a;  
  
    normal = normalize(normal);  
      
    return normal;  
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

 

 





