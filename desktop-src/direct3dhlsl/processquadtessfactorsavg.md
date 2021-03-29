---
title: ProcessQuadTessFactorsAvg fonction)
description: Génère les facteurs de pavage corrigés pour un correctif Quad. | ProcessQuadTessFactorsAvg fonction)
ms.assetid: 3af1dad3-1923-45f3-9908-ca403e7f0cfe
keywords:
- ProcessQuadTessFactorsAvg fonction HLSL
topic_type:
- apiref
api_name:
- ProcessQuadTessFactorsAvg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36a50dd971161f3e03514947db447774da5b6a62
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992049"
---
# <a name="processquadtessfactorsavg-function"></a>ProcessQuadTessFactorsAvg fonction)

Génère les facteurs de pavage corrigés pour un correctif Quad.

## <a name="syntax"></a>Syntaxe

``` syntax
void ProcessQuadTessFactorsAvg(
  in  float4 RawEdgeFactors,
  in  float InsideScale,
  out float4 RoundedEdgeTessFactors,
  out float2 RoundedInsideTessFactors,
  out float2 UnroundedInsideTessFactors
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*RawEdgeFactors* \[ dans\]
</dt> <dd>

Type : **float4**

Facteurs de pavage Edge, passés à l’étape du paveur.

</dd> <dt>

*InsideScale* \[ dans\]
</dt> <dd>

Type : **float**

Facteur d’échelle appliqué aux facteurs de pavage UV calculés par l’étape de pavage. La plage autorisée pour InsideScale est 0,0 à 1,0.

</dd> <dt>

*RoundedEdgeTessFactors* \[ à\]
</dt> <dd>

Type : **float4**

Facteurs de pavage de bords arrondis calculés par l’étape du paveur.

</dd> <dt>

*RoundedInsideTessFactors* \[ à\]
</dt> <dd>

Type : **float2**

Facteurs de pavage arrondis calculés par l’étape du paveur pour les bords intérieurs.

</dd> <dt>

*UnroundedInsideTessFactors* \[ à\]
</dt> <dd>

Type : **float2**

Facteurs de pavage calculés par l’étape du paveur pour les bords intérieurs.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Génère les facteurs de pavage corrigés pour un correctif Quad, en calculant les facteurs de pavage intérieurs comme la moyenne des facteurs de pavage Edge. Les facteurs Tess internes seront des valeurs identiques déterminées par la moyenne des quatre bords mis à l’échelle par InsideScale. Le résultat est ensuite arrondi selon le mode de partitionnement, mais les résultats non arrondis sont disponibles à l’aide du paramètre UnroundedInsideTessFactors.

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Prise en charge |
|-----------------------------------------------------------------------------|-----------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | Oui       |



 

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




