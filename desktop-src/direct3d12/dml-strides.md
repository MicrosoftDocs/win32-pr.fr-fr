---
title: Utilisation de Strides pour exprimer le remplissage et la disposition de la mémoire
description: Les dizaines de DirectML sont décrits par des propriétés connues sous le nom de *tailles* et de *Strides* du tenseur.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: b944b1a2600febe27f209bffcc0e355c6a9fc7db
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104548536"
---
# <a name="using-strides-to-express-padding-and-memory-layout"></a>Utilisation de Strides pour exprimer le remplissage et la disposition de la mémoire

Les dizaines &mdash; de DirectML qui sont sauvegardés par les tampons Direct3D 12 &mdash; sont décrits par des propriétés connues sous le nom de *tailles* et de *Strides* du tenseur. Les *tailles* de tenseur décrivent les dimensions logiques du tenseur. Par exemple, un tenseur 2D peut avoir une hauteur de 2 et une largeur de 3. Logiquement, tenseur a 6 éléments distincts, bien que les tailles ne spécifient pas la manière dont ces éléments sont stockés en mémoire. Les *Strides* de tenseur décrivent la disposition de la mémoire physique des éléments du tenseur.

## <a name="two-dimensional-2d-arrays"></a>Tableaux à deux dimensions (2D)

Prenons un tenseur 2D qui a une hauteur de 2 et une largeur de 3 ; les données comprennent des caractères textuels. En C/C++, cela peut être exprimé à l’aide d’un tableau multidimensionnel.

```cpp
constexpr int rows = 2;
constexpr int columns = 3;
char tensor[rows][columns];
tensor[0][0] = 'A';
tensor[0][1] = 'B';
tensor[0][2] = 'C';
tensor[1][0] = 'D';
tensor[1][1] = 'E';
tensor[1][2] = 'F';
```

La vue logique du tenseur ci-dessus est visualisée ci-dessous.

```console
A B C
D E F
```

En C/C++, un tableau multidimensionnel est stocké dans l’ordre ligne-principal. En d’autres termes, les éléments consécutifs le long de la dimension de largeur sont stockés de façon contiguë dans l’espace mémoire linéaire.

Décalage :|0|1|2|3|4|5
-|-|-|-|-|-|-
Valeur :|Un|B|C|D|E|F

Le *Stride* d’une dimension est le nombre d’éléments à ignorer afin d’accéder à l’élément suivant dans cette dimension. Strides Express la disposition des tenseur en mémoire. Avec un ordre ligne-grand, le Stride de la dimension width est toujours égal à 1, car les éléments adjacents le long de la dimension sont stockés de façon contiguë. Le Stride de la dimension de hauteur dépend de la taille de la dimension de largeur ; dans l’exemple ci-dessus, la distance entre les éléments consécutifs le long de la dimension de la hauteur (par exemple, A à D) est égale à la largeur du tenseur (qui est 3 dans cet exemple).

Pour illustrer une disposition différente, pensez à l’ordre des colonnes. En d’autres termes, les éléments consécutifs le long de la dimension de hauteur sont stockés de façon contiguë dans l’espace mémoire linéaire. Dans ce cas, la hauteur-Stride est toujours 1 et la largeur-Stride est 2 (la taille de la dimension de hauteur).

Décalage :|0|1|2|3|4|5
-|-|-|-|-|-|-
Valeur :|Un|D|B|E|C|F

## <a name="higher-dimensions"></a>Dimensions supérieures

Lorsqu’il s’agit de plus de deux dimensions, il est difficile de faire référence à une disposition en tant que ligne-principale ou colonne-majeure. Ainsi, le reste de cette rubrique utilise des termes et des étiquettes tels que ceux-ci.

- 2D : la hauteur « HW » &mdash; est la dimension de l’ordre le plus élevé (ligne-principale).
- 2D : la largeur « WH » &mdash; est la dimension de l’ordre le plus élevé (colonne-principale).
- 3D : la profondeur « DHW » &mdash; est la dimension de l’ordre le plus élevé, suivie de la hauteur, puis de la largeur.
- 3D : la largeur de « WHD » &mdash; est la dimension de l’ordre le plus élevé, suivie de la hauteur, puis de la profondeur.
- 4D : « NCHW » &mdash; nombre d’images (taille de lot), le nombre de canaux, puis la hauteur, la largeur.

