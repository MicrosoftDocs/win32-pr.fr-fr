---
title: mul
description: Multiplie x et y à l’aide d’une matrice mathématique. La dimension interne x-Columns et la ligne y doivent être égales.
ms.assetid: 9945388a-d802-4dbe-bdb7-4eadb8751c39
keywords:
- langage Mul (HLSL)
topic_type:
- apiref
api_name:
- mul
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6362c734cbbf30defa8fed75f28c6f39397d75977488d9efc170d2647a9b3d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950359"
---
# <a name="mul"></a>mul

Multiplie x et y à l’aide d’une matrice mathématique. La dimension interne x-Columns et la ligne y doivent être égales.



| RET Mul (x, y) |
|---------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                                                                           |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[dans \] la valeur d’entrée x. Si x est un vecteur, il est traité comme un vecteur de ligne.<br/>    |
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[dans \] la valeur d’entrée y. Si y est un vecteur, il est traité comme un vecteur de colonne.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Résultat de x Times y. Le résultat contient la dimension x lignes x y-colonnes.

## <a name="type-description"></a>Description du type

Il existe 9 versions surchargées de cette fonction ; les versions surchargées gèrent les différents cas pour les types et les tailles des arguments d’entrée.



| Version | Nom | Objectif | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md) | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille                                                                     |
|---------|------|---------|---------------------------------------------------------------|----------------------------------------------------------------|--------------------------------------------------------------------------|
| 1       |      |         |                                                               |                                                                |                                                                          |
|         | x    | commencer      | scalaire                                                        | float, int                                                     | 1                                                                        |
|         | y    | commencer      | scalaire                                                        | identique à l’entrée x                                                | 1                                                                        |
|         | Av  | out     | scalaire                                                        | identique à l’entrée x                                                | 1                                                                        |
| 2       |      |         |                                                               |                                                                |                                                                          |
|         | x    | commencer      | scalaire                                                        | float, int                                                     | 1                                                                        |
|         | y    | commencer      | vecteur                                                        | float, int                                                     | n'importe laquelle                                                                      |
|         | Av  | out     | vecteur                                                        | float, int                                                     | la ou les mêmes dimensions comme entrée y                                             |
| 3       |      |         |                                                               |                                                                |                                                                          |
|         | x    | commencer      | scalaire                                                        | float, int                                                     | 1                                                                        |
|         | y    | commencer      | matrice                                                        | float, int                                                     | n'importe laquelle                                                                      |
|         | Av  | out     | matrice                                                        | identique à l’entrée y                                                | la ou les mêmes dimensions comme entrée y                                             |
| 4       |      |         |                                                               |                                                                |                                                                          |
|         | x    | commencer      | vecteur                                                        | float, int                                                     | n'importe laquelle                                                                      |
|         | y    | commencer      | scalaire                                                        | float, int                                                     | 1                                                                        |
|         | Av  | out     | vecteur                                                        | float, int                                                     | la ou les mêmes dimensions comme entrée x                                             |
| 5       |      |         |                                                               |                                                                |                                                                          |
|         | x    | commencer      | vecteur                                                        | float, int                                                     | n'importe laquelle                                                                      |
|         | y    | commencer      | vecteur                                                        | float, int                                                     | la ou les mêmes dimensions comme entrée x                                             |
|         | Av  | out     | scalaire                                                        | float, int                                                     | 1                                                                        |
| 6       |      |         |                                                               |                                                                |                                                                          |
|         | x    | commencer      | vecteur                                                        | float, int                                                     | n'importe laquelle                                                                      |
|         | y    | commencer      | matrice                                                        | float, int                                                     | Rows = la ou les mêmes dimensions en entrée x, Columns = any                       |
|         | Av  | out     | vecteur                                                        | float, int                                                     | la ou les mêmes dimensions en tant que colonnes d’entrée y                                     |
| 7       |      |         |                                                               |                                                                |                                                                          |
|         | x    | commencer      | matrice                                                        | float, int                                                     | n'importe laquelle                                                                      |
|         | y    | commencer      | scalaire                                                        | float, int                                                     | 1                                                                        |
|         | Av  | out     | matrice                                                        | float, int                                                     | la ou les mêmes dimensions comme entrée x                                             |
| 8       |      |         |                                                               |                                                                |                                                                          |
|         | x    | commencer      | matrice                                                        | float, int                                                     | n'importe laquelle                                                                      |
|         | y    | commencer      | vecteur                                                        | float, int                                                     | nombre de colonnes dans l’entrée x                                             |
|         | Av  | out     | vecteur                                                        | float, int                                                     | nombre de lignes dans l’entrée x                                                |
| 9       |      |         |                                                               |                                                                |                                                                          |
|         | x    | commencer      | matrice                                                        | float, int                                                     | n'importe laquelle                                                                      |
|         | y    | commencer      | matrice                                                        | float, int                                                     | lignes = nombre de colonnes dans l’entrée x                                      |
|         | Av  | out     | matrice                                                        | float, int                                                     | Rows = nombre de lignes dans l’entrée x, Columns = nombre de colonnes dans l’entrée y |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                       | Pris en charge |
|------------------------------------------------------------------------------------|-----------|
| [Nuancier Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) et modèles de nuanceur plus élevés | oui       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





