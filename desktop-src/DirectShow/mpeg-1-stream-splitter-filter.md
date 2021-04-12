---
description: Filtre de fractionnement de flux MPEG-1
ms.assetid: abadf37f-2876-496d-90e7-77c3475a0064
title: Filtre de fractionnement de flux MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec47e5ad8df16446c588beec2c5d1c2606b9b1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109647"
---
# <a name="mpeg-1-stream-splitter-filter"></a><span data-ttu-id="90cab-103">Filtre de fractionnement de flux MPEG-1</span><span class="sxs-lookup"><span data-stu-id="90cab-103">MPEG-1 Stream Splitter Filter</span></span>

<span data-ttu-id="90cab-104">Ce filtre fractionne un flux système MPEG-1 en flux audio et vidéo de composant.</span><span class="sxs-lookup"><span data-stu-id="90cab-104">This filter splits an MPEG-1 system stream into its component audio and video streams.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="90cab-105">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="90cab-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="90cab-106"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="90cab-106"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90cab-107">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="90cab-107">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="90cab-108">Type majeur : MEDIATYPE_Stream</span><span class="sxs-lookup"><span data-stu-id="90cab-108">Major type: MEDIATYPE_Stream</span></span><br/> <span data-ttu-id="90cab-109">Sous-types</span><span class="sxs-lookup"><span data-stu-id="90cab-109">Subtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="90cab-110">MEDIASUBTYPE_MPEG1System</span><span class="sxs-lookup"><span data-stu-id="90cab-110">MEDIASUBTYPE_MPEG1System</span></span></li>
<li><span data-ttu-id="90cab-111">MEDIASUBTYPE_MPEG1VideoCD</span><span class="sxs-lookup"><span data-stu-id="90cab-111">MEDIASUBTYPE_MPEG1VideoCD</span></span></li>
<li><span data-ttu-id="90cab-112">MEDIASUBTYPE_Audio</span><span class="sxs-lookup"><span data-stu-id="90cab-112">MEDIASUBTYPE_Audio</span></span></li>
<li><span data-ttu-id="90cab-113">MEDIASUBTYPE_Video</span><span class="sxs-lookup"><span data-stu-id="90cab-113">MEDIASUBTYPE_Video</span></span></li>
</ul>
<span data-ttu-id="90cab-114">Voir <a href="mpeg-1-media-types.md"> <strong>types de média MPEG-1</strong></a></span><span class="sxs-lookup"><span data-stu-id="90cab-114">See <a href="mpeg-1-media-types.md"><strong>MPEG-1 Media Types</strong></a></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90cab-115">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="90cab-115">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="90cab-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="90cab-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90cab-117">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="90cab-117">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="90cab-118">Type principal : MEDIATYPE_Audio ou MEDIATYPE_Video</span><span class="sxs-lookup"><span data-stu-id="90cab-118">Major type: MEDIATYPE_Audio or MEDIATYPE_Video</span></span><br/> <span data-ttu-id="90cab-119">Sous-type : MEDIASUBTYPE_MPEG1Payload ou MEDIASUBTYPE_MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="90cab-119">Subtype: MEDIASUBTYPE_MPEG1Payload or MEDIASUBTYPE_MPEG1Packet</span></span><br/> <span data-ttu-id="90cab-120">Voir <a href="mpeg-1-media-types.md"> <strong>types de média MPEG-1</strong></a></span><span class="sxs-lookup"><span data-stu-id="90cab-120">See <a href="mpeg-1-media-types.md"><strong>MPEG-1 Media Types</strong></a></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90cab-121">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="90cab-121">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="90cab-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="90cab-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90cab-123">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="90cab-123">Filter CLSID</span></span></td>
<td><span data-ttu-id="90cab-124">CLSID_MPEG1Splitter</span><span class="sxs-lookup"><span data-stu-id="90cab-124">CLSID_MPEG1Splitter</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90cab-125">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="90cab-125">Property Page CLSID</span></span></td>
<td><span data-ttu-id="90cab-126">Aucune page de propriétés</span><span class="sxs-lookup"><span data-stu-id="90cab-126">No property page</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90cab-127">Exécutable</span><span class="sxs-lookup"><span data-stu-id="90cab-127">Executable</span></span></td>
<td><span data-ttu-id="90cab-128">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="90cab-128">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90cab-129"><a href="merit.md">Mérite</a></span><span class="sxs-lookup"><span data-stu-id="90cab-129"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="90cab-130">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="90cab-130">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90cab-131"><a href="filter-categories.md">Catégorie de filtre</a></span><span class="sxs-lookup"><span data-stu-id="90cab-131"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="90cab-132">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="90cab-132">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="90cab-133">Notes</span><span class="sxs-lookup"><span data-stu-id="90cab-133">Remarks</span></span>

