---
description: Séparateur MPEG-2
ms.assetid: 06704a5a-e7ae-4187-ae36-32512d951aaf
title: Séparateur MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0f04062660df7711a573dd17deb82f90897454a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200797"
---
# <a name="mpeg-2-splitter"></a><span data-ttu-id="35305-103">Séparateur MPEG-2</span><span class="sxs-lookup"><span data-stu-id="35305-103">MPEG-2 Splitter</span></span>

<span data-ttu-id="35305-104">À compter de Microsoft® Windows® XP, le filtre de séparateur MPEG-2 est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="35305-104">Starting in Microsoft® Windows® XP, the MPEG-2 Splitter filter is deprecated.</span></span> <span data-ttu-id="35305-105">Utilisez plutôt le [démultiplexeur MPEG-2](mpeg-2-demultiplexer.md) .</span><span class="sxs-lookup"><span data-stu-id="35305-105">Use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) instead.</span></span>

<span data-ttu-id="35305-106">Sur les plateformes antérieures, utilisez le séparateur MPEG-2 pour les flux de programme MPEG-2 fournis en mode par extraction qui contiennent au moins l’un des types de flux suivants : MPEG-2 Video ; Audio MPEG-2 ; AC3 audio codé comme défini pour la vidéo sur DVD ; ou le fichier audio PCM encodé comme défini pour la vidéo DVD.</span><span class="sxs-lookup"><span data-stu-id="35305-106">On earlier platforms, use the MPEG-2 Splitter for MPEG-2 program streams delivered in pull mode that contain at least one of the following stream types: MPEG-2 video; MPEG-2 audio; AC3 audio encoded as defined for DVD video; or PCM audio encoded as defined for DVD video.</span></span> <span data-ttu-id="35305-107">Ce filtre analyse les flux, crée une broche de sortie pour chaque flux et génère les paquets audio ou vidéo MPEG compressés dans un filtre de décodeur MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="35305-107">This filter parses the streams, creates an output pin for each stream, and outputs the compressed MPEG audio or video packets to an MPEG-2 decoder filter.</span></span>

<span data-ttu-id="35305-108">Pour les flux de programme et de transport remis en mode push, utilisez le [démultiplexeur MPEG-2](mpeg-2-demultiplexer.md), sur toutes les plateformes.</span><span class="sxs-lookup"><span data-stu-id="35305-108">For program and transport streams delivered in push-mode, use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md), on all platforms.</span></span>

> [!Note]  
> <span data-ttu-id="35305-109">Le séparateur MPEG-2 ne prend pas en charge la recherche avec une précision de trame.</span><span class="sxs-lookup"><span data-stu-id="35305-109">The MPEG-2 Splitter does not support frame-accurate seeking.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="35305-110">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="35305-110">Filter Interfaces</span></span></td>
<td><span data-ttu-id="35305-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong>, <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a></span><span class="sxs-lookup"><span data-stu-id="35305-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong>, <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35305-112">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="35305-112">Input Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="35305-113">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</span><span class="sxs-lookup"><span data-stu-id="35305-113">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</span></span></li>
<li><span data-ttu-id="35305-114">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</span><span class="sxs-lookup"><span data-stu-id="35305-114">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</span></span></li>
<li><span data-ttu-id="35305-115">MEDIATYPE_Stream, MEDIASUBTYPE_NULL</span><span class="sxs-lookup"><span data-stu-id="35305-115">MEDIATYPE_Stream, MEDIASUBTYPE_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35305-116">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="35305-116">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="35305-117"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="35305-117"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35305-118">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="35305-118">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="35305-119">Dépend du type de flux.</span><span class="sxs-lookup"><span data-stu-id="35305-119">Depends on the stream type.</span></span> <span data-ttu-id="35305-120">Voir <a href="mpeg-2-splitter-media-types.md">types de média MPEG-2 Splitter</a></span><span class="sxs-lookup"><span data-stu-id="35305-120">See <a href="mpeg-2-splitter-media-types.md">MPEG-2 Splitter Media Types</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35305-121">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="35305-121">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="35305-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="35305-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35305-123">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="35305-123">Filter CLSID</span></span></td>
<td><span data-ttu-id="35305-124">CLSID_MMSPLITTER</span><span class="sxs-lookup"><span data-stu-id="35305-124">CLSID_MMSPLITTER</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35305-125">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="35305-125">Property Page CLSID</span></span></td>
<td><span data-ttu-id="35305-126">Non applicable</span><span class="sxs-lookup"><span data-stu-id="35305-126">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35305-127">Exécutable</span><span class="sxs-lookup"><span data-stu-id="35305-127">Executable</span></span></td>
<td><span data-ttu-id="35305-128">mpg2splt.ax</span><span class="sxs-lookup"><span data-stu-id="35305-128">mpg2splt.ax</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35305-129"><a href="merit.md">Mérite</a></span><span class="sxs-lookup"><span data-stu-id="35305-129"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="35305-130">MERIT_NORMAL + 1</span><span class="sxs-lookup"><span data-stu-id="35305-130">MERIT_NORMAL + 1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35305-131"><a href="filter-categories.md">Catégorie de filtre</a></span><span class="sxs-lookup"><span data-stu-id="35305-131"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="35305-132">CLSID_AudioInputDeviceCategory</span><span class="sxs-lookup"><span data-stu-id="35305-132">CLSID_AudioInputDeviceCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="35305-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="35305-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35305-134">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="35305-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="35305-135">Utilisation du séparateur MPEG-2</span><span class="sxs-lookup"><span data-stu-id="35305-135">Using the MPEG-2 Splitter</span></span>](using-the-mpeg-2-splitter.md)
</dt> </dl>

 

 



