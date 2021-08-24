---
title: ddx_coarse fonction)
description: Calcule une dérivée partielle de faible précision par rapport à la coordonnée x de l’espace d’écran.
ms.assetid: 5719f45d-b2ae-4916-8f31-c2797b661814
keywords:
- ddx_coarse fonction HLSL
topic_type:
- apiref
api_name:
- ddx_coarse
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d5521da56804156485fcacb37b43cbf27d8d4b3659cbced918eaea2c12b308ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855369"
---
# <a name="ddx_coarse-function"></a>\_fonction grossiste DDX

Calcule une dérivée partielle de faible précision par rapport à la coordonnée x de l’espace d’écran.

## <a name="syntax"></a>Syntaxe

``` syntax
float ddx_coarse(
  in float value
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ dans\]
</dt> <dd>

Type : **float**

Valeur d'entrée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **float**

Dérivée partiel de faible précision de la *valeur*.

## <a name="remarks"></a>Remarques

Les versions surchargées suivantes sont également disponibles :

``` syntax
float2 ddx_coarse(float2 value);
float3 ddx_coarse(float3 value);
float4 ddx_coarse(float4 value);
```

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Pris en charge |
|-----------------------------------------------------------------------------|-----------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | oui       |



 

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




