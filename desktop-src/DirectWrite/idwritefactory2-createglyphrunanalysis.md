---
title: Méthode IDWriteFactory2 CreateGlyphRunAnalysis
description: Crée un objet d’analyse de série de glyphes, qui encapsule les informations utilisées pour restituer une exécution de glyphe.
ms.assetid: 13cecfbf-8bb6-88a2-c8b2-3243f6cb92fd
keywords:
- Écriture directe de la méthode CreateGlyphRunAnalysis
- Méthode CreateGlyphRunAnalysis Write directe, interface IDWriteFactory2
- Écriture directe de l’interface IDWriteFactory2, méthode CreateGlyphRunAnalysis
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateGlyphRunAnalysis
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abd944c45fc271a22a0942556038073ebcc591cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384927"
---
# <a name="idwritefactory2createglyphrunanalysis-method"></a><span data-ttu-id="0bac4-106">IDWriteFactory2 :: CreateGlyphRunAnalysis, méthode</span><span class="sxs-lookup"><span data-stu-id="0bac4-106">IDWriteFactory2::CreateGlyphRunAnalysis method</span></span>

<span data-ttu-id="0bac4-107">Crée un objet d’analyse de série de glyphes, qui encapsule les informations utilisées pour restituer une exécution de glyphe.</span><span class="sxs-lookup"><span data-stu-id="0bac4-107">Creates a glyph run analysis object, which encapsulates information used to render a glyph run.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bac4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0bac4-108">Syntax</span></span>


