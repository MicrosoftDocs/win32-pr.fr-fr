---
title: Méthode IDWriteFontFace GetGdiCompatibleGlyphMetrics
description: Obtient des métriques de glyphes dans les unités de conception de police avec les valeurs de retour compatibles avec ce que le GDI produirait.
ms.assetid: 7bda3916-6db3-4f56-b18c-288506c0b646
keywords:
- Écriture directe de la méthode GetGdiCompatibleGlyphMetrics
- Méthode GetGdiCompatibleGlyphMetrics Write directe, interface IDWriteFontFace
- Écriture directe de l’interface IDWriteFontFace, méthode GetGdiCompatibleGlyphMetrics
topic_type:
- apiref
api_name:
- IDWriteFontFace.GetGdiCompatibleGlyphMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a949edbdad2f25d748e5af64ebe408c79c7372b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543235"
---
# <a name="idwritefontfacegetgdicompatibleglyphmetrics-method"></a><span data-ttu-id="4a4fb-106">IDWriteFontFace :: GetGdiCompatibleGlyphMetrics, méthode</span><span class="sxs-lookup"><span data-stu-id="4a4fb-106">IDWriteFontFace::GetGdiCompatibleGlyphMetrics method</span></span>

<span data-ttu-id="4a4fb-107">Obtient des métriques de glyphes dans les unités de conception de police avec les valeurs de retour compatibles avec ce que le GDI produirait.</span><span class="sxs-lookup"><span data-stu-id="4a4fb-107">Obtains glyph metrics in font design units with the return values compatible with what GDI would produce.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a4fb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a4fb-108">Syntax</span></span>


