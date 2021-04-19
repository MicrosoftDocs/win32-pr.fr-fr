---
description: Filtre de l’analyseur WAVE
ms.assetid: 53a9538d-7a79-40bb-9468-d710eb238925
title: Filtre de l’analyseur WAVE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb30465a25ab3a6eef190b5fbecd4a4878c2744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522236"
---
# <a name="wave-parser-filter"></a><span data-ttu-id="f33de-103">Filtre de l’analyseur WAVE</span><span class="sxs-lookup"><span data-stu-id="f33de-103">WAVE Parser Filter</span></span>

<span data-ttu-id="f33de-104">Le filtre de l’analyseur WAVE analyse les données audio au format WAV à partir des fichiers. wav,... ou. AIF.</span><span class="sxs-lookup"><span data-stu-id="f33de-104">The WAVE Parser filter parses WAV-format audio data from .wav, .au, or .aif files.</span></span> <span data-ttu-id="f33de-105">Le filtre amont doit être le filtre de [source de fichier Async](file-source--async--filter.md) , le filtre de [source du fichier d’URL](file-source--url--filter.md) ou un filtre de source asynchrone tiers compatible qui contient les données audio WAV.</span><span class="sxs-lookup"><span data-stu-id="f33de-105">The upstream filter must be the [Async File Source](file-source--async--filter.md) filter, [URL File Source](file-source--url--filter.md) filter, or a compatible third-party asynchronous source filter that contains WAV audio data.</span></span> <span data-ttu-id="f33de-106">Le flux de sortie est données audio, que vous pouvez connecter directement à un filtre de rendu audio ou à un filtre de transformation audio intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="f33de-106">The output stream is audio data, which you can connect directly to an audio rendering filter or to an intervening audio transform filter.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f33de-107">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="f33de-107">Filter Interfaces</span></span></td>
<td><span data-ttu-id="f33de-108"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a></span><span class="sxs-lookup"><span data-stu-id="f33de-108"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f33de-109">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="f33de-109">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="f33de-110">Type majeur : MEDIATYPE_StreamThe sous-types suivants sont valides :</span><span class="sxs-lookup"><span data-stu-id="f33de-110">Major type: MEDIATYPE_StreamThe following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="f33de-111">MEDIASUBTYPE_AIFF</span><span class="sxs-lookup"><span data-stu-id="f33de-111">MEDIASUBTYPE_AIFF</span></span></li>
<li><span data-ttu-id="f33de-112">MEDIASUBTYPE_AU</span><span class="sxs-lookup"><span data-stu-id="f33de-112">MEDIASUBTYPE_AU</span></span></li>
<li><span data-ttu-id="f33de-113">MEDIASUBTYPE_WAVE</span><span class="sxs-lookup"><span data-stu-id="f33de-113">MEDIASUBTYPE_WAVE</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f33de-114">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="f33de-114">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="f33de-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="f33de-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f33de-116">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="f33de-116">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="f33de-117">Type majeur : MEDIATYPE_AudioSubtype : MEDIASUBTYPE_PCM ou un autre type de compression.</span><span class="sxs-lookup"><span data-stu-id="f33de-117">Major type: MEDIATYPE_AudioSubtype: MEDIASUBTYPE_PCM or other compression type.</span></span> <span data-ttu-id="f33de-118">(Voir <a href="audio-subtypes.md"><strong>sous-types audio</strong></a>.)</span><span class="sxs-lookup"><span data-stu-id="f33de-118">(See <a href="audio-subtypes.md"><strong>Audio Subtypes</strong></a>.)</span></span><br/> <span data-ttu-id="f33de-119">Type de format : FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="f33de-119">Format type: FORMAT_WaveFormatEx</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f33de-120">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="f33de-120">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="f33de-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="f33de-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f33de-122">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="f33de-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="f33de-123">{D51BD5A1-7548-11cf-A520-0080C77EF58A}</span><span class="sxs-lookup"><span data-stu-id="f33de-123">{D51BD5A1-7548-11cf-A520-0080C77EF58A}</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f33de-124">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="f33de-124">Property Page CLSID</span></span></td>
<td><span data-ttu-id="f33de-125">Aucune page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="f33de-125">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f33de-126">Exécutable</span><span class="sxs-lookup"><span data-stu-id="f33de-126">Executable</span></span></td>
<td><span data-ttu-id="f33de-127">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="f33de-127">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f33de-128"><a href="merit.md">Mérite</a></span><span class="sxs-lookup"><span data-stu-id="f33de-128"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="f33de-129">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="f33de-129">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f33de-130"><a href="filter-categories.md">Catégorie de filtre</a></span><span class="sxs-lookup"><span data-stu-id="f33de-130"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="f33de-131">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="f33de-131">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="f33de-132">Notes</span><span class="sxs-lookup"><span data-stu-id="f33de-132">Remarks</span></span>

<span data-ttu-id="f33de-133">Ce filtre prend en charge les types de fichiers suivants :</span><span class="sxs-lookup"><span data-stu-id="f33de-133">This filter supports the following file types:</span></span>

-   <span data-ttu-id="f33de-134">VAGUE (. wav)</span><span class="sxs-lookup"><span data-stu-id="f33de-134">WAVE (.wav)</span></span>
-   <span data-ttu-id="f33de-135">AIFF et AIFF-C (. AIF)</span><span class="sxs-lookup"><span data-stu-id="f33de-135">AIFF and AIFF-C (.aif)</span></span>
-   <span data-ttu-id="f33de-136">Au (. au)</span><span class="sxs-lookup"><span data-stu-id="f33de-136">AU (.au)</span></span>

<span data-ttu-id="f33de-137">Toutefois, il présente les limitations suivantes au format audio :</span><span class="sxs-lookup"><span data-stu-id="f33de-137">However, it has the following limitations on the audio format:</span></span>

-   <span data-ttu-id="f33de-138">L’audio doit être un PCM linéaire 8 bits ou 16 bits.</span><span class="sxs-lookup"><span data-stu-id="f33de-138">The audio must be 8-bit or 16-bit linear PCM.</span></span>
-   <span data-ttu-id="f33de-139">Pour les fichiers AIFF-C, l’audio doit être décompressé, dans l’ordre de primauté des octets de poids fort (type de compression « aucun »).</span><span class="sxs-lookup"><span data-stu-id="f33de-139">For AIFF-C files, the audio must be uncompressed, in big-endian byte order (compression type 'NONE').</span></span>

## <a name="related-topics"></a><span data-ttu-id="f33de-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f33de-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f33de-141">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="f33de-141">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




