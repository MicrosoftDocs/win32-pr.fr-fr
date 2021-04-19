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
ms.openlocfilehash: f548e5fd20ce8814dc59657ff7bb422387c959fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542231"
---
# <a name="idwritetextanalyzergetgdicompatibleglyphplacements-method"></a><span data-ttu-id="b91c6-106">IDWriteTextAnalyzer :: GetGdiCompatibleGlyphPlacements, méthode</span><span class="sxs-lookup"><span data-stu-id="b91c6-106">IDWriteTextAnalyzer::GetGdiCompatibleGlyphPlacements method</span></span>

<span data-ttu-id="b91c6-107">Placez la sortie des glyphes à partir de la méthode [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) en fonction de la police et des règles de rendu du système d’écriture.</span><span class="sxs-lookup"><span data-stu-id="b91c6-107">Place glyphs output from the [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) method according to the font and the writing system's rendering rules.</span></span>

## <a name="syntax"></a><span data-ttu-id="b91c6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b91c6-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="b91c6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b91c6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b91c6-110">*textString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b91c6-110">*textString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b91c6-111">Type : **const WCHAR \***</span><span class="sxs-lookup"><span data-stu-id="b91c6-111">Type: **const WCHAR\***</span></span>

<span data-ttu-id="b91c6-112">Tableau de caractères contenant la chaîne d’origine à partir de laquelle les glyphes sont fournis.</span><span class="sxs-lookup"><span data-stu-id="b91c6-112">An array of characters containing the original string from which the glyphs came.</span></span>

</dd> <dt>

<span data-ttu-id="b91c6-113">*ClusterMap* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b91c6-113">*clusterMap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b91c6-114">Type : **const UINT16 \***</span><span class="sxs-lookup"><span data-stu-id="b91c6-114">Type: **const UINT16\***</span></span>

