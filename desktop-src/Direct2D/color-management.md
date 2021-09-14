---
title: Effet de gestion des couleurs
description: Utilisez l’effet gestion des couleurs pour transformer une image d’un profil de couleurs ICC (International Color Consortium) en un autre. L’effet transforme l’image en fonction de la spécification ICC.
ms.assetid: 7351C4B4-F289-4236-BB42-1B3BD8753248
keywords:
- effet de gestion des couleurs
ms.topic: article
ms.date: 02/05/2019
ms.openlocfilehash: 5f3783132e0e2af511a99fd8c44d5f899e577a3a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114149"
---
# <a name="color-management-effect"></a>Effet de gestion des couleurs

Utilisez l’effet gestion des couleurs pour transformer une image d’un profil de couleurs ICC (International Color Consortium) en un autre. L’effet transforme l’image en fonction de la [spécification ICC](https://www.color.org).

Le CLSID de cet effet est CLSID \_ D2D1ColorManagement.

- [Propriétés d’effet](#effect-properties)
- [Modes d’intention de rendu](#rendering-intent-modes)
- [Images d’entrée en mode Alpha](#input-image-alpha-modes)
- [Conformité avec la spécification ICC](#compliance-with-icc-specification)
- [Comportement du canal alpha](#alpha-channel-behavior)
- [Modes de qualité](#quality-modes)
- [Exemple de code](#sample-code)
- [Configuration requise](#requirements)
- [Rubriques connexes](#related-topics)

## <a name="effect-properties"></a>Propriétés d’effet

| Nom complet et énumération d’index | Description |
|-|-|
| SourceContext<br/> \_Contexte de \_ \_ couleur source \_ d2d1 COLORMANAGEMENT prop \_<br/> | Informations sur l’espace colorimétrique source. Le type est [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).<br/> La valeur par défaut est NULL.<br/> |
| SourceIntent<br/> \_Intention de \_ \_ rendu source \_ d2d1 COLORMANAGEMENT prop \_<br/> | L’intention de rendu ICC à utiliser. Le type est D2D1 \_ COLORMANAGEMENT \_ rendu \_ intentionnel.<br/> La valeur par défaut est D2D1 \_ COLORMANAGEMENT de \_ rendu \_ Intent \_ .<br/> |
| DestinationContext<br/> Contexte de la \_ couleur de destination d2d1 COLORMANAGEMENT \_ prop \_ \_ \_<br/> | Informations sur l’espace colorimétrique de destination. Le type est [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).<br/> La valeur par défaut est NULL.<br/> |
| DestinationIntent<br/> \_Intention de \_ \_ rendu de destination d2d1 COLORMANAGEMENT prop \_ \_<br/> | L’intention de rendu ICC à utiliser. Le type est D2D1 \_ COLORMANAGEMENT \_ rendu \_ intentionnel.<br/> La valeur par défaut est D2D1 \_ COLORMANAGEMENT de \_ rendu \_ Intent \_ .<br/> |
| AlphaMode<br/> \_ \_ \_ Mode Alpha d2d1 COLORMANAGEMENT \_ prop<br/> | Comment interpréter les données alpha contenues dans l’image d’entrée. Le type est D2D1 \_ COLORMANAGEMENT \_ alpha \_ mode.<br/> La valeur par défaut est \_ d2d1 \_ COLORMANAGEMENT \_ en mode Alpha \_ prémultiplié.<br/> |
| Qualité<br/> \_Qualité d2d1 COLORMANAGEMENT \_ prop \_<br/> | Niveau de qualité de la transformation. Le type est D2D1 \_ COLORMANAGEMENT \_ Quality.<br/> La valeur par défaut est D2D1 \_ COLORMANAGEMENT \_ Quality \_ normal.<br/> |

## <a name="rendering-intent-modes"></a>Modes d’intention de rendu

| Énumération | Description |
|-|-|
| Perception de l’intention de rendu D2D1 \_ COLORMANAGEMENT \_ \_ \_ | L’effet compresse ou développe la gamme complète des couleurs de l’image pour remplir la gamme des couleurs de l’appareil, afin que la balance grise soit préservée mais que la précision colorimétrique ne puisse pas être préservée. |
| \_ \_ \_ \_ \_ Colorimétrie relative à l’intention de rendu d2d1 COLORMANAGEMENT | L’effet préserve la chrominance des couleurs de l’image au détriment de la teinte et de la luminosité. |
| SATURATION de l’intention de rendu D2D1 \_ COLORMANAGEMENT \_ \_ \_ | L’effet ajuste les couleurs qui se trouvent en dehors de la plage de couleurs que le périphérique de sortie affiche sur la couleur la plus proche disponible. Elle ne conserve pas le point blanc. |
| \_ \_ \_ \_ COLORIMÉTRIE absolue de rendu d2d1 \_ COLORMANAGEMENT | L’effet ajuste toutes les couleurs qui se trouvent en dehors de la plage que le périphérique de sortie peut afficher sur la couleur la plus proche qui peut être rendue. L’effet ne change pas les autres couleurs et conserve le point blanc. |

## <a name="input-image-alpha-modes"></a>Images d’entrée en mode Alpha

| Énumération | Description |
|-|-|
| D2D1 \_ COLORMANAGEMENT \_ \_ en mode Alpha \_ prémultiplié | L’effet suppose que le mode Alpha est prémultiplié. |
| \_Mode d2d1 \_ COLORMANAGEMENT \_ alpha \_ simple | L’effet suppose que le mode Alpha est droit. |

## <a name="d2d1_gamma1_g2084-behavior-changes"></a>D2D1_GAMMA1_G2084 les changements de comportement
    
Si votre application utilise l’espace de [D2D1_GAMMA1_G2084](/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_gamma1) , ou l’une des valeurs d’énumération [DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) qui utilisent l’espace de couleurs SMPTE St. 084 (perception du quantificateur), l’application envisage d’utiliser les données HDR.

Les API [**ID2D1DeviceContext5 :: CreateColorContextFromSimpleColorProfile**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile__id2d1colorcontext1)) et [**ID2D1DeviceContext5 :: CreateColorContextFromDxgiColorSpace**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace) ne sont pas en compte pour cela ; au lieu de cela, le contenu HDR est mis à l’échelle pour s’ajuster à la plage 0-1 au cours de l’opération G2084 Degamma.

Dans la pratique, le contenu encodé dans cet espace gamma utilise un WhiteLevel de référence de 10 000 nits, qui serait normalement représenté dans CCCS en tant que 10 000/80 = 125,0. Ainsi, pour mieux faciliter votre application, il est plus simple pour cette conversion gamma de faire évoluer également la luminance d’un facteur de 125. à partir de Windows 10, version 1809 (10,0 ; Build 17763), le comportement de l’effet de gestion des couleurs est tel qu’il applique cette mise à l’échelle. Cela signifie que vous, en tant que développeur, n’avez pas besoin d’appliquer un deuxième [effet de réglage de niveau blanc](white-level-adjustment-effect.md) dans le pipeline.

## <a name="compliance-with-icc-specification"></a>Conformité avec la spécification ICC

L’effet de gestion des couleurs est conforme à la spécification ICC v 4.3, avec les limitations suivantes :

- L’effet prend en charge les espaces colorimétriques 1, 3 et 4 canaux.
- L’effet ne prend pas en charge les profils de couleurs ColorSpace ou nommés.

## <a name="alpha-channel-behavior"></a>Comportement du canal alpha

En général, l’effet définit alpha sur 1 (opaque) s’il n’y a aucune donnée alpha dans l’image source et les données alpha sont ignorées si l’image de destination ne contient aucune place. Le tableau ci-dessous décrit le comportement alpha.

<table>
<thead>
<tr class="header">
<th>Colorspace source, format de pixel</th>
<th>Colorspace de destination, format de pixel</th>
<th>Comportement alpha</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4">1 canal, format de pixel R $ {REMOVE} $<br />
</td>
<td>1 canal, format de pixel R</td>
<td>(Aucune donnée alpha)</td>
</tr>
<tr class="even">
<td>1 canal, format de pixel RVBA</td>
<td>Les données alpha sont définies sur 1 (opaque)</td>

</tr>
<tr class="odd">
<td>3 canaux, format de pixel RVBA</td>
<td>Les données alpha sont définies sur 1 (opaque)</td>

</tr>
<tr class="even">
<td>4 canaux, format de pixel RVBA</td>
<td>(Aucune donnée alpha)</td>

</tr>
<tr class="odd">
<td rowspan="4">1 canal, format de pixel RVBA $ {REMOVE} $<br />
</td>
<td>1 canal, format de pixel R</td>
<td>Les données alpha sont ignorées</td>
</tr>
<tr class="even">
<td>1 canal, format de pixel RVBA</td>
<td>Les données alpha sont transmises</td>

</tr>
<tr class="odd">
<td>3 canaux, format de pixel RVBA</td>
<td>Les données alpha sont transmises</td>

</tr>
<tr class="even">
<td>4 canaux, format de pixel RVBA</td>
<td>Les données alpha sont ignorées</td>

</tr>
<tr class="odd">
<td rowspan="4">3 canaux, format de pixel RVBA $ {REMOVE} $<br />
</td>
<td>1 canal, format de pixel R</td>
<td>Les données alpha sont ignorées</td>
</tr>
<tr class="even">
<td>1 canal, format de pixel RVBA</td>
<td>Les données alpha sont transmises</td>

</tr>
<tr class="odd">
<td>3 canaux, format de pixel RVBA</td>
<td>Les données alpha sont transmises</td>

</tr>
<tr class="even">
<td>4 canaux, format de pixel RVBA</td>
<td>Les données alpha sont ignorées</td>

</tr>
<tr class="odd">
<td rowspan="4">4 canaux, format de pixel RVBA $ {REMOVE} $<br />
</td>
<td>1 canal, format de pixel R</td>
<td>(Aucune donnée alpha)</td>
</tr>
<tr class="even">
<td>1 canal, format de pixel RVBA</td>
<td>Les données alpha sont définies sur 1 (opaque)</td>

</tr>
<tr class="odd">
<td>3 canaux, format de pixel RVBA</td>
<td>Les données alpha sont définies sur 1 (opaque)</td>

</tr>
<tr class="even">
<td>4 canaux, format de pixel RVBA</td>
<td>(Aucune donnée alpha)</td>

</tr>
</tbody>
</table>

## <a name="quality-modes"></a>Modes de qualité

| Mode | Description |
|-|-|
| \_Preuve de \_ qualité d2d1 COLORMANAGEMENT \_ | Mode de qualité le plus bas. Ce mode nécessite le niveau de fonctionnalité 9 \_ 1 ou supérieur. |
| D2D1 \_ COLORMANAGEMENT \_ Quality \_ normal | Mode de qualité normal. Ce mode nécessite le niveau de fonctionnalité 9 \_ 1 ou supérieur. |
| \_ \_ Meilleure qualité d2d1 \_ COLORMANAGEMENT | Mode de qualité optimal. Ce mode requiert le niveau de fonctionnalité 10 \_ 0 ou supérieur, ainsi que les mémoires tampons de précision à virgule flottante. Ce mode prend en charge la précision à virgule flottante, ainsi que la plage étendue, comme défini dans la spécification ICC v 4.3. |

L’effet de gestion des couleurs échoue lors du dessin si l’application demande un mode de qualité qui n’est pas pris en charge par le matériel. Vous pouvez déterminer le niveau de fonctionnalité quand vous appelez [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice). Vous pouvez vérifier la prise en charge de la mémoire tampon à virgule flottante en appelant [**ID2D1EffectContext :: IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported) avec la valeur d2d1 de précision de la [**\_ mémoire tampon \_ \_ 32BPC \_ float**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_buffer_precision).

## <a name="sample-code"></a>Exemple de code

Pour obtenir un exemple de cet effet, téléchargez l' [exemple ajustement des photos des effets Direct2D](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)et consultez la leçon 4 de l’exemple.

## <a name="requirements"></a>Spécifications

| Condition requise | Valeur |
|-|-|
| Client minimal pris en charge | mise à jour Windows 8 et de plateforme pour les applications de bureau Windows 7 Windows les applications du windows \[ \| Store\] |
| Serveur minimal pris en charge | mise à jour Windows 8 et de plateforme pour les applications de bureau Windows 7 Windows les applications du windows \[ \| Store\] |
| En-tête | d2d1effects. h |
| Bibliothèque | d2d1. lib, dxguid. lib |

## <a name="related-topics"></a>Rubriques connexes

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
