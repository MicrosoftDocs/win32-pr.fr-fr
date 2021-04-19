---
description: Ce filtre démultiplexe les flux de transport MPEG-2 et les flux de programme qui sont fournis en mode push.
ms.assetid: 99bfc55d-6519-4e85-98ce-cad27bd71ffb
title: Démultiplexeur MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ea71727dc273bd0dc5d65ac49b28385b4898067
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106544548"
---
# <a name="mpeg-2-demultiplexer"></a><span data-ttu-id="f2b71-103">Démultiplexeur MPEG-2</span><span class="sxs-lookup"><span data-stu-id="f2b71-103">MPEG-2 Demultiplexer</span></span>

<span data-ttu-id="f2b71-104">Ce filtre démultiplexe les flux de transport MPEG-2 et les flux de programme qui sont fournis en mode push.</span><span class="sxs-lookup"><span data-stu-id="f2b71-104">This filter demultiplexes MPEG-2 transport and program streams that are delivered in push-mode.</span></span> <span data-ttu-id="f2b71-105">À partir de Windows XP, ce filtre prend également en charge les flux de programme en mode par extraction (lecture de fichier).</span><span class="sxs-lookup"><span data-stu-id="f2b71-105">Starting in Windows XP, this filter also supports program streams in pull mode (file playback).</span></span> <span data-ttu-id="f2b71-106">Sur les plateformes antérieures, utilisez le filtre de [séparateur MPEG-2](mpeg-2-splitter.md) pour les flux de programme en mode par extraction.</span><span class="sxs-lookup"><span data-stu-id="f2b71-106">On earlier platforms, use the [MPEG-2 Splitter](mpeg-2-splitter.md) filter for program streams in pull mode.</span></span> <span data-ttu-id="f2b71-107">Ce filtre peut être utilisé dans n’importe quel type de graphique de filtre, y compris un graphique de filtre TV numérique BDA.</span><span class="sxs-lookup"><span data-stu-id="f2b71-107">This filter can be used in any type of filter graph, including a BDA digital TV filter graph.</span></span>

