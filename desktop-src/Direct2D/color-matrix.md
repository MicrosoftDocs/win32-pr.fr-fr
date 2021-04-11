---
title: Effet matrice de couleurs
description: Utilisez l’effet matrice de couleurs pour modifier les valeurs RVBA d’une image bitmap.
ms.assetid: 093EEEF1-8C38-414E-8261-58A6C3DD930D
keywords:
- effet matrice de couleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1078b1858bc68396546e1036c717e01acb1069c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032736"
---
# <a name="color-matrix-effect"></a>Effet matrice de couleurs

Utilisez l’effet matrice de couleurs pour modifier les valeurs RVBA d’une image bitmap.

Vous pouvez utiliser cet effet pour :

-   Supprimer un canal de couleur d’une image.
-   Réduisez la couleur d’une image.
-   Permuter les canaux de couleurs.
-   Combiner des canaux de couleurs.

De nombreux effets intégrés sont des spécialisations de matrice de couleur optimisées pour l’utilisation prévue des effets. Les exemples incluent [saturation](saturation.md), [teinte](hue-rotate.md), [sépia](sepia-effect.md), [température et teinte](temperature-and-tint-effect.md).

Le CLSID de cet effet est CLSID \_ D2D1ColorMatrix.

-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
-   [Modes alpha](#alpha-modes)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image

L’exemple ci-dessous montre les images d’entrée et de sortie de l’effet de matrice de couleurs qui échangent les canaux rouge et bleu.



| Avant                                                       |
|--------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)   |
| After                                                        |
| ![image après la transformation.](images/15-colormatrix.png) |



 


```C++
ComPtr<ID2D1Effect> colorMatrixEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ColorMatrix, &colorMatrixEffect);

colorMatrixEffect->SetInput(0, bitmap);
D2D1_MATRIX_5X4_F matrix = D2D1::Matrix5x4F(0, 0, 1, 0,   0, 1, 0, 0,   1, 0, 0, 0,   0, 0, 0, 1,   0, 0, 0, 0);
colorMatrixEffect->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(colorMatrixEffect.Get());
m_d2dContext->EndDraw();
```



Cet effet multiplie les valeurs RVBA de l’image par une matrice principale de colonne 5x4, comme indiqué dans cette équation.

![exemple de définition de matrice.](images/color-matrix-formula.png)

Cet effet fonctionne sur les images alpha directes et prémultipliées.

## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ColorMatrix<br/> \_Matrice de couleurs d2d1 COLORMATRIX \_ prop \_ \_<br/> | Matrice 5x4 de valeurs float. Les éléments de la matrice ne sont pas limités et sont sans unité.<br/> La valeur par défaut est la matrice d’identité.<br/> Le type est D2D1 \_ Matrix \_ 5x4 \_ F.<br/> La valeur par défaut est Matrix5x4F (1, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 0, 0). <br/>                                                                                                                                                                                                                        |
| AlphaMode<br/> \_ \_ \_ Mode Alpha d2d1 COLORMATRIX \_ prop<br/>     | Mode Alpha de la sortie. Pour plus d’informations, consultez [modes alpha](#alpha-modes) . <br/> Le type est D2D1 \_ COLORMATRIX \_ alpha \_ mode.<br/> La valeur par défaut est \_ d2d1 \_ COLORMATRIX \_ en mode Alpha \_ prémultiplié.<br/>                                                                                                                                                                                                                                                                                                    |
| ClampOutput<br/> \_Sortie de Clamp d2d1 COLORMATRIX \_ prop \_ \_<br/> | Si l’effet fixe les valeurs de couleur entre 0 et 1 avant que l’effet ne passe les valeurs à l’effet suivant dans le graphique. L’effet serre les valeurs avant de prémultiplier le alpha.<br/> Si vous affectez la valeur TRUE à cet effet, les valeurs sont ancrées. Si vous définissez cette valeur sur FALSe, l’effet n’attache pas les valeurs de couleur, mais d’autres effets et la surface de sortie peuvent fixer les valeurs si elles n’ont pas une précision suffisamment élevée.<br/> Le type est BOOL.<br/> La valeur par défaut est FALSE.<br/> |



 

## <a name="alpha-modes"></a>Modes alpha



| Nom                                          | Description                                                                                               |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| D2D1 \_ COLORMATRIX \_ \_ en mode Alpha \_ prémultiplié | L’effet annule la prémultiplication de l’entrée, applique la matrice de couleurs et prémultiplie la sortie.<br/> |
| \_Mode d2d1 \_ COLORMATRIX \_ alpha \_ simple      | L’effet applique la matrice de couleurs directement à l’entrée et ne prémultiplie pas la sortie.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge | Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\] |
| Serveur minimal pris en charge | Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\] |
| En-tête                   | d2d1effects. h                                                                      |
| Bibliothèque                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

