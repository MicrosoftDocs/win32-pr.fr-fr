---
title: Énumérations DirectWrite
description: DirectWrite définit les énumérations suivantes.
ms.assetid: 809ccacd-ff23-4d7b-a177-e7a9937c0c5a
keywords:
- DirectWrite, énumérations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baf26901583a84e34d64a2a1c72fdfa17bbc903b
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587928"
---
# <a name="directwrite-enumerations"></a>Énumérations DirectWrite

DirectWrite définit les énumérations suivantes.

## <a name="in-this-section"></a>Contenu de cette section

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rubrique</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_automatic_font_axes"><strong>DWRITE_AUTOMATIC_FONT_AXES</strong></a></td>
<td>Définit des constantes qui spécifient certains axes qui peuvent être appliqués automatiquement dans la disposition pendant la sélection de la police.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_baseline"><strong>DWRITE_BASELINE</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_baseline"><strong>DWRITE_BASELINE</strong></a> contient des valeurs qui spécifient la ligne de base pour l’alignement du texte.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_break_condition"><strong>DWRITE_BREAK_CONDITION</strong></a></td>
<td>Indique la condition à la périphérie de l’objet inline ou du texte utilisé pour déterminer le comportement de saut de ligne.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_container_type"><strong>DWRITE_CONTAINER_TYPE</strong></a></td>
<td>Spécifie le format de conteneur d’une ressource de police. Un format de conteneur est différent d’un format de fichier de police (DWRITE_FONT_FILE_TYPE), car le conteneur décrit le conteneur dans lequel le fichier de police sous-jacent est empaqueté. </td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type"><strong>DWRITE_FACTORY_TYPE</strong></a></td>
<td>Spécifie le type d’objet de fabrique DirectWrite.</td>
</tr>
<tr>
<td><a href="/windows/windows-app-sdk/api/win32/dwrite/ne-dwrite-dwrite_factory_type"><strong>DWRITE_FACTORY_TYPE (DWriteCore)</strong></a></td>
<td>Spécifie le type d’objet de fabrique DirectWrite.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_flow_direction"><strong>DWRITE_FLOW_DIRECTION</strong></a></td>
<td>Indique la direction de la position des lignes de texte l’une par rapport à l’autre. </td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_attributes"><strong>DWRITE_FONT_AXIS_ATTRIBUTES</strong></a></td>
<td>Définit des constantes qui spécifient des attributs pour un axe des polices.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_tag"><strong>DWRITE_FONT_AXIS_TAG</strong></a></td>
<td>Définit des constantes qui spécifient un identificateur à quatre caractères pour un axe des polices.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_face_type"><strong>DWRITE_FONT_FACE_TYPE</strong></a></td>
<td>Indique le format de fichier d’une police complète.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_family_model"><strong>DWRITE_FONT_FAMILY_MODEL</strong></a></td>
<td>Définit des constantes qui spécifient comment les familles de polices sont regroupées.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag"><strong>DWRITE_FONT_FEATURE_TAG</strong></a></td>
<td>Valeur qui indique la fonctionnalité typographique du texte fourni par la police.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_file_type"><strong>DWRITE_FONT_FILE_TYPE</strong></a></td>
<td>Type d’une police représentée par un fichier de police unique. Les formats de police qui se composent de plusieurs fichiers, par exemple, tapez 1. PFM et. PFB, ont des valeurs d’énumération distinctes pour chacun des types de fichiers.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_line_gap_usage"><strong>DWRITE_FONT_LINE_GAP_USAGE</strong></a></td>
<td>Spécifiez si la valeur <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics"><strong>DWRITE_FONT_METRICS</strong></a>:: lineGap doit faire partie des métriques de ligne</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id"><strong>DWRITE_FONT_PROPERTY_ID</strong></a></td>
<td>Identifie une chaîne dans une police.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_simulations"><strong>DWRITE_FONT_SIMULATIONS</strong></a></td>
<td>Spécifie les simulations de style algorithmique à appliquer au type de police. Les simulations de gras et oblique peuvent être combinées via une opération de bits or.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_source_type"><strong>DWRITE_FONT_SOURCE_TYPE</strong></a></td>
<td>Définit des constantes qui spécifient le mécanisme par lequel une police a été incluse dans un jeu de polices.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch"><strong>DWRITE_FONT_STRETCH</strong></a></td>
<td>Représente le degré auquel une police a été étirée par rapport aux proportions normales d’une police.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style"><strong>DWRITE_FONT_STYLE</strong></a></td>
<td>Représente le style d’un type de police comme normal, italique ou oblique.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight"><strong>DWRITE_FONT_WEIGHT</strong></a></td>
<td>Représente la densité d’un caractère, en termes de clarté ou d’épaisseur des traits.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats"><strong>DWRITE_GLYPH_IMAGE_FORMATS</strong></a></td>
<td>Spécifie les formats pris en charge dans la police, à l’échelle de la police ou par glyphe.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_glyph_orientation_angle"><strong>DWRITE_GLYPH_ORIENTATION_ANGLE</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_glyph_orientation_angle"><strong>DWRITE_GLYPH_ORIENTATION_ANGLE</strong></a> contient des valeurs qui spécifient la façon dont le glyphe est orienté vers l’axe des x.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode"><strong>DWRITE_GRID_FIT_MODE</strong></a></td>
<td>Spécifie s’il faut activer l’ajustement de la grille des contours de glyphe (également appelé affinage).</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_informational_string_id"><strong>DWRITE_INFORMATIONAL_STRING_ID</strong></a></td>
<td>Énumération de chaîne informatif qui identifie une chaîne incorporée dans un fichier de police.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_line_spacing_method"><strong>DWRITE_LINE_SPACING_METHOD</strong></a></td>
<td>Méthode utilisée pour l’interligne dans une disposition de texte.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_locality"><strong>DWRITE_LOCALITY</strong></a></td>
<td>Spécifie l’emplacement d’une ressource.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode"><strong>DWRITE_MEASURING_MODE</strong></a></td>
<td>Indique la méthode de mesure utilisée pour la disposition du texte.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_number_substitution_method"><strong>DWRITE_NUMBER_SUBSTITUTION_METHOD</strong></a></td>
<td>Spécifie comment appliquer la substitution de nombres aux chiffres et à la ponctuation associée.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_optical_alignment"><strong>DWRITE_OPTICAL_ALIGNMENT</strong></a></td>
<td>Mode d’alignement de la marge optique.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_outline_threshold"><strong>DWRITE_OUTLINE_THRESHOLD</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_outline_threshold"><strong>DWRITE_OUTLINE_THRESHOLD</strong></a> contient des valeurs qui spécifient la stratégie utilisée par la méthode <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getrecommendedrenderingmode"><strong>IDWriteFontFace1 :: GetRecommendedRenderingMode</strong></a> pour déterminer s’il faut restituer les glyphes en mode plan.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_arm_style"><strong>DWRITE_PANOSE_ARM_STYLE</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_arm_style"><strong>DWRITE_PANOSE_ARM_STYLE</strong></a> contient des valeurs qui spécifient le style d’arrêt des tiges et des letterforms arrondis pour le texte.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_aspect"><strong>DWRITE_PANOSE_ASPECT</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_aspect"><strong>DWRITE_PANOSE_ASPECT</strong></a> contient des valeurs qui spécifient le rapport entre la largeur et la hauteur de la face de caractère.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_aspect_ratio"><strong>DWRITE_PANOSE_ASPECT_RATIO</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_aspect_ratio"><strong>DWRITE_PANOSE_ASPECT_RATIO</strong></a> contient des valeurs qui spécifient des informations sur le rapport entre la largeur et la hauteur de la face de caractère.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_character_ranges"><strong>DWRITE_PANOSE_CHARACTER_RANGES</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_character_ranges"><strong>DWRITE_PANOSE_CHARACTER_RANGES</strong></a> contient des valeurs qui spécifient le type de caractères disponibles dans la police.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_contrast"><strong>DWRITE_PANOSE_CONTRAST</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_contrast"><strong>DWRITE_PANOSE_CONTRAST</strong></a> contient des valeurs qui spécifient le rapport entre le point le plus épais et le point le plus fin du trait pour une lettre comme « O » majuscule.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_decorative_class"><strong>DWRITE_PANOSE_DECORATIVE_CLASS</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_decorative_class"><strong>DWRITE_PANOSE_DECORATIVE_CLASS</strong></a> contient des valeurs qui spécifient l’apparence générale de la face de caractère.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_decorative_topology"><strong>DWRITE_PANOSE_DECORATIVE_TOPOLOGY</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_decorative_topology"><strong>DWRITE_PANOSE_DECORATIVE_TOPOLOGY</strong></a> contient des valeurs qui spécifient les caractéristiques de forme globale de la police.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_family"><strong>DWRITE_PANOSE_FAMILY</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_family"><strong>DWRITE_PANOSE_FAMILY</strong></a> contient des valeurs qui spécifient le type de classification de police.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_fill"><strong>DWRITE_PANOSE_FILL</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_fill"><strong>DWRITE_PANOSE_FILL</strong></a> contient des valeurs qui spécifient le type de traitement du remplissage et de la ligne.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_finials"><strong>DWRITE_PANOSE_FINIALS</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_finials"><strong>DWRITE_PANOSE_FINIALS</strong></a> contient des valeurs qui spécifient comment le caractère se termine et où les hampes rien sont traités.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_letterform"><strong>DWRITE_PANOSE_LETTERFORM</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_letterform"><strong>DWRITE_PANOSE_LETTERFORM</strong></a> contient des valeurs qui spécifient l’arrondi de LETTERFORM pour le texte.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_lining"><strong>DWRITE_PANOSE_LINING</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_lining"><strong>DWRITE_PANOSE_LINING</strong></a> contient des valeurs qui spécifient la gestion du contour pour la police décorative.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_midline"><strong>DWRITE_PANOSE_MIDLINE</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_midline"><strong>DWRITE_PANOSE_MIDLINE</strong></a> contient des valeurs qui spécifient des informations sur le placement de la ligne d’interligne entre les caractères majuscules et le traitement des sommets de la souche diagonale.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_proportion"><strong>DWRITE_PANOSE_PROPORTION</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_proportion"><strong>DWRITE_PANOSE_PROPORTION</strong></a> contient des valeurs qui spécifient la proportion de la forme de glyphe en prenant en compte des détails supplémentaires aux caractères standard.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_script_form"><strong>DWRITE_PANOSE_SCRIPT_FORM</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_script_form"><strong>DWRITE_PANOSE_SCRIPT_FORM</strong></a> contient des valeurs qui spécifient l’apparence générale de la face de caractère, en tenant compte de ses pentes et de ses queues.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_script_topology"><strong>DWRITE_PANOSE_SCRIPT_TOPOLOGY</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_script_topology"><strong>DWRITE_PANOSE_SCRIPT_TOPOLOGY</strong></a> contient des valeurs qui spécifient la topologie de letterforms.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_serif_style"><strong>DWRITE_PANOSE_SERIF_STYLE</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_serif_style"><strong>DWRITE_PANOSE_SERIF_STYLE</strong></a> contient des valeurs qui spécifient l’apparence du texte Serif.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_spacing"><strong>DWRITE_PANOSE_SPACING</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_spacing"><strong>DWRITE_PANOSE_SPACING</strong></a> contient des valeurs qui spécifient l’espacement des caractères (à espacement fixe et proportionnel).</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_stroke_variation"><strong>DWRITE_PANOSE_STROKE_VARIATION</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_stroke_variation"><strong>DWRITE_PANOSE_STROKE_VARIATION</strong></a> contient des valeurs qui spécifient la relation entre les tiges fines et épaisses de caractères de texte.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_symbol_aspect_ratio"><strong>DWRITE_PANOSE_SYMBOL_ASPECT_RATIO</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_symbol_aspect_ratio"><strong>DWRITE_PANOSE_SYMBOL_ASPECT_RATIO</strong></a> contient des valeurs qui spécifient les proportions des caractères symboliques.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_symbol_kind"><strong>DWRITE_PANOSE_SYMBOL_KIND</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_symbol_kind"><strong>DWRITE_PANOSE_SYMBOL_KIND</strong></a> contient des valeurs qui spécifient le type de jeu de symboles.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_tool_kind"><strong>DWRITE_PANOSE_TOOL_KIND</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_tool_kind"><strong>DWRITE_PANOSE_TOOL_KIND</strong></a> contient des valeurs qui spécifient le genre d’outil utilisé pour créer des formes de caractères.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_weight"><strong>DWRITE_PANOSE_WEIGHT</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_weight"><strong>DWRITE_PANOSE_WEIGHT</strong></a> contient des valeurs qui spécifient le poids des caractères.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_xascent"><strong>DWRITE_PANOSE_XASCENT</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_xascent"><strong>DWRITE_PANOSE_XASCENT</strong></a> contient des valeurs qui spécifient la taille relative des lettres minuscules.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_xheight"><strong>DWRITE_PANOSE_XHEIGHT</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_xheight"><strong>DWRITE_PANOSE_XHEIGHT</strong></a> contient des valeurs qui spécifient des informations sur la taille relative des lettres minuscules et le traitement des marques diacritiques (XHEIGHT).</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_paragraph_alignment"><strong>DWRITE_PARAGRAPH_ALIGNMENT</strong></a></td>
<td>Spécifie l’alignement du texte du paragraphe le long de l’axe du sens du déroulement, par rapport au haut et au bas de la zone de disposition du fluide. </td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry"><strong>DWRITE_PIXEL_GEOMETRY</strong></a></td>
<td>Représente la structure interne d’un pixel de périphérique (autrement dit, la disposition physique des composants de couleur rouge, vert et bleu) qui est utilisée pour le rendu du texte. </td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_reading_direction"><strong>DWRITE_READING_DIRECTION</strong></a></td>
<td>Spécifie la direction dans laquelle la lecture progresse. 
<blockquote>
[!Note]<br />Les 
<strong>DWRITE_READING_DIRECTION_TOP_TO_BOTTOM</strong> et les <strong>DWRITE_READING_DIRECTION_BOTTOM_TO_TOP</strong> sont disponibles dans Windows 8.1 et versions ultérieures, uniquement.
</blockquote>
</td>
</tr>
<tr>
<td><a href="/windows/win32/directwrite/dwrite-rendering-mode-enumerations">Énumérations de DWRITE_RENDERING_MODE</a></td>
<td>À compter de Windows 8, l’énumération <strong>DWRITE_RENDERING_MODE</strong> a ajouté de nouvelles valeurs d’énumération et déconseillé d’autres valeurs.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_rendering_mode1"><strong>DWRITE_RENDERING_MODE1</strong></a></td>
<td>Spécifie le mode de rendu des glyphes.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_script_shapes"><strong>DWRITE_SCRIPT_SHAPES</strong></a></td>
<td>Indique des exigences de mise en forme supplémentaires pour le texte.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment"><strong>DWRITE_TEXT_ALIGNMENT</strong></a></td>
<td>Spécifie l’alignement du texte de paragraphe le long de l’axe de direction de lecture, par rapport aux bords de début et de fin de la zone de disposition.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode"><strong>DWRITE_TEXT_ANTIALIAS_MODE</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode"><strong>DWRITE_TEXT_ANTIALIAS_MODE</strong></a> contient des valeurs qui spécifient le type d’anticrénelage à utiliser pour le texte lorsque le mode de rendu appelle l’anticrénelage.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_texture_type"><strong>DWRITE_TEXTURE_TYPE</strong></a></td>
<td>Identifie un type de texture alpha.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_trimming_granularity"><strong>DWRITE_TRIMMING_GRANULARITY</strong></a></td>
<td>Spécifie la granularité du texte utilisée pour découper le texte débordement de la zone de disposition.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_vertical_glyph_orientation"><strong>DWRITE_VERTICAL_GLYPH_ORIENTATION</strong></a></td>
<td>L’énumération <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_vertical_glyph_orientation"><strong>DWRITE_VERTICAL_GLYPH_ORIENTATION</strong></a> contient des valeurs qui spécifient le type souhaité d’orientation de glyphe pour le texte.</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_word_wrapping"><strong>DWRITE_WORD_WRAPPING</strong></a></td>
<td>Spécifie le retour automatique à la ligne à utiliser dans un paragraphe multiligne particulier. 
<blockquote>
[!Note]<br />
<strong>DWRITE_WORD_WRAPPING_EMERGENCY_BREAK</strong>, <strong>DWRITE_WORD_WRAPPING_WHOLE _WORD</strong>et <strong>DWRITE_WORD_WRAPPING_CHARACTER</strong> sont disponibles dans Windows 8.1 et versions ultérieures, uniquement.
</blockquote>
</td>
</tr>
</tbody>
</table>



 

 

 





