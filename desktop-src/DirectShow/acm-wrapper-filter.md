---
description: Filtre de wrappers ACM
ms.assetid: f3cd8e90-8949-482a-8ada-47711f6c935f
title: Filtre de wrappers ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da0c1283ac6d4980f51d40001b38c719f5e31c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516357"
---
# <a name="acm-wrapper-filter"></a><span data-ttu-id="36eb6-103">Filtre de wrappers ACM</span><span class="sxs-lookup"><span data-stu-id="36eb6-103">ACM Wrapper Filter</span></span>

<span data-ttu-id="36eb6-104">Le filtre de wrapper ACM permet aux codecs du gestionnaire de compression audio (ACM) de joindre un graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="36eb6-104">The ACM Wrapper filter enables Audio Compression Manager (ACM) codecs to join a filter graph.</span></span> <span data-ttu-id="36eb6-105">Il peut agir soit comme filtre de décompression, soit comme filtre de compression.</span><span class="sxs-lookup"><span data-stu-id="36eb6-105">It can act either as a decompression filter or as a compression filter.</span></span>

<span data-ttu-id="36eb6-106">En tant que filtre de décompression, le wrapper ACM apparaît dans la catégorie « filtres DirectShow » (CLSID \_ LegacyAmFilterCategory) et a un mérite de mérite \_ normal.</span><span class="sxs-lookup"><span data-stu-id="36eb6-106">As a decompression filter, the ACM Wrapper appears in the "DirectShow Filters" category (CLSID\_LegacyAmFilterCategory) and has a merit of MERIT\_NORMAL.</span></span> <span data-ttu-id="36eb6-107">Le type de support de connexion sur la broche d’entrée détermine le codec utilisé par le filtre.</span><span class="sxs-lookup"><span data-stu-id="36eb6-107">The connection media type on the input pin determines which codec the filter uses.</span></span> <span data-ttu-id="36eb6-108">En règle générale, l’application n’a pas besoin d’ajouter le filtre au graphique de filtre ; elle est automatiquement extraite par le gestionnaire de graphique de filtre, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="36eb6-108">Typically, the application does not need to add the filter to the filter graph; it is pulled in automatically by the Filter Graph Manager when needed.</span></span> <span data-ttu-id="36eb6-109">La décompression concerne uniquement les signaux audio PCM.</span><span class="sxs-lookup"><span data-stu-id="36eb6-109">Decompression is only to PCM audio.</span></span>

<span data-ttu-id="36eb6-110">En tant que filtre de compression, le wrapper ACM apparaît dans la catégorie « compresseurs audio » (CLSID \_ AudioCompressorCategory) et a un mérite de mérite \_ n' \_ \_ utilise pas.</span><span class="sxs-lookup"><span data-stu-id="36eb6-110">As a compression filter, the ACM Wrapper appears in the "Audio Compressors" category (CLSID\_AudioCompressorCategory) and has a merit of MERIT\_DO\_NOT\_USE.</span></span> <span data-ttu-id="36eb6-111">Chaque codec s’affiche sous la forme d’une instance distincte.</span><span class="sxs-lookup"><span data-stu-id="36eb6-111">Each codec appears as a separate instance.</span></span> <span data-ttu-id="36eb6-112">Pour la compression, vous ne pouvez pas créer directement le filtre avec CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="36eb6-112">For compression, you cannot directly create the filter with CoCreateInstance.</span></span> <span data-ttu-id="36eb6-113">Au lieu de cela, vous devez utiliser l’énumérateur du périphérique système.</span><span class="sxs-lookup"><span data-stu-id="36eb6-113">Instead, you must use the system device enumerator.</span></span> <span data-ttu-id="36eb6-114">Pour plus d’informations, consultez [utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="36eb6-114">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36eb6-115">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="36eb6-115">Filter interfaces</span></span></td>
<td><span data-ttu-id="36eb6-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, IPersist, IPersistPropertyBag</span><span class="sxs-lookup"><span data-stu-id="36eb6-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, IPersist, IPersistPropertyBag</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36eb6-117">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="36eb6-117">Input pin media types</span></span></td>
<td><span data-ttu-id="36eb6-118">MEDIATYPE_Audio, MEDIASUBTYPE_NULL FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="36eb6-118">MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36eb6-119">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="36eb6-119">Input pin interfaces</span></span></td>
<td><span data-ttu-id="36eb6-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="36eb6-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36eb6-121">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="36eb6-121">Output pin media types</span></span></td>
<td><span data-ttu-id="36eb6-122">MEDIATYPE_Audio, MEDIASUBTYPE_PCM FORMAT_WaveFormatEx. les combinaisons suivantes sont possibles :</span><span class="sxs-lookup"><span data-stu-id="36eb6-122">MEDIATYPE_Audio, MEDIASUBTYPE_PCM, FORMAT_WaveFormatEx.Any combination of the following are possible:</span></span><br/>
<ul>
<li><span data-ttu-id="36eb6-123">Échantillons par seconde (kHz) : 44,1, 22,05, 11,025 ou 8,0.</span><span class="sxs-lookup"><span data-stu-id="36eb6-123">Samples per second (kHz): 44.1, 22.05, 11.025, or 8.0.</span></span></li>
<li><span data-ttu-id="36eb6-124">Canaux : stéréo ou mono.</span><span class="sxs-lookup"><span data-stu-id="36eb6-124">Channels: Stereo or mono.</span></span></li>
<li><span data-ttu-id="36eb6-125">Bits par échantillon : 8 ou 16.</span><span class="sxs-lookup"><span data-stu-id="36eb6-125">Bits per sample: 8 or 16.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36eb6-126">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="36eb6-126">Output pin interfaces</span></span></td>
<td><span data-ttu-id="36eb6-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="36eb6-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36eb6-128">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="36eb6-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="36eb6-129">CLSID_ACMWrapper</span><span class="sxs-lookup"><span data-stu-id="36eb6-129">CLSID_ACMWrapper</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36eb6-130">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="36eb6-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="36eb6-131">Aucune page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="36eb6-131">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36eb6-132">Exécutable</span><span class="sxs-lookup"><span data-stu-id="36eb6-132">Executable</span></span></td>
<td><span data-ttu-id="36eb6-133">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="36eb6-133">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36eb6-134"><a href="merit.md">Mérite</a></span><span class="sxs-lookup"><span data-stu-id="36eb6-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="36eb6-135">MERIT_NORMAL ou MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="36eb6-135">MERIT_NORMAL or MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36eb6-136"><a href="filter-categories.md">Catégorie de filtre</a></span><span class="sxs-lookup"><span data-stu-id="36eb6-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="36eb6-137">CLSID_LegacyAmFilterCategory ou CLSID_AudioCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="36eb6-137">CLSID_LegacyAmFilterCategory or CLSID_AudioCompressorCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="36eb6-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="36eb6-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36eb6-139">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="36eb6-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




