---
description: Filtre de décompresseur QT
ms.assetid: d013075f-deab-40ef-8438-4fb09820da3e
title: Filtre de décompresseur QT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e586eb9d65ee00509f4a434f3283bd762d535b26
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481473"
---
# <a name="qt-decompressor-filter"></a><span data-ttu-id="0db5d-103">Filtre de décompresseur QT</span><span class="sxs-lookup"><span data-stu-id="0db5d-103">QT Decompressor Filter</span></span>

<span data-ttu-id="0db5d-104">Ce composant a été supprimé de Windows Vista et des systèmes d’exploitation ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="0db5d-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="0db5d-105">Il peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0db5d-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="0db5d-106">Le filtre de décompresseur QT décompresse la vidéo Apple® QuickTime® 2,0.</span><span class="sxs-lookup"><span data-stu-id="0db5d-106">The QT Decompressor filter decompresses Apple® QuickTime® 2.0 video.</span></span> <span data-ttu-id="0db5d-107">Ce format est généralement utilisé dans les anciens fichiers QuickTime.</span><span class="sxs-lookup"><span data-stu-id="0db5d-107">This format is typically used in older QuickTime files.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0db5d-108">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="0db5d-108">Filter Interfaces</span></span></td>
<td><span data-ttu-id="0db5d-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="0db5d-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0db5d-110">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="0db5d-110">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="0db5d-111">MEDIATYPE_Video, FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="0db5d-111">MEDIATYPE_Video, FORMAT_VideoInfo</span></span><br/> <span data-ttu-id="0db5d-112">Les sous-types suivants sont valides :</span><span class="sxs-lookup"><span data-stu-id="0db5d-112">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="0db5d-113">MEDIASUBTYPE_QTRpza</span><span class="sxs-lookup"><span data-stu-id="0db5d-113">MEDIASUBTYPE_QTRpza</span></span></li>
<li><span data-ttu-id="0db5d-114">MEDIASUBTYPE_QTSmc</span><span class="sxs-lookup"><span data-stu-id="0db5d-114">MEDIASUBTYPE_QTSmc</span></span></li>
<li><span data-ttu-id="0db5d-115">MEDIASUBTYPE_QTRle</span><span class="sxs-lookup"><span data-stu-id="0db5d-115">MEDIASUBTYPE_QTRle</span></span></li>
<li><span data-ttu-id="0db5d-116">MEDIASUBTYPE_QTJpeg</span><span class="sxs-lookup"><span data-stu-id="0db5d-116">MEDIASUBTYPE_QTJpeg</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0db5d-117">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="0db5d-117">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="0db5d-118"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="0db5d-118"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0db5d-119">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="0db5d-119">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="0db5d-120">MEDIATYPE_Video, MEDIASUBTYPE_NULL FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="0db5d-120">MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0db5d-121">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="0db5d-121">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="0db5d-122"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="0db5d-122"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0db5d-123">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="0db5d-123">Filter CLSID</span></span></td>
<td><span data-ttu-id="0db5d-124">CLSID_QTDec</span><span class="sxs-lookup"><span data-stu-id="0db5d-124">CLSID_QTDec</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0db5d-125">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="0db5d-125">Property Page CLSID</span></span></td>
<td><span data-ttu-id="0db5d-126">Aucune page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="0db5d-126">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0db5d-127">Exécutable</span><span class="sxs-lookup"><span data-stu-id="0db5d-127">Executable</span></span></td>
<td><span data-ttu-id="0db5d-128">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="0db5d-128">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0db5d-129"><a href="merit.md">Mérite</a></span><span class="sxs-lookup"><span data-stu-id="0db5d-129"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="0db5d-130">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="0db5d-130">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0db5d-131"><a href="filter-categories.md">Catégorie de filtre</a></span><span class="sxs-lookup"><span data-stu-id="0db5d-131"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="0db5d-132">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="0db5d-132">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="0db5d-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0db5d-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0db5d-134">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="0db5d-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




