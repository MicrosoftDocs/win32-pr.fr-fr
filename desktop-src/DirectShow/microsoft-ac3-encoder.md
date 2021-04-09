---
description: Le filtre d’encodeur AC-3 microsoft Encode le son stéréo PCM sur un flux de données numérique Dolby Digital.
ms.assetid: 59d46ee2-d45f-4492-938d-39c55a7368e1
title: Encodeur AC-3 Microsoft (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 160b020e07bb3ba4e4dc5636b58dd0e66f581a6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109179"
---
# <a name="microsoft-ac-3-encoder"></a><span data-ttu-id="17d93-103">Encodeur AC-3 Microsoft</span><span class="sxs-lookup"><span data-stu-id="17d93-103">Microsoft AC-3 Encoder</span></span>

<span data-ttu-id="17d93-104">Le filtre d’encodeur AC-3 microsoft Encode le son stéréo PCM sur un flux de données numérique Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="17d93-104">The Microsoft AC-3 Encoder filter encodes stereo PCM audio to a Dolby Digital bitstream.</span></span>

> [!Note]  
> <span data-ttu-id="17d93-105">L’implémentation Microsoft de la technologie Dolby Digital est limitée aux termes du programme de gestion de licences Dolby Digital à utiliser par les applications Microsoft.</span><span class="sxs-lookup"><span data-stu-id="17d93-105">The Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

> [!Note]  
> <span data-ttu-id="17d93-106">Ce filtre n’est pas pris en charge sur les plateformes IA-64.</span><span class="sxs-lookup"><span data-stu-id="17d93-106">This filter is not supported on IA-64-based platforms.</span></span>

 



<span data-ttu-id="17d93-107">Informations de filtre</span><span class="sxs-lookup"><span data-stu-id="17d93-107">Filter Information</span></span>

<span data-ttu-id="17d93-108">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="17d93-108">Filter Interfaces</span></span>

[<span data-ttu-id="17d93-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="17d93-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/>

<span data-ttu-id="17d93-110">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="17d93-110">Input Pin Media Types</span></span>

<span data-ttu-id="17d93-111">**MediaType \_ Audio**, **MEDIASUBTYPE \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="17d93-111">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_PCM**</span></span><br/> <span data-ttu-id="17d93-112">Le type d’entrée doit être stéréo de 48 kHz, 16 bits par échantillon.</span><span class="sxs-lookup"><span data-stu-id="17d93-112">The input type must be 48-kHz stereo, 16 bits per sample.</span></span><br/>

<span data-ttu-id="17d93-113">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="17d93-113">Input Pin Interfaces</span></span>

[<span data-ttu-id="17d93-114">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="17d93-114">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="17d93-115">**IPin**</span><span class="sxs-lookup"><span data-stu-id="17d93-115">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="17d93-116">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="17d93-116">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="17d93-117">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="17d93-117">Output Pin Media Types</span></span>

<span data-ttu-id="17d93-118">**MediaType \_ Audio**, **MEDIASUBTYPE \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="17d93-118">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_AC3**</span></span><br/> <span data-ttu-id="17d93-119">**MediaType \_ Stream**, **MEDIASUBTYPE \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="17d93-119">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_DOLBY\_AC3**</span></span><br/>

<span data-ttu-id="17d93-120">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="17d93-120">Output Pin Interfaces</span></span>

[<span data-ttu-id="17d93-121">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="17d93-121">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="17d93-122">**IPin**</span><span class="sxs-lookup"><span data-stu-id="17d93-122">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="17d93-123">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="17d93-123">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="17d93-124">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="17d93-124">Filter CLSID</span></span>

<span data-ttu-id="17d93-125">**CLSID \_ CMSAC3Enc** (déclaré dans wmcodecdsp. h)</span><span class="sxs-lookup"><span data-stu-id="17d93-125">**CLSID\_CMSAC3Enc** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="17d93-126">Exécutable</span><span class="sxs-lookup"><span data-stu-id="17d93-126">Executable</span></span>

<span data-ttu-id="17d93-127">msac3enc.dll</span><span class="sxs-lookup"><span data-stu-id="17d93-127">msac3enc.dll</span></span>

[<span data-ttu-id="17d93-128">Mérite</span><span class="sxs-lookup"><span data-stu-id="17d93-128">Merit</span></span>](merit.md)

<span data-ttu-id="17d93-129">**MÉRITE \_ n' \_ \_ utilise pas**</span><span class="sxs-lookup"><span data-stu-id="17d93-129">**MERIT\_DO\_NOT\_USE**</span></span>

[<span data-ttu-id="17d93-130">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="17d93-130">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="17d93-131">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="17d93-131">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="17d93-132">Notes</span><span class="sxs-lookup"><span data-stu-id="17d93-132">Remarks</span></span>

<span data-ttu-id="17d93-133">Ce filtre n’est pas disponible pour une utilisation par des applications tierces.</span><span class="sxs-lookup"><span data-stu-id="17d93-133">This filter is not available for use by third-party applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="17d93-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17d93-134">Requirements</span></span>



| <span data-ttu-id="17d93-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17d93-135">Requirement</span></span> | <span data-ttu-id="17d93-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="17d93-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17d93-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17d93-137">Minimum supported client</span></span><br/> | <span data-ttu-id="17d93-138">Windows Vista Édition familiale Premium, Windows Vista Édition intégrale, Windows 7 Édition familiale Premium, Windows 7 professionnel, Windows 7 entreprise, applications de bureau Windows 7 édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17d93-138">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="17d93-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17d93-139">Minimum supported server</span></span><br/> | <span data-ttu-id="17d93-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="17d93-140">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="17d93-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="17d93-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="17d93-142"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="17d93-142"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="17d93-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17d93-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17d93-144">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="17d93-144">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




