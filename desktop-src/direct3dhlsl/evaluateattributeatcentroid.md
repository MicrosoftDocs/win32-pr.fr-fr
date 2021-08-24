---
title: EvaluateAttributeAtCentroid fonction)
description: Évalue au centre de gravité du pixel.
ms.assetid: 6735b3f4-765f-4cd9-9f38-326a52709021
keywords:
- EvaluateAttributeAtCentroid fonction HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtCentroid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 867f7dadc2ccf7d86eed602dd9e65d07be7558f0a8a00426e3a45bc1c2c97a3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744039"
---
# <a name="evaluateattributeatcentroid-function"></a>EvaluateAttributeAtCentroid fonction)

Évalue au centre de gravité du pixel.

## <a name="syntax"></a>Syntaxe

``` syntax
numeric EvaluateAttributeAtCentroid(
  in attrib numeric value
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ dans\]
</dt> <dd>

Type : **Attrib Numeric**

Valeur d'entrée.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le mode d’interpolation peut être **linéaire** ou **linéaire, \_ sans \_ perspective** sur la variable. L’utilisation de l’argument de centre de **gravité** ou d' **échantillon** est ignorée. Les attributs avec interpolation constante sont également autorisés. dans ce cas, l’exemple d’index est ignoré.

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

 

 