En général, le Stride *condensé* d’une dimension est égal au produit de la taille des dimensions de l’ordre inférieur. Par exemple, avec une disposition « DHW », la valeur D-Stride est égale à H * W ; la valeur H-Stride est égale à W ; et W-Stride est égal à 1. Les Strides sont considérés comme *conditionnés* lorsque la taille physique totale du tenseur est égale à la taille logique totale du tenseur ; en d’autres termes, il n’y a pas d’espace supplémentaire ni d’éléments qui se chevauchent.

Nous allons étendre l’exemple 2D à trois dimensions, afin que nous ayons un tenseur avec la profondeur 2, la hauteur 2 et la largeur 3 (pour un total de 12 éléments logiques).

```console
A B C
D E F

G H I
J K L
```

Avec une disposition « DHW », ce tenseur est stocké comme suit.

Décalage :|0|1|2|3|4|5|6|7|8|9|10|11|
-|-|-|-|-|-|-|-|-|-|-|-|-|
Valeur :|Un|B|C|D|E|F|G|H|I|J|K|L|

- D-Stride = hauteur (2) * largeur (3) = 6 (par exemple, la distance entre « A » et « G »).
- H-Stride = Width (3) = 3 (par exemple, la distance entre « A » et « d »).
- W-STRIDE = 1 (par exemple, la distance entre « A » et « B »).

Le produit scalaire des index/coordonnées d’un élément et des Strides fournit le décalage vers cet élément dans la mémoire tampon. Par exemple, le décalage de l’élément H (d = 1, H = 0, w = 1) est 7.

{1, 0, 1} ⋅ {6, 3, 1} = 1 * 6 + 0 * 3 + 1 * 1 = 7

## <a name="packed-tensors"></a>Dizaines compressés

Les exemples ci-dessus illustrent des dizaines *compressés* . Un tenseur est dit *compressé* lorsque la taille logique du tenseur (dans les éléments) est égale à la taille physique de la mémoire tampon (dans les éléments), et que chaque élément a une adresse/un décalage unique. Par exemple, un tenseur 2x2x3 est compressé si la mémoire tampon est de 12 éléments et si aucune paire d’éléments ne partagent le même offset dans la mémoire tampon. Les dizaines compressés sont les cas les plus courants. mais les Strides permettent des dispositions de mémoire plus complexes.

## <a name="broadcasting-with-strides"></a>Diffusion avec Strides

Si la taille de mémoire tampon d’un tenseur (dans les éléments) est inférieure au produit de ses dimensions logiques, il doit y avoir un chevauchement d’éléments. Le cas habituel est appelé « *diffusion*». où les éléments d’une dimension sont un doublon d’une autre dimension. Par exemple, revenons à l’exemple 2D. Supposons que nous voulons un tenseur logiquement 2x3, mais la deuxième ligne est identique à la première ligne. Voici à quoi cela ressemble.

```console
A B C
A B C
```

Cela peut être stocké sous la forme d’un tenseur de matériel/ligne-principal compressé. Mais un stockage plus compact contient uniquement 3 éléments (A, B et C) et utilise une hauteur-Stride de 0 au lieu de 3. Dans ce cas, la taille physique du tenseur est de 3 éléments, mais la taille logique est de 6 éléments.

En général, si le Stride d’une dimension est égal à 0, tous les éléments dans les dimensions de l’ordre inférieur sont répétés le long de la dimension diffusée. par exemple, si tenseur est NCHW et que C-Stride est égal à 0, chaque canal a les mêmes valeurs le long de H et W.

## <a name="padding-with-strides"></a>Remplissage avec des Strides

Un tenseur est dit *rempli* si sa taille physique est supérieure à la taille minimale requise pour ajuster ses éléments. Lorsqu’il n’y a pas d’éléments de diffusion ou de chevauchement, la taille minimale du tenseur (dans les éléments) est simplement le produit de ses dimensions. Vous pouvez utiliser la fonction d’assistance `DMLCalcBufferTensorSize` (consultez [fonctions d’assistance DirectML](dml-helper-functions.md) pour obtenir une liste de cette fonction) afin de calculer la taille de mémoire tampon *minimale* pour vos dizaines de DirectML.

Supposons qu’une mémoire tampon contient les valeurs suivantes (les éléments « x » indiquent des valeurs de remplissage).

