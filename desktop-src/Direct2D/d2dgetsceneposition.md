---
title: D2DGetScenePosition, fonction (D2d1effecthelpers. h)
description: Retourne la valeur de la position de la scène d’entrée \_ . Disponible uniquement lorsque D2D \_ requiert \_ que \_ la position de scène soit déclarée dans le fichier source.
ms.assetid: 451E4C31-D93D-44B6-81D1-AC5FD986ACBD
keywords:
- D2DGetScenePosition fonction Direct2D
topic_type:
- apiref
api_name:
- D2DGetScenePosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace0ee4d60f8c140825e41ba47de941bca09e67c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534868"
---
# <a name="d2dgetsceneposition-function"></a>D2DGetScenePosition fonction)

Retourne la valeur de la position de la scène d’entrée \_ . Disponible uniquement lorsque D2D \_ requiert \_ que \_ la position de scène soit déclarée dans le fichier source.

## <a name="syntax"></a>Syntaxe

``` syntax
float4 WINAPI D2DGetScenePosition(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

La fonction retourne un **float4** au format position de la scène \_ .

## <a name="remarks"></a>Notes

L’exemple suivant illustre l’utilisation de la fonction dans la génération d’un modèle de dissolution.

``` syntax
D2D_PS_ENTRY(BlendDissolve)  
{  
    min16float4 dest   = D2DGetInput(0);  
    min16float4 source = D2DGetInput(1);  
  
    min16float4 color = dest;  
  
    if ((source.a > 0.0) && (source.a >= Rand((min16float2)D2DGetScenePosition().xy)))  
    {  
        // TODO: perform  dissovlve math
    }  
  
    return color;  
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

 

 





