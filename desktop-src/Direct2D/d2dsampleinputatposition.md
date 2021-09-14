---
title: D2DSampleInputAtPosition, fonction (D2d1effecthelpers. h)
description: Échantillonne l’entrée N à une position de scène absolue, plutôt qu’une position relative à l’entrée. Disponible uniquement pour les entrées complexes.
ms.assetid: E839287F-91D1-4591-8DE7-1DFC3001A23D
keywords:
- D2DSampleInputAtPosition fonction Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInputAtPosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e12bba2b83f3956cf4b654c00b0650a6a0ce9a54
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113398"
---
# <a name="d2dsampleinputatposition-function"></a>D2DSampleInputAtPosition fonction)

Échantillonne l’entrée N à une position de scène absolue, plutôt qu’une position relative à l’entrée. Disponible uniquement pour les entrées complexes.

## <a name="syntax"></a>Syntaxe

``` syntax
float4 WINAPI D2DSampleInputAtPosition(
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

## <a name="return-value"></a>Valeur de retour

La fonction retourne un **float4**, au format TEXCOORDN.

## <a name="remarks"></a>Notes

L’exemple suivant illustre la fonction utilisée dans un retour circulaire à la ligne.

``` syntax
  
D2D_PS_ENTRY(CircularWrapPS)  
{  
    // TODO: perform math to calculate a circular wrap
  
    // Find the input scene position.  
    float2 inputScenePosition = float2( TODO: add math parameters );  
  
    return D2DSampleInputAtPosition(0, inputScenePosition);  
}
```

## <a name="requirements"></a>Spécifications



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

 

 





