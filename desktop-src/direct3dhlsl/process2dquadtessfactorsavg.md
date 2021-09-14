---
title: Process2DQuadTessFactorsAvg fonction)
description: Génère les facteurs de pavage corrigés pour un correctif Quad. | Process2DQuadTessFactorsAvg fonction)
ms.assetid: 7f96f634-0ad5-4037-a08e-b0b99b89cd91
keywords:
- Process2DQuadTessFactorsAvg fonction HLSL
topic_type:
- apiref
api_name:
- Process2DQuadTessFactorsAvg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4012d99a1f7714fae68f4679991aedcf810d1b4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118418"
---
# <a name="process2dquadtessfactorsavg-function"></a>Process2DQuadTessFactorsAvg fonction)

Génère les facteurs de pavage corrigés pour un correctif Quad.

## <a name="syntax"></a>Syntaxe

``` syntax
void Process2DQuadTessFactorsAvg(
  in  float4 RawEdgeFactors,
  in  float2 InsideScale,
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

Type : **float2**

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

Génère les facteurs de pavage corrigés pour un correctif Quad, en calculant les facteurs de pavage intérieurs comme la moyenne des facteurs de pavage Edge. Les facteurs de pavage à l’intérieur de votre et de V sont calculés indépendamment à l’aide de la moyenne des côtés opposés du domaine, puis sont mis à l’échelle par InsideScale. Le résultat est ensuite arrondi selon le mode de partitionnement, mais les résultats non arrondis sont disponibles à l’aide du paramètre UnroundedInsideTessFactors.

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Prise en charge |
|-----------------------------------------------------------------------------|-----------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | Oui       |



 

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




