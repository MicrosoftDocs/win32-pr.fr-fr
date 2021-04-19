---
description: Filtre de décodeur de ligne 21
ms.assetid: 48fa5484-1f8c-4133-b2e1-888cb1834402
title: Filtre de décodeur de ligne 21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839a6ff8e77f4815b74f5de65b8f0e2a565cdc2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515525"
---
# <a name="line-21-decoder-filter"></a><span data-ttu-id="0a65e-103">Filtre de décodeur de ligne 21</span><span class="sxs-lookup"><span data-stu-id="0a65e-103">Line 21 Decoder Filter</span></span>

<span data-ttu-id="0a65e-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0a65e-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="0a65e-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="0a65e-105">It may be altered or unavailable in subsequent versions.</span></span>

<span data-ttu-id="0a65e-106">Ce filtre de décodeur de ligne 21 décode les données de la ligne 21 et dessine le texte de la légende sur les bitmaps.</span><span class="sxs-lookup"><span data-stu-id="0a65e-106">This Line 21 Decoder filter decodes line 21 data and draws the caption text onto bitmaps.</span></span>

<span data-ttu-id="0a65e-107">La broche d’entrée se connecte à n’importe quel fournisseur de données de ligne 21, généralement un décodeur vidéo DVD ou le filtre de [décodeur CC](cc-decoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="0a65e-107">The input pin connects to any line 21 data provider, typically either a DVD video decoder or the [CC Decoder](cc-decoder-filter.md) filter.</span></span> <span data-ttu-id="0a65e-108">Le décodeur CC fournit des données de ligne 21 à partir du VBI d’un signal de télévision analogique.</span><span class="sxs-lookup"><span data-stu-id="0a65e-108">The CC Decoder provides line 21 data from the VBI of an analog television signal.</span></span> <span data-ttu-id="0a65e-109">La broche de sortie se connecte à un code PIN secondaire sur le [mélangeur de superposition](overlay-mixer-filter.md) ou à un autre convertisseur vidéo, tel que VMR.</span><span class="sxs-lookup"><span data-stu-id="0a65e-109">The output pin connects to a secondary pin on the [Overlay Mixer](overlay-mixer-filter.md) or to another video renderer, such as the VMR.</span></span>

<span data-ttu-id="0a65e-110">Ce filtre accepte les données de ligne 21 dans le format de paire d’octets standard ou, pour les DVD, en tant que paquet pour l’ensemble du groupe d’images (GOP).</span><span class="sxs-lookup"><span data-stu-id="0a65e-110">This filter accepts line 21 data in the standard byte-pair format or, for DVD, as a packet for the whole group of pictures (GOP).</span></span> <span data-ttu-id="0a65e-111">Pour chaque groupe d’images dans le flux vidéo DVD, il peut y avoir un paquet de données utilisateur qui contient les informations d’en-tête de ce groupe d’images et les données de ligne 21.</span><span class="sxs-lookup"><span data-stu-id="0a65e-111">For every GOP in the DVD video stream, there can be a user data packet that has that particular GOP's header information and line 21 data.</span></span> <span data-ttu-id="0a65e-112">Le format des paires d’octets est défini dans la norme EIA/CEA-608-B ; Pour plus d’informations, reportez-vous à cette norme.</span><span class="sxs-lookup"><span data-stu-id="0a65e-112">The format of the byte pairs is defined in the EIA/CEA-608-B standard; please refer to that standard for more information.</span></span>

<span data-ttu-id="0a65e-113">Deux versions de ce filtre sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="0a65e-113">Two versions of this filter are available:</span></span>



| <span data-ttu-id="0a65e-114">Filtrer</span><span class="sxs-lookup"><span data-stu-id="0a65e-114">Filter</span></span>            | <span data-ttu-id="0a65e-115">CLSID</span><span class="sxs-lookup"><span data-stu-id="0a65e-115">CLSID</span></span>                 |
|-------------------|-----------------------|
| <span data-ttu-id="0a65e-116">Décodeur de ligne 21</span><span class="sxs-lookup"><span data-stu-id="0a65e-116">Line 21 Decoder</span></span>   | <span data-ttu-id="0a65e-117">CLSID \_ Line21Decoder</span><span class="sxs-lookup"><span data-stu-id="0a65e-117">CLSID\_Line21Decoder</span></span>  |
| <span data-ttu-id="0a65e-118">Décodeur de ligne 21 2</span><span class="sxs-lookup"><span data-stu-id="0a65e-118">Line 21 Decoder 2</span></span> | <span data-ttu-id="0a65e-119">CLSID \_ Line21Decoder2</span><span class="sxs-lookup"><span data-stu-id="0a65e-119">CLSID\_Line21Decoder2</span></span> |



 

<span data-ttu-id="0a65e-120">Le filtre version 1 est utilisé sur les plateformes Microsoft® Windows® 95/98/me et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="0a65e-120">The version 1 filter is used on Microsoft® Windows® 95/98/Me and Windows 2000 platforms.</span></span> <span data-ttu-id="0a65e-121">Le filtre de la version 2 est disponible dans Microsoft Windows XP et versions ultérieures, et est utilisé chaque fois que le convertisseur de mixage vidéo se trouve dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="0a65e-121">The version 2 filter is available in Microsoft Windows XP and later, and is used whenever the Video Mixing Renderer is in the graph.</span></span>

<span data-ttu-id="0a65e-122">Les informations du tableau suivant s’appliquent aux deux versions du filtre :</span><span class="sxs-lookup"><span data-stu-id="0a65e-122">The information in the following table applies to both versions of the filter:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0a65e-123">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="0a65e-123">Filter Interfaces</span></span></td>
<td><span data-ttu-id="0a65e-124"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a65e-124"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a65e-125">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="0a65e-125">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="0a65e-126">Type majeur : MEDIATYPE_AUXLine21DataSubtype :</span><span class="sxs-lookup"><span data-stu-id="0a65e-126">Major Type: MEDIATYPE_AUXLine21DataSubtype:</span></span><br/>
<ul>
<li><span data-ttu-id="0a65e-127">MEDIASUBTYPE_Line21_BytePair (ligne standard 21)</span><span class="sxs-lookup"><span data-stu-id="0a65e-127">MEDIASUBTYPE_Line21_BytePair (standard line 21)</span></span></li>
<li><span data-ttu-id="0a65e-128">MEDIASUBTYPE_Line21_GOPPacket (ligne DVD 21)</span><span class="sxs-lookup"><span data-stu-id="0a65e-128">MEDIASUBTYPE_Line21_GOPPacket (DVD line 21)</span></span></li>
</ul>
<span data-ttu-id="0a65e-129">Type de format : FORMAT_VideoInfo ou GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="0a65e-129">Format Type: FORMAT_VideoInfo or GUID_NULL</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a65e-130">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="0a65e-130">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="0a65e-131"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a65e-131"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a65e-132">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="0a65e-132">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="0a65e-133">Type majeur : MEDIATYPE_VideoSubtype :</span><span class="sxs-lookup"><span data-stu-id="0a65e-133">Major type: MEDIATYPE_VideoSubtype:</span></span><br/>
<ul>
<li><span data-ttu-id="0a65e-134">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="0a65e-134">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="0a65e-135">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="0a65e-135">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="0a65e-136">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="0a65e-136">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="0a65e-137">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="0a65e-137">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="0a65e-138">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="0a65e-138">MEDIASUBTYPE_RGB32</span></span></li>
</ul>
<span data-ttu-id="0a65e-139">Type de format : FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="0a65e-139">Format Type: FORMAT_VideoInfo</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a65e-140">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="0a65e-140">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="0a65e-141"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a65e-141"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a65e-142">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="0a65e-142">Filter CLSID</span></span></td>
<td><span data-ttu-id="0a65e-143">Voir le tableau précédent</span><span class="sxs-lookup"><span data-stu-id="0a65e-143">See previous table</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a65e-144">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="0a65e-144">Property Page CLSID</span></span></td>
<td><span data-ttu-id="0a65e-145">Aucun</span><span class="sxs-lookup"><span data-stu-id="0a65e-145">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a65e-146">Exécutable</span><span class="sxs-lookup"><span data-stu-id="0a65e-146">Executable</span></span></td>
<td><span data-ttu-id="0a65e-147">qdvd.dll</span><span class="sxs-lookup"><span data-stu-id="0a65e-147">qdvd.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a65e-148"><a href="merit.md">Mérite</a></span><span class="sxs-lookup"><span data-stu-id="0a65e-148"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="0a65e-149">Décodeur de ligne 21 : MERIT_NORMALLine 21 décodeur 2 : MERIT_NORMAL + 2</span><span class="sxs-lookup"><span data-stu-id="0a65e-149">Line 21 Decoder: MERIT_NORMALLine 21 Decoder 2: MERIT_NORMAL + 2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a65e-150"><a href="filter-categories.md">Catégorie de filtre</a></span><span class="sxs-lookup"><span data-stu-id="0a65e-150"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="0a65e-151">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="0a65e-151">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="0a65e-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0a65e-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a65e-153">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="0a65e-153">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="0a65e-154">Sous-titres et télétexte</span><span class="sxs-lookup"><span data-stu-id="0a65e-154">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)
</dt> <dt>

[<span data-ttu-id="0a65e-155">Configuration du graphique de filtre DVD</span><span class="sxs-lookup"><span data-stu-id="0a65e-155">DVD Filter Graph Configuration</span></span>](dvd-filter-graph-configuration.md)
</dt> </dl>

 

 