<span data-ttu-id="b91c6-115">Pointeur vers le mappage entre les plages de caractères et les plages de glyphes.</span><span class="sxs-lookup"><span data-stu-id="b91c6-115">A pointer to the mapping from character ranges to glyph ranges.</span></span> <span data-ttu-id="b91c6-116">Elle est retournée par [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span><span class="sxs-lookup"><span data-stu-id="b91c6-116">This is returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="b91c6-117">*textProps* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b91c6-117">*textProps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b91c6-118">Type : **[ **DWRITE \_ \_ \_ Propriétés du texte** de mise en forme](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties)\***</span><span class="sxs-lookup"><span data-stu-id="b91c6-118">Type: **[**DWRITE\_SHAPING\_TEXT\_PROPERTIES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties)\***</span></span>

<span data-ttu-id="b91c6-119">Pointeur vers un tableau de structures qui contient des propriétés de mise en forme pour chaque caractère.</span><span class="sxs-lookup"><span data-stu-id="b91c6-119">A pointer to an array of structures that contains shaping properties for each character.</span></span> <span data-ttu-id="b91c6-120">Cette structure est retournée par [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span><span class="sxs-lookup"><span data-stu-id="b91c6-120">This structure is returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="b91c6-121">*textLength*</span><span class="sxs-lookup"><span data-stu-id="b91c6-121">*textLength*</span></span> 
</dt> <dd>

<span data-ttu-id="b91c6-122">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b91c6-122">Type: **UINT32**</span></span>

<span data-ttu-id="b91c6-123">Longueur du texte de *textString*.</span><span class="sxs-lookup"><span data-stu-id="b91c6-123">The text length of *textString*.</span></span>

</dd> <dt>

<span data-ttu-id="b91c6-124">*GlyphIndices* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b91c6-124">*glyphIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b91c6-125">Type : **const UINT16 \***</span><span class="sxs-lookup"><span data-stu-id="b91c6-125">Type: **const UINT16\***</span></span>

<span data-ttu-id="b91c6-126">Tableau d’index de glyphe retournés par [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span><span class="sxs-lookup"><span data-stu-id="b91c6-126">An array of glyph indices returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="b91c6-127">*glyphProps* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b91c6-127">*glyphProps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b91c6-128">Type : **const DWRITE mise en forme des \* [**\_ \_ \_ Propriétés de glyphe**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties)**</span><span class="sxs-lookup"><span data-stu-id="b91c6-128">Type: **const [**DWRITE\_SHAPING\_GLYPH\_PROPERTIES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties)\***</span></span>

<span data-ttu-id="b91c6-129">Pointeur vers un tableau de structures qui contiennent des propriétés de mise en forme pour chaque glyphe retourné par [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span><span class="sxs-lookup"><span data-stu-id="b91c6-129">A pointer to an array of structures that contain shaping properties for each glyph returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="b91c6-130">*glyphCount*</span><span class="sxs-lookup"><span data-stu-id="b91c6-130">*glyphCount*</span></span> 
</dt> <dd>

<span data-ttu-id="b91c6-131">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b91c6-131">Type: **UINT32**</span></span>

<span data-ttu-id="b91c6-132">Nombre de glyphes retournés par [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span><span class="sxs-lookup"><span data-stu-id="b91c6-132">The number of glyphs returned from [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="b91c6-133">*fontFace* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b91c6-133">*fontFace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b91c6-134">Type : **[ **IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***</span><span class="sxs-lookup"><span data-stu-id="b91c6-134">Type: **[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***</span></span>

<span data-ttu-id="b91c6-135">Pointeur vers le type de police qui est la source des glyphes de sortie.</span><span class="sxs-lookup"><span data-stu-id="b91c6-135">A pointer to the font face that is the source for the output glyphs.</span></span>

</dd> <dt>

<span data-ttu-id="b91c6-136">*fontEmSize*</span><span class="sxs-lookup"><span data-stu-id="b91c6-136">*fontEmSize*</span></span> 
</dt> <dd>

<span data-ttu-id="b91c6-137">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="b91c6-137">Type: **FLOAT**</span></span>

<span data-ttu-id="b91c6-138">Taille de police logique dans des DIP.</span><span class="sxs-lookup"><span data-stu-id="b91c6-138">The logical font size in DIPs.</span></span>

</dd> <dt>

<span data-ttu-id="b91c6-139">*pixelsPerDip*</span><span class="sxs-lookup"><span data-stu-id="b91c6-139">*pixelsPerDip*</span></span> 
</dt> <dd>

<span data-ttu-id="b91c6-140">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="b91c6-140">Type: **FLOAT**</span></span>

<span data-ttu-id="b91c6-141">Nombre de pixels physiques par DIP.</span><span class="sxs-lookup"><span data-stu-id="b91c6-141">The number of physical pixels per DIP.</span></span>

</dd> <dt>

<span data-ttu-id="b91c6-142">*transformation* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b91c6-142">*transform* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b91c6-143">Type : **const [**DWRITE \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***</span><span class="sxs-lookup"><span data-stu-id="b91c6-143">Type: **const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\***</span></span>

<span data-ttu-id="b91c6-144">Transformation facultative appliquée aux glyphes et à leurs positions.</span><span class="sxs-lookup"><span data-stu-id="b91c6-144">An optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="b91c6-145">Cette transformation est appliquée après la mise à l’échelle spécifiée par la taille de police et *pixelsPerDip*.</span><span class="sxs-lookup"><span data-stu-id="b91c6-145">This transform is applied after the scaling specified by the font size and *pixelsPerDip*.</span></span>

</dd> <dt>

<span data-ttu-id="b91c6-146">*useGdiNatural*</span><span class="sxs-lookup"><span data-stu-id="b91c6-146">*useGdiNatural*</span></span> 
</dt> <dd>

<span data-ttu-id="b91c6-147">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="b91c6-147">Type: **BOOL**</span></span>

<span data-ttu-id="b91c6-148">Quand la valeur est **false**, les mesures sont les mêmes que celles du texte d’alias GDI.</span><span class="sxs-lookup"><span data-stu-id="b91c6-148">When set to **FALSE**, the metrics are the same as the metrics of GDI aliased text.</span></span> <span data-ttu-id="b91c6-149">Quand la valeur est **true**, les métriques sont les mêmes que les métriques du texte mesurées par GDI à l’aide d’une police créée avec la **\_ \_ qualité naturelle CLEARTYPE**.</span><span class="sxs-lookup"><span data-stu-id="b91c6-149">When set to **TRUE**, the metrics are the same as the metrics of text measured by GDI using a font created with **CLEARTYPE\_NATURAL\_QUALITY**.</span></span>

</dd> <dt>

 <span data-ttu-id="b91c6-150">*isSideways*</span><span class="sxs-lookup"><span data-stu-id="b91c6-150">*isSideways*</span></span> 
</dt> <dd>

<span data-ttu-id="b91c6-151">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="b91c6-151">Type: **BOOL**</span></span>

<span data-ttu-id="b91c6-152">Indicateur booléen défini sur **true** si le texte est destiné à être dessiné verticalement.</span><span class="sxs-lookup"><span data-stu-id="b91c6-152">A Boolean flag set to **TRUE** if the text is intended to be drawn vertically.</span></span>

</dd> <dt>

 <span data-ttu-id="b91c6-153">*isRightToLeft*</span><span class="sxs-lookup"><span data-stu-id="b91c6-153">*isRightToLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="b91c6-154">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="b91c6-154">Type: **BOOL**</span></span>

<span data-ttu-id="b91c6-155">Indicateur booléen défini sur **true** pour le texte de droite à gauche.</span><span class="sxs-lookup"><span data-stu-id="b91c6-155">A Boolean flag set to **TRUE** for right-to-left text.</span></span>

</dd> <dt>

 <span data-ttu-id="b91c6-156">*scriptAnalysis* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b91c6-156">*scriptAnalysis* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b91c6-157">Type : **const [**DWRITE \_ script \_ Analysis**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) \***</span><span class="sxs-lookup"><span data-stu-id="b91c6-157">Type: **const [**DWRITE\_SCRIPT\_ANALYSIS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis)\***</span></span>

<span data-ttu-id="b91c6-158">Pointeur vers le résultat de l’analyse d’un script à partir d’un appel [**AnalyzeScript**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript) .</span><span class="sxs-lookup"><span data-stu-id="b91c6-158">A pointer to a Script analysis result from an [**AnalyzeScript**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript) call.</span></span>

</dd> <dt>

 <span data-ttu-id="b91c6-159">*localeName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b91c6-159">*localeName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b91c6-160">Type : **const WCHAR \***</span><span class="sxs-lookup"><span data-stu-id="b91c6-160">Type: **const WCHAR\***</span></span>

<span data-ttu-id="b91c6-161">Tableau de caractères contenant les paramètres régionaux à utiliser lors de la sélection de glyphes.</span><span class="sxs-lookup"><span data-stu-id="b91c6-161">An array of characters containing the locale to use when selecting glyphs.</span></span> <span data-ttu-id="b91c6-162">Par exemple, le même caractère peut être mappé à différents glyphes pour ja-JP et zh-CHS.</span><span class="sxs-lookup"><span data-stu-id="b91c6-162">For example, the same character may map to different glyphs for ja-jp versus zh-chs.</span></span> <span data-ttu-id="b91c6-163">Si la **valeur est null**, le mappage par défaut basé sur le script est utilisé.</span><span class="sxs-lookup"><span data-stu-id="b91c6-163">If this is **NULL**, then the default mapping based on the script is used.</span></span>

</dd> <dt>

 <span data-ttu-id="b91c6-164">*fonctionnalités* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b91c6-164">*features* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b91c6-165">Type : **\* \* const [**DWRITE \_ , \_ fonctionnalités typographiques**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features)**</span><span class="sxs-lookup"><span data-stu-id="b91c6-165">Type: **const [**DWRITE\_TYPOGRAPHIC\_FEATURES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features)\*\***</span></span>

<span data-ttu-id="b91c6-166">Tableau de pointeurs vers les jeux de fonctionnalités typographiques à utiliser dans chaque plage de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="b91c6-166">An array of pointers to the sets of typographic features to use in each feature range.</span></span>

</dd> <dt>

 <span data-ttu-id="b91c6-167">*featureRangeLengths* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b91c6-167">*featureRangeLengths* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b91c6-168">Type : **const UInt32 \***</span><span class="sxs-lookup"><span data-stu-id="b91c6-168">Type: **const UINT32\***</span></span>

<span data-ttu-id="b91c6-169">Longueur de chaque plage de fonctionnalités, en caractères.</span><span class="sxs-lookup"><span data-stu-id="b91c6-169">The length of each feature range, in characters.</span></span> <span data-ttu-id="b91c6-170">La somme de toutes les longueurs doit être égale à *TextLength*.</span><span class="sxs-lookup"><span data-stu-id="b91c6-170">The sum of all lengths should be equal to *textLength*.</span></span>

</dd> <dt>

 <span data-ttu-id="b91c6-171">*featureRanges*</span><span class="sxs-lookup"><span data-stu-id="b91c6-171">*featureRanges*</span></span> 
</dt> <dd>

<span data-ttu-id="b91c6-172">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b91c6-172">Type: **UINT32**</span></span>

<span data-ttu-id="b91c6-173">Nombre de plages de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="b91c6-173">The number of feature ranges.</span></span>

</dd> <dt>

 <span data-ttu-id="b91c6-174">*glyphAdvances* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b91c6-174">*glyphAdvances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b91c6-175">Type : **float \***</span><span class="sxs-lookup"><span data-stu-id="b91c6-175">Type: **FLOAT\***</span></span>

<span data-ttu-id="b91c6-176">Lorsque cette méthode est retournée, contient la largeur d’avance de chaque glyphe.</span><span class="sxs-lookup"><span data-stu-id="b91c6-176">When this method returns, contains the advance width of each glyph.</span></span>

</dd> <dt>

 <span data-ttu-id="b91c6-177">*GlyphOffsets* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b91c6-177">*glyphOffsets* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b91c6-178">Type : **[ **\_ \_ décalage de glyphe DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset)\***</span><span class="sxs-lookup"><span data-stu-id="b91c6-178">Type: **[**DWRITE\_GLYPH\_OFFSET**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset)\***</span></span>

<span data-ttu-id="b91c6-179">Lorsque cette méthode est retournée, contient le décalage de l’origine de chaque glyphe.</span><span class="sxs-lookup"><span data-stu-id="b91c6-179">When this method returns, contains the offset of the origin of each glyph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b91c6-180">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b91c6-180">Return value</span></span>

<span data-ttu-id="b91c6-181">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b91c6-181">Type: **HRESULT**</span></span>

<span data-ttu-id="b91c6-182">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b91c6-182">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b91c6-183">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b91c6-183">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b91c6-184">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b91c6-184">Requirements</span></span>



| <span data-ttu-id="b91c6-185">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b91c6-185">Requirement</span></span> | <span data-ttu-id="b91c6-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="b91c6-186">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b91c6-187">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b91c6-187">Library</span></span><br/> | <dl> <span data-ttu-id="b91c6-188"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b91c6-188"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="b91c6-189">DLL</span><span class="sxs-lookup"><span data-stu-id="b91c6-189">DLL</span></span><br/>     | <dl> <span data-ttu-id="b91c6-190"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b91c6-190"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b91c6-191">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b91c6-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b91c6-192">**IDWriteTextAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="b91c6-192">**IDWriteTextAnalyzer**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer)
</dt> </dl>

 

