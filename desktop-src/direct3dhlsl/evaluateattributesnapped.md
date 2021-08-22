---
title: EvaluateAttributeSnapped fonction)
description: Évalue le centre de gravité des pixels avec un décalage.
ms.assetid: f5085016-0e94-49bb-96b6-42fa15c30b9f
keywords:
- EvaluateAttributeSnapped fonction HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeSnapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5408b2c8133947b948bc42eb6ff0c725584b0cf2c60ccf0731a9d584d3c898a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512016"
---
# <a name="evaluateattributesnapped-function"></a>EvaluateAttributeSnapped fonction)

Évalue le centre de gravité des pixels avec un décalage.

## <a name="syntax"></a>Syntaxe

``` syntax
numeric EvaluateAttributeSnapped(
  in attrib numeric value,
  in 
            int2 offset
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ dans\]
</dt> <dd>

Type : **Attrib Numeric**

Valeur d'entrée.

</dd> <dt>

*décalage* \[ dans\]
</dt> <dd>

Type : **Int2**

Décalage 2D à partir du centre de pixels à l’aide d’une grille 16x16.

</dd> </dl>

## <a name="remarks"></a>Remarques

La plage du paramètre *offset* doit être définie par le code d’octet suivant.

Seuls les 4 bits les moins significatifs des deux premiers composants (U, V) de l’offset de pixel sont utilisés. La conversion du point fixe 4 bits en float est la suivante (MSB... LSB), où le MSB est à la fois une partie de la fraction et détermine le signe :

-   1000 =-0,5 f (-8/16)
-   1001 =-0.4375 f (-7/16)
-   1010 =-0.375 f (-6/16)
-   1011 =-0.3125 f (-5/16)
-   1100 =-0,25 f (-4/16)
-   1101 =-0.1875 f (-3/16)
-   1110 =-0,125 f (-2/16)
-   1111 =-0.0625 f (-1/16)
-   0000 = 0.0 f (0/16)
-   0001 = 0.0625 f (1/16)
-   0010 = 0,125 f (2/16)
-   0011 = 0.1875 f (3/16)
-   0100 = 0,25 f (4/16)
-   0101 = 0.3125 f (5/16)
-   0110 = 0.375 f (6/16)
-   0111 = 0.4375 f (7/16)

> [!Note]  
> Les bords gauche et supérieur d’un pixel sont inclus dans le décalage ; Toutefois, les bords inférieur et droit ne sont pas inclus. Tous les autres bits dans l’entier 32 bits et les valeurs de décalage V sont ignorés.

 

Une implémentation peut prendre le décalage fourni par le nuanceur et obtenir une valeur à virgule fixe 32 bits complète (28,4), qui s’étend sur la plage valide, en effectuant le calcul suivant :


```
iU = (iU<<28)>>28  // keep lowest 4 bits and sign extend, which yields [-8..7]
```



Si une implémentation doit mapper le décalage à un décalage à virgule flottante, elle effectue le calcul suivant :


```
fU = ((float)iU)/16
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

 

 