0|1|2|3|4|5|6|7|8|9|
-|-|-|-|-|-|-|-|-|-|
Un|B|C|x|x|D|E|F|x|x

Le tenseur rempli peut être décrit en utilisant une hauteur-Stride de 5 au lieu de 3. Au lieu d’effectuer un pas à pas de trois éléments pour passer à la ligne suivante, l’étape est de 5 éléments (3 éléments *réels* plus 2 éléments de remplissage). Le remplissage est courant dans les graphiques informatiques, par exemple, pour s’assurer qu’une image a un alignement de puissance de deux.

```console
A B C
D E F
```

## <a name="directml-buffer-tensor-descriptions"></a>Descriptions des tenseur de tampon DirectML

DirectML peut fonctionner avec une grande variété de dispositions tenseur physiques, puisque la [structure **DML_BUFFER_TENSOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) a à la fois des `Sizes` `Strides` membres et. Certaines implémentations d’opérateur peuvent être plus efficaces avec une disposition spécifique. il n’est donc pas rare de modifier la façon dont les données tenseur sont stockées pour de meilleures performances.

La plupart des opérateurs DirectML requièrent des dizaines 4D ou 5J, et l’ordre des valeurs de tailles et de Strides est fixe. En résolvant l’ordre des tailles et des valeurs Stride dans une description tenseur, il est possible pour DirectML de déduire différentes dispositions physiques.

**4D**
- [**DML_BUFFER_TENSOR_DESC :: tailles**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) = {N-Size, C-Size, H-Size, W-Size}
- [**DML_BUFFER_TENSOR_DESC :: Strides**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) = {N-Stride, C-Stride, H-Stride, W-Stride}

**5D**
- **DML_BUFFER_TENSOR_DESC :: tailles** = {N-Size, C-Size, D-size, H-Size, W-Size}
- **DML_BUFFER_TENSOR_DESC :: Strides** = {N-Stride, C-Stride, D-Stride, H-Stride, W-Stride}

Si un opérateur DirectML requiert un tenseur 4D ou un 5D, mais que les données réelles ont un rang inférieur (par exemple, 2D), les dimensions principales doivent être remplies avec 1. Par exemple, un tenseur « HW » est défini à l’aide de **DML_BUFFER_TENSOR_DESC :: Sizes** = {1, 1, H, W}.

Si les données tenseur sont stockées dans NCHW/NCDHW, il n’est pas nécessaire de définir **DML_BUFFER_TENSOR_DESC :: Strides**, sauf si vous souhaitez la diffusion ou le remplissage. Vous pouvez définir le champ Strides sur `nullptr` . Toutefois, si les données tenseur sont stockées dans une autre mise en page, par exemple NHWC, vous avez besoin de Strides afin d’exprimer la transformation de NCHW à cette disposition.

Pour obtenir un exemple simple, prenez en compte la description d’un tenseur 2D avec la hauteur 3 et la largeur 5.

**NCHW compressés (Strides implicites)**
- **DML_BUFFER_TENSOR_DESC :: tailles** = {1, 1, 3, 5}
- **DML_BUFFER_TENSOR_DESC :: Strides** = `nullptr`

**NCHW compressés (Strides explicites)**
- N-Stride = C-Size * H-Size * W-size = 1 * 3 * 5 = 15
- C-Stride = H-Size * W-size = 3 * 5 = 15
- H-Stride = W-Size = 5
- W-STRIDE = 1
- **DML_BUFFER_TENSOR_DESC :: tailles** = {1, 1, 3, 5}
- **DML_BUFFER_TENSOR_DESC :: Strides** = {15, 15, 5, 1}

**NHWC condensé**
- N-Stride = H-Size * W-SIZE * C-size = 3 * 5 * 1 = 15
- H-Stride = W-SIZE * C-Size = 5 * 1 = 5
- W-Stride = C-size = 1
- C-STRIDE = 1
- **DML_BUFFER_TENSOR_DESC :: tailles** = {1, 1, 3, 5}
- **DML_BUFFER_TENSOR_DESC :: Strides** = {15, 1, 5, 1}

## <a name="see-also"></a>Voir aussi

* [Fonctions d’assistance DirectML](dml-helper-functions.md)
* [Structure DML_BUFFER_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc)
