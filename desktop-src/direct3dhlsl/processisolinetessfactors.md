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
ms.openlocfilehash: 34c6f4d579ee7fbaee9416d7a607e3856a7793021cca7149723d3d6e5a2b4a49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986289"
---
# <a name="processisolinetessfactors-function"></a>ProcessIsolineTessFactors fonction)

Génère les facteurs de pavage arrondis pour une isoligne.

## <a name="syntax"></a>Syntaxe

``` syntax
void ProcessIsolineTessFactors(
  in  float RawDetailFactor,
  in  float RawDensityFactor,
  out float RoundedDetailFactor,
  out float RoundedDensityFactor
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

## <a name="remarks"></a>Remarques

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

 

 