```C++
virtual HRESULT CreateGlyphRunAnalysis(
  [in]           const DWRITE_GLYPH_RUN           *glyphRun,
  [in, optional] const DWRITE_MATRIX              *transform,
                       DWRITE_RENDERING_MODE      renderingMode,
                       DWRITE_MEASURING_MODE      measuringMode,
                       DWRITE_GRID_FIT_MODE       gridFitMode,
                       DWRITE_TEXT_ANTIALIAS_MODE antialiasMode,
                       FLOAT                      baselineOriginX,
                       FLOAT                      baselineOriginY,
  [out]                IDWriteGlyphRunAnalysis    **glyphRunAnalysis
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="0bac4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0bac4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bac4-110">*GlyphRun* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0bac4-110">*glyphRun* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bac4-111">Type : \**const [**DWRITE \_ Glyphs \_ Run**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) \** _</span><span class="sxs-lookup"><span data-stu-id="0bac4-111">Type: \**const [**DWRITE\_GLYPH\_RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run)\** _</span></span>

<span data-ttu-id="0bac4-112">Structure spécifiant les propriétés de l’exécution du glyphe.</span><span class="sxs-lookup"><span data-stu-id="0bac4-112">Structure specifying the properties of the glyph run.</span></span>

</dd> <dt>

<span data-ttu-id="0bac4-113">_transform \* \[ in, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="0bac4-113">_transform\* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0bac4-114">Type : \**const [**DWRITE \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \** _</span><span class="sxs-lookup"><span data-stu-id="0bac4-114">Type: \**const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\** _</span></span>

<span data-ttu-id="0bac4-115">Transformation facultative appliquée aux glyphes et à leurs positions.</span><span class="sxs-lookup"><span data-stu-id="0bac4-115">Optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="0bac4-116">Cette transformation est appliquée après la mise à l’échelle spécifiée par emSize et pixelsPerDip.</span><span class="sxs-lookup"><span data-stu-id="0bac4-116">This transform is applied after the scaling specified by the emSize and pixelsPerDip.</span></span>

</dd> <dt>

<span data-ttu-id="0bac4-117">_renderingMode \*</span><span class="sxs-lookup"><span data-stu-id="0bac4-117">_renderingMode\*</span></span> 
</dt> <dd>

<span data-ttu-id="0bac4-118">Type : **\_ \_ mode de rendu DWRITE**</span><span class="sxs-lookup"><span data-stu-id="0bac4-118">Type: **DWRITE\_RENDERING\_MODE**</span></span>

<span data-ttu-id="0bac4-119">Spécifie le mode de rendu, qui doit être l’un des modes de rendu raster (c.-à-d., pas par défaut ni plan).</span><span class="sxs-lookup"><span data-stu-id="0bac4-119">Specifies the rendering mode, which must be one of the raster rendering modes (i.e., not default and not outline).</span></span>

</dd> <dt>

<span data-ttu-id="0bac4-120">*measuringMode*</span><span class="sxs-lookup"><span data-stu-id="0bac4-120">*measuringMode*</span></span> 
</dt> <dd>

<span data-ttu-id="0bac4-121">Type : **[ **\_ \_ mode de mesure DWRITE**](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode)**</span><span class="sxs-lookup"><span data-stu-id="0bac4-121">Type: **[**DWRITE\_MEASURING\_MODE**](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode)**</span></span>

<span data-ttu-id="0bac4-122">Spécifie la méthode pour mesurer les glyphes.</span><span class="sxs-lookup"><span data-stu-id="0bac4-122">Specifies the method to measure glyphs.</span></span>

</dd> <dt>

<span data-ttu-id="0bac4-123">*gridFitMode*</span><span class="sxs-lookup"><span data-stu-id="0bac4-123">*gridFitMode*</span></span> 
</dt> <dd>

<span data-ttu-id="0bac4-124">Type : **[ **\_ \_ \_ mode ajuster à la grille DWRITE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span><span class="sxs-lookup"><span data-stu-id="0bac4-124">Type: **[**DWRITE\_GRID\_FIT\_MODE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span></span>

<span data-ttu-id="0bac4-125">Comment adapter les contours de glyphe.</span><span class="sxs-lookup"><span data-stu-id="0bac4-125">How to grid-fit glyph outlines.</span></span> <span data-ttu-id="0bac4-126">Il ne doit pas être défini par défaut.</span><span class="sxs-lookup"><span data-stu-id="0bac4-126">This must be non-default.</span></span>

</dd> <dt>

<span data-ttu-id="0bac4-127">*antialiasMode*</span><span class="sxs-lookup"><span data-stu-id="0bac4-127">*antialiasMode*</span></span> 
</dt> <dd>

<span data-ttu-id="0bac4-128">Type : **[ **DWRITE \_ Text \_ anticrénelage \_ mode**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)**</span><span class="sxs-lookup"><span data-stu-id="0bac4-128">Type: **[**DWRITE\_TEXT\_ANTIALIAS\_MODE**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)**</span></span>

<span data-ttu-id="0bac4-129">Spécifie le mode d’anticrénelage.</span><span class="sxs-lookup"><span data-stu-id="0bac4-129">Specifies the antialias mode.</span></span>

</dd> <dt>

<span data-ttu-id="0bac4-130">*baselineOriginX*</span><span class="sxs-lookup"><span data-stu-id="0bac4-130">*baselineOriginX*</span></span> 
</dt> <dd>

<span data-ttu-id="0bac4-131">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="0bac4-131">Type: **FLOAT**</span></span>

<span data-ttu-id="0bac4-132">Position horizontale de l’origine de la ligne de base, en DIP.</span><span class="sxs-lookup"><span data-stu-id="0bac4-132">Horizontal position of the baseline origin, in DIPs.</span></span>

</dd> <dt>

<span data-ttu-id="0bac4-133">*baselineOriginY*</span><span class="sxs-lookup"><span data-stu-id="0bac4-133">*baselineOriginY*</span></span> 
</dt> <dd>

<span data-ttu-id="0bac4-134">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="0bac4-134">Type: **FLOAT**</span></span>

<span data-ttu-id="0bac4-135">Position verticale de l’origine de la ligne de base, en DIP.</span><span class="sxs-lookup"><span data-stu-id="0bac4-135">Vertical position of the baseline origin, in DIPs.</span></span>

</dd> <dt>

<span data-ttu-id="0bac4-136">*glyphRunAnalysis* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0bac4-136">*glyphRunAnalysis* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0bac4-137">Type : **[ **IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis)\*\***</span><span class="sxs-lookup"><span data-stu-id="0bac4-137">Type: **[**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis)\*\***</span></span>

<span data-ttu-id="0bac4-138">Reçoit un pointeur vers l’objet nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="0bac4-138">Receives a pointer to the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bac4-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0bac4-139">Return value</span></span>

<span data-ttu-id="0bac4-140">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0bac4-140">Type: **HRESULT**</span></span>

<span data-ttu-id="0bac4-141">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0bac4-141">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0bac4-142">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0bac4-142">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bac4-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0bac4-143">Requirements</span></span>



| <span data-ttu-id="0bac4-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0bac4-144">Requirement</span></span> | <span data-ttu-id="0bac4-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bac4-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bac4-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bac4-146">Minimum supported client</span></span><br/> | <span data-ttu-id="0bac4-147">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0bac4-147">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="0bac4-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bac4-148">Minimum supported server</span></span><br/> | <span data-ttu-id="0bac4-149">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0bac4-149">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="0bac4-150">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bac4-150">Minimum supported phone</span></span><br/>  | <span data-ttu-id="0bac4-151">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="0bac4-151">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="0bac4-152">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0bac4-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="0bac4-153"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0bac4-153"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0bac4-154">DLL</span><span class="sxs-lookup"><span data-stu-id="0bac4-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bac4-155"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bac4-155"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0bac4-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bac4-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bac4-157">**IDWriteFactory2**</span><span class="sxs-lookup"><span data-stu-id="0bac4-157">**IDWriteFactory2**</span></span>](idwritefactory2.md)
</dt> </dl>

 

