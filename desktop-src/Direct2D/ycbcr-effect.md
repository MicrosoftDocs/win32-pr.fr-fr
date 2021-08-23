---
title: Effet YCbCr
description: Convertit les données JPEG d’échantillonnages planaires et de couleur planaire en RVB.
ms.assetid: E4492996-54DA-4C5F-B44C-8FBE97C8DD7D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5302300cc539571fabb1c3d786686ffc514636133391e706fc5963002656764
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636089"
---
# <a name="ycbcr-effect"></a>Effet YCbCr

Convertit les données JPEG YC<sub>b</sub>C<sub>r</sub> de l’échantillon planaire et couleur en RVB. Cet effet suppose que les données YC<sub>b</sub>C<sub>r</sub> sont mises en forme conformément à la norme JPEG. Les données des entrées peuvent être obtenues à partir de IWICPlanarBitmapSourceTransform. L’effet YC<sub>b</sub>C<sub>r</sub> requiert deux entrées ; la première doit être une \_ bitmap de format dxgi \_ R8 contenant les données de luminance, tandis que la seconde doit être un \_ format dxgi \_ R8G8 bitmap contenant les données de Chroma échantillonnées. Pour plus d’informations sur l’utilisation de cet effet, consultez [prise en charge d’JPEG YCbCr](/windows/desktop/wic/jpeg-ycbcr-support).

Le CLSID de cet effet est CLSID \_ D2D1YCbCr.