```C++
virtual HRESULT GetGdiCompatibleGlyphMetrics(
                       FLOAT                emSize,
                       FLOAT                pixelsPerDip,
  [in, optional] const DWRITE_MATRIX        *transform,
                       BOOL                 useGdiNatural,
  [in]           const UINT16               *glyphIndices,
                       UINT32               glyphCount,
  [out]                DWRITE_GLYPH_METRICS *glyphMetrics,
                       BOOL                 isSideways = FALSE
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="4a4fb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a4fb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a4fb-110">*emSize*</span><span class="sxs-lookup"><span data-stu-id="4a4fb-110">*emSize*</span></span> 
</dt> <dd>

<span data-ttu-id="4a4fb-111">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="4a4fb-111">Type: **FLOAT**</span></span>

<span data-ttu-id="4a4fb-112">Taille ogique de la police en unités DIP.</span><span class="sxs-lookup"><span data-stu-id="4a4fb-112">The ogical size of the font in DIP units.</span></span>

</dd> <dt>

<span data-ttu-id="4a4fb-113">*pixelsPerDip*</span><span class="sxs-lookup"><span data-stu-id="4a4fb-113">*pixelsPerDip*</span></span> 
</dt> <dd>

<span data-ttu-id="4a4fb-114">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="4a4fb-114">Type: **FLOAT**</span></span>

<span data-ttu-id="4a4fb-115">Nombre de pixels physiques par DIP.</span><span class="sxs-lookup"><span data-stu-id="4a4fb-115">The number of physical pixels per DIP.</span></span>

</dd> <dt>

<span data-ttu-id="4a4fb-116">*transformation* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="4a4fb-116">*transform* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4a4fb-117">Type : **const [**DWRITE \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***</span><span class="sxs-lookup"><span data-stu-id="4a4fb-117">Type: **const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\***</span></span>

<span data-ttu-id="4a4fb-118">Transformation facultative appliquée aux glyphes et à leurs positions.</span><span class="sxs-lookup"><span data-stu-id="4a4fb-118">An optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="4a4fb-119">Cette transformation est appliquée après la mise à l’échelle spécifiée par la taille de police et *pixelsPerDip*.</span><span class="sxs-lookup"><span data-stu-id="4a4fb-119">This transform is applied after the scaling specified by the font size and *pixelsPerDip*.</span></span>

</dd> <dt>

<span data-ttu-id="4a4fb-120">*useGdiNatural*</span><span class="sxs-lookup"><span data-stu-id="4a4fb-120">*useGdiNatural*</span></span> 
</dt> <dd>

<span data-ttu-id="4a4fb-121">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="4a4fb-121">Type: **BOOL**</span></span>

<span data-ttu-id="4a4fb-122">Quand la valeur est **false**, les mesures sont les mêmes que celles du texte d’alias GDI.</span><span class="sxs-lookup"><span data-stu-id="4a4fb-122">When set to **FALSE**, the metrics are the same as the metrics of GDI aliased text.</span></span> <span data-ttu-id="4a4fb-123">Quand la valeur est **true**, les métriques sont les mêmes que les métriques du texte mesurées par GDI à l’aide d’une police créée avec la **\_ \_ qualité naturelle CLEARTYPE**.</span><span class="sxs-lookup"><span data-stu-id="4a4fb-123">When set to **TRUE**, the metrics are the same as the metrics of text measured by GDI using a font created with **CLEARTYPE\_NATURAL\_QUALITY**.</span></span>

</dd> <dt>

<span data-ttu-id="4a4fb-124">*GlyphIndices* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4a4fb-124">*glyphIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a4fb-125">Type : **const UINT16 \***</span><span class="sxs-lookup"><span data-stu-id="4a4fb-125">Type: **const UINT16\***</span></span>

<span data-ttu-id="4a4fb-126">Tableau d’index de glyphes pour lequel calculer les métriques.</span><span class="sxs-lookup"><span data-stu-id="4a4fb-126">An array of glyph indices for which to compute the metrics.</span></span>

</dd> <dt>

<span data-ttu-id="4a4fb-127">*glyphCount*</span><span class="sxs-lookup"><span data-stu-id="4a4fb-127">*glyphCount*</span></span> 
</dt> <dd>

<span data-ttu-id="4a4fb-128">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4a4fb-128">Type: **UINT32**</span></span>

<span data-ttu-id="4a4fb-129">Nombre d’éléments dans le tableau *GlyphIndices* .</span><span class="sxs-lookup"><span data-stu-id="4a4fb-129">The number of elements in the *glyphIndices* array.</span></span>

</dd> <dt>

<span data-ttu-id="4a4fb-130">*glyphMetrics* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4a4fb-130">*glyphMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a4fb-131">Type : **[ **\_ \_ métriques de glyphe DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="4a4fb-131">Type: **[**DWRITE\_GLYPH\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)\***</span></span>

<span data-ttu-id="4a4fb-132">Tableau de structures [**de \_ \_ métriques de glyphes DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) remplies par cette fonction.</span><span class="sxs-lookup"><span data-stu-id="4a4fb-132">An array of [**DWRITE\_GLYPH\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) structures filled by this function.</span></span> <span data-ttu-id="4a4fb-133">Les métriques sont des unités de conception de police.</span><span class="sxs-lookup"><span data-stu-id="4a4fb-133">The metrics are in font design units.</span></span>

</dd> <dt>

<span data-ttu-id="4a4fb-134">*isSideways*</span><span class="sxs-lookup"><span data-stu-id="4a4fb-134">*isSideways*</span></span> 
</dt> <dd>

<span data-ttu-id="4a4fb-135">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="4a4fb-135">Type: **BOOL**</span></span>

<span data-ttu-id="4a4fb-136">Valeur BOOLÉENNE qui indique si la police est utilisée dans une exécution latérale.</span><span class="sxs-lookup"><span data-stu-id="4a4fb-136">A BOOL value that indicates whether the font is being used in a sideways run.</span></span> <span data-ttu-id="4a4fb-137">Cela peut affecter les métriques de glyphe si la police a une simulation oblique, car la simulation oblique latérale diffère de la simulation oblique non latérale.</span><span class="sxs-lookup"><span data-stu-id="4a4fb-137">This can affect the glyph metrics if the font has oblique simulation because sideways oblique simulation differs from non-sideways oblique simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a4fb-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4a4fb-138">Return value</span></span>

<span data-ttu-id="4a4fb-139">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4a4fb-139">Type: **HRESULT**</span></span>

<span data-ttu-id="4a4fb-140">Code d’erreur **HRESULT** standard.</span><span class="sxs-lookup"><span data-stu-id="4a4fb-140">Standard **HRESULT** error code.</span></span> <span data-ttu-id="4a4fb-141">Si l’un des index de glyphes d’entrée se trouve en dehors de la plage d’index de glyphes valide pour le type de police actuel, **E \_ INVALIDARG** sera retourné.</span><span class="sxs-lookup"><span data-stu-id="4a4fb-141">If any of the input glyph indices are outside of the valid glyph index range for the current font face, **E\_INVALIDARG** will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a4fb-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a4fb-142">Requirements</span></span>



| <span data-ttu-id="4a4fb-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a4fb-143">Requirement</span></span> | <span data-ttu-id="4a4fb-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a4fb-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a4fb-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4a4fb-145">Library</span></span><br/> | <dl> <span data-ttu-id="4a4fb-146"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a4fb-146"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="4a4fb-147">DLL</span><span class="sxs-lookup"><span data-stu-id="4a4fb-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="4a4fb-148"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a4fb-148"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a4fb-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a4fb-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a4fb-150">**IDWriteFontFace**</span><span class="sxs-lookup"><span data-stu-id="4a4fb-150">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[<span data-ttu-id="4a4fb-151">**IDWriteFontFace**</span><span class="sxs-lookup"><span data-stu-id="4a4fb-151">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 

