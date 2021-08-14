---
title: Effet de la carte de tonalité HDR
description: Cet effet ajuste la plage dynamique d’une image pour mieux adapter son contenu à la capacité de l’affichage de sortie.
ms.topic: article
ms.date: 02/01/2019
ms.openlocfilehash: ce47159abe4bdf0615a76960c4c5e2db289156e89989012f659e437e93727cca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260061"
---
# <a name="hdr-tone-map-effect"></a>Effet de la carte de tonalité HDR

Cet effet ajuste la plage dynamique d’une image pour mieux adapter son contenu à la capacité de l’affichage de sortie.

Les propriétés de cet effet sont identifiées par l' [**énumération D2D1_HDRTONEMAP_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_prop), et le CLSID est **CLSID_D2D1HdrToneMap**.

## <a name="effect-properties"></a>Propriétés d’effet

| Nom complet et énumération d’index | Type et valeur par défaut | Description |
|-|-|-|
| InputMaxLuminance, D2D1_HDRTONEMAP_PROP_INPUT_MAX_LUMINANCE | FLOAT | Niveau de lumière maximal (ou MaxCLL) de l’image, en nits. |
| OutputMaxLuminance, D2D1_HDRTONEMAP_PROP_OUTPUT_MAX_LUMINANCE | FLOAT | Le MaxCLL pris en charge par la cible de sortie, dans nits, est &mdash; généralement défini sur le MaxCLL de l’affichage. |
| DisplayMode, D2D1_HDRTONEMAP_PROP_DISPLAY_MODE | [**D2D1_HDRTONEMAP_DISPLAY_MODE**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_display_mode) | Quand la valeur est **_HDR**, la courbe de mappage de la tonalité est ajustée pour s’adapter au comportement des affichages HDR courants. |

## <a name="remarks"></a>Remarques
La valeur de `InputMaxLuminance` est généralement dérivée des métadonnées de l’image. Dans les cas où les métadonnées ne sont pas présentes, vous pouvez utiliser la fonction **D2DAdvancedColorImagesRenderer :: ComputeHdrMetadata** (dans l' [exemple de rendu d’image colorimétrique avancée de Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages)) pour calculer le niveau de lumière maximal (MaxCLL) d’une image, en nits.

La valeur de `OutputMaxLuminance` est conçue pour être dérivée de l’affichage, à l’aide de [**DXGI_OUTPUT_DESC1 :: MaxLuminance**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1).

L’effet carte de tonalité HDR présente des courbes de cartes de tonalité différentes selon que l’affichage est un affichage HDR ou un affichage SDR/WCG.

Cet effet est destiné à être combiné avec l' [effet de réglage de niveau blanc](white-level-adjustment-effect.md) pour vous permettre de restituer des images HDR dans Direct2D avec une gestion des couleurs et un mappage des tons appropriés. elle est destinée à n’importe quel framework qui souhaite fournir une expérience d’affichage d’images hdr de meilleure qualité qui gère tous les formats d’image hdr Windows et s’adapte aux fonctionnalités de l’affichage (que ce soit en hdr ou WCG/SDR). Les effets sont regroupés dans l’ordre, comme décrit ci-dessous.

- Prenez l’image d’entrée, dont l’espace colorimétrique est défini par son codec. Les métadonnées peuvent spécifier whitePoint. Les métadonnées peuvent spécifier un niveau de luminance d’entrée.
- Appliquez l’effet gestion des couleurs. Convertir en espace ScRVB (CCCS).
- Appliquez l’effet carte de tonalité HDR. Réduisez le niveau de lumière de l’image au niveau souhaité.
- Appliquez l’effet d’ajustement de niveau blanc. Mettez à l’échelle le niveau blanc de l’image au niveau de blanc requis par la chaîne de permutation.
- Appliquez à nouveau l’effet gestion des couleurs. En cas de rendu dans 8bpc, convertissez-le en sRVB.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| Client minimal pris en charge | Windows 10, version 1809 (10,0 ; Build 17763) \[ applications de bureau \| UWP\] |
| En-tête | d2d1effects \_ 2. h |
| Bibliothèque | d2d1. lib, dxguid. lib |

## <a name="related-topics"></a>Rubriques connexes

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
* [Énumération D2D1_HDRTONEMAP_PROP](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_prop)
