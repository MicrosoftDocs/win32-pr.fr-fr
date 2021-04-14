---
title: Effet d’échelle
description: Utilisez cet effet pour mettre à l’échelle une image. L’effet a six modes de mise à l’échelle, linéaires, linéaires, cubiques, multi-échantillonnage linéaire, anisotrope et de haute qualité.
ms.assetid: 99DFA8DB-384B-4F64-90A2-0D3D7E1ACF27
keywords:
- effet de mise à l’échelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3af77bc24db387fff0854e0432c270fa2ce6d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384495"
---
# <a name="scale-effect"></a>Effet d’échelle

Utilisez cet effet pour mettre à l’échelle une image. L’effet a six modes de mise à l’échelle : le plus proche voisin, linéaire, cubique, multi-échantillon linéaire, anisotrope et de haute qualité.

Le CLSID de cet effet est CLSID \_ D2D1Scale.

-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
    -   [Modes de bordure](#border-modes)
-   [Modes d’interpolation](#interpolation-modes)
-   [Bitmap de sortie](#output-bitmap)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image

Cet exemple montre l’effet de mise à l’échelle dans 2 fois l’entrée et le rognage à la taille d’origine.



| Avant                                                     |
|------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg) |
| After                                                      |
| ![image après la transformation.](images/22-scale.png)     |



 


```C++
ComPtr<ID2D1Effect> scaleEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Scale, &scaleEffect);

scaleEffect->SetInput(0, bitmap);

scaleEffect->SetValue(D2D1_SCALE_PROP_CENTER_POINT, D2D1::Vector2F(256.0f, 192.0f));
scaleEffect->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(2.0f, 2.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(scaleEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriétés d’effet



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nom complet et énumération d’index</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Scale<br/> D2D1_SCALE_PROP_SCALE<br/></td>
<td>Le montant de l’échelle de la direction X et Y en tant que rapport entre la taille de sortie et la taille d’entrée. Cette propriété a D2D1_VECTOR_2Fdefined en tant que : (X Scale, échelle Y). Les valeurs de mise à l’échelle sont FLOAT, sans unité, et doivent être positives ou égales à 0.<br/> Le type est D2D1_VECTOR_2F.<br/> La valeur par défaut est {1.0 f, 1.0 f}.<br/></td>
</tr>
<tr class="even">
<td>CenterPoint<br/> D2D1_SCALE_PROP_CENTER_POINT<br/></td>
<td>Point central de mise à l’échelle de l’image. Cette propriété est une D2D1_VECTOR_2F définie comme suit : (point X, point Y). Les unités sont en DIP.<br/> Utilisez la propriété point central pour mettre à l’échelle un point autre que l’angle supérieur gauche.<br/> Le type est D2D1_VECTOR_2F.<br/> La valeur par défaut est {0.0 f, 0.0 f}.<br/></td>
</tr>
<tr class="odd">
<td>BorderMode<br/> D2D1_SCALE_PROP_BORDER_MODE<br/></td>
<td>Le mode utilisé pour calculer la bordure de l’image, soft ou Hard. Pour plus d’informations, consultez <a href="#border-modes">modes de bordure</a> . <br/> Le type est D2D1_BORDER_MODE.<br/> La valeur par défaut est D2D1_BORDER_MODE_SOFT.<br/></td>
</tr>
<tr class="even">
<td>Netteté<br/> D2D1_SCALE_PROP_SHARPNESS<br/></td>
<td>Dans le mode d’interpolation cubique de haute qualité, le niveau de netteté du filtre de mise à l’échelle est une valeur float comprise entre 0 et 1. Les valeurs sont sans unité. Vous pouvez utiliser la netteté pour ajuster la qualité d’une image lors de la mise à l’échelle de l’image.<br/> Le facteur de netteté affecte la forme du noyau. Plus le facteur de netteté est élevé, plus le noyau est petit.<br/>
<blockquote>
[!Note]<br />
Cette propriété affecte uniquement le mode d’interpolation cubique de haute qualité.
</blockquote>
<br/> Le type est FLOAT.<br/> La valeur par défaut est 0.0 f.<br/></td>
</tr>
<tr class="odd">
<td>InterpolationMode<br/> D2D1_SCALE_PROP_INTERPOLATION_MODE<br/></td>
<td>Mode d’interpolation utilisé par l’effet pour mettre l’image à l’échelle. Il existe 6 modes de mise à l’échelle qui vont de la qualité et de la vitesse. Pour plus d’informations, consultez <a href="#interpolation-modes">modes d’interpolation</a> . <br/> Le type est D2D1_SCALE_INTERPOLATION_MODE.<br/> La valeur par défaut est D2D1_SCALE_INTERPOLATION_MODE_LINEAR.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="border-modes"></a>Modes de bordure



| Nom                     | Description                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Mode de bordure d2d1 \_ \_ | L’effet remplit l’image d’entrée avec des pixels noirs transparents pour les échantillons en dehors des limites d’entrée lorsqu’elle applique le noyau de convolution. Cela crée une bordure douce pour l’image et, dans le processus, développe la bitmap de sortie de la taille du noyau.<br/> |
| D2D1 \_ mode de bordure \_ \_ difficile | L’effet étend l’image d’entrée avec une transformation de bordure de type miroir pour les exemples en dehors des limites d’entrée. La taille de l’image bitmap de sortie est égale à la taille de l’image bitmap d’entrée.<br/>                                                                       |



 

\`

## <a name="interpolation-modes"></a>Modes d’interpolation



| Énumération                                             | Description                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ \_ mode d’interpolation \_ \_ le plus proche \_ voisin     | Échantillonne le point unique le plus proche et l’utilise. Ce mode utilise moins de temps de traitement, mais génère l’image de qualité la plus faible.                                                                           |
| D2D1 \_ \_ \_ mode interpolation \_ linéaire                | Utilise un échantillon à quatre points et une interpolation linéaire. Ce mode utilise plus de temps de traitement que le mode voisin le plus proche, mais génère une image de qualité supérieure.                                           |
| D2D1 \_ \_ \_ mode interpolation \_ cubique                 | Utilise un exemple de noyau cubique 16 pour l’interpolation. Ce mode utilise le plus de temps de traitement, mais génère une image de qualité supérieure.                                                                        |
| \_Mode interpolation à l’échelle d2d1 multi- \_ \_ \_ \_ exemple \_ linéaire | Utilise 4 échantillons linéaires au sein d’un même pixel pour une bonne anticrénelage. Ce mode est adapté à la réduction de la taille des images avec quelques pixels.                                              |
| D2D1 \_ \_ mode d’interpolation \_ \_ anisotrope           | Utilise le filtrage anisotrope pour échantillonner un modèle en fonction de la forme transformée de l’image bitmap.                                                                                                     |
| D2D1 mise à l' \_ échelle \_ \_ en mode interpolation de \_ haute \_ qualité \_ cubique  | Utilise un noyau cubique de haute qualité variable pour effectuer une pré-réduire de l’image si downscaling est impliqué dans la matrice de transformation. Utilise ensuite le mode d’interpolation cubique pour la sortie finale. |



 

> [!Note]  
> Si vous ne sélectionnez pas de mode, l’effet par défaut est D2D1 mettre à l' \_ échelle le \_ \_ mode interpolation \_ linéaire.

 

> [!Note]  
> Le mode anisotrope génère des mipmaps lors de la mise à l’échelle. Toutefois, si vous affectez à la propriété **Cached** la valeur true sur les effets entrés dans cet effet, le des mipmaps ne sera pas généré à chaque fois pour des images suffisamment petites.

 

## <a name="output-bitmap"></a>Bitmap de sortie

L’emplacement et la taille de l’image bitmap de sortie dépendent du facteur d’échelle et du point central spécifiés.

Vous pouvez calculer la taille de l’image bitmap de sortie à l’aide de cette équation :<dl> BitmapSize? (Pixels) = mettre à l’échelle ? \* Taille de la bitmap d’origine ? (DIP) \* (UserDPI/96)  
BitmapSize<sub>y</sub>(pixels) = mettre à l’échelle<sub>y</sub> \* taille de bitmap d’origine<sub>y</sub> (DIP) \* (UserDPI/96)  
</dl>

L’effet arrondit les fractions de pixels au pixel entier le plus proche.

L’emplacement de la bitmap est (0,0) ou la valeur de la propriété du point central.

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

 

