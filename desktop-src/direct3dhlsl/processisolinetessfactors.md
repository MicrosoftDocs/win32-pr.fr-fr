---
title: ProcessIsolineTessFactors fonction)
description: Génère les facteurs de pavage arrondis pour une isoligne.
ms.assetid: 0816b3e0-cb03-4a7a-9732-e84c637b3d48
keywords:
- ProcessIsolineTessFactors fonction HLSL
topic_type:
- apiref
api_name:
- ProcessIsolineTessFactors
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 10da0e5bf0f2138c57da3fcfe962bc6a88800068
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678746"
---
# <a name="processisolinetessfactors-function"></a>ProcessIsolineTessFactors fonction)

Génère les facteurs de pavage arrondis pour une isoligne.

## <a name="syntax"></a>Syntaxe

``` syntax
void ProcessIsolineTessFactors(
  in  float RawDetailFactor,
  in  float RawDensityFactor,
  out float RoundedDetailFactor,
  out float RoundedDensityFactor
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*RawDetailFactor* \[ dans\]
</dt> <dd>

Type : **float**

Facteur de détail souhaité.

</dd> <dt>

*RawDensityFactor* \[ dans\]
</dt> <dd>

Type : **float**

Facteur de densité souhaité.

</dd> <dt>

*RoundedDetailFactor* \[ à\]
</dt> <dd>

Type : **float**

Facteur de détail arrondi à une plage qui peut être utilisée par le du paveur.

</dd> <dt>

*RoundedDensityFactor* \[ à\]
</dt> <dd>

Type : **float**

Le facteur de densité arrondie avec un rangethat peut être utilisé par le du paveur.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

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

 

 




