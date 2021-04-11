---
description: Filtre de l’analyseur de film QuickTime
ms.assetid: 9537dd7b-9aeb-4e73-a31d-86053874ef13
title: Filtre de l’analyseur de film QuickTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a046e143487a1455aeeb125910bbf4452b4f947
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317757"
---
# <a name="quicktime-movie-parser-filter"></a><span data-ttu-id="b809f-103">Filtre de l’analyseur de film QuickTime</span><span class="sxs-lookup"><span data-stu-id="b809f-103">QuickTime Movie Parser Filter</span></span>

<span data-ttu-id="b809f-104">Ce composant a été supprimé de Windows Vista et des systèmes d’exploitation ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="b809f-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="b809f-105">Il peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b809f-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="b809f-106">Le filtre de l’analyseur de film QuickTime fractionne les données Apple® QuickTime® en flux audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="b809f-106">The QuickTime Movie Parser filter splits Apple® QuickTime® data into audio and video streams.</span></span> <span data-ttu-id="b809f-107">Il prend en charge QuickTime 2,0 et versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="b809f-107">It supports QuickTime 2.0 and earlier.</span></span> <span data-ttu-id="b809f-108">La broche d’entrée se connecte à un filtre source, tel que le filtre de [source de fichier Async](file-source--async--filter.md) ou le filtre de [source du fichier d’URL](file-source--url--filter.md) .</span><span class="sxs-lookup"><span data-stu-id="b809f-108">The input pin connects to a source filter such as the [Async File Source](file-source--async--filter.md) filter or the [URL File Source](file-source--url--filter.md) filter.</span></span> <span data-ttu-id="b809f-109">L’analyseur utilise le filtre de [décompresseur AVI](avi-decompressor-filter.md) ou [QT](qt-decompressor-filter.md) pour décompresser les fichiers QuickTime.</span><span class="sxs-lookup"><span data-stu-id="b809f-109">The Parser uses the [AVI Decompressor](avi-decompressor-filter.md) or [QT Decompressor](qt-decompressor-filter.md) filter to decompress QuickTime files.</span></span> <span data-ttu-id="b809f-110">Le filtre crée une broche de sortie pour le flux vidéo et une broche de sortie pour le flux audio.</span><span class="sxs-lookup"><span data-stu-id="b809f-110">The filter creates one output pin for the video stream and one output pin for the audio stream.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b809f-111">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="b809f-111">Filter Interfaces</span></span></td>
<td><span data-ttu-id="b809f-112"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="b809f-112"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b809f-113">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="b809f-113">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="b809f-114">MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie ;</span><span class="sxs-lookup"><span data-stu-id="b809f-114">MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b809f-115">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="b809f-115">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="b809f-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="b809f-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b809f-117">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="b809f-117">Output Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="b809f-118">MEDIATYPE_Video, MEDIASUBTYPE_NULL FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="b809f-118">MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</span></span></li>
<li><span data-ttu-id="b809f-119">MEDIATYPE_Audio, MEDIASUBTYPE_NULL FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="b809f-119">MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b809f-120">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="b809f-120">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="b809f-121"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="b809f-121"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b809f-122">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="b809f-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="b809f-123">CLSID_QuickTimeParser</span><span class="sxs-lookup"><span data-stu-id="b809f-123">CLSID_QuickTimeParser</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b809f-124">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="b809f-124">Property Page CLSID</span></span></td>
<td><span data-ttu-id="b809f-125">Aucune page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="b809f-125">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b809f-126">Exécutable</span><span class="sxs-lookup"><span data-stu-id="b809f-126">Executable</span></span></td>
<td><span data-ttu-id="b809f-127">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="b809f-127">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b809f-128"><a href="merit.md">Mérite</a></span><span class="sxs-lookup"><span data-stu-id="b809f-128"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="b809f-129">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="b809f-129">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b809f-130"><a href="filter-categories.md">Catégorie de filtre</a></span><span class="sxs-lookup"><span data-stu-id="b809f-130"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="b809f-131">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="b809f-131">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="b809f-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b809f-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b809f-133">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="b809f-133">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