<span data-ttu-id="90cab-134">Ce fichier prend en charge le mode par extraction via [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) uniquement. elle ne prend pas en charge le mode push.</span><span class="sxs-lookup"><span data-stu-id="90cab-134">This file supports pull mode via [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) only; it does not support push mode.</span></span>

<span data-ttu-id="90cab-135">Étant donné que le contenu MPEG-1 n’est pas indexé, la recherche peut être très approximative.</span><span class="sxs-lookup"><span data-stu-id="90cab-135">Because MPEG-1 content is not indexed, seeking can be very approximate.</span></span> <span data-ttu-id="90cab-136">Il est généralement bon pour un flux de système MPEG-1 à débit binaire fixe (généralement généré par le matériel pour CD vidéo).</span><span class="sxs-lookup"><span data-stu-id="90cab-136">It is usually good for a fixed bitrate MPEG-1 system stream (which is usually hardware generated for video CD).</span></span>

<span data-ttu-id="90cab-137">Le filtre prend en charge l’interface [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) pour la récupération des métadonnées ID3.</span><span class="sxs-lookup"><span data-stu-id="90cab-137">The filter supports the [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) interface for retrieving ID3 metadata.</span></span>

<span data-ttu-id="90cab-138">Tous les exemples MPEG n’ont pas de datage.</span><span class="sxs-lookup"><span data-stu-id="90cab-138">Not all MPEG samples have time stamps.</span></span> <span data-ttu-id="90cab-139">L’absence d’horodatage sur un échantillon MPEG n’est pas une erreur.</span><span class="sxs-lookup"><span data-stu-id="90cab-139">The lack of a time stamp on an MPEG sample is not an error.</span></span> <span data-ttu-id="90cab-140">Pour les développeurs de filtre, cela signifie que vous ne devez pas retourner de code d’erreur à partir de la méthode **Receive** de votre code confidentiel d’entrée si [**IMediaSample :: getTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) échoue.</span><span class="sxs-lookup"><span data-stu-id="90cab-140">For filter developers, this means that you should not return an error code from your input pin's **Receive** method if [**IMediaSample::GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) fails.</span></span> <span data-ttu-id="90cab-141">Si **Receive** retourne une valeur autre que S \_ OK, le séparateur va arrêter l’envoi d’exemples.</span><span class="sxs-lookup"><span data-stu-id="90cab-141">If **Receive** returns any value other than S\_OK, it will cause the splitter to stop sending samples.</span></span>

<span data-ttu-id="90cab-142">Si le fichier contient un flux vidéo, le séparateur de flux MPEG-1 prend en charge la recherche par numéro de frame.</span><span class="sxs-lookup"><span data-stu-id="90cab-142">If the file contains a video stream, the MPEG-1 Stream Splitter supports seeking by frame number.</span></span> <span data-ttu-id="90cab-143">Pour activer la recherche basée sur des frames, appelez [**IMediaSeeking :: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) sur le [Gestionnaire de graphique de filtre](filter-graph-manager.md) avec le **\_ \_ cadre de format d’heure** de valeur.</span><span class="sxs-lookup"><span data-stu-id="90cab-143">To enable frame-based seeking, call [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the [Filter Graph Manager](filter-graph-manager.md) with the value **TIME\_FORMAT\_FRAME**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90cab-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="90cab-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90cab-145">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="90cab-145">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




