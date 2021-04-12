---
title: Méthode IDWriteFactory2 CreateCustomRenderingParams
description: Crée un objet de paramètres de rendu avec les propriétés spécifiées.
ms.assetid: 947d50fd-888c-2f0b-25c2-b19b0e6fad58
keywords:
- Écriture directe de la méthode CreateCustomRenderingParams
- Méthode CreateCustomRenderingParams Write directe, interface IDWriteFactory2
- Écriture directe de l’interface IDWriteFactory2, méthode CreateCustomRenderingParams
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateCustomRenderingParams
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bd69cde6858061b69b8143dcdd0560342e65f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384928"
---
# <a name="idwritefactory2createcustomrenderingparams-method"></a><span data-ttu-id="3aede-106">IDWriteFactory2 :: CreateCustomRenderingParams, méthode</span><span class="sxs-lookup"><span data-stu-id="3aede-106">IDWriteFactory2::CreateCustomRenderingParams method</span></span>

<span data-ttu-id="3aede-107">Crée un objet de paramètres de rendu avec les propriétés spécifiées.</span><span class="sxs-lookup"><span data-stu-id="3aede-107">Creates a rendering parameters object with the specified properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aede-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3aede-108">Syntax</span></span>


```C++
virtual HRESULT CreateCustomRenderingParams(
        FLOAT                   gamma,
        FLOAT                   enhancedContrast,
        FLOAT                   grayscaleEnhancedContrast,
        FLOAT                   clearTypeLevel,
        DWRITE_PIXEL_GEOMETRY   pixelGeometry,
        DWRITE_RENDERING_MODE   renderingMode,
        DWRITE_GRID_FIT_MODE    gridFitMode,
  [out] IDWriteRenderingParams2 **renderingParams
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="3aede-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3aede-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3aede-110">*gamma*</span><span class="sxs-lookup"><span data-stu-id="3aede-110">*gamma*</span></span> 
</dt> <dd>

<span data-ttu-id="3aede-111">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="3aede-111">Type: **FLOAT**</span></span>

<span data-ttu-id="3aede-112">Valeur gamma utilisée pour la correction gamma, qui doit être supérieure à zéro et ne peut pas dépasser 256.</span><span class="sxs-lookup"><span data-stu-id="3aede-112">The gamma value used for gamma correction, which must be greater than zero and cannot exceed 256.</span></span>

</dd> <dt>

<span data-ttu-id="3aede-113">*enhancedContrast*</span><span class="sxs-lookup"><span data-stu-id="3aede-113">*enhancedContrast*</span></span> 
</dt> <dd>

<span data-ttu-id="3aede-114">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="3aede-114">Type: **FLOAT**</span></span>

<span data-ttu-id="3aede-115">La quantité d’amélioration du contraste, zéro ou une valeur supérieure.</span><span class="sxs-lookup"><span data-stu-id="3aede-115">The amount of contrast enhancement, zero or greater.</span></span>

</dd> <dt>

<span data-ttu-id="3aede-116">*grayscaleEnhancedContrast*</span><span class="sxs-lookup"><span data-stu-id="3aede-116">*grayscaleEnhancedContrast*</span></span> 
</dt> <dd>

<span data-ttu-id="3aede-117">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="3aede-117">Type: **FLOAT**</span></span>

<span data-ttu-id="3aede-118">La quantité d’amélioration du contraste, zéro ou une valeur supérieure.</span><span class="sxs-lookup"><span data-stu-id="3aede-118">The amount of contrast enhancement, zero or greater.</span></span>

</dd> <dt>

<span data-ttu-id="3aede-119">*clearTypeLevel*</span><span class="sxs-lookup"><span data-stu-id="3aede-119">*clearTypeLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="3aede-120">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="3aede-120">Type: **FLOAT**</span></span>

<span data-ttu-id="3aede-121">Degré de niveau ClearType, de 0.0 f (no ClearType) à 1.0 f (Full ClearType).</span><span class="sxs-lookup"><span data-stu-id="3aede-121">The degree of ClearType level, from 0.0f (no ClearType) to 1.0f (full ClearType).</span></span>

</dd> <dt>

<span data-ttu-id="3aede-122">*pixelGeometry*</span><span class="sxs-lookup"><span data-stu-id="3aede-122">*pixelGeometry*</span></span> 
</dt> <dd>

<span data-ttu-id="3aede-123">Type : **[ **DWRITE \_ pixel \_ Geometry**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry)**</span><span class="sxs-lookup"><span data-stu-id="3aede-123">Type: **[**DWRITE\_PIXEL\_GEOMETRY**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry)**</span></span>

<span data-ttu-id="3aede-124">Géométrie d’un pixel d’appareil.</span><span class="sxs-lookup"><span data-stu-id="3aede-124">The geometry of a device pixel.</span></span>

</dd> <dt>

<span data-ttu-id="3aede-125">*renderingMode*</span><span class="sxs-lookup"><span data-stu-id="3aede-125">*renderingMode*</span></span> 
</dt> <dd>

<span data-ttu-id="3aede-126">Type : **[ **\_ \_ mode de rendu DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)**</span><span class="sxs-lookup"><span data-stu-id="3aede-126">Type: **[**DWRITE\_RENDERING\_MODE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)**</span></span>

<span data-ttu-id="3aede-127">Méthode de rendu des glyphes.</span><span class="sxs-lookup"><span data-stu-id="3aede-127">Method of rendering glyphs.</span></span> <span data-ttu-id="3aede-128">Dans la plupart des cas, il doit s’agir du \_ mode de rendu DWRITE \_ \_ par défaut pour utiliser automatiquement un mode approprié.</span><span class="sxs-lookup"><span data-stu-id="3aede-128">In most cases, this should be DWRITE\_RENDERING\_MODE\_DEFAULT to automatically use an appropriate mode.</span></span>

</dd> <dt>

<span data-ttu-id="3aede-129">*gridFitMode*</span><span class="sxs-lookup"><span data-stu-id="3aede-129">*gridFitMode*</span></span> 
</dt> <dd>

<span data-ttu-id="3aede-130">Type : **[ **\_ \_ \_ mode ajuster à la grille DWRITE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span><span class="sxs-lookup"><span data-stu-id="3aede-130">Type: **[**DWRITE\_GRID\_FIT\_MODE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span></span>

<span data-ttu-id="3aede-131">Comment ajuster les contours de glyphes.</span><span class="sxs-lookup"><span data-stu-id="3aede-131">How to grid fit glyph outlines.</span></span> <span data-ttu-id="3aede-132">Dans la plupart des cas, il doit s’agir de la \_ grille DWRITE \_ \_ par défaut pour choisir automatiquement un mode approprié.</span><span class="sxs-lookup"><span data-stu-id="3aede-132">In most cases, this should be DWRITE\_GRID\_FIT\_DEFAULT to automatically choose an appropriate mode.</span></span>

</dd> <dt>

<span data-ttu-id="3aede-133">*renderingParams* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3aede-133">*renderingParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3aede-134">Type : **[ **IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2)\*\***</span><span class="sxs-lookup"><span data-stu-id="3aede-134">Type: **[**IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2)\*\***</span></span>

<span data-ttu-id="3aede-135">Contient l’objet de paramètres de rendu nouvellement créé, ou NULL en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="3aede-135">Holds the newly created rendering parameters object, or NULL in case of failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3aede-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3aede-136">Return value</span></span>

<span data-ttu-id="3aede-137">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3aede-137">Type: **HRESULT**</span></span>

<span data-ttu-id="3aede-138">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3aede-138">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3aede-139">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3aede-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3aede-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3aede-140">Requirements</span></span>



| <span data-ttu-id="3aede-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3aede-141">Requirement</span></span> | <span data-ttu-id="3aede-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="3aede-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3aede-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3aede-143">Minimum supported client</span></span><br/> | <span data-ttu-id="3aede-144">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3aede-144">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="3aede-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3aede-145">Minimum supported server</span></span><br/> | <span data-ttu-id="3aede-146">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3aede-146">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="3aede-147">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3aede-147">Minimum supported phone</span></span><br/>  | <span data-ttu-id="3aede-148">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="3aede-148">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="3aede-149">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3aede-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="3aede-150"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3aede-150"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="3aede-151">DLL</span><span class="sxs-lookup"><span data-stu-id="3aede-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3aede-152"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3aede-152"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3aede-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3aede-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aede-154">**IDWriteFactory2**</span><span class="sxs-lookup"><span data-stu-id="3aede-154">**IDWriteFactory2**</span></span>](idwritefactory2.md)
</dt> </dl>

 

