---
title: D2DGetInput, fonction (D2d1effecthelpers. h)
description: Retourne la couleur de l’entrée N à la coordonnée d’entrée. Disponible uniquement pour les entrées simples.
ms.assetid: 74B6F814-53C7-4C8C-B45C-3CB23B9D8BED
keywords:
- D2DGetInput fonction Direct2D
topic_type:
- apiref
api_name:
- D2DGetInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37de536eb6ac36af3e8aa1ffca61c3840cf6c84e585466a56a447522c4d628d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075313"
---
# <a name="d2dgetinput-function"></a>D2DGetInput fonction)

Retourne la couleur de l’entrée N à la coordonnée d’entrée. Disponible uniquement pour les entrées simples.

## <a name="syntax"></a>Syntaxe

``` syntax
float4 WINAPI D2DGetInput(
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

La fonction retourne un **float4**, contenant la couleur RVBA dans le format d’entrée.

## <a name="remarks"></a>Remarques

L’exemple suivant illustre la fonction utilisée dans le cadre d’un effet composite arithmétique.

``` syntax
  
D2D_PS_ENTRY(PS_NAME)  
{  
    MIN_TYPE(float4) sourceColor = D2DGetInput(0);  
    MIN_TYPE(float4) destColor   = D2DGetInput(1);  
      
    MIN_TYPE(float4) output = // TODO: add math to composite source and dest

    return output;  
}  
```

Reportez-vous également à la section Remarques sur l’entrée de l' [ \_ \_ élément](d2d-ps-entry.md) de rapport D2D pour obtenir un autre exemple d’utilisation de cette fonction.

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

 

 





