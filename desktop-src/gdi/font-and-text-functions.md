---
description: Les fonctions suivantes sont utilisées avec les polices et le texte.
ms.assetid: 69c04ed7-52da-4cb6-9fd2-f2a8c044df8b
title: Fonctions de police et de texte (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a4dd6f000356dfb0e52c34fadef81bd6e8843e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528353"
---
# <a name="font-and-text-functions-windows-gdi"></a>Fonctions de police et de texte (Windows GDI)

Les fonctions suivantes sont utilisées avec les polices et le texte.



| Fonction                                                   | Description                                                                                                          |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**AddFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-addfontmemresourceex)       | Ajoute une police incorporée à la table des polices système.                                                                      |
| [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea)                 | Ajoute une ressource de police à la table des polices système.                                                                       |
| [**AddFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourceexa)             | Ajoute une police privée ou non énumérable à la table des polices système.                                                      |
| [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta)                           | Crée une police logique.                                                                                              |
| [**CreateFontIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta)           | Crée une police logique à partir d’une structure.                                                                             |
| [**CreateFontIndirectEx**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirectexa)       | Crée une police logique à partir d’une structure.                                                                             |
| [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext)                               | Dessine du texte mis en forme dans un rectangle.                                                                                 |
| [**DrawTextEx**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa)                           | Dessine le texte mis en forme dans le rectangle.                                                                                   |
| [**EnumFontFamExProc**](/previous-versions//dd162618(v=vs.85))             | Fonction definedcallback de l’application utilisée avec [**EnumFontFamiliesEx**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesexa) pour traiter les polices. |
| [**EnumFontFamiliesEx**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesexa)           | Énumère toutes les polices du système avec certaines caractéristiques.                                                     |
| [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)                           | Dessine une chaîne de caractères.                                                                                            |
| [**GetAspectRatioFilterEx**](/windows/desktop/api/Wingdi/nf-wingdi-getaspectratiofilterex)   | Obtient le paramètre pour le filtre de proportions.                                                                        |
| [**GetCharABCWidths**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa)               | Obtient la largeur des caractères consécutifs de la police TrueType.                                                    |
| [**GetCharABCWidthsFloat**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsfloata)     | Obtient la largeur des caractères consécutifs à partir de la police actuelle.                                                     |
| [**GetCharABCWidthsI**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsi)             | Obtient les largeurs d’index de glyphes consécutifs ou d’un tableau d’index de glyphes de la police TrueType.               |
| [**GetCharacterPlacement**](/windows/desktop/api/Wingdi/nf-wingdi-getcharacterplacementa)     | Obtient des informations sur une chaîne de caractères.                                                                           |
| [**GetCharWidth32**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a)                   | Obtient la largeur des caractères consécutifs à partir de la police actuelle.                                                     |
| [**GetCharWidthFloat**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthfloata)             | Obtient la largeur fractionnaire des caractères consécutifs de la police actuelle.                                          |
| [**GetCharWidthI**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthi)                     | Obtient la largeur des index de glyphe consécutifs ou un tableau d’index de glyphes à partir de la police actuelle.                     |
| [**GetFontData**](/windows/desktop/api/Wingdi/nf-wingdi-getfontdata)                         | Obtient les données métriques pour une police TrueType.                                                                                |
| [**GetFontLanguageInfo**](/windows/desktop/api/Wingdi/nf-wingdi-getfontlanguageinfo)         | Retourne des informations sur la police sélectionnée pour un contexte d’affichage.                                                   |
| [**GetFontUnicodeRanges**](/windows/desktop/api/Wingdi/nf-wingdi-getfontunicoderanges)       | Indique quels caractères Unicode sont pris en charge par une police.                                                              |
| [**GetGlyphIndices**](/windows/desktop/api/Wingdi/nf-wingdi-getglyphindicesa)                 | Convertit une chaîne en un tableau d’index de glyphes.                                                                  |
| [**GetGlyphOutline**](/windows/desktop/api/Wingdi/nf-wingdi-getglyphoutlinea)                 | Obtient le contour ou l’image bitmap d’un caractère dans la police TrueType.                                                     |
| [**GetKerningPairs**](/windows/desktop/api/WinGdi/nf-wingdi-getkerningpairsa)                 | Obtient les paires de crénage de caractères pour une police.                                                                         |
| [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa)     | Obtient les métriques du texte pour les polices TrueType.                                                                                |
| [**GetRasterizerCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getrasterizercaps)             | Indique si les polices TrueType sont installées.                                                                          |
| [**GetTabbedTextExtent**](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta)         | Calcule la largeur et la hauteur d’une chaîne de caractères, y compris les onglets.                                                 |
| [**GetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign)                       | Obtient le paramètre d’alignement du texte pour un contexte de périphérique.                                                                |
| [**GetTextCharacterExtra**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra)     | Obtient l’espacement entre les intercaractères actuel pour un contexte de périphérique.                                                        |
| [**GetTextColor**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcolor)                       | Obtient la couleur du texte pour un contexte de périphérique.                                                                            |
| [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa)       | Obtient le nombre de caractères dans une chaîne qui tient dans un espace.                                              |
| [**GetTextExtentExPointI**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointi)     | Obtient le nombre d’index de glyphes qui tiennent dans un espace.                                                       |
| [**GetTextExtentPoint32**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a)       | Calcule la largeur et la hauteur d’une chaîne de texte.                                                                   |
| [**GetTextExtentPointI**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpointi)         | Calcule la largeur et la hauteur d’un tableau d’index de glyphes.                                                          |
| [**GetTextFace**](/windows/desktop/api/Wingdi/nf-wingdi-gettextfacea)                         | Obtient le nom de la police qui est sélectionnée dans un contexte de périphérique.                                                    |
| [**GetTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics)                   | Remplit une mémoire tampon avec les métriques d’une police.                                                                          |
| [**PolyTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-polytextouta)                         | Dessine plusieurs chaînes à l’aide des couleurs de police et de texte dans un contexte de périphérique.                                            |
| [**RemoveFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex) | Supprime une police dont la source a été incorporée dans un document à partir de la table des polices système.                                   |
| [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea)           | Supprime les polices dans un fichier de la table des polices système.                                                              |
| [**RemoveFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa)       | Supprime une police privée ou non énumérable de la table des polices système.                                                 |
| [**SetMapperFlags**](/windows/desktop/api/Wingdi/nf-wingdi-setmapperflags)                   | Modifie l’algorithme utilisé pour mapper des polices logiques à des polices physiques.                                                    |
| [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign)                       | Définit les indicateurs d’alignement du texte pour un contexte de périphérique.                                                                  |
| [**SetTextCharacterExtra**](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra)     | Définit l’espacement entre les caractères.                                                                                     |
| [**SetTextColor**](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor)                       | Définit la couleur du texte pour un contexte de périphérique.                                                                            |
| [**SetTextJustification**](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification)       | Spécifie la quantité d’espace que le système doit ajouter aux caractères de saut de ligne dans une chaîne.                             |
| [**TabbedTextOut**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta)                     | Écrit une chaîne de caractères à un emplacement, en développant les onglets aux valeurs spécifiées.                                         |
| [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta)                                 | Écrit une chaîne de caractères à un emplacement.                                                                             |



 

## <a name="obsolete-functions"></a>Fonctions obsolètes

Ces fonctions sont fournies uniquement à des fins de compatibilité avec les versions 16 bits de Windows.

-   [**CreateScalableFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-createscalablefontresourcea)
-   [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa)
-   [**EnumFontFamProc**](/previous-versions//dd162621(v=vs.85))
-   [**EnumFonts**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa)
-   [**EnumFontsProc**](/previous-versions//dd162623(v=vs.85))
-   [**GetCharWidth**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidtha)
-   [**GetTextExtentPoint**](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa)

 

 
