---
title: Glyphes et exécutions de glyphes
description: les glyphes et les exécutions de glyphes sont disponibles dans la couche la plus basse des fonctionnalités de l’API DirectWrite, la couche de rendu de glyphes.
ms.assetid: e670cb65-1fcb-46fd-ac0b-02eaaaa51996
keywords:
- DirectWrite, glyphes
- DirectWrite, exécutions de glyphes
- exécutions de glyphes
- glyphes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b39d1ca47249adf11f4e1e2072620f24553f7e299e0690c1cc147c4f74a4939f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902918"
---
# <a name="glyphs-and-glyph-runs"></a>Glyphes et exécutions de glyphes

les glyphes et les exécutions de glyphes sont disponibles dans la couche la plus basse des fonctionnalités de l’API [DirectWrite](direct-write-portal.md) , la couche de rendu de glyphes.

## <a name="glyphs"></a>Glyphes

Un glyphe est une représentation physique d’un caractère dans une police donnée. Les caractères peuvent avoir de nombreux glyphes, chaque police d’un système pouvant définir un glyphe différent pour ce caractère.

Au moins deux glyphes peuvent également être combinés en un seul glyphe, ce processus est appelé composition de glyphes. Cela peut également être effectué dans le sens inverse, un seul glyphe fractionné en plusieurs glyphes, appelé décomposition de glyphes.

### <a name="alternate-glyphs"></a>Autres glyphes

Les polices peuvent fournir des glyphes alternatifs pour les caractères, tels que les glyphes de substitution stylistiques pour la police OpenType Pericles, comme indiqué dans la capture d’écran suivante. Les caractères « A », « E » et « O » sont rendus avec des glyphes de substitution stylistiques.

![capture d’écran de « antiquité Green Mythology », avec les glyphes « a », « e » et « o » à l’aide de glyphes alternatifs](images/opentypealternateglyphs.png)

Des glyphes ornés sont un autre exemple de glyphes de substitution. La capture d’écran suivante montre les glyphes standard et les glyphes à lettres ornées pour la police Pescadero.

![capture d’écran des lettres « a » à « n » dans les glyphes standard et ornés](images/opentypeswashstandard.png)

Les lettres ornées et autres caractéristiques typographiques, y compris les glyphes de substitution plus élaborés, sont disponibles via [OpenType](../intl/opentype-font-format.md). Les fonctionnalités typographiques OpenType peuvent être appliquées à une plage de texte à l’aide de [**IDWriteTextLayout :: SetTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) et en passant la constante d’énumération de [**\_ \_ \_ balise de la fonctionnalité de police DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) associée à la fonctionnalité souhaitée.

## <a name="glyph-runs"></a>Exécutions de glyphes

Une exécution de glyphes représente un jeu contigu de glyphes qui ont tous le même type et la même taille de police, ainsi que le même effet de dessin client, le cas échéant. Le soulignement et le barré ne font pas partie de l’exécution de glyphes de la plage de texte à laquelle ils sont appliqués, et sont dessinés ultérieurement. Les objets insérés, tels que les images, sont également dessinés séparément, car ils ne font pas partie d’une police.

### <a name="the-idwritefontface-interface"></a>Interface IDWriteFontFace

[DirectWrite](direct-write-portal.md) utilise le même système pour la classification des polices que Windows Pesentation Foundation (WPF), il peut donc y avoir plusieurs polices physiques pour chaque famille de polices. un type de police, tel que l’interface [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) dans DirectWrite, représente une police physique, avec une pondération, une inclinaison et une étirement spécifiques. Il contient le type de type de police, les références de fichier appropriées, les données d’identification de visage et diverses données de police telles que les métriques, les noms et les contours de glyphe.

Le [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) peut être créé directement à partir d’un nom de police ou obtenu à partir d’une collection de polices.

### <a name="glyph-metrics"></a>Métriques de glyphe

Des métriques sont associées à des glyphes individuels. Vous pouvez obtenir les métriques de tous les glyphes d’une exécution de glyphe à l’aide de la méthode [**IDWriteFontFace :: GetDesignGlyphMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getdesignglyphmetrics) . Cela retourne une structure de [**\_ \_ métriques de glyphes DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) qui a la largeur d’avance, le palier gauche et le côté droit, le palier de haut en bas, la hauteur et l’origine de la ligne de base verticale.

Le diagramme suivant montre différentes métriques de deux caractères de glyphe différents.

![diagramme des métriques de deux glyphes différents](images/twoglyphs.png)

## <a name="drawing-a-glyph-run"></a>Dessin d’une exécution de glyphe

Lors de l’implémentation d’un convertisseur de texte personnalisé, le rendu des glyphes est géré par [**IDWriteTextRenderer ::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), une méthode de rappel que vous implémentez dans le cadre d’une classe dérivée de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer). La structure d' [**\_ \_ exécution de glyphes DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) transmise à [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) contient un objet [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) , nommé *fontFace*, qui représente le type de police pour l’exécution de glyphe entière.

L’objet [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) fournit également la méthode [**GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) , qui calcule les contours de glyphe à l’aide d’un rappel de récepteur Geometry spécifié, tel que [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) lors du rendu avec [Direct2D](../direct2d/direct2d-portal.md).

Pour plus d’informations, consultez la rubrique [comment implémenter un convertisseur de texte personnalisé](how-to-implement-a-custom-text-renderer.md) .

 

 