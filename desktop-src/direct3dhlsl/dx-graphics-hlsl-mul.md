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
ms.openlocfilehash: a2e9fe545cb16f8ac1fef1935b9d7e97075521b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030018"
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
|         | x    | in      | scalaire                                                        | float, int                                                     | 1                                                                        |
|         | y    | in      | scalaire                                                        | identique à l’entrée x                                                | 1                                                                        |
|         | Av  | out     | scalaire                                                        | identique à l’entrée x                                                | 1                                                                        |
| 2       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | scalaire                                                        | float, int                                                     | 1                                                                        |
|         | y    | in      | vecteur                                                        | float, int                                                     | n'importe laquelle                                                                      |
|         | Av  | out     | vecteur                                                        | float, int                                                     | la ou les mêmes dimensions comme entrée y                                             |
| 3       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | scalaire                                                        | float, int                                                     | 1                                                                        |
|         | y    | in      | matrice                                                        | float, int                                                     | n'importe laquelle                                                                      |
|         | Av  | out     | matrice                                                        | identique à l’entrée y                                                | la ou les mêmes dimensions comme entrée y                                             |
| 4       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | vecteur                                                        | float, int                                                     | n'importe laquelle                                                                      |
|         | y    | in      | scalaire                                                        | float, int                                                     | 1                                                                        |
|         | Av  | out     | vecteur                                                        | float, int                                                     | la ou les mêmes dimensions comme entrée x                                             |
| 5       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | vecteur                                                        | float, int                                                     | n'importe laquelle                                                                      |
|         | y    | in      | vecteur                                                        | float, int                                                     | la ou les mêmes dimensions comme entrée x                                             |
|         | Av  | out     | scalaire                                                        | float, int                                                     | 1                                                                        |
| 6       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | vecteur                                                        | float, int                                                     | n'importe laquelle                                                                      |
|         | y    | in      | matrice                                                        | float, int                                                     | Rows = la ou les mêmes dimensions en entrée x, Columns = any                       |
|         | Av  | out     | vecteur                                                        | float, int                                                     | la ou les mêmes dimensions en tant que colonnes d’entrée y                                     |
| 7       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | matrice                                                        | float, int                                                     | n'importe laquelle                                                                      |
|         | y    | in      | scalaire                                                        | float, int                                                     | 1                                                                        |
|         | Av  | out     | matrice                                                        | float, int                                                     | la ou les mêmes dimensions comme entrée x                                             |
| 8       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | matrice                                                        | float, int                                                     | n'importe laquelle                                                                      |
|         | y    | in      | vecteur                                                        | float, int                                                     | nombre de colonnes dans l’entrée x                                             |
|         | Av  | out     | vecteur                                                        | float, int                                                     | nombre de lignes dans l’entrée x                                                |
| 9       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | matrice                                                        | float, int                                                     | n'importe laquelle                                                                      |
|         | y    | in      | matrice                                                        | float, int                                                     | lignes = nombre de colonnes dans l’entrée x                                      |
|         | Av  | out     | matrice                                                        | float, int                                                     | Rows = nombre de lignes dans l’entrée x, Columns = nombre de colonnes dans l’entrée y |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                       | Prise en charge |
|------------------------------------------------------------------------------------|-----------|
| [Nuancier Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) et modèles de nuanceur plus élevés | Oui       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





