---
title: EvaluateAttributeAtSample fonction)
description: Évalue à l’emplacement de l’exemple indexé.
ms.assetid: b5886004-5960-461d-a0d2-f4c3b0d09d94
keywords:
- EvaluateAttributeAtSample fonction HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtSample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b183f86599d08a6892e33c169b938dc09a2b55de
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292030"
---
# <a name="evaluateattributeatsample-function"></a>EvaluateAttributeAtSample fonction)

Évalue à l’emplacement de l’exemple indexé.

## <a name="syntax"></a>Syntaxe

``` syntax
numeric EvaluateAttributeAtSample(
  in attrib numeric value,
  in uint sampleindex
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ dans\]
</dt> <dd>

Type : **Attrib Numeric**

Valeur d'entrée.

</dd> <dt>

*sampleindex* \[ dans\]
</dt> <dd>

Type : **uint**

Emplacement de l’exemple.

</dd> </dl>

## <a name="remarks"></a>Notes

Le mode d’interpolation peut être **linéaire** ou **linéaire, \_ sans \_ perspective** sur la variable. L’utilisation de l’argument de centre de **gravité** ou d' **échantillon** est ignorée. Les attributs avec interpolation constante sont également autorisés. dans ce cas, l’exemple d’index est ignoré.

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Prise en charge |
|-----------------------------------------------------------------------------|-----------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | Oui       |



 

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




