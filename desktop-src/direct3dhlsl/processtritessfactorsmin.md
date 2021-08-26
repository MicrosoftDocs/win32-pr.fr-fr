---
title: ProcessTriTessFactorsMin fonction)
description: Génère les facteurs de pavage corrigés pour un correctif triple. | ProcessTriTessFactorsMin fonction)
ms.assetid: fa1e19c2-fadf-42d4-9574-834eaf871393
keywords:
- ProcessTriTessFactorsMin fonction HLSL
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 09cb10f8adac68511a5b4bb5b469ab3e4f630aab0b9a58b539100914f0668114
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023739"
---
# <a name="processtritessfactorsmin-function"></a>ProcessTriTessFactorsMin fonction)

Génère les facteurs de pavage corrigés pour un correctif triple.

## <a name="syntax"></a>Syntaxe

``` syntax
void ProcessTriTessFactorsMin(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactors,
  out float UnroundedInsideTessFactors
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

*RoundedInsideTessFactors* \[ à\]
</dt> <dd>

Type : **float**

Facteurs de pavage arrondis calculés par l’étape du paveur pour les bords intérieurs.

</dd> <dt>

*UnroundedInsideTessFactors* \[ à\]
</dt> <dd>

Type : **float**

Facteurs de pavage calculés par l’étape du paveur pour les bords intérieurs.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Génère les facteurs de pavage corrigés pour un correctif triple, en calculant le facteur de pavage intérieur comme au minimum des facteurs de pavage Edge, qui est ensuite mis à l’échelle par InsideScale. Le résultat est ensuite arrondi selon le mode de partitionnement, mais les résultats non arrondis sont disponibles à l’aide du paramètre UnroundedInsideTessFactor.

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

 

 




