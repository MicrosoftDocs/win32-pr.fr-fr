---
title: Méthode IDWriteTextAnalyzer GetGdiCompatibleGlyphPlacements
description: Placez la sortie des glyphes à partir de la méthode GetGlyphs en fonction de la police et des règles de rendu du système d’écriture.
ms.assetid: 49312b03-9ee9-44ef-b3eb-a35631a6e693
keywords:
- Écriture directe de la méthode GetGdiCompatibleGlyphPlacements
- Méthode GetGdiCompatibleGlyphPlacements Write directe, interface IDWriteTextAnalyzer
- Écriture directe de l’interface IDWriteTextAnalyzer, méthode GetGdiCompatibleGlyphPlacements
topic_type:
- apiref
api_name:
- IDWriteTextAnalyzer.GetGdiCompatibleGlyphPlacements
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d05fcf5595500f34730a720e4a4c2e80d68922929d8055b754a26a1dc92f63c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650009"
---
# <a name="idwritetextanalyzergetgdicompatibleglyphplacements-method"></a>IDWriteTextAnalyzer :: GetGdiCompatibleGlyphPlacements, méthode

Placez la sortie des glyphes à partir de la méthode [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) en fonction de la police et des règles de rendu du système d’écriture.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT GetGdiCompatibleGlyphPlacements(
  [in]           const WCHAR                           *textString,
  [in]           const UINT16                          *clusterMap,
  [in]                 DWRITE_SHAPING_TEXT_PROPERTIES  *textProps,
                       UINT32                          textLength,
  [in]           const UINT16                          *glyphIndices,
  [in]           const DWRITE_SHAPING_GLYPH_PROPERTIES *glyphProps,
                       UINT32                          glyphCount,
  [in]                 IDWriteFontFace                 *fontFace,
                       FLOAT                           fontEmSize,
                       FLOAT                           pixelsPerDip,
  [in, optional] const DWRITE_MATRIX                   *transform,
                       BOOL                            useGdiNatural,
                       BOOL                             isSideways,
                       BOOL                             isRightToLeft,
  [in]           const DWRITE_SCRIPT_ANALYSIS          * scriptAnalysis,
  [in, optional] const WCHAR                           * localeName,
  [in, optional] const DWRITE_TYPOGRAPHIC_FEATURES     ** features,
  [in, optional] const UINT32                          * featureRangeLengths,
                       UINT32                           featureRanges,
  [out]                FLOAT                           * glyphAdvances,
  [out]                DWRITE_GLYPH_OFFSET             * glyphOffsets
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*textString* \[ dans\]
</dt> <dd>

Type : **const WCHAR \***

Tableau de caractères contenant la chaîne d’origine à partir de laquelle les glyphes sont fournis.

</dd> <dt>

*ClusterMap* \[ dans\]
</dt> <dd>

Type : **const UINT16 \***

Pointeur vers le mappage entre les plages de caractères et les plages de glyphes. Elle est retournée par [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*textProps* \[ dans\]
</dt> <dd>

Type : **[ **DWRITE \_ \_ \_ Propriétés du texte** de mise en forme](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties)\***

Pointeur vers un tableau de structures qui contient des propriétés de mise en forme pour chaque caractère. Cette structure est retournée par [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*textLength* 
</dt> <dd>

Type : **UInt32**

Longueur du texte de *textString*.

</dd> <dt>

*GlyphIndices* \[ dans\]
</dt> <dd>

Type : **const UINT16 \***

Tableau d’index de glyphe retournés par [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*glyphProps* \[ dans\]
</dt> <dd>

Type : **const DWRITE mise en forme des \* [**\_ \_ \_ Propriétés de glyphe**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties)**

Pointeur vers un tableau de structures qui contiennent des propriétés de mise en forme pour chaque glyphe retourné par [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*glyphCount* 
</dt> <dd>

Type : **UInt32**

Nombre de glyphes retournés par [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*fontFace* \[ dans\]
</dt> <dd>

Type : **[ **IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***

Pointeur vers le type de police qui est la source des glyphes de sortie.

</dd> <dt>

*fontEmSize* 
</dt> <dd>

Type : **float**

Taille de police logique dans des DIP.

</dd> <dt>

*pixelsPerDip* 
</dt> <dd>

Type : **float**

Nombre de pixels physiques par DIP.

</dd> <dt>

*transformation* \[ dans, facultatif\]
</dt> <dd>

Type : **const [**DWRITE \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***

Transformation facultative appliquée aux glyphes et à leurs positions. Cette transformation est appliquée après la mise à l’échelle spécifiée par la taille de police et *pixelsPerDip*.

</dd> <dt>

*useGdiNatural* 
</dt> <dd>

Type : **bool**

Quand la valeur est **false**, les mesures sont les mêmes que celles du texte d’alias GDI. Quand la valeur est **true**, les métriques sont les mêmes que les métriques du texte mesurées par GDI à l’aide d’une police créée avec la **\_ \_ qualité naturelle CLEARTYPE**.

</dd> <dt>

 *isSideways* 
</dt> <dd>

Type : **bool**

Indicateur booléen défini sur **true** si le texte est destiné à être dessiné verticalement.

</dd> <dt>

 *isRightToLeft* 
</dt> <dd>

Type : **bool**

Indicateur booléen défini sur **true** pour le texte de droite à gauche.

</dd> <dt>

 *scriptAnalysis* \[ dans\]
</dt> <dd>

Type : **const [**DWRITE \_ script \_ Analysis**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) \***

Pointeur vers le résultat de l’analyse d’un script à partir d’un appel [**AnalyzeScript**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript) .

</dd> <dt>

 *localeName* \[ dans, facultatif\]
</dt> <dd>

Type : **const WCHAR \***

Tableau de caractères contenant les paramètres régionaux à utiliser lors de la sélection de glyphes. Par exemple, le même caractère peut être mappé à différents glyphes pour ja-JP et zh-CHS. Si la **valeur est null**, le mappage par défaut basé sur le script est utilisé.

</dd> <dt>

 *fonctionnalités* \[ dans, facultatif\]
</dt> <dd>

Type : **\* \* const [**DWRITE \_ , \_ fonctionnalités typographiques**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features)**

Tableau de pointeurs vers les jeux de fonctionnalités typographiques à utiliser dans chaque plage de fonctionnalités.

</dd> <dt>

 *featureRangeLengths* \[ dans, facultatif\]
</dt> <dd>

Type : **const UInt32 \***

Longueur de chaque plage de fonctionnalités, en caractères. La somme de toutes les longueurs doit être égale à *TextLength*.

</dd> <dt>

 *featureRanges* 
</dt> <dd>

Type : **UInt32**

Nombre de plages de fonctionnalités.

</dd> <dt>

 *glyphAdvances* \[ à\]
</dt> <dd>

Type : **float \***

Lorsque cette méthode est retournée, contient la largeur d’avance de chaque glyphe.

</dd> <dt>

 *GlyphOffsets* \[ à\]
</dt> <dd>

Type : **[ **\_ \_ décalage de glyphe DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset)\***

Lorsque cette méthode est retournée, contient le décalage de l’origine de chaque glyphe.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothèque<br/> | <dl> <dt>DWrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDWriteTextAnalyzer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer)
</dt> </dl>

 

