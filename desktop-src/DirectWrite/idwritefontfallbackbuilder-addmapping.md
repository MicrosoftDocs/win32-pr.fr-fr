---
title: Méthode IDWriteFontFallbackBuilder AddMapping
description: Ajoute un mappage unique à la liste. Appelez cette fois pour chaque mappage supplémentaire.
ms.assetid: FCA3CD9C-9FB3-49BD-B4D1-53AEAAAAEE8A
keywords:
- Écriture directe de la méthode AddMapping
- Méthode AddMapping Write directe, interface IDWriteFontFallbackBuilder
- Écriture directe de l’interface IDWriteFontFallbackBuilder, méthode AddMapping
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder.AddMapping
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a084aa2a9df0e34741c8bf5f39ae00933d49cfe7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384920"
---
# <a name="idwritefontfallbackbuilderaddmapping-method"></a><span data-ttu-id="594f9-107">IDWriteFontFallbackBuilder :: AddMapping, méthode</span><span class="sxs-lookup"><span data-stu-id="594f9-107">IDWriteFontFallbackBuilder::AddMapping method</span></span>

<span data-ttu-id="594f9-108">Ajoute un mappage unique à la liste.</span><span class="sxs-lookup"><span data-stu-id="594f9-108">Appends a single mapping to the list.</span></span> <span data-ttu-id="594f9-109">Appelez cette fois pour chaque mappage supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="594f9-109">Call this once for each additional mapping.</span></span>

## <a name="syntax"></a><span data-ttu-id="594f9-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="594f9-110">Syntax</span></span>


```C++
HRESULT AddMapping(
                       DWRITE_UNICODE_RANGE  *ranges,
                       UINT32                rangesCount,
  [in]           const WCHAR                 **targetFamilyNames,
                       UINT32                targetFamilyNamesCount,
  [in, optional]       IDWriteFontCollection fontCollection = nullptr,
  [in, optional] const WCHAR                 *localeName = nullptr,
  [in, optional] const WCHAR                 *baseFamilyName = nullptr,
                       FLOAT                 scale = 1
);
```



## <a name="parameters"></a><span data-ttu-id="594f9-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="594f9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="594f9-112">*gamme*</span><span class="sxs-lookup"><span data-stu-id="594f9-112">*ranges*</span></span> 
</dt> <dd>

<span data-ttu-id="594f9-113">Type : \**[**DWRITE \_ Unicode \_ Range**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_unicode_range) \** _</span><span class="sxs-lookup"><span data-stu-id="594f9-113">Type: \**[**DWRITE\_UNICODE\_RANGE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_unicode_range)\** _</span></span>

<span data-ttu-id="594f9-114">Plages Unicode qui s’appliquent à ce mappage.</span><span class="sxs-lookup"><span data-stu-id="594f9-114">Unicode ranges that apply to this mapping.</span></span>

</dd> <dt>

<span data-ttu-id="594f9-115">_rangesCount \*</span><span class="sxs-lookup"><span data-stu-id="594f9-115">_rangesCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="594f9-116">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="594f9-116">Type: **UINT32**</span></span>

<span data-ttu-id="594f9-117">Nombre de plages Unicode.</span><span class="sxs-lookup"><span data-stu-id="594f9-117">Number of Unicode ranges.</span></span>

</dd> <dt>

<span data-ttu-id="594f9-118">*targetFamilyNames* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="594f9-118">*targetFamilyNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="594f9-119">Type : **const WCHAR \* \***</span><span class="sxs-lookup"><span data-stu-id="594f9-119">Type: **const WCHAR\*\***</span></span>

<span data-ttu-id="594f9-120">Liste des chaînes du nom de la famille cible.</span><span class="sxs-lookup"><span data-stu-id="594f9-120">List of target family name strings.</span></span>

</dd> <dt>

<span data-ttu-id="594f9-121">*targetFamilyNamesCount*</span><span class="sxs-lookup"><span data-stu-id="594f9-121">*targetFamilyNamesCount*</span></span> 
</dt> <dd>

<span data-ttu-id="594f9-122">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="594f9-122">Type: **UINT32**</span></span>

<span data-ttu-id="594f9-123">Nombre de noms de familles cibles.</span><span class="sxs-lookup"><span data-stu-id="594f9-123">Number of target family names.</span></span>

</dd> <dt>

<span data-ttu-id="594f9-124">*fontCollection* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="594f9-124">*fontCollection* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="594f9-125">Type : **[ **IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)**</span><span class="sxs-lookup"><span data-stu-id="594f9-125">Type: **[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)**</span></span>

<span data-ttu-id="594f9-126">Collection de polices explicites facultative pour ce mappage.</span><span class="sxs-lookup"><span data-stu-id="594f9-126">Optional explicit font collection for this mapping.</span></span>

</dd> <dt>

<span data-ttu-id="594f9-127">*localeName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="594f9-127">*localeName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="594f9-128">Type : \**const WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="594f9-128">Type: \**const WCHAR\** _</span></span>

<span data-ttu-id="594f9-129">Paramètres régionaux du contexte.</span><span class="sxs-lookup"><span data-stu-id="594f9-129">Locale of the context.</span></span>

</dd> <dt>

<span data-ttu-id="594f9-130">_baseFamilyName \* \[ in, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="594f9-130">_baseFamilyName\* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="594f9-131">Type : \**const WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="594f9-131">Type: \**const WCHAR\** _</span></span>

<span data-ttu-id="594f9-132">Nom de famille de base avec lequel effectuer la correspondance, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="594f9-132">Base family name to match against, if applicable.</span></span>

</dd> <dt>

<span data-ttu-id="594f9-133">_scale \*</span><span class="sxs-lookup"><span data-stu-id="594f9-133">_scale\*</span></span> 
</dt> <dd>

<span data-ttu-id="594f9-134">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="594f9-134">Type: **FLOAT**</span></span>

<span data-ttu-id="594f9-135">Facteur d’échelle pour multiplier la police de la cible du résultat par.</span><span class="sxs-lookup"><span data-stu-id="594f9-135">Scale factor to multiply the result target font by.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="594f9-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="594f9-136">Return value</span></span>

<span data-ttu-id="594f9-137">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="594f9-137">Type: **HRESULT**</span></span>

<span data-ttu-id="594f9-138">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="594f9-138">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="594f9-139">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="594f9-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="594f9-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="594f9-140">Requirements</span></span>



| <span data-ttu-id="594f9-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="594f9-141">Requirement</span></span> | <span data-ttu-id="594f9-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="594f9-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="594f9-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="594f9-143">Minimum supported client</span></span><br/> | <span data-ttu-id="594f9-144">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="594f9-144">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="594f9-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="594f9-145">Minimum supported server</span></span><br/> | <span data-ttu-id="594f9-146">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="594f9-146">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="594f9-147">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="594f9-147">Minimum supported phone</span></span><br/>  | <span data-ttu-id="594f9-148">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="594f9-148">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="594f9-149">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="594f9-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="594f9-150"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="594f9-150"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="594f9-151">DLL</span><span class="sxs-lookup"><span data-stu-id="594f9-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="594f9-152"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="594f9-152"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="594f9-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="594f9-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="594f9-154">**IDWriteFontFallbackBuilder**</span><span class="sxs-lookup"><span data-stu-id="594f9-154">**IDWriteFontFallbackBuilder**</span></span>](idwritefontfallbackbuilder.md)
</dt> </dl>

 

