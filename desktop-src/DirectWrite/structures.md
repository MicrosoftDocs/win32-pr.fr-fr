---
title: Structures DirectWrite
description: DirectWrite définit les structures suivantes.
ms.assetid: 348dd001-bad9-4f1a-a5f5-84b118a5e2d4
keywords:
- DirectWrite, structures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea132cde1ea6b740cc02b938767f941e9c999e5a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106543547"
---
# <a name="directwrite-structures"></a>Structures DirectWrite

DirectWrite définit les structures suivantes.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md) | Représente des données bitmap au format BGRA32. |
| [**\_mesures du signe insertion DWRITE \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_caret_metrics) | La structure de [**\_ \_ métriques du signe insertion DWRITE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_caret_metrics) spécifie les métriques pour l’emplacement du signe insertion dans une police. |
| [**\_métriques de cluster DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_cluster_metrics) | Contient des informations sur un cluster de glyphes. |
| [**DWRITE \_ couleur \_ F**](dwrite-color-f.md) | Décrit les composants rouge, vert, bleu et alpha d’une couleur. |
| [**DWRITE de l’exécution du glyphe de \_ couleur \_ \_**](/windows/win32/api/DWrite_2/ns-dwrite_2-dwrite_color_glyph_run) | Contient les informations requises par les convertisseurs pour dessiner des exécutions de glyphe avec les informations de couleur de glyphe. |
| [**DWRITE \_ de \_ glyphe de couleur \_ run1**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_color_glyph_run1) | Représente une exécution de glyphes de couleurs. La méthode IDWriteFactory4 :: TranslateColorGlyphRun retourne une collection ordonnée de séquences de glyphes de couleurs de types variables en fonction de ce que la police prend en charge. |
| [**\_fragment de fichier DWRITE \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_file_fragment) | Représente une plage d’octets dans un fichier de police. |
| [**DWRITE_FONT_AXIS_RANGE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range) | Représente la plage minimale et maximale des valeurs possibles pour un axe des polices. |
| [**DWRITE_FONT_AXIS_VALUE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value) | Représente une valeur pour un axe des polices. Utilisé lors de l’interrogation et de la création d’instances de police. |
| [**\_fonctionnalité de police DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) | Spécifie les propriétés utilisées pour identifier et exécuter des fonctionnalités typographiques dans le type de police actuel. |
| [**\_métriques de police DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) | La structure de [**\_ \_ métriques de police DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) spécifie les mesures qui s’appliquent à tous les glyphes dans le type de police. |
| [**DWRITE \_ police \_ METRICS1**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1) | La structure [**DWRITE \_ font \_ METRICS1**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1) spécifie les métriques qui s’appliquent à tous les glyphes dans le type de police. |
| [**DWRITE \_ , \_ propriété de police**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) | Propriété font utilisée pour le filtrage des jeux de polices et la génération d’un jeu de polices avec des propriétés explicites. |
| [**\_données d' \_ image de glyphe DWRITE \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_glyph_image_data) | Données pour un glyphe unique à partir de GetGlyphImageData. |
| [**\_métriques du GLYPHE DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) | Spécifie les métriques d’un glyphe individuel. |
| [**\_décalage du GLYPHE DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) | Ajustement facultatif de la position d’un glyphe. |
| [**\_exécution du GLYPHE DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) | Contient les informations requises par les convertisseurs pour dessiner des exécutions de glyphes. |
| [**Description de l' \_ exécution du GLYPHE DWRITE \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run_description) | Contient des propriétés supplémentaires relatives à celles dans [**DWRITE \_ Glyphs \_ Run**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run). |
| [**\_ \_ métriques de test de positionnement DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_hit_test_metrics) | Décrit la région obtenue par un test de positionnement. |
| [**\_métriques de l’objet Inline DWRITE \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) | Contient des propriétés décrivant la mesure géométrique d’un objet Inline défini par l’application. |
| [**\_opportunité de justification DWRITE \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) | La structure d' [**\_ \_ opportunité de justification DWRITE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) spécifie les informations de justification par glyphe. |
| [**point d’arrêt de \_ ligne DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_line_breakpoint) | Caractéristiques des points d’arrêt de ligne d’un caractère. |
| [**\_métriques de ligne DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_line_metrics) | Contient des informations sur une ligne de texte mise en forme. |
| [**DWRITE \_ ligne \_ METRICS1**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_metrics1) | Contient des informations sur une ligne de texte mise en forme. |
| [**DWRITE de \_ ligne \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_spacing) | |
| [**\_matrice DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) | La structure de la [**\_ matrice DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) spécifie la transformation Graphics à appliquer aux glyphes rendus. |
| [**\_métriques de dépassement DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics) | Indique combien de DIP (device independent pixels) visibles surpassent chaque côté de la disposition ou des objets en ligne. |
| [**DWRITE \_ Panose**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose) | L’Union [**DWRITE \_ Panose**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose) décrit les valeurs de classification des polices que vous utilisez avec [**IDWriteFont1 :: GetPanose**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getpanose) pour sélectionner et faire correspondre à la police. |
| [**\_analyse de script DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) | Stocke l’Association de texte et son script de système d’écriture, ainsi que certains attributs d’affichage. |
| [**\_Propriétés du script DWRITE \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties) | La structure des [**\_ \_ Propriétés du script DWRITE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties) spécifie les propriétés de script pour la navigation et la justification du signe insertion. |
| [**Propriétés de glyphe de mise en \_ forme DWRITE \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties) | Contient les propriétés de sortie de mise en forme d’un glyphe de sortie. |
| [**Propriétés du texte de mise en \_ forme DWRITE \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties) | Mise en forme des propriétés de sortie pour un glyphe de sortie. |
| [**DWRITE \_ barré**](/windows/win32/api/dwrite/ns-dwrite-dwrite_strikethrough) | Contient des informations relatives à la taille et à l’emplacement de strikethroughs. |
| [**\_métriques de texte DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_metrics) | Contient les métriques associées au texte après la disposition. |
| [**DWRITE \_ texte \_ METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1) | Contient les métriques associées au texte après la disposition. |
| [**\_plage de texte DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) | Spécifie une plage de positions de texte où le format est appliqué dans le texte représenté par un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . |
| [**suppression de DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_trimming) | Spécifie l’option de suppression pour le débordement du texte dans la zone de disposition.  |
| [**\_fonctionnalités typographiques DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features) | Contient un ensemble de fonctionnalités typographiques à appliquer pendant la mise en forme du texte. |
| [**DWRITE \_ souligné**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) | Contient des informations sur la largeur, l’épaisseur, le décalage, la hauteur d’exécution, le sens de lecture et le sens du déroulement d’un trait de soulignement.  |
| [**\_plage Unicode \_ DWRITE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range) | La structure de [**\_ \_ plage Unicode DWRITE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range) spécifie la plage de points de code Unicode. |



 

