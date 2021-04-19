---
title: Méthode IDWriteFontFace GetGdiCompatibleMetrics
description: Obtient les unités de conception et les métriques communes pour le type de police. Ces métriques sont applicables à tous les glyphes d’un fontface et sont utilisées par les applications pour les calculs de disposition.
ms.assetid: 9e132ec0-64cb-4681-b079-02a0047badd5
keywords:
- Écriture directe de la méthode GetGdiCompatibleMetrics
- Méthode GetGdiCompatibleMetrics Write directe, interface IDWriteFontFace
- Écriture directe de l’interface IDWriteFontFace, méthode GetGdiCompatibleMetrics
topic_type:
- apiref
api_name:
- IDWriteFontFace.GetGdiCompatibleMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81b1c00c872352c984c87ee84f7eaed5baffafd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525179"
---
# <a name="idwritefontfacegetgdicompatiblemetrics-method"></a><span data-ttu-id="a87fe-107">IDWriteFontFace :: GetGdiCompatibleMetrics, méthode</span><span class="sxs-lookup"><span data-stu-id="a87fe-107">IDWriteFontFace::GetGdiCompatibleMetrics method</span></span>

<span data-ttu-id="a87fe-108">Obtient les unités de conception et les métriques communes pour le type de police.</span><span class="sxs-lookup"><span data-stu-id="a87fe-108">Obtains design units and common metrics for the font face.</span></span> <span data-ttu-id="a87fe-109">Ces métriques sont applicables à tous les glyphes d’un fontface et sont utilisées par les applications pour les calculs de disposition.</span><span class="sxs-lookup"><span data-stu-id="a87fe-109">These metrics are applicable to all the glyphs within a fontface and are used by applications for layout calculations.</span></span>

## <a name="syntax"></a><span data-ttu-id="a87fe-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a87fe-110">Syntax</span></span>


```C++
virtual HRESULT GetGdiCompatibleMetrics(
                       FLOAT               emSize,
                       FLOAT               pixelsPerDip,
  [in, optional] const DWRITE_MATRIX       *transform,
  [out]                DWRITE_FONT_METRICS *fontFaceMetrics
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="a87fe-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a87fe-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a87fe-112">*emSize*</span><span class="sxs-lookup"><span data-stu-id="a87fe-112">*emSize*</span></span> 
</dt> <dd>

<span data-ttu-id="a87fe-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="a87fe-113">Type: **FLOAT**</span></span>

<span data-ttu-id="a87fe-114">Taille logique de la police en unités DIP.</span><span class="sxs-lookup"><span data-stu-id="a87fe-114">The logical size of the font in DIP units.</span></span>

</dd> <dt>

<span data-ttu-id="a87fe-115">*pixelsPerDip*</span><span class="sxs-lookup"><span data-stu-id="a87fe-115">*pixelsPerDip*</span></span> 
</dt> <dd>

<span data-ttu-id="a87fe-116">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="a87fe-116">Type: **FLOAT**</span></span>

<span data-ttu-id="a87fe-117">Nombre de pixels physiques par DIP.</span><span class="sxs-lookup"><span data-stu-id="a87fe-117">The number of physical pixels per DIP.</span></span>

</dd> <dt>

<span data-ttu-id="a87fe-118">*transformation* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="a87fe-118">*transform* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a87fe-119">Type : **const [**DWRITE \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***</span><span class="sxs-lookup"><span data-stu-id="a87fe-119">Type: **const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\***</span></span>

<span data-ttu-id="a87fe-120">Transformation facultative appliquée aux glyphes et à leurs positions.</span><span class="sxs-lookup"><span data-stu-id="a87fe-120">An optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="a87fe-121">Cette transformation est appliquée après la mise à l’échelle spécifiée par la taille de police et *pixelsPerDip*.</span><span class="sxs-lookup"><span data-stu-id="a87fe-121">This transform is applied after the scaling specified by the font size and *pixelsPerDip*.</span></span>

</dd> <dt>

<span data-ttu-id="a87fe-122">*fontFaceMetrics* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a87fe-122">*fontFaceMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a87fe-123">Type : **[ **\_ \_ métriques de police DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="a87fe-123">Type: **[**DWRITE\_FONT\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)\***</span></span>

<span data-ttu-id="a87fe-124">Pointeur vers une structure [**de \_ \_ mesure de police DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)à remplir.</span><span class="sxs-lookup"><span data-stu-id="a87fe-124">A pointer to a [**DWRITE\_FONT\_METRIC**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)S structure to fill in.</span></span> <span data-ttu-id="a87fe-125">Les métriques retournées par cette fonction se trouvent dans les unités de conception de police.</span><span class="sxs-lookup"><span data-stu-id="a87fe-125">The metrics returned by this function are in font design units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a87fe-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a87fe-126">Return value</span></span>

<span data-ttu-id="a87fe-127">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a87fe-127">Type: **HRESULT**</span></span>

<span data-ttu-id="a87fe-128">Code d’erreur HRESULT standard.</span><span class="sxs-lookup"><span data-stu-id="a87fe-128">Standard HRESULT error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a87fe-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a87fe-129">Requirements</span></span>



| <span data-ttu-id="a87fe-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a87fe-130">Requirement</span></span> | <span data-ttu-id="a87fe-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="a87fe-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a87fe-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a87fe-132">Library</span></span><br/> | <dl> <span data-ttu-id="a87fe-133"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a87fe-133"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="a87fe-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a87fe-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="a87fe-135"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a87fe-135"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a87fe-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a87fe-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a87fe-137">**IDWriteFontFace**</span><span class="sxs-lookup"><span data-stu-id="a87fe-137">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[<span data-ttu-id="a87fe-138">**IDWriteFontFace**</span><span class="sxs-lookup"><span data-stu-id="a87fe-138">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 