-   [Propriétés d’effet](#effect-properties)
-   [Modes de sous-échantillonnage](#subsampling-modes)
-   [Modes d’interpolation](#interpolation-modes)
-   [Bitmap de sortie](#output-bitmap)
-   [Requirements](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                                          | Description                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ChromaSubsampling<br/> Sous \_ - \_ échantillonnage de chrominance d2d1 YCbCr \_<br/>    | Spécifie le sous-échantillonnage de chrominance de l’image de chrominance d’entrée. <br/> Le type est D2D1 \_ d' \_ échantillonnage de chrominance YCbCr \_ .<br/> La valeur par défaut est D2D1 le sous- \_ \_ échantillonnage de chrominance YCbCr \_ \_ auto.<br/>                                                                                                |
| TransformMatrix <br/> \_Matrice de transformation d2d1 YCbCr \_ prop \_ \_<br/> | [Matrice matrice](/previous-versions/dotnet/netframework-3.0/ms750596(v=vs.85)) spécifiant la transformation affine alignée sur l’axe de l’image. Les transformations alignées sur l’axe incluent les rotations d’échelle, de retournement et de degré 90. <br/> Le type est D2D1 \_ Matrix \_ matrice \_ F.<br/> La valeur par défaut est Matrix3x2F :: Identity ().<br/> |
| InterpolationMode<br/> \_Mode d' \_ interpolation YCbCr \_ d2d1<br/>    | Mode d’interpolation.<br/> Le type est D2D1 \_ \_ mode d’interpolation YCbCr \_ .<br/>                                                                                                                                                                                                             |



 

## <a name="subsampling-modes"></a>Modes de sous-échantillonnage



| Énumération                                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Auto- \_ échantillonnage de chrominance d2d1 YCbCr \_ \_<br/> | Ce mode tente de déduire le sous-échantillonnage de chrominance à partir des limites des images d’entrée. Lorsque cette option est sélectionnée, le plus petit plan est échantillonné à la taille du plan le plus grand et le rectangle de sortie de cet effet est l’intersection des deux plans. Quand vous utilisez ce mode, vous devez veiller à appliquer des effets aux plans d’entrée qui modifient les limites d’image, tels que la transformation de bordure, afin que le rapport de taille souhaité entre les plans soit conservé. <br/> |
| D2D1 \_ YCbCr \_ - \_ échantillonnage de chrominance \_ 420<br/>  | Le plan de chrominance est sous-échantillonné horizontalement par et sous-échantillonné verticalement par. Lorsque cette option est sélectionnée, le plan de chrominance est échantillonné horizontalement et verticalement par 2x et le rectangle de sortie de cet effet est l’intersection des deux plans.<br/>                                                                                                                                                                                                                          |
| D2D1 \_ YCbCr \_ - \_ échantillonnage de chrominance \_ 422<br/>  | Le plan de chrominance est sous-échantillonné horizontalement par. Lorsque cette option est sélectionnée, le plan de chrominance est échantillonné horizontalement par 2x et le rectangle de sortie de cet effet est l’intersection des deux plans.<br/>                                                                                                                                                                                                                                                                        |
| D2D1 \_ YCbCr \_ - \_ échantillonnage de chrominance \_ 444<br/>  | Le plan Chroma n’est pas sous-échantillonné. Lorsque cette option est sélectionnée, le rectangle de sortie de cet effet est l’intersection des deux plans.<br/>                                                                                                                                                                                                                                                                                                                                            |
| D2D1 \_ YCbCr \_ - \_ échantillonnage de chrominance \_ 440<br/>  | Le plan de chrominance est sous-échantillonné verticalement par. Lorsque cette option est sélectionnée, le plan de chrominance est échantillonné verticalement par 2x et le rectangle de sortie de cet effet est l’intersection des deux plans.<br/>                                                                                                                                                                                                                                                                            |



 

## <a name="interpolation-modes"></a>Modes d’interpolation



| Énumération                                             | Description                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Mode d' \_ interpolation YCbCr \_ d2d1 \_ le plus proche \_ voisin     | Échantillonne le point unique le plus proche et l’utilise. Ce mode utilise moins de temps de traitement, mais génère l’image de qualité la plus faible.                                                                           |
| D2D1 \_ \_ mode d’interpolation \_ YCbCr \_ linéaire                | Utilise un échantillon à quatre points et une interpolation linéaire. Ce mode utilise plus de temps de traitement que le mode voisin le plus proche, mais génère une image de qualité supérieure.                                           |
| D2D1 \_ \_ mode d’interpolation \_ YCbCr \_ cubique                 | Utilise un exemple de noyau cubique 16 pour l’interpolation. Ce mode utilise le plus de temps de traitement, mais génère une image de qualité supérieure.                                                                        |
| \_Mode d' \_ interpolation YCbCr d2d1 multi- \_ \_ \_ exemple \_ linéaire | Utilise 4 échantillons linéaires au sein d’un même pixel pour une bonne anticrénelage. Ce mode est adapté à la réduction de la taille des images avec quelques pixels.                                              |
| D2D1 \_ \_ mode d’interpolation \_ YCbCr \_ anisotrope           | Utilise le filtrage anisotrope pour échantillonner un modèle en fonction de la forme transformée de l’image bitmap.                                                                                                     |
| D2D1 \_ mode d’interpolation YCbCr de \_ \_ \_ haute \_ qualité \_ cubique  | Utilise un noyau cubique de haute qualité variable pour effectuer une pré-réduire de l’image si downscaling est impliqué dans la matrice de transformation. Utilise ensuite le mode d’interpolation cubique pour la sortie finale. |



 

## <a name="output-bitmap"></a>Bitmap de sortie

La taille de l’image bitmap de sortie dépend de la matrice de transformation appliquée à l’image.

L’effet exécute l’opération de transformation, puis applique un cadre englobant autour du résultat. La bitmap de sortie correspond à la taille du cadre englobant.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------------|---------------------------------------------------------------|
| Client minimal pris en charge | applications de \[ bureau Windows 8.1 \| Windows applications du windows Store\]            |
| Serveur minimal pris en charge | Windows Server 2012 applications de \[ bureau R2 \| Windows applications du windows Store\] |
| En-tête                   | d2d1effects \_ 1. h                                              |
| Bibliothèque                  | d2d1. lib, dxguid. lib                                          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> <dt>

[Prise en charge d’JPEG YCbCr](/windows/desktop/wic/jpeg-ycbcr-support)
</dt> <dt>

[**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)
</dt> </dl>

 

