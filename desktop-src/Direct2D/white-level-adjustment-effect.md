---
title: Effet de la carte de ton blanc
description: Cet effet permet de mettre à l’échelle de manière linéaire le niveau de blanc d’une image. Cela s’avère particulièrement utile lorsque vous convertissez un espace de luminance à l’écran et un espace de luminance référencé, ou vice versa.
ms.topic: article
ms.date: 02/01/2019
ms.openlocfilehash: 70a38f37f5a5461b968099bebe4be120a727c053
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942366"
---
# <a name="white-level-adjustment-effect"></a>Effet de réglage du niveau blanc

Cet effet permet de mettre à l’échelle de manière linéaire le niveau de blanc d’une image. Cela s’avère particulièrement utile lorsque vous convertissez un espace de luminance à l’écran et un espace de luminance référencé, ou vice versa.

Les propriétés de cet effet sont identifiées par l' [**énumération D2D1_WHITELEVELADJUSTMENT_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_whiteleveladjustment_prop), et le CLSID est **CLSID_D2D1WhiteLevelAdjustment**.

## <a name="effect-properties"></a>Propriétés d’effet

| Nom complet et énumération d’index | Type et valeur par défaut | Description |
|-|-|-|
| InputWhiteLevel, D2D1_WHITELEVELADJUSTMENT_PROP_INPUT_WHITE_LEVEL | FLOAT | Niveau de blanc de l’image d’entrée, en nits. |
| OutputWhiteLevel, D2D1_WHITELEVELADJUSTMENT_PROP_OUTPUT_WHITE_LEVEL | FLOAT | Niveau de blanc de l’image de sortie, en nits. |

## <a name="remarks"></a>Notes
Cet effet est destiné à être combiné avec l' [effet carte de tonalité HDR](hdr-tone-map-effect.md) pour vous permettre de restituer des images HDR dans Direct2D avec une gestion des couleurs et un mappage des tons appropriés. Pour plus d’informations, consultez les **Remarques** de cette rubrique. Ces effets sont destinés à toute infrastructure qui souhaite fournir une expérience d’affichage d’image HDR de meilleure qualité qui gère tous les formats d’image HDR Windows et s’adapte aux fonctionnalités de l’affichage (que ce soit en HDR ou WCG/SDR).

Sur Windows, tout le contenu SDR/WCG est supposé être dans un espace de luminance à l’écran, ce qui signifie que le niveau de blanc du contenu doit être mis à l’échelle jusqu’au niveau blanc de l’affichage avant d’être présenté au final. Toutefois, ce n’est pas toujours la responsabilité de votre application. En revanche, le contenu HDR est supposé être dans un espace de luminance à la scène, ce qui signifie qu’il ne doit pas être mis à l’échelle pour correspondre au niveau de blanc de l’affichage. Cela dit, votre application devra peut-être effectuer une mise à l’échelle dans certaines circonstances lors du rendu du contenu HDR pour s’assurer qu’il s’agit du résultat net.

Lorsque le bureau Windows est en mode SDR ou WCG, le bureau est constitué d’un espace de luminance à l’écran. Toutefois, si le bureau Windows est en mode HDR, la composition du Bureau se produit dans l’espace de luminance à la scène. Cela dit, le Gestionnaire de fenêtrage (DWM) lui-même effectue des réglages de luminance (souvent appelés SDRBoost) pour les surfaces de composition 8 bits et simplifie votre application pour ce cas. Même dans ce cas, l’augmentation automatique signifie que le rôle de votre application dans la conversion d’un espace de luminance à un autre dépend du format de composition utilisé par votre application pour présenter son contenu.

Le tableau ci-dessous décrit les cas où votre application doit et ne doit pas effectuer un ajustement de niveau blanc, ainsi que la nature de cette modification. En général, l’ajustement dépend de trois facteurs.

1. Colorspace de contenu d’entrée. Si votre contenu d’entrée contient ou non des valeurs de luminance HDR (High dynamique Range). Le contenu WCG se comporte comme SDR pour le comportement de luminance.
2. Format de composition. Format de pixel de la surface cible présentée au DWM &mdash; , par exemple, une chaîne de [permutation](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) ou une [surface de composition](/uwp/api/Windows.UI.Composition.ICompositionSurface). Lors du rendu à l’aide de Direct2D, il peut s’agir de **UINT8** ou **FP16**.
3. Mode couleur avancée du bureau. Indique si le DWM s’exécute en mode SDR, WCG ou HDR pour l’affichage actuel. Obtenez ces informations par le biais de [**DXGI_OUTPUT_DESC1 :: colorspace**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1) ou [**AdvancedColorInfo. CurrentAdvancedColorKind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind).

Sur la base de ces trois facteurs, vous devez définir les valeurs appropriées pour les `InputWhiteLevel` `OutputWhiteLevel` Propriétés et.

|Contenu d’entrée|Format de composition|Mode de couleurs avancé|InputWhiteLevel|OutputWhiteLevel|
|-|-|-|-|-|
|SDR/WCG|**DESTINÉES**|Quelconque|N/A|N/A|
|SDR/WCG|**FP16**|SDR/WCG|N/A|N/A|
|SDR/WCG|**FP16**|ÉTENDUE|SDRWhite|80|
|ÉTENDUE|Quelconque|SDR/WCG|80|[**DXGI_OUTPUT_DESC1 :: MaxLuminance**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1)|
|ÉTENDUE|**DESTINÉES**|ÉTENDUE|80|SDRWhite|
|ÉTENDUE|**FP16**|ÉTENDUE|N/A|N/A|

Dans le tableau, la valeur 80 est le niveau de référence blanc, en nits, pour le contenu sRVB ou ScRVB. Pour ce faire, vous pouvez utiliser la constante [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](/windows/desktop/direct2d/direct2d-constants), qui est définie dans `d2d1effects_2.h` . La valeur `SDRWhite` est le nombre de nits que l’affichage doit utiliser pour afficher le contenu en blanc sRVB. Vous pouvez récupérer cette valeur en accédant à la propriété [**AdvancedColorInfo. SdrWhiteLevelInNits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits) . La valeur N/A signifie que le réglage du niveau de blanc n’est pas utilisé dans ce scénario. vous pouvez soit supprimer l’effet de votre graphique, soit définir des valeurs pour une absence d’opération.

Notez que, dans les cas où un réglage du niveau de blanc n’est pas requis par l’application, le DWM ou l’affichage peut gérer la conversion de l’espace de luminance à l’affichage et l’espace de luminance référencé.

- En mode SDR/WCG, la conversion se produit après la composition DWM et s’applique à tout le contenu présenté à cet affichage. L’affichage effectue implicitement cette conversion.
- En mode HDR, la conversion est effectuée automatiquement par le DWM avant la composition, tant que la surface de composition de votre application est SDR.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| Client minimal pris en charge | Windows 10, version 1809 (10,0 ; Build 17763) \[ applications de bureau \| UWP\] |
| En-tête | d2d1effects \_ 2. h |
| Bibliothèque | d2d1. lib, dxguid. lib |

## <a name="related-topics"></a>Rubriques connexes

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
* [Énumération D2D1_WHITELEVELADJUSTMENT_PROP](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_whiteleveladjustment_prop)
