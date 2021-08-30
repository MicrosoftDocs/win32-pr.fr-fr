---
title: ProcessTriTessFactorsMax fonction)
description: Génère les facteurs de pavage corrigés pour un correctif triple. | ProcessTriTessFactorsMax fonction)
ms.assetid: a24cc1a8-5e6e-4963-b36b-e2265475580e
keywords:
- ProcessTriTessFactorsMax fonction HLSL
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 738eaca371055d8162df38bc3ed8bce669fdb3abede59c76b47223d03876aa12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118309"
---
# <a name="processtritessfactorsmax-function"></a>ProcessTriTessFactorsMax fonction)

Génère les facteurs de pavage corrigés pour un correctif triple.

## <a name="syntax"></a>Syntaxe

``` syntax
void ProcessTriTessFactorsMax(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactor,
  out float UnroundedInsideTessFactor
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*RawEdgeFactors* \[ dans\]
</dt> <dd>

Type : **float3**

Facteurs de pavage Edge, passés à l’étape du paveur.

</dd> <dt>

*InsideScale* \[ dans\]
</dt> <dd>

Type : **float**

Facteur d’échelle appliqué aux facteurs de pavage UV calculés par l’étape de pavage. La plage autorisée pour InsideScale est 0,0 à 1,0.

</dd> <dt>

*RoundedEdgeTessFactors* \[ à\]
</dt> <dd>

Type : **float3**

Facteurs de pavage de bords arrondis calculés par l’étape du paveur.

</dd> <dt>

*RoundedInsideTessFactor* \[ à\]
</dt> <dd>

Type : **float**

Facteurs de pavage calculés par l’étape du paveur et arrondis.

</dd> <dt>

*UnroundedInsideTessFactor* \[ à\]
</dt> <dd>

Type : **float**

Facteurs de pavage UV originaux et inarrondis calculés par l’étape de pavage.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Génère les facteurs de pavage corrigés pour un correctif triple, en calculant le facteur de pavage intérieur comme le maximum des facteurs de pavage Edge, qui est ensuite mis à l’échelle par InsideScale. Le résultat est ensuite arrondi selon le mode de partitionnement, mais les résultats non arrondis sont disponibles à l’aide du paramètre UnroundedInsideTessFactor.

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Pris en charge |
|-----------------------------------------------------------------------------|-----------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | oui       |



 

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