> [!Note]  
> <span data-ttu-id="f2b71-108">Le démultiplexeur MPEG-2 ne prend pas en charge la recherche avec précision de trame.</span><span class="sxs-lookup"><span data-stu-id="f2b71-108">The MPEG-2 Demultiplexer does not support frame-accurate seeking.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f2b71-109">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="f2b71-109">Filter Interfaces</span></span></td>
<td><span data-ttu-id="f2b71-110">Tous les modes :</span><span class="sxs-lookup"><span data-stu-id="f2b71-110">All modes:</span></span><br/>
<ul>
<li><span data-ttu-id="f2b71-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="f2b71-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="f2b71-112"><strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="f2b71-112"><strong>ISpecifyPropertyPages</strong></span></span></li>
</ul>
<span data-ttu-id="f2b71-113">Mode push uniquement :</span><span class="sxs-lookup"><span data-stu-id="f2b71-113">Push mode only:</span></span><br/>
<ul>
<li><span data-ttu-id="f2b71-114"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span><span class="sxs-lookup"><span data-stu-id="f2b71-114"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span></span></li>
<li><span data-ttu-id="f2b71-115"><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></span><span class="sxs-lookup"><span data-stu-id="f2b71-115"><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></span></span></li>
<li><span data-ttu-id="f2b71-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span><span class="sxs-lookup"><span data-stu-id="f2b71-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f2b71-117">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="f2b71-117">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="f2b71-118">Type majeur : MEDIATYPE_STREAM</span><span class="sxs-lookup"><span data-stu-id="f2b71-118">Major type: MEDIATYPE_STREAM</span></span><br/> <span data-ttu-id="f2b71-119">Sous-type</span><span class="sxs-lookup"><span data-stu-id="f2b71-119">Subtype:</span></span><br/>
<ul>
<li><span data-ttu-id="f2b71-120">KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</span><span class="sxs-lookup"><span data-stu-id="f2b71-120">KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</span></span></li>
<li><span data-ttu-id="f2b71-121">MEDIASUBTYPE_MPEG2_PROGRAM</span><span class="sxs-lookup"><span data-stu-id="f2b71-121">MEDIASUBTYPE_MPEG2_PROGRAM</span></span></li>
<li><span data-ttu-id="f2b71-122">MEDIASUBTYPE_MPEG2_TRANSPORT</span><span class="sxs-lookup"><span data-stu-id="f2b71-122">MEDIASUBTYPE_MPEG2_TRANSPORT</span></span></li>
<li><span data-ttu-id="f2b71-123">MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</span><span class="sxs-lookup"><span data-stu-id="f2b71-123">MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</span></span></li>
</ul>
<span data-ttu-id="f2b71-124">Pour plus d’informations, consultez <a href="mpeg-2-demultiplexer-media-types.md"><strong>types de média MPEG-2 DEMULTIPLEXEUR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f2b71-124">For more information, see <a href="mpeg-2-demultiplexer-media-types.md"><strong>MPEG-2 Demultiplexer Media Types</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f2b71-125">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="f2b71-125">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="f2b71-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="f2b71-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f2b71-127">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="f2b71-127">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="f2b71-128">Les flux élémentaires audio et vidéo doivent avoir un type MEDIATYPE_Audio ou MEDIATYPE_Video principal.</span><span class="sxs-lookup"><span data-stu-id="f2b71-128">Audio and video elementary streams must have a major type of MEDIATYPE_Audio or MEDIATYPE_Video.</span></span><br/> <span data-ttu-id="f2b71-129">Pour plus d’informations, consultez <a href="mpeg-2-demultiplexer-media-types.md"><strong>types de média MPEG-2 DEMULTIPLEXEUR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f2b71-129">For more information, see <a href="mpeg-2-demultiplexer-media-types.md"><strong>MPEG-2 Demultiplexer Media Types</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f2b71-130">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="f2b71-130">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="f2b71-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>mode Push uniquement : <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>IAMPushSource</strong></a>, <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a></span><span class="sxs-lookup"><span data-stu-id="f2b71-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>Push mode only: <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>IAMPushSource</strong></a>, <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a></span></span><br/> <span data-ttu-id="f2b71-132">Mode par extraction uniquement : <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="f2b71-132">Pull mode only: <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f2b71-133">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="f2b71-133">Filter CLSID</span></span></td>
<td><span data-ttu-id="f2b71-134">CLSID_MPEG2Demultiplexer</span><span class="sxs-lookup"><span data-stu-id="f2b71-134">CLSID_MPEG2Demultiplexer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f2b71-135">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="f2b71-135">Property Page CLSID</span></span></td>
<td><span data-ttu-id="f2b71-136">Disponible à des fins de test uniquement.</span><span class="sxs-lookup"><span data-stu-id="f2b71-136">Available for testing only.</span></span> <span data-ttu-id="f2b71-137">Utiliser l’interface <strong>ISpecifyPropertyPages</strong> pour accéder aux pages de propriétés</span><span class="sxs-lookup"><span data-stu-id="f2b71-137">Use the <strong>ISpecifyPropertyPages</strong> interface to access the property pages</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f2b71-138">Exécutable</span><span class="sxs-lookup"><span data-stu-id="f2b71-138">Executable</span></span></td>
<td><span data-ttu-id="f2b71-139">mpg2splt.ax</span><span class="sxs-lookup"><span data-stu-id="f2b71-139">mpg2splt.ax</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f2b71-140"><a href="merit.md">Mérite</a></span><span class="sxs-lookup"><span data-stu-id="f2b71-140"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="f2b71-141">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="f2b71-141">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f2b71-142"><a href="filter-categories.md">Catégorie de filtre</a></span><span class="sxs-lookup"><span data-stu-id="f2b71-142"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="f2b71-143">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="f2b71-143">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="f2b71-144">Notes</span><span class="sxs-lookup"><span data-stu-id="f2b71-144">Remarks</span></span>

<span data-ttu-id="f2b71-145">Pour sortir des flux de données audio et vidéo élémentaires, le demux doit recevoir les flux PCR et SCR.</span><span class="sxs-lookup"><span data-stu-id="f2b71-145">To output audio and video elementary streams, the demux must receive the PCR and SCR streams.</span></span> <span data-ttu-id="f2b71-146">Du côté de l’entrée, cela signifie qu’un flux de transport doit contenir les tables PAT et VPM qui définissent le PID du flux PCR. et les flux de programme doivent contenir au moins un en-tête pack.</span><span class="sxs-lookup"><span data-stu-id="f2b71-146">On the input side, this means a transport stream must contain the PAT and PMT tables that define the PID for the PCR stream; and program streams must contain at least one pack header.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2b71-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2b71-147">Requirements</span></span>



| <span data-ttu-id="f2b71-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2b71-148">Requirement</span></span> | <span data-ttu-id="f2b71-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2b71-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f2b71-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2b71-150">Minimum supported client</span></span><br/> | <span data-ttu-id="f2b71-151">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2b71-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f2b71-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2b71-152">Minimum supported server</span></span><br/> | <span data-ttu-id="f2b71-153">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2b71-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f2b71-154">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="f2b71-154">End of server support</span></span><br/>    | <span data-ttu-id="f2b71-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f2b71-155">Windows Server 2003 R2</span></span><br/>                          |



## <a name="see-also"></a><span data-ttu-id="f2b71-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2b71-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2b71-157">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="f2b71-157">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="f2b71-158">Utilisation du démultiplexeur MPEG-2</span><span class="sxs-lookup"><span data-stu-id="f2b71-158">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 




