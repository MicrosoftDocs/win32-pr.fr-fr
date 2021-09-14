---
description: Cette section décrit les fonctions de typographie et de traitement de script complexe.
ms.assetid: 876e36f5-a91c-490b-87bd-b7cb4993f8c4
title: Uniscribe, fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f623c8da04f985f88d091f8e9e2b4cb724c0801
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224156"
---
# <a name="uniscribe-functions"></a>Uniscribe, fonctions

Cette section décrit les fonctions de typographie et de traitement de script complexe.



| Fonction                                                               | Description                                                                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution)   | Applique les paramètres de substitution de chiffres spécifiés au contrôle de script et aux structures d’état de script spécifiés.                                                                    |
| [**ScriptApplyLogicalWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptapplylogicalwidth)             | Prend un tableau de largeurs d’avance pour une exécution et génère un tableau de largeurs de glyphes avancés ajustés.                                                                               |
| [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)                                     | Récupère des informations pour déterminer les sauts de ligne.                                                                                                                                |
| [**ScriptCacheGetHeight**](/windows/desktop/api/Usp10/nf-usp10-scriptcachegetheight)                   | Récupère la hauteur de la police actuellement mise en cache.                                                                                                                                |
| [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox)                                     | Génère le décalage x à partir du bord gauche ou du bord de tête d’une exécution vers le bord de début ou de fin d’un cluster de caractères logiques.                                          |
| [**ScriptFreeCache**](/windows/desktop/api/Usp10/nf-usp10-scriptfreecache)                             | Libère un cache de script.                                                                                                                                                             |
| [**ScriptGetCMap**](/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap)                                 | Récupère les index de glyphes des caractères Unicode dans une chaîne en fonction de la table CMAP TrueType ou de la table CMAP standard implémentée pour les anciennes polices.         |
| [**ScriptGetFontAlternateGlyphs**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)   | Récupère une liste de glyphes de remplacement pour un caractère spécifié accessible par le biais d’une fonctionnalité OpenType spécifiée.                                                         |
| [**ScriptGetFontFeatureTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)           | Récupère une liste de fonctionnalités typographiques pour le système d’écriture défini pour le traitement OpenType.                                                                                  |
| [**ScriptGetFontLanguageTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)         | Récupère une liste des balises de langue disponibles pour l’élément spécifié et sont prises en charge par une balise de script spécifiée pour le traitement OpenType.                                  |
| [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties)             | Récupère des informations à partir du cache de polices sur les glyphes spéciaux utilisés par une police.                                                                                                   |
| [**ScriptGetFontScriptTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)             | Récupère une liste de scripts disponibles dans la police pour le traitement OpenType.                                                                                                        |
| [**ScriptGetGlyphABCWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptgetglyphabcwidth)               | Récupère la largeur ABC d’un glyphe donné.                                                                                                                                         |
| [**ScriptGetLogicalWidths**](/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths)               | Convertit les largeurs d’avance de glyphe pour une police spécifique en largeurs logiques.                                                                                                        |
| [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties)                     | Récupère des informations sur les scripts actuels.                                                                                                                                  |
| [**ScriptIsComplex**](/windows/desktop/api/Usp10/nf-usp10-scriptiscomplex)                             | Détermine si une chaîne Unicode requiert un traitement complexe des scripts.                                                                                                           |
| [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize)                                 | Divise une chaîne Unicode en éléments individuels à mettre en forme.                                                                                                                        |
| [**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)                 | Divise une chaîne Unicode en éléments individuels et fournit un tableau de balises de fonctionnalités pour chaque élément à mettre en forme pour le traitement OpenType.                                  |
| [**ScriptJustify**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify)                                 | Crée un tableau de largeurs d’avance pour permettre la justification du texte lorsqu’il est passé à la fonction [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) .                                                   |
| [**ScriptLayout**](/windows/desktop/api/Usp10/nf-usp10-scriptlayout)                                   | Convertit un tableau de niveaux d’incorporation de série en une carte de position visuelle à logique et/ou d’une position logique en visuel.                                                               |
| [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)                                     | Génère des informations de largeur avancée de glyphe et de décalage à deux dimensions à partir de la sortie de [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape).                                                       |
| [**ScriptPlaceOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)                     | Génère des glyphes et des attributs visuels pour une exécution Unicode avec des informations OpenType à partir de la sortie de [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype).                         |
| [**ScriptPositionSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)         | Positionne un glyphe unique avec un seul ajustement à l’aide d’une fonctionnalité spécifiée fournie dans la police pour le traitement OpenType.                                                         |
| [**ScriptRecordDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptrecorddigitsubstitution) | Lit les paramètres de substitution de chiffres et de chiffres natifs NLS (National Language Support) et les enregistre dans une structure de [**script \_ DIGITSUBSTITUTE**](/windows/win32/api/usp10/ns-usp10-script_digitsubstitute) . |
| [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)                                     | Génère des glyphes et des attributs visuels pour une exécution Unicode.                                                                                                                         |
| [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)                     | Génère des glyphes et des attributs visuels pour une exécution Unicode avec des informations OpenType.                                                                                               |
| [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)                     | Analyse une chaîne de texte brut.                                                                                                                                                     |
| [**ScriptStringCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox)                         | Récupère la coordonnée x du bord de début ou de fin d’une position de caractère.                                                                                              |
| [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree)                           | Libère une structure [**d' \_ \_ analyse de chaîne de script**](script-string-analysis.md) .                                                                                                     |
| [**ScriptStringGetLogicalWidths**](/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths)   | Convertit les largeurs visuelles en largeurs logiques.                                                                                                                                       |
| [**ScriptStringGetOrder**](/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder)                   | Crée un tableau qui mappe une position de caractère d’origine à une position de glyphe.                                                                                                    |
| [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout)                             | Affiche une chaîne générée par un appel antérieur à [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) et ajoute éventuellement la mise en surbrillance.                                               |
| [**ScriptString \_ pcOutChars**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars)            | Retourne un pointeur vers la longueur d’une chaîne après le découpage.                                                                                                                       |
| [**ScriptString \_ pLogAttr**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr)                | Retourne un pointeur vers une mémoire tampon d’attributs logiques pour une chaîne analysée.                                                                                                          |
| [**ScriptString \_ psize**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize)                      | Retourne un pointeur vers une structure de [**taille**](/previous-versions//dd145106(v=vs.85)) pour une chaîne analysée.                                                                                                     |
| [**ScriptStringValidate**](/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate)                   | Vérifie une structure d' [**\_ \_ analyse de chaîne de script**](script-string-analysis.md) pour les séquences non valides.                                                                              |
| [**ScriptStringXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp)                         | Convertit une coordonnée x en une position de caractère.                                                                                                                                 |
| [**ScriptSubstituteSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)     | Autorise la substitution d’un seul glyphe avec une autre forme du même glyphe pour le traitement OpenType.                                                                         |
| [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout)                                 | Affiche le texte de la forme de script spécifiée et les informations de place.                                                                                                               |
| [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp)                                     | Génère le bord de début ou de fin d’un cluster de caractères logiques à partir du décalage x d’une exécution.                                                                                 |



 

 

 
