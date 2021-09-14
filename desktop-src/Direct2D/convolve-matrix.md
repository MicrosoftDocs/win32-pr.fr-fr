---
title: Effet de matrice de convolution
description: Utilisez l’effet matrice convolution pour appliquer un noyau 2D arbitraire à une image. Vous pouvez utiliser cet effet pour brouiller, détecter les bords, faire un relief ou améliorer la netteté d’une image.
ms.assetid: D9C23AC4-0090-4F16-AC59-B952FB616FA9
keywords:
- effet matrice conversion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27951f5b9145dc46188e6b3112892d1a61856236
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114126"
---
# <a name="convolve-matrix-effect"></a>Effet de matrice de convolution

Utilisez l’effet matrice convolution pour appliquer un noyau 2D arbitraire à une image. Vous pouvez utiliser cet effet pour brouiller, détecter les bords, faire un relief ou améliorer la netteté d’une image.

Le CLSID de cet effet est CLSID \_ D2D1ConvolveMatrix.

-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
-   [Modes de mise à l’échelle](#scale-modes)
-   [Modes de bordure](#border-modes)
-   [Bitmap de sortie](#output-bitmap)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image

L’exemple ci-dessous montre l’entrée et la sortie de l’effet de matrice convolution avec un noyau 3 x 3.



| Avant                                                         |
|----------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)     |
| After                                                          |
| ![image après la transformation.](images/6-convolvematrix.png) |



 


```C++
ComPtr<ID2D1Effect> convolveMatrixEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ConvolveMatrix, &convolveMatrixEffect);

convolveMatrixEffect->SetInput(0, bitmap);
float matrix[9] = {-1, -1, -1, -1, 9, -1, -1, -1, -1};
convolveMatrixEffect->SetValue(D2D1_CONVOLVEMATRIX_PROP_KERNEL_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(convolveMatrixEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                                                      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| KernelUnitLength<br/> Longueur de l' \_ unité de noyau d2d1 CONVOLVEMATRIX \_ prop \_ \_ \_<br/> | Taille d’une unité dans le noyau. Les unités sont en (DIP/unité noyau), où une unité de noyau est la taille de l’élément dans le noyau de convolution. Une valeur de 1 (unité de noyau/DIP) correspond à un pixel dans une image à 96 ppp.<br/> Le type est FLOAT.<br/> La valeur par défaut est 1,0 f.<br/>                                                                                                                                                                                                                   |
| Devient<br/> MODE de mise à l' \_ échelle d2d1 CONVOLVEMATRIX \_ prop \_ \_<br/>                 | Mode d’interpolation utilisé par l’effet pour mettre l’image à l’échelle de la longueur de l’unité de noyau correspondante. Il existe six modes de mise à l’échelle qui vont de la qualité et de la vitesse.<br/> Le type est D2D1 \_ CONVOLVEMATRIX \_ Scale \_ mode.<br/> La valeur par défaut est D2D1 \_ CONVOLVEMATRIX \_ Scale \_ mode \_ linéaire.<br/>                                                                                                                                                                                                                     |
| KernelSizeX<br/> \_ \_ \_ Taille du noyau d2d1 CONVOLVEMATRIX prop \_ \_ X<br/>           | Largeur de la matrice du noyau. Les unités sont spécifiées en unités de noyau. Le type est UINT32.<br/> La valeur par défaut est 3.<br/>                                                                                                                                                                                                                                                                                                                                                                                        |
| KernelSizeY<br/> \_ \_ Taille du noyau de d2d1 CONVOLVEMATRIX prop \_ \_ \_ Y<br/>           | Hauteur de la matrice de noyau. Les unités sont spécifiées en unités de noyau. Le type est UINT32.<br/> La valeur par défaut est 3.<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| KernelMatrix<br/> \_Matrice de noyau d2d1 CONVOLVEMATRIX \_ prop \_ \_<br/>           | Matrice de noyau à appliquer à l’image. Les éléments de noyau ne sont pas limités et sont spécifiés en tant que valeurs float.<br/> Le premier ensemble de nombres *KernelSizeX* dans le float \[ \] correspond à la première ligne du noyau. Le deuxième ensemble de nombres *KernelSizeX* correspond à la deuxième ligne, et ainsi de suite jusqu’à *KernelSizeY* lignes.<br/> Le type est FLOAT \[ \] .<br/> La valeur par défaut est {0.0 f, 0.0 f, 0.0 f, 0.0 f, 1.0 f, 0.0 f, 0.0 f, 0.0 f, 0.0 f}.<br/>                                                       |
| Diviseur<br/> \_Diviseur d2d1 CONVOLVEMATRIX \_ prop \_<br/>                       | La matrice du noyau est appliquée à un pixel, puis le résultat est divisé par cette valeur. <br/> 0 se comporte comme une valeur de float Epsilon.<br/> Le type est FLOAT.<br/> La valeur par défaut est 1,0 f.<br/>                                                                                                                                                                                                                                                                                                           |
| Décalage<br/> D2D1 \_ CONVOLVEMATRIX \_ prop \_<br/>                             | L’effet applique la matrice du noyau, le diviseur, puis le biais est ajouté au résultat. Le biais est illimité et sans unité. Le type est FLOAT.<br/> La valeur par défaut est 0.0 f.<br/>                                                                                                                                                                                                                                                                                                                              |
| KernelOffset<br/> \_ \_ \_ Décalage du noyau d2d1 CONVOLVEMATRIX prop \_<br/>           | Décale le noyau de convolution d’une position centrée sur le pixel de sortie vers une position que vous spécifiez à gauche/à droite et vers le haut/vers le haut. Le décalage est défini en unités de noyau.<br/> Avec des décalages et des tailles de noyau, les exemples de noyau de convolution ne s’afficheront pas sur un centre d’images en pixels. Les valeurs de pixel de l’exemple de noyau sont calculées par une interpolation bilinéaire.<br/> Le type est D2D1 \_ Vector \_ 2F.<br/> La valeur par défaut est {0.0 f, 0.0 f}.<br/>                                                          |
| PreserveAlpha<br/> D2D1 \_ CONVOLVEMATRIX \_ prop \_ conserver \_ alpha<br/>         | Spécifie si le noyau de convolution est appliqué au canal alpha ou uniquement aux canaux de couleur.<br/> Si vous affectez la valeur **true** , le noyau de convolution est appliqué uniquement aux canaux de couleur.<br/> Si vous définissez cette valeur sur **false** , le noyau de convolution est appliqué à tous les canaux.<br/> Le type est BOOL.<br/> La valeur par défaut est FALSE.<br/>                                                                                                                                               |
| BorderMode<br/> \_Mode de bordure d2d1 CONVOLVEMATRIX \_ prop \_ \_<br/>               | Le mode utilisé pour calculer la bordure de l’image, soft ou Hard. Pour plus d’informations, consultez [modes de bordure](https://www.bing.com/search?q=Border+modes) .<br/> Le type est D2D1 \_ Border \_ mode.<br/> La valeur par défaut est \_ d2d1 \_ en mode bordure \_ souple.<br/>                                                                                                                                                                                                                                                                                     |
| ClampOutput<br/> \_Sortie de Clamp d2d1 CONVOLVEMATRIX \_ prop \_ \_<br/>             | Si l’effet fixe les valeurs de couleur entre 0 et 1 avant que l’effet ne passe les valeurs à l’effet suivant dans le graphique. L’effet serre les valeurs avant de prémultiplier le alpha.<br/> Si vous affectez la valeur TRUE à cet effet, les valeurs sont ancrées. Si vous définissez cette valeur sur FALSe, l’effet n’attache pas les valeurs de couleur, mais d’autres effets et la surface de sortie peuvent fixer les valeurs si elles n’ont pas une précision suffisamment élevée.<br/> Le type est BOOL.<br/> La valeur par défaut est FALSE.<br/> |



 

## <a name="scale-modes"></a>Modes de mise à l’échelle



| Énumération                                              | Description                                                                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MODE de mise à l' \_ échelle d2d1 CONVOLVEMATRIX \_ \_ \_ le plus proche \_ voisin     | Échantillonne le point unique le plus proche et l’utilise. Ce mode utilise moins de temps de traitement, mais génère l’image de qualité la plus faible.                                                                           |
| D2D1 mode de mise à l' \_ \_ échelle CONVOLVEMATRIX \_ \_ linéaire                | Utilise un échantillon à quatre points et une interpolation linéaire. Ce mode génère une image de qualité supérieure à celle du mode voisin le plus proche.                                                                              |
| D2D1 mode de mise à l' \_ \_ échelle CONVOLVEMATRIX \_ \_ cubique                 | Utilise un exemple de noyau cubique 16 pour l’interpolation. Ce mode utilise le plus de temps de traitement, mais génère une image de qualité supérieure.                                                                        |
| MODE de mise à l' \_ échelle d2d1 CONVOLVEMATRIX \_ multi- \_ \_ \_ exemple \_ linéaire | Utilise 4 échantillons linéaires au sein d’un même pixel pour une bonne anticrénelage. Ce mode est adapté à la réduction de la taille des images avec quelques pixels.                                              |
| D2D1 \_ \_ mode Scale \_ CONVOLVEMATRIX \_ anisotrope           | Utilise le filtrage anisotrope pour échantillonner un modèle en fonction de la forme transformée de l’image bitmap.                                                                                                     |
| D2D1 \_ CONVOLVEMATRIX \_ \_ en mode Scale de \_ haute \_ qualité \_ cubique  | Utilise un noyau cubique de haute qualité variable pour effectuer une pré-réduire de l’image si downscaling est impliqué dans la matrice de transformation. Utilise ensuite le mode d’interpolation cubique pour la sortie finale. |



 

> [!Note]  
> Si vous ne sélectionnez pas de mode, l’effet par défaut est D2D1 \_ CONVOLVEMATRIX \_ Scale \_ mode \_ linéaire.

 

## <a name="border-modes"></a>Modes de bordure



| Nom                     | Description                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Mode de bordure d2d1 \_ \_ | L’effet remplit l’image d’entrée avec des pixels noirs transparents pour les échantillons en dehors des limites d’entrée lorsqu’elle applique le noyau de convolution. Cela crée une bordure douce pour l’image et, dans le processus, développe la bitmap de sortie de la taille du noyau.<br/> |
| D2D1 \_ mode de bordure \_ \_ difficile | L’effet étend l’image d’entrée avec une transformation de bordure de type miroir pour les exemples en dehors des limites d’entrée. La taille de l’image bitmap de sortie est égale à la taille de l’image bitmap d’entrée.<br/>                                                                       |



 

## <a name="output-bitmap"></a>Bitmap de sortie

La taille de la sortie de l’effet dépend de la taille du noyau de convolution, du décalage du noyau, de la longueur de l’unité du noyau et du paramètre de mode de bordure.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge | mise à jour Windows 8 et de plateforme pour les applications de bureau Windows 7 Windows les applications du windows \[ \| Store\] |
| Serveur minimal pris en charge | mise à jour Windows 8 et de plateforme pour les applications de bureau Windows 7 Windows les applications du windows \[ \| Store\] |
| En-tête                   | d2d1effects. h                                                                      |
| Bibliothèque                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

