---
title: Type de matrice
description: Une matrice est un type de données spécial qui contient entre un et seize composants. Chaque composant d’une matrice doit être du même type.
ms.assetid: 728eb472-103d-4c7f-b6f6-e515fc024801
keywords:
- Type de matrice HLSL
topic_type:
- apiref
api_name:
- Matrix Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9e6b98309c760a3da4d1e9c488e4aed049aa34f0b449042e8f00a02426cc513
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726169"
---
# <a name="matrix-type"></a>Type de matrice

Une matrice est un type de données spécial qui contient entre un et seize composants. Chaque composant d’une matrice doit être du même type.



|                         |
|-------------------------|
| **Nom de TypeComponents** |



 

## <a name="components"></a>Composants



| Élément                                                                                                                             | Description                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**<br/> | Nom unique qui contient trois parties. La première partie est l’un des types [scalaires](dx-graphics-hlsl-data-types.md) . La deuxième partie est le nombre de lignes. La troisième partie est le nombre de colonnes. Le nombre de lignes et de colonnes est un entier positif compris entre 1 et 4 inclus.<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomme**<br/>                                         | Chaîne ASCII qui identifie de façon unique le nom de la variable.<br/>                                                                                                                                                                                                                            |



 

## <a name="examples"></a>Exemples

Voici quelques exemples :


```
int1x1    iMatrix;   // integer matrix with 1 row,  1 column
int4x1    iMatrix;   // integer matrix with 4 rows, 1 column
int1x4    iMatrix;   // integer matrix with 1 row, 4 columns
double3x3 dMatrix;   // double matrix with 3 rows, 3 columns

float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



Une matrice peut également être déclarée à l’aide de cette syntaxe :


```
matrix <Type, Number> VariableName
```



Le type de matrice utilise les crochets angulaires pour spécifier le type, le nombre de lignes et le nombre de colonnes. Cet exemple crée une matrice à virgule flottante, avec deux lignes et deux colonnes. Tous les types de données scalaires peuvent être utilisés.

Voici un exemple :


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de données (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





