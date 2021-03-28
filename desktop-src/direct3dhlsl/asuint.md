---
title: asuint fonction)
description: Réinterprète le modèle binaire d’une valeur 64 bits comme deux entiers 32 bits non signés.
ms.assetid: 29671661-4fec-46e5-9b6f-56fba8e1d756
keywords:
- asuint fonction HLSL
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c54ed89e112482df4a54f35e24a04694e88fa490
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030388"
---
# <a name="asuint-function"></a>asuint fonction)

Réinterprète le modèle binaire d’une valeur 64 bits comme deux entiers 32 bits non signés.

## <a name="syntax"></a>Syntaxe

``` syntax
void asuint(
  in  double value,
  out uint lowbits,
  out uint highbits
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ dans\]
</dt> <dd>

Type : **double**

Valeur d'entrée.

</dd> <dt>

*lowbits* \[ à\]
</dt> <dd>

Type : **uint**

Modèle de *valeur* faible 32 bits.

</dd> <dt>

*highbits* \[ à\]
</dt> <dd>

Type : **uint**

Modèle de *valeur* élevée 32 bits.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette fonction est une autre version de l’intrinsèque [**asuint**](dx-graphics-hlsl-asuint.md) qui est disponible dans les modèles de nuanceur précédents et qui a été introduite pour le Shader Model 5. La fonction d’origine (reconnue dans le compilateur HLSL par sa signature différente) reste disponible pour le Shader Model 5.

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Prise en charge |
|-----------------------------------------------------------------------------|-----------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | Oui       |



 

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




