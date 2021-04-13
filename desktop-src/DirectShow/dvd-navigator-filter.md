---
description: Filtre de navigateur DVD
ms.assetid: 3b2c01a2-d52c-4497-8fc9-d1113e8507e8
title: Filtre de navigateur DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53bb1c6f46e3dd846ffccda32fece2c2f04c8992
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481856"
---
# <a name="dvd-navigator-filter"></a><span data-ttu-id="3023e-103">Filtre de navigateur DVD</span><span class="sxs-lookup"><span data-stu-id="3023e-103">DVD Navigator Filter</span></span>

<span data-ttu-id="3023e-104">Le filtre de navigateur DVD est le filtre source pour un graphique de filtre de lecture DVD-Video.</span><span class="sxs-lookup"><span data-stu-id="3023e-104">The DVD Navigator filter is the source filter for a DVD-Video playback filter graph.</span></span> <span data-ttu-id="3023e-105">Il ouvre tous les fichiers nécessaires dans un volume DVD-Video, parcourt les fichiers linéaires DVD-Video. VOB et analyse le flux de programme MPEG-2 résultant, en fractionnant le flux en trois broches de sortie (vidéo, audio, sous-image).</span><span class="sxs-lookup"><span data-stu-id="3023e-105">It opens all necessary files in a DVD-Video volume, navigates through the linear DVD-Video .vob files, and parses the resulting MPEG-2 program stream, splitting the stream into three (video, audio, subpicture) output pins.</span></span>

<span data-ttu-id="3023e-106">Le filtre de navigateur DVD implémente également les interfaces [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) et [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) qui permettent à une application de lecture de DVD de contrôler DVD-Video la lecture.</span><span class="sxs-lookup"><span data-stu-id="3023e-106">The DVD Navigator filter also implements the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) and [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) interfaces that enable a DVD playback application to control DVD-Video playback.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3023e-107">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="3023e-107">Filter Interfaces</span></span></td>
<td><span data-ttu-id="3023e-108"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>IFileSourceFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="3023e-108"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>IFileSourceFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3023e-109">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="3023e-109">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="3023e-110">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</span><span class="sxs-lookup"><span data-stu-id="3023e-110">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3023e-111">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="3023e-111">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="3023e-112">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="3023e-112">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3023e-113">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="3023e-113">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="3023e-114">Types de base :</span><span class="sxs-lookup"><span data-stu-id="3023e-114">Base types:</span></span><br/>
<ul>
<li><span data-ttu-id="3023e-115">Vidéo : <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="3023e-115">Video: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
<li><span data-ttu-id="3023e-116">Audio : <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="3023e-116">Audio: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
<li><span data-ttu-id="3023e-117">Sous-image : <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="3023e-117">Subpicture: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
</ul>
<span data-ttu-id="3023e-118">Types étendus :</span><span class="sxs-lookup"><span data-stu-id="3023e-118">Extended types:</span></span><br/> <span data-ttu-id="3023e-119">Vidéo :</span><span class="sxs-lookup"><span data-stu-id="3023e-119">Video:</span></span><br/>
<ul>
<li><span data-ttu-id="3023e-120"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="3023e-120"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
<li><span data-ttu-id="3023e-121"><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="3023e-121"><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
<li><span data-ttu-id="3023e-122"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="3023e-122"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
</ul>
<span data-ttu-id="3023e-123">Audio :</span><span class="sxs-lookup"><span data-stu-id="3023e-123">Audio:</span></span><br/>
<ul>
<li><span data-ttu-id="3023e-124"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="3023e-124"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
<li><span data-ttu-id="3023e-125"><strong>MEDIATYPE_Audio</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="3023e-125"><strong>MEDIATYPE_Audio</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
<li><span data-ttu-id="3023e-126"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="3023e-126"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
</ul>
<span data-ttu-id="3023e-127">Sous-titres</span><span class="sxs-lookup"><span data-stu-id="3023e-127">Subpicture:</span></span><br/>
<ul>
<li><span data-ttu-id="3023e-128"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="3023e-128"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
<li><span data-ttu-id="3023e-129"><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="3023e-129"><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
<li><span data-ttu-id="3023e-130"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="3023e-130"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
</ul>
<span data-ttu-id="3023e-131">Pour activer les types étendus, appelez <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>IDvdControl2 :: SetOption</strong></a> et définissez le</span><span class="sxs-lookup"><span data-stu-id="3023e-131">To enable the extended types, call <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>IDvdControl2::SetOption</strong></a> and set the</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3023e-132">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="3023e-132">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="3023e-133"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="3023e-133"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3023e-134">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="3023e-134">Filter CLSID</span></span></td>
<td><span data-ttu-id="3023e-135">CLSID_DVDNavigator</span><span class="sxs-lookup"><span data-stu-id="3023e-135">CLSID_DVDNavigator</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3023e-136">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="3023e-136">Property Page CLSID</span></span></td>
<td><span data-ttu-id="3023e-137">Aucune page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="3023e-137">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3023e-138">Exécutable</span><span class="sxs-lookup"><span data-stu-id="3023e-138">Executable</span></span></td>
<td><span data-ttu-id="3023e-139">qdvd.dll</span><span class="sxs-lookup"><span data-stu-id="3023e-139">qdvd.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3023e-140"><a href="merit.md">Mérite</a></span><span class="sxs-lookup"><span data-stu-id="3023e-140"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="3023e-141">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="3023e-141">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3023e-142"><a href="filter-categories.md">Catégorie de filtre</a></span><span class="sxs-lookup"><span data-stu-id="3023e-142"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="3023e-143">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="3023e-143">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="3023e-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3023e-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3023e-145">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="3023e-145">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="3023e-146">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="3023e-146">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 




