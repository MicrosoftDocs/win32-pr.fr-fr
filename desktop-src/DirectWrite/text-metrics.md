---
title: Mesures de texte
description: pour faciliter la mise en page, la sélection personnalisée des polices et d’autres opérations gourmandes en métriques, à partir de Windows 8, DirectWrite dispose d’un certain nombre de nouvelles api pour exprimer toutes les informations relatives aux polices dont vous pouvez avoir besoin pour développer des applications de texte enrichi.
ms.assetid: 9df8c675-6f4d-4de7-916e-7dc51f5f04aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73647ae4521b23afb399a4c66c8b25cdc46ba1b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009968"
---
# <a name="text-metrics"></a>Mesures de texte

pour faciliter la mise en page, la sélection personnalisée des polices et d’autres opérations gourmandes en métriques, à partir de Windows 8, [DirectWrite](direct-write-portal.md) dispose d’un certain nombre de nouvelles api pour exprimer toutes les informations relatives aux polices dont vous pouvez avoir besoin pour développer des applications de texte enrichi.

## <a name="panose"></a>PANOSE

Panose est un système de classification visuelle permettant d’identifier les polices. La classification Panose contient des informations sur la famille, le style Serif, le poids, la proportion, le contraste, le trait, le style ARM, la hauteur X, etc. Ces informations décrivent le style visuel de la police. Ces informations sont importantes car les polices avec des valeurs Panose similaires semblent similaires. Cela est très utile dans les situations où une police n’est pas disponible et que l’application doit revenir à une police disponible. La comparaison de valeurs Panose pour les polices vous permet de choisir une police similaire visuellement à la police d’origine.

Pour accéder aux informations Panose pour une police, utilisez la méthode [**GetPanose**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getpanose) sur les interfaces [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) et [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) . Cette méthode retourne une énumération [**\_ Panose DWRITE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_panose) qui contient toutes les informations Panose pour cette police.

## <a name="additional-metrics"></a>Métriques supplémentaires

à partir de Windows 8, l’API [DirectWrite](direct-write-portal.md) prend également en charge un certain nombre de nouvelles métriques afin d’exprimer des informations utiles sur les polices pour votre application. Ces nouvelles métriques incluent ces informations.

-   Métriques du cadre englobant des glyphes gauche, droit, supérieur et inférieur.
-   Positionnement X et Y pour les éléments en exposant et en indice.
-   Informations de mise à l’échelle X et Y pour les éléments en exposant et en indice.
-   Indique si la police a des métriques typographiques.

Ces informations sont toutes disponibles via la nouvelle méthode [**GetMetrics**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getmetrics) sur les interfaces [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) et [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) . Cette méthode retourne une structure [**DWRITE \_ font \_ METRICS1**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_font_metrics1) qui contient toutes ces informations.

## <a name="caret-metrics"></a>Mesures du signe insertion

Pour créer des applications de modification de texte, vous devez accéder aux informations sur la façon de dessiner le signe insertion qui parcourt le texte. à partir de Windows 8, [DirectWrite](direct-write-portal.md) fournit la méthode [**GetCaretMetrics**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getcaretmetrics) sur les interfaces [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) et [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) pour ce scénario. **GetCaretMetrics** retourne une énumération de [**\_ \_ mesures du signe insertion DWRITE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_caret_metrics) qui contient des informations sur la pente et le décalage du signe insertion le long de la ligne de base.

Ces informations sont particulièrement utiles si vous souhaitez être en mesure de faire en sorte que la pente du signe insertion soit appropriée avec du texte en italique.

## <a name="monospaced-discoverability"></a>Détectabilité à espacement fixe

Les applications qui permettent à vos utilisateurs d’écrire du code informatique utilisent souvent des polices à espacement fixe à la place de polices plus traditionnelles. vous pouvez ainsi avoir davantage de contrôle sur la sélection des polices dans les applications liées au développement, [DirectWrite](direct-write-portal.md) exprime si une police est à espacement fixe ou non à l’aide de l’API. La méthode [**IsMonospacedFont**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-ismonospacedfont) sur l’interface [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) retourne une valeur booléenne qui indique si la police est à espacement fixe.

## <a name="font-name-matching"></a>Correspondance de nom de police

Les applications de texte enrichi comme les lecteurs PDF doivent être en mesure de faire correspondre les polices de leur contenu avec les polices du système. vous devez donc accéder aux noms complets des polices dans plusieurs formats. vous pouvez ainsi mieux faire correspondre les polices, [DirectWrite](direct-write-portal.md) contient une énumération qui exprime les informations d’attribution de noms complètes sur une police dans de nombreux formats.

vous utilisez l’énumération de l' [**\_ ID de \_ chaîne \_ d’information DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_informational_string_id) pour obtenir le nom complet, le nom PostScript et PostScript nom CID de toute police sur le système. Ces informations sont utiles lorsque vous devez faire correspondre les polices de votre application aux polices appropriées sur le système local.

## <a name="glyph-advances"></a>Avances de glyphe

La méthode **GetGlyphAdvances** sur les interfaces [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) et [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) prend le nombre de glyphes et les index dont vous avez besoin pour obtenir des informations sur, puis retourne les avances pour les glyphes en question.

## <a name="unicode-ranges"></a>Plages Unicode

Les applications qui souhaitent gérer leur propre sélection de police doivent accéder aux plages Unicode prises en charge par la police. De cette façon, si un point de contenu Unicode n’est pas pris en charge par la police, l’application peut choisir une police appropriée qui contient ce glyphe. Sans ces informations, l’application peut utiliser une police qui ne contient pas tous les glyphes nécessaires pour afficher les informations présentes.

La méthode [**GetUnicodeRanges**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getunicoderanges) sur les interfaces [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) et [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) prend le nombre maximal de plages transmises à partir du client et retourne les plages réelles prises en charge par la police.

## <a name="eudc-font-collection"></a>Collection de polices EUDC

Utilisez la méthode [**GetEudcFontCollection**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefactory1-geteudcfontcollection) sur l’interface [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1) pour accéder à la collection de polices EUDC. Cette méthode fonctionne de la même façon que [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection), mais retourne à la place un pointeur vers une collection de polices EUDC.

 

 