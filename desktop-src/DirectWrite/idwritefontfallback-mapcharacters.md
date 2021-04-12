---
title: Méthode IDWriteFontFallback MapCharacters
description: Détermine une police appropriée à utiliser pour restituer la plage de texte de début.
ms.assetid: 9D3DBBF7-72D4-473D-A321-E64BC94493D5
keywords:
- Écriture directe de la méthode MapCharacters
- Méthode MapCharacters Write directe, interface IDWriteFontFallback
- Écriture directe de l’interface IDWriteFontFallback, méthode MapCharacters
topic_type:
- apiref
api_name:
- IDWriteFontFallback.MapCharacters
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 428778afc12c668d284dffb5a8a6f734c03f0705
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317310"
---
# <a name="idwritefontfallbackmapcharacters-method"></a><span data-ttu-id="d69c5-106">IDWriteFontFallback :: MapCharacters, méthode</span><span class="sxs-lookup"><span data-stu-id="d69c5-106">IDWriteFontFallback::MapCharacters method</span></span>

<span data-ttu-id="d69c5-107">Détermine une police appropriée à utiliser pour restituer la plage de texte de début.</span><span class="sxs-lookup"><span data-stu-id="d69c5-107">Determines an appropriate font to use to render the beginning range of text.</span></span>

## <a name="syntax"></a><span data-ttu-id="d69c5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d69c5-108">Syntax</span></span>


```C++
HRESULT MapCharacters(
                       IDWriteTextAnalysisSource *source,
                       UINT32                    textPosition,
                       UINT32                    textLength,
  [in, optional]       IDWriteFontCollection     *baseFontCollection,
  [in, optional] const wchar_t                   *baseFamilyName,
                       DWRITE_FONT_WEIGHT        baseWeight,
                       DWRITE_FONT_STYLE         baseStyle,
                       DWRITE_FONT_STRETCH       baseStretch,
  [out]                UINT32                    *mappedLength,
  [out]                IDWriteFont               **mappedFont,
  [out]                FLOAT                     *scale
);
```



## <a name="parameters"></a><span data-ttu-id="d69c5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d69c5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d69c5-110">*source*</span><span class="sxs-lookup"><span data-stu-id="d69c5-110">*source*</span></span> 
</dt> <dd>

<span data-ttu-id="d69c5-111">Tapez : \**[**IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource) \** _</span><span class="sxs-lookup"><span data-stu-id="d69c5-111">Type: \**[**IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource)\** _</span></span>

<span data-ttu-id="d69c5-112">L’implémentation de la source de texte contient le texte et les paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="d69c5-112">The text source implementation holds the text and locale.</span></span>

</dd> <dt>

<span data-ttu-id="d69c5-113">_textPosition \*</span><span class="sxs-lookup"><span data-stu-id="d69c5-113">_textPosition\*</span></span> 
</dt> <dd>

<span data-ttu-id="d69c5-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d69c5-114">Type: **UINT32**</span></span>

<span data-ttu-id="d69c5-115">Position de départ à analyser.</span><span class="sxs-lookup"><span data-stu-id="d69c5-115">Starting position to analyze.</span></span>

</dd> <dt>

<span data-ttu-id="d69c5-116">*textLength*</span><span class="sxs-lookup"><span data-stu-id="d69c5-116">*textLength*</span></span> 
</dt> <dd>

<span data-ttu-id="d69c5-117">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d69c5-117">Type: **UINT32**</span></span>

<span data-ttu-id="d69c5-118">Longueur du texte à analyser.</span><span class="sxs-lookup"><span data-stu-id="d69c5-118">Length of the text to analyze.</span></span>

</dd> <dt>

<span data-ttu-id="d69c5-119">*baseFontCollection* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d69c5-119">*baseFontCollection* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d69c5-120">Tapez : \**[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) \** _</span><span class="sxs-lookup"><span data-stu-id="d69c5-120">Type: \**[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)\** _</span></span>

<span data-ttu-id="d69c5-121">Collection de polices par défaut à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d69c5-121">Default font collection to use.</span></span>

</dd> <dt>

<span data-ttu-id="d69c5-122">_baseFamilyName \* \[ in, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d69c5-122">_baseFamilyName\* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d69c5-123">Type : \**const WCHAR \_ t \** _</span><span class="sxs-lookup"><span data-stu-id="d69c5-123">Type: \**const wchar\_t\** _</span></span>

<span data-ttu-id="d69c5-124">Nom de famille de la police de base.</span><span class="sxs-lookup"><span data-stu-id="d69c5-124">Family name of the base font.</span></span> <span data-ttu-id="d69c5-125">Si vous transmettez la valeur null, aucune correspondance n’est effectuée par rapport à la famille.</span><span class="sxs-lookup"><span data-stu-id="d69c5-125">If you pass null, no matching will be done against the family.</span></span>

</dd> <dt>

<span data-ttu-id="d69c5-126">_baseWeight \*</span><span class="sxs-lookup"><span data-stu-id="d69c5-126">_baseWeight\*</span></span> 
</dt> <dd>

<span data-ttu-id="d69c5-127">Type : épaisseur de la **[ **\_ police \_ DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)**</span><span class="sxs-lookup"><span data-stu-id="d69c5-127">Type: **[**DWRITE\_FONT\_WEIGHT**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)**</span></span>

<span data-ttu-id="d69c5-128">Poids souhaité.</span><span class="sxs-lookup"><span data-stu-id="d69c5-128">The desired weight.</span></span>

</dd> <dt>

<span data-ttu-id="d69c5-129">*baseStyle*</span><span class="sxs-lookup"><span data-stu-id="d69c5-129">*baseStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="d69c5-130">Type : **[ **DWRITE \_ \_ style de police**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)**</span><span class="sxs-lookup"><span data-stu-id="d69c5-130">Type: **[**DWRITE\_FONT\_STYLE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)**</span></span>

<span data-ttu-id="d69c5-131">Style souhaité.</span><span class="sxs-lookup"><span data-stu-id="d69c5-131">The desired style.</span></span>

</dd> <dt>

<span data-ttu-id="d69c5-132">*baseStretch*</span><span class="sxs-lookup"><span data-stu-id="d69c5-132">*baseStretch*</span></span> 
</dt> <dd>

<span data-ttu-id="d69c5-133">Type : **[ **\_ \_ étirement de police DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)**</span><span class="sxs-lookup"><span data-stu-id="d69c5-133">Type: **[**DWRITE\_FONT\_STRETCH**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)**</span></span>

<span data-ttu-id="d69c5-134">Étirement souhaité.</span><span class="sxs-lookup"><span data-stu-id="d69c5-134">The desired stretch.</span></span>

</dd> <dt>

<span data-ttu-id="d69c5-135">*mappedLength* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d69c5-135">*mappedLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d69c5-136">Type : \**UInt32 \** _</span><span class="sxs-lookup"><span data-stu-id="d69c5-136">Type: \**UINT32\** _</span></span>

<span data-ttu-id="d69c5-137">Longueur du texte mappé à la police mappée.</span><span class="sxs-lookup"><span data-stu-id="d69c5-137">Length of text mapped to the mapped font.</span></span> <span data-ttu-id="d69c5-138">Cela sera toujours inférieur ou égal à la longueur du texte et supérieur à zéro (si la longueur du texte est différente de zéro), de sorte que l’appelant avance au moins un caractère.</span><span class="sxs-lookup"><span data-stu-id="d69c5-138">This will always be less than or equal to the text length and greater than zero (if the text length is non-zero) so the caller advances at least one character.</span></span>

</dd> <dt>

<span data-ttu-id="d69c5-139">_mappedFont \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d69c5-139">_mappedFont\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d69c5-140">Type : **[ **IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***</span><span class="sxs-lookup"><span data-stu-id="d69c5-140">Type: **[**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***</span></span>

<span data-ttu-id="d69c5-141">Police qui doit être utilisée pour afficher les premiers caractères *mappedLength* du texte.</span><span class="sxs-lookup"><span data-stu-id="d69c5-141">The font that should be used to render the first *mappedLength* characters of the text.</span></span> <span data-ttu-id="d69c5-142">Si elle retourne NULL, cela signifie qu’aucune police ne peut restituer le texte, et *mappedLength* est le nombre de caractères à ignorer (rendu avec un glyphe manquant).</span><span class="sxs-lookup"><span data-stu-id="d69c5-142">If it returns NULL, that means that no font can render the text, and *mappedLength* is the number of characters to skip (rendered with a missing glyph).</span></span>

</dd> <dt>

<span data-ttu-id="d69c5-143">mise à l' *échelle* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d69c5-143">*scale* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d69c5-144">Type : \**float \** _</span><span class="sxs-lookup"><span data-stu-id="d69c5-144">Type: \**FLOAT\** _</span></span>

<span data-ttu-id="d69c5-145">Facteur d’échelle pour multiplier la taille em de la police retournée par.</span><span class="sxs-lookup"><span data-stu-id="d69c5-145">Scale factor to multiply the em size of the returned font by.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d69c5-146">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d69c5-146">Return value</span></span>

<span data-ttu-id="d69c5-147">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="d69c5-147">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="d69c5-148">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d69c5-148">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d69c5-149">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d69c5-149">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d69c5-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d69c5-150">Requirements</span></span>



| <span data-ttu-id="d69c5-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d69c5-151">Requirement</span></span> | <span data-ttu-id="d69c5-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="d69c5-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d69c5-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d69c5-153">Minimum supported client</span></span><br/> | <span data-ttu-id="d69c5-154">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d69c5-154">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d69c5-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d69c5-155">Minimum supported server</span></span><br/> | <span data-ttu-id="d69c5-156">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d69c5-156">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d69c5-157">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d69c5-157">Minimum supported phone</span></span><br/>  | <span data-ttu-id="d69c5-158">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="d69c5-158">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="d69c5-159">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d69c5-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="d69c5-160"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d69c5-160"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d69c5-161">DLL</span><span class="sxs-lookup"><span data-stu-id="d69c5-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d69c5-162"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d69c5-162"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d69c5-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d69c5-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d69c5-164">**IDWriteFontFallback**</span><span class="sxs-lookup"><span data-stu-id="d69c5-164">**IDWriteFontFallback**</span></span>](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)
</dt> </dl>

 

