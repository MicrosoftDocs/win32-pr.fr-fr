---
description: Filtre de convertisseur audio (WaveOut)
ms.assetid: a3f2776b-974b-4886-82a3-38e00b607a07
title: Filtre de convertisseur audio (WaveOut)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5f47018d22bcbbdcf884f5eb4356d1d0b3fe60d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106512871"
---
# <a name="audio-renderer-waveout-filter"></a><span data-ttu-id="0f978-103">Filtre de convertisseur audio (WaveOut)</span><span class="sxs-lookup"><span data-stu-id="0f978-103">Audio Renderer (WaveOut) Filter</span></span>

<span data-ttu-id="0f978-104">Ce filtre utilise l' \* API WaveOut pour restituer l’audio de forme d’onde.</span><span class="sxs-lookup"><span data-stu-id="0f978-104">This filter uses the waveOut\* API to render waveform audio.</span></span> <span data-ttu-id="0f978-105">Toutefois, le [filtre de convertisseur DirectSound](directsound-renderer-filter.md) fournit les mêmes fonctionnalités à l’aide de DirectSound.</span><span class="sxs-lookup"><span data-stu-id="0f978-105">However, the [DirectSound Renderer Filter](directsound-renderer-filter.md) provides the same functionality using DirectSound.</span></span> <span data-ttu-id="0f978-106">Par défaut, le gestionnaire de graphes de filtre utilise le convertisseur DirectSound à la place de ce filtre.</span><span class="sxs-lookup"><span data-stu-id="0f978-106">By default, the Filter Graph Manager uses the DirectSound Renderer instead of this filter.</span></span> <span data-ttu-id="0f978-107">Le mixage audio est désactivé dans le convertisseur audio waveOut. par conséquent, si vous devez mélanger plusieurs flux audio pendant la lecture, utilisez le convertisseur DirectSound.</span><span class="sxs-lookup"><span data-stu-id="0f978-107">Audio mixing is disabled in the waveOut Audio Renderer, so if you need to mix multiple audio streams during playback, use the DirectSound renderer.</span></span>

<span data-ttu-id="0f978-108">Ce filtre ne vérifie pas le sous-type du flux audio.</span><span class="sxs-lookup"><span data-stu-id="0f978-108">This filter does not check the audio stream's subtype.</span></span> <span data-ttu-id="0f978-109">La structure [**WaveFormat**](/windows/win32/api/mmreg/ns-mmreg-waveformat) ou [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) passée dans le format contient les informations nécessaires à la connexion.</span><span class="sxs-lookup"><span data-stu-id="0f978-109">The [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) or [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure passed in the format contains the information needed for the connection.</span></span>

<span data-ttu-id="0f978-110">Ce filtre prend en charge une plage de taux d’échantillonnage qui dépend du pilote audio.</span><span class="sxs-lookup"><span data-stu-id="0f978-110">This filter supports a range of sample rates that depends on the audio driver.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0f978-111">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="0f978-111">Filter Interfaces</span></span></td>
<td><ul>
<li><span data-ttu-id="0f978-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f978-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a></span></span></li>
<li><span data-ttu-id="0f978-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f978-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a></span></span></li>
<li><span data-ttu-id="0f978-114"><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f978-114"><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a></span></span></li>
<li><span data-ttu-id="0f978-115"><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f978-115"><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a></span></span></li>
<li><span data-ttu-id="0f978-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f978-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="0f978-117"><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f978-117"><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a></span></span></li>
<li><span data-ttu-id="0f978-118"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f978-118"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></span></span></li>
<li><span data-ttu-id="0f978-119"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f978-119"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></li>
<li><span data-ttu-id="0f978-120">IPersistPropertyBag</span><span class="sxs-lookup"><span data-stu-id="0f978-120">IPersistPropertyBag</span></span></li>
<li><span data-ttu-id="0f978-121">IPersistStream</span><span class="sxs-lookup"><span data-stu-id="0f978-121">IPersistStream</span></span></li>
<li><span data-ttu-id="0f978-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f978-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="0f978-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f978-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f978-124">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="0f978-124">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="0f978-125"><strong>MEDIATYPE_Audio</strong></span><span class="sxs-lookup"><span data-stu-id="0f978-125"><strong>MEDIATYPE_Audio</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f978-126">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="0f978-126">Input Pin Interfaces</span></span></td>
<td><ul>
<li><span data-ttu-id="0f978-127"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f978-127"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
<li><span data-ttu-id="0f978-128"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f978-128"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="0f978-129"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="0f978-129"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f978-130">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="0f978-130">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="0f978-131">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="0f978-131">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f978-132">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="0f978-132">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="0f978-133">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="0f978-133">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f978-134">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="0f978-134">Filter CLSID</span></span></td>
<td><span data-ttu-id="0f978-135"><strong>CLSID_AudioRender</strong></span><span class="sxs-lookup"><span data-stu-id="0f978-135"><strong>CLSID_AudioRender</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f978-136">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="0f978-136">Property Page CLSID</span></span></td>
<td><span data-ttu-id="0f978-137"><strong>CLSID_AudioProperties</strong>, <strong>CLSID_AudioRendererAdvancedProperties</strong></span><span class="sxs-lookup"><span data-stu-id="0f978-137"><strong>CLSID_AudioProperties</strong>, <strong>CLSID_AudioRendererAdvancedProperties</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f978-138">Exécutable</span><span class="sxs-lookup"><span data-stu-id="0f978-138">Executable</span></span></td>
<td><span data-ttu-id="0f978-139">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="0f978-139">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f978-140"><a href="merit.md">Mérite</a></span><span class="sxs-lookup"><span data-stu-id="0f978-140"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="0f978-141"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="0f978-141"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f978-142"><a href="filter-categories.md">Catégorie de filtre</a></span><span class="sxs-lookup"><span data-stu-id="0f978-142"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="0f978-143"><strong>CLSID_AudioRendererCategory</strong></span><span class="sxs-lookup"><span data-stu-id="0f978-143"><strong>CLSID_AudioRendererCategory</strong></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="0f978-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0f978-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f978-145">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="0f978-145">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
