---
description: Les tableaux suivants répertorient les CLSID pour les catégories de filtre DirectShow.
ms.assetid: cab4e2c9-eab9-4836-adfc-870490ca5b6b
title: Filtrer les catégories
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c4ccb9443c405abcbd0b9afbd406d6faf2558a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385568"
---
# <a name="filter-categories"></a><span data-ttu-id="3d055-103">Filtrer les catégories</span><span class="sxs-lookup"><span data-stu-id="3d055-103">Filter Categories</span></span>

<span data-ttu-id="3d055-104">Les tableaux suivants répertorient les CLSID pour les catégories de filtre DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3d055-104">The following tables list the CLSIDs for the DirectShow filter categories.</span></span>

-   [<span data-ttu-id="3d055-105">Catégories de filtre DirectShow</span><span class="sxs-lookup"><span data-stu-id="3d055-105">DirectShow Filter Categories</span></span>](#directshow-filter-categories)
-   [<span data-ttu-id="3d055-106">Autres catégories de filtres</span><span class="sxs-lookup"><span data-stu-id="3d055-106">Other Filter Categories</span></span>](#other-filter-categories)
-   [<span data-ttu-id="3d055-107">Méta-catégorie de filtre DirectShow</span><span class="sxs-lookup"><span data-stu-id="3d055-107">DirectShow Filter Meta-Category</span></span>](#directshow-filter-meta-category)
-   [<span data-ttu-id="3d055-108">Catégories DMO</span><span class="sxs-lookup"><span data-stu-id="3d055-108">DMO Categories</span></span>](#dmo-categories)
-   [<span data-ttu-id="3d055-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3d055-109">Related topics</span></span>](#related-topics)

## <a name="directshow-filter-categories"></a><span data-ttu-id="3d055-110">Catégories de filtre DirectShow</span><span class="sxs-lookup"><span data-stu-id="3d055-110">DirectShow Filter Categories</span></span>

<span data-ttu-id="3d055-111">Les catégories répertoriées ici sont énumérées par le [Mappeur de filtre](filter-mapper.md).</span><span class="sxs-lookup"><span data-stu-id="3d055-111">The categories listed here are enumerated by the [Filter Mapper](filter-mapper.md).</span></span> <span data-ttu-id="3d055-112">Toutefois, par défaut, le mappeur de filtre ignore les catégories dont les mérites de mérite \_ n' \_ \_ utilisent pas ou moins.</span><span class="sxs-lookup"><span data-stu-id="3d055-112">By default, however, the Filter Mapper ignores categories with merits of MERIT\_DO\_NOT\_USE or less.</span></span> <span data-ttu-id="3d055-113">Pour plus d’informations, consultez [**IFilterMapper2 :: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters).</span><span class="sxs-lookup"><span data-stu-id="3d055-113">For more information, see [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters).</span></span> <span data-ttu-id="3d055-114">Toutes les catégories répertoriées ici peuvent également être énumérées avec l' [énumérateur de périphérique système](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="3d055-114">All of the categories listed here can also be enumerated with the [System Device Enumerator](system-device-enumerator.md).</span></span>

<span data-ttu-id="3d055-115">Les catégories suivantes sont déclarées dans UUID. h.</span><span class="sxs-lookup"><span data-stu-id="3d055-115">The following categories are declared in Uuids.h.</span></span> <span data-ttu-id="3d055-116">Incluez le fichier d’en-tête DShow. h.</span><span class="sxs-lookup"><span data-stu-id="3d055-116">Include the header file Dshow.h.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3d055-117">Nom convivial</span><span class="sxs-lookup"><span data-stu-id="3d055-117">Friendly Name</span></span></th>
<th><span data-ttu-id="3d055-118">CLSID</span><span class="sxs-lookup"><span data-stu-id="3d055-118">CLSID</span></span></th>
<th><span data-ttu-id="3d055-119">Mérite</span><span class="sxs-lookup"><span data-stu-id="3d055-119">Merit</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3d055-120">Sources de capture audio</span><span class="sxs-lookup"><span data-stu-id="3d055-120">Audio Capture Sources</span></span></td>
<td><span data-ttu-id="3d055-121"><strong>CLSID_AudioInputDeviceCategory</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-121"><strong>CLSID_AudioInputDeviceCategory</strong></span></span></td>
<td><span data-ttu-id="3d055-122"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-122"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d055-123">Compresseurs audio</span><span class="sxs-lookup"><span data-stu-id="3d055-123">Audio Compressors</span></span></td>
<td><span data-ttu-id="3d055-124"><strong>CLSID_AudioCompressorCategory</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-124"><strong>CLSID_AudioCompressorCategory</strong></span></span></td>
<td><span data-ttu-id="3d055-125"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-125"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d055-126">Convertisseurs audio</span><span class="sxs-lookup"><span data-stu-id="3d055-126">Audio Renderers</span></span></td>
<td><span data-ttu-id="3d055-127"><strong>CLSID_AudioRendererCategory</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-127"><strong>CLSID_AudioRendererCategory</strong></span></span></td>
<td><span data-ttu-id="3d055-128"><strong>MERIT_NORMAL</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-128"><strong>MERIT_NORMAL</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d055-129">Filtres de contrôle de périphérique</span><span class="sxs-lookup"><span data-stu-id="3d055-129">Device Control Filters</span></span></td>
<td><span data-ttu-id="3d055-130"><strong>CLSID_DeviceControlCategory</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-130"><strong>CLSID_DeviceControlCategory</strong></span></span></td>
<td><span data-ttu-id="3d055-131"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-131"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d055-132">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="3d055-132">DirectShow Filters</span></span></td>
<td><span data-ttu-id="3d055-133"><strong>CLSID_LegacyAmFilterCategory</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-133"><strong>CLSID_LegacyAmFilterCategory</strong></span></span></td>
<td><span data-ttu-id="3d055-134"><strong>MERIT_NORMAL</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-134"><strong>MERIT_NORMAL</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d055-135">Convertisseurs externes</span><span class="sxs-lookup"><span data-stu-id="3d055-135">External Renderers</span></span></td>
<td><span data-ttu-id="3d055-136"><strong>CLSID_TransmitCategory</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-136"><strong>CLSID_TransmitCategory</strong></span></span></td>
<td><span data-ttu-id="3d055-137"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-137"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d055-138">Convertisseurs midi</span><span class="sxs-lookup"><span data-stu-id="3d055-138">Midi Renderers</span></span></td>
<td><span data-ttu-id="3d055-139"><strong>CLSID_MidiRendererCategory</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-139"><strong>CLSID_MidiRendererCategory</strong></span></span></td>
<td><span data-ttu-id="3d055-140"><strong>MERIT_NORMAL</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-140"><strong>MERIT_NORMAL</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d055-141">Sources de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="3d055-141">Video Capture Sources</span></span></td>
<td><span data-ttu-id="3d055-142"><strong>CLSID_VideoInputDeviceCategory</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-142"><strong>CLSID_VideoInputDeviceCategory</strong></span></span></td>
<td><span data-ttu-id="3d055-143"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-143"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d055-144">Compresseurs vidéo</span><span class="sxs-lookup"><span data-stu-id="3d055-144">Video Compressors</span></span></td>
<td><span data-ttu-id="3d055-145"><strong>CLSID_VideoCompressorCategory</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-145"><strong>CLSID_VideoCompressorCategory</strong></span></span></td>
<td><span data-ttu-id="3d055-146"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-146"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d055-147">Périphériques de décompression de flux WDM</span><span class="sxs-lookup"><span data-stu-id="3d055-147">WDM Stream Decompression Devices</span></span></td>
<td><span data-ttu-id="3d055-148"><strong>CLSID_DVDHWDecodersCategory</strong>
</span><span class="sxs-lookup"><span data-stu-id="3d055-148"><strong>CLSID_DVDHWDecodersCategory</strong>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="3d055-149">Cette catégorie contient les décodeurs de DVD matériels.</span><span class="sxs-lookup"><span data-stu-id="3d055-149">This category contains hardware DVD decoders.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="3d055-150"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-150"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d055-151">Périphériques de capture de streaming WDM</span><span class="sxs-lookup"><span data-stu-id="3d055-151">WDM Streaming Capture Devices</span></span></td>
<td><span data-ttu-id="3d055-152"><strong>AM_KSCATEGORY_CAPTURE</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-152"><strong>AM_KSCATEGORY_CAPTURE</strong></span></span></td>
<td><span data-ttu-id="3d055-153"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-153"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d055-154">Périphériques de distributeur de streaming WDM</span><span class="sxs-lookup"><span data-stu-id="3d055-154">WDM Streaming Crossbar Devices</span></span></td>
<td><span data-ttu-id="3d055-155"><strong>AM_KSCATEGORY_CROSSBAR</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-155"><strong>AM_KSCATEGORY_CROSSBAR</strong></span></span></td>
<td><span data-ttu-id="3d055-156"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-156"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d055-157">Périphériques de rendu de streaming WDM</span><span class="sxs-lookup"><span data-stu-id="3d055-157">WDM Streaming Rendering Devices</span></span></td>
<td><span data-ttu-id="3d055-158"><strong>AM_KSCATEGORY_RENDER</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-158"><strong>AM_KSCATEGORY_RENDER</strong></span></span></td>
<td><span data-ttu-id="3d055-159"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-159"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d055-160">Périphériques de streaming WDM/Splitter</span><span class="sxs-lookup"><span data-stu-id="3d055-160">WDM Streaming Tee/Splitter Devices</span></span></td>
<td><span data-ttu-id="3d055-161"><strong>AM_KSCATEGORY_SPLITTER</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-161"><strong>AM_KSCATEGORY_SPLITTER</strong></span></span></td>
<td><span data-ttu-id="3d055-162"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-162"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d055-163">Périphériques audio de diffusion en continu WDM</span><span class="sxs-lookup"><span data-stu-id="3d055-163">WDM Streaming TV Audio Devices</span></span></td>
<td><span data-ttu-id="3d055-164"><strong>AM_KSCATEGORY_TVAUDIO</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-164"><strong>AM_KSCATEGORY_TVAUDIO</strong></span></span></td>
<td><span data-ttu-id="3d055-165"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-165"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d055-166">Périphériques Tuner TV WDM streaming</span><span class="sxs-lookup"><span data-stu-id="3d055-166">WDM Streaming TV Tuner Devices</span></span></td>
<td><span data-ttu-id="3d055-167"><strong>AM_KSCATEGORY_TVTUNER</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-167"><strong>AM_KSCATEGORY_TVTUNER</strong></span></span></td>
<td><span data-ttu-id="3d055-168"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-168"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d055-169">Codecs VBI de streaming WDM</span><span class="sxs-lookup"><span data-stu-id="3d055-169">WDM Streaming VBI Codecs</span></span></td>
<td><span data-ttu-id="3d055-170"><strong>AM_KSCATEGORY_VBICODEC</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-170"><strong>AM_KSCATEGORY_VBICODEC</strong></span></span></td>
<td><span data-ttu-id="3d055-171"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="3d055-171"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3d055-172">Les catégories suivantes sont déclarées dans le fichier d’en-tête KS. h.</span><span class="sxs-lookup"><span data-stu-id="3d055-172">The following categories are declared in the header file Ks.h.</span></span>



| <span data-ttu-id="3d055-173">Nom convivial</span><span class="sxs-lookup"><span data-stu-id="3d055-173">Friendly Name</span></span>                          | <span data-ttu-id="3d055-174">CLSID</span><span class="sxs-lookup"><span data-stu-id="3d055-174">CLSID</span></span>                                   | <span data-ttu-id="3d055-175">Mérite</span><span class="sxs-lookup"><span data-stu-id="3d055-175">Merit</span></span>                   |
|----------------------------------------|-----------------------------------------|-------------------------|
| <span data-ttu-id="3d055-176">Transformations de communication de streaming WDM</span><span class="sxs-lookup"><span data-stu-id="3d055-176">WDM Streaming Communication Transforms</span></span> | <span data-ttu-id="3d055-177">**KSCATEGORY \_ COMMUNICATIONSTRANSFORM**</span><span class="sxs-lookup"><span data-stu-id="3d055-177">**KSCATEGORY\_COMMUNICATIONSTRANSFORM**</span></span> | <span data-ttu-id="3d055-178">**MÉRITE \_ n' \_ \_ utilise pas**</span><span class="sxs-lookup"><span data-stu-id="3d055-178">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="3d055-179">Transformations de données de streaming WDM</span><span class="sxs-lookup"><span data-stu-id="3d055-179">WDM Streaming Data Transforms</span></span>          | <span data-ttu-id="3d055-180">**KSCATEGORY \_ DATATRANSFORM**</span><span class="sxs-lookup"><span data-stu-id="3d055-180">**KSCATEGORY\_DATATRANSFORM**</span></span>           | <span data-ttu-id="3d055-181">**MÉRITE \_ n' \_ \_ utilise pas**</span><span class="sxs-lookup"><span data-stu-id="3d055-181">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="3d055-182">Transformations de l’interface de streaming WDM</span><span class="sxs-lookup"><span data-stu-id="3d055-182">WDM Streaming Interface Transforms</span></span>     | <span data-ttu-id="3d055-183">**KSCATEGORY \_ INTERFACETRANSFORM**</span><span class="sxs-lookup"><span data-stu-id="3d055-183">**KSCATEGORY\_INTERFACETRANSFORM**</span></span>      | <span data-ttu-id="3d055-184">**MÉRITE \_ n' \_ \_ utilise pas**</span><span class="sxs-lookup"><span data-stu-id="3d055-184">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="3d055-185">Périphériques de mixage de streaming WDM</span><span class="sxs-lookup"><span data-stu-id="3d055-185">WDM Streaming Mixer Devices</span></span>            | <span data-ttu-id="3d055-186">**\_mélangeur KSCATEGORY**</span><span class="sxs-lookup"><span data-stu-id="3d055-186">**KSCATEGORY\_MIXER**</span></span>                   | <span data-ttu-id="3d055-187">**MÉRITE \_ n' \_ \_ utilise pas**</span><span class="sxs-lookup"><span data-stu-id="3d055-187">**MERIT\_DO\_NOT\_USE**</span></span> |



 

<span data-ttu-id="3d055-188">Les catégories suivantes sont déclarées dans le fichier d’en-tête Bdamedia. h.</span><span class="sxs-lookup"><span data-stu-id="3d055-188">The following categories are declared in the header file Bdamedia.h.</span></span> <span data-ttu-id="3d055-189">Incluez les fichiers d’en-tête suivants : KS. h, ksmedia. h et bdamedia. h.</span><span class="sxs-lookup"><span data-stu-id="3d055-189">Include the following header files: ks.h, ksmedia.h, and bdamedia.h.</span></span>



| <span data-ttu-id="3d055-190">Nom convivial</span><span class="sxs-lookup"><span data-stu-id="3d055-190">Friendly Name</span></span>                       | <span data-ttu-id="3d055-191">CLSID</span><span class="sxs-lookup"><span data-stu-id="3d055-191">CLSID</span></span>                                       | <span data-ttu-id="3d055-192">Mérite</span><span class="sxs-lookup"><span data-stu-id="3d055-192">Merit</span></span>                   |
|-------------------------------------|---------------------------------------------|-------------------------|
| <span data-ttu-id="3d055-193">Fournisseurs de réseau BDA</span><span class="sxs-lookup"><span data-stu-id="3d055-193">BDA Network Providers</span></span>               | <span data-ttu-id="3d055-194">**\_fournisseur de \_ réseau KSCATEGORY BDA \_**</span><span class="sxs-lookup"><span data-stu-id="3d055-194">**KSCATEGORY\_BDA\_NETWORK\_PROVIDER**</span></span>      | <span data-ttu-id="3d055-195">**MÉRITE \_ normal**</span><span class="sxs-lookup"><span data-stu-id="3d055-195">**MERIT\_NORMAL**</span></span>       |
| <span data-ttu-id="3d055-196">Composants du récepteur BDA</span><span class="sxs-lookup"><span data-stu-id="3d055-196">BDA Receiver Components</span></span>             | <span data-ttu-id="3d055-197">**\_ \_ composant récepteur KSCATEGORY \_ BDA**</span><span class="sxs-lookup"><span data-stu-id="3d055-197">**KSCATEGORY\_BDA\_RECEIVER\_COMPONENT**</span></span>    | <span data-ttu-id="3d055-198">**MÉRITE \_ n' \_ \_ utilise pas**</span><span class="sxs-lookup"><span data-stu-id="3d055-198">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="3d055-199">Filtres de rendu BDA</span><span class="sxs-lookup"><span data-stu-id="3d055-199">BDA Rendering Filters</span></span>               | <span data-ttu-id="3d055-200">**\_récepteur IP \_ KSCATEGORY**</span><span class="sxs-lookup"><span data-stu-id="3d055-200">**KSCATEGORY\_IP\_SINK**</span></span>                    | <span data-ttu-id="3d055-201">**MÉRITE \_ n' \_ \_ utilise pas**</span><span class="sxs-lookup"><span data-stu-id="3d055-201">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="3d055-202">Filtres sources BDA</span><span class="sxs-lookup"><span data-stu-id="3d055-202">BDA Source Filters</span></span>                  | <span data-ttu-id="3d055-203">**\_ \_ tuner réseau KSCATEGORY \_ BDA**</span><span class="sxs-lookup"><span data-stu-id="3d055-203">**KSCATEGORY\_BDA\_NETWORK\_TUNER**</span></span>         | <span data-ttu-id="3d055-204">**MÉRITE \_ n' \_ \_ utilise pas**</span><span class="sxs-lookup"><span data-stu-id="3d055-204">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="3d055-205">Convertisseurs d’informations de transport BDA</span><span class="sxs-lookup"><span data-stu-id="3d055-205">BDA Transport Information Renderers</span></span> | <span data-ttu-id="3d055-206">**\_ \_ informations sur le transport BDA KSCATEGORY \_**</span><span class="sxs-lookup"><span data-stu-id="3d055-206">**KSCATEGORY\_BDA\_TRANSPORT\_INFORMATION**</span></span> | <span data-ttu-id="3d055-207">**MÉRITE \_ normal**</span><span class="sxs-lookup"><span data-stu-id="3d055-207">**MERIT\_NORMAL**</span></span>       |



 

> [!Note]  
> <span data-ttu-id="3d055-208">Les décodeurs sont inscrits sous la catégorie « filtres DirectShow » (CLSID \_ LegacyAmFilterCategory).</span><span class="sxs-lookup"><span data-stu-id="3d055-208">Decoders are registered under the "DirectShow Filters" category (CLSID\_LegacyAmFilterCategory).</span></span>

 

## <a name="other-filter-categories"></a><span data-ttu-id="3d055-209">Autres catégories de filtres</span><span class="sxs-lookup"><span data-stu-id="3d055-209">Other Filter Categories</span></span>

<span data-ttu-id="3d055-210">Les catégories répertoriées ici peuvent être énumérées avec l’énumérateur de périphérique système, mais ne sont pas visibles par le mappeur de filtre et ne sont pas utilisées par la [connexion intelligente](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="3d055-210">The categories listed here can be enumerated with the System Device Enumerator, but are not visible to the Filter Mapper and are not used by [Intelligent Connect](intelligent-connect.md).</span></span>

<span data-ttu-id="3d055-211">Les catégories suivantes sont déclarées dans le fichier d’en-tête qedit. h.</span><span class="sxs-lookup"><span data-stu-id="3d055-211">The following categories are declared in the header file Qedit.h.</span></span>



| <span data-ttu-id="3d055-212">Nom convivial</span><span class="sxs-lookup"><span data-stu-id="3d055-212">Friendly Name</span></span>            | <span data-ttu-id="3d055-213">Call</span><span class="sxs-lookup"><span data-stu-id="3d055-213">CLID</span></span>                             | <span data-ttu-id="3d055-214">Mérite</span><span class="sxs-lookup"><span data-stu-id="3d055-214">Merit</span></span>                   |
|--------------------------|----------------------------------|-------------------------|
| <span data-ttu-id="3d055-215">Effets vidéo (1 entrée)</span><span class="sxs-lookup"><span data-stu-id="3d055-215">Video Effects (1 input)</span></span>  | <span data-ttu-id="3d055-216">**CLSID \_ VideoEffects1Category**</span><span class="sxs-lookup"><span data-stu-id="3d055-216">**CLSID\_VideoEffects1Category**</span></span> | <span data-ttu-id="3d055-217">**MÉRITE \_ n' \_ \_ utilise pas**</span><span class="sxs-lookup"><span data-stu-id="3d055-217">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="3d055-218">Effets vidéo (2 entrées)</span><span class="sxs-lookup"><span data-stu-id="3d055-218">Video Effects (2 inputs)</span></span> | <span data-ttu-id="3d055-219">**CLSID \_ VideoEffects2Category**</span><span class="sxs-lookup"><span data-stu-id="3d055-219">**CLSID\_VideoEffects2Category**</span></span> | <span data-ttu-id="3d055-220">**MÉRITE \_ n' \_ \_ utilise pas**</span><span class="sxs-lookup"><span data-stu-id="3d055-220">**MERIT\_DO\_NOT\_USE**</span></span> |



 

<span data-ttu-id="3d055-221">Ces catégories contiennent des effets vidéo et des transitions pour les [services de modification DirectShow](directshow-editing-services.md):</span><span class="sxs-lookup"><span data-stu-id="3d055-221">These categories contain video effects and transitions for [DirectShow Editing Services](directshow-editing-services.md):</span></span>

-   <span data-ttu-id="3d055-222">« Effets vidéo (1 entrée) » contient des effets vidéo.</span><span class="sxs-lookup"><span data-stu-id="3d055-222">"Video Effects (1 input)" contains video effects.</span></span>
-   <span data-ttu-id="3d055-223">« Effets vidéo (2 entrées) » contient des transitions vidéo.</span><span class="sxs-lookup"><span data-stu-id="3d055-223">"Video Effects (2 input)" contains video transitions.</span></span>

<span data-ttu-id="3d055-224">Pour plus d’informations, consultez [énumération des effets et des transitions](enumerating-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="3d055-224">For more information, see [Enumerating Effects and Transitions](enumerating-effects-and-transitions.md).</span></span>

<span data-ttu-id="3d055-225">Les catégories suivantes sont déclarées dans le fichier d’en-tête UUID. h.</span><span class="sxs-lookup"><span data-stu-id="3d055-225">The following categories are declared in the header file Uuids.h.</span></span> <span data-ttu-id="3d055-226">Incluez le fichier d’en-tête DShow. h.</span><span class="sxs-lookup"><span data-stu-id="3d055-226">Include the header file Dshow.h.</span></span>



| <span data-ttu-id="3d055-227">Nom convivial</span><span class="sxs-lookup"><span data-stu-id="3d055-227">Friendly Name</span></span>       | <span data-ttu-id="3d055-228">Call</span><span class="sxs-lookup"><span data-stu-id="3d055-228">CLID</span></span>                                | <span data-ttu-id="3d055-229">Mérite</span><span class="sxs-lookup"><span data-stu-id="3d055-229">Merit</span></span>                   |
|---------------------|-------------------------------------|-------------------------|
| <span data-ttu-id="3d055-230">Encodeurs encodeurs</span><span class="sxs-lookup"><span data-stu-id="3d055-230">EncAPI Encoders</span></span>     | <span data-ttu-id="3d055-231">**CLSID \_ MediaEncoderCategory**</span><span class="sxs-lookup"><span data-stu-id="3d055-231">**CLSID\_MediaEncoderCategory**</span></span>     | <span data-ttu-id="3d055-232">**MÉRITE \_ n' \_ \_ utilise pas**</span><span class="sxs-lookup"><span data-stu-id="3d055-232">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="3d055-233">Multiplexeurs encapis</span><span class="sxs-lookup"><span data-stu-id="3d055-233">EncAPI Multiplexers</span></span> | <span data-ttu-id="3d055-234">**CLSID \_ MediaMultiplexerCategory**</span><span class="sxs-lookup"><span data-stu-id="3d055-234">**CLSID\_MediaMultiplexerCategory**</span></span> | <span data-ttu-id="3d055-235">**MÉRITE \_ n' \_ \_ utilise pas**</span><span class="sxs-lookup"><span data-stu-id="3d055-235">**MERIT\_DO\_NOT\_USE**</span></span> |



 

## <a name="directshow-filter-meta-category"></a><span data-ttu-id="3d055-236">Meta-Category de filtre DirectShow</span><span class="sxs-lookup"><span data-stu-id="3d055-236">DirectShow Filter Meta-Category</span></span>



| <span data-ttu-id="3d055-237">Nom convivial</span><span class="sxs-lookup"><span data-stu-id="3d055-237">Friendly Name</span></span>                 | <span data-ttu-id="3d055-238">CLSID</span><span class="sxs-lookup"><span data-stu-id="3d055-238">CLSID</span></span>                            | <span data-ttu-id="3d055-239">Mérite</span><span class="sxs-lookup"><span data-stu-id="3d055-239">Merit</span></span>          |
|-------------------------------|----------------------------------|----------------|
| <span data-ttu-id="3d055-240">Catégories de filtre ActiveMovie</span><span class="sxs-lookup"><span data-stu-id="3d055-240">ActiveMovie Filter Categories</span></span> | <span data-ttu-id="3d055-241">**CLSID \_ ActiveMovieCategories**</span><span class="sxs-lookup"><span data-stu-id="3d055-241">**CLSID\_ActiveMovieCategories**</span></span> | <span data-ttu-id="3d055-242">Non applicable</span><span class="sxs-lookup"><span data-stu-id="3d055-242">Not applicable</span></span> |



 

<span data-ttu-id="3d055-243">Cette catégorie méta contient une liste de catégories de filtres.</span><span class="sxs-lookup"><span data-stu-id="3d055-243">This meta-category contains a list of filter categories.</span></span> <span data-ttu-id="3d055-244">Si une catégorie de filtre n’apparaît pas dans cette liste, le [Mappeur de filtre](filter-mapper.md) ignore la catégorie, ce qui signifie que le filtre n’est pas disponible pour la [connexion intelligente](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="3d055-244">If a filter category does not appear within this list, the [Filter Mapper](filter-mapper.md) ignores the category, which means the filter is not available for [Intelligent Connect](intelligent-connect.md).</span></span>

<span data-ttu-id="3d055-245">Pour énumérer la liste des catégories de filtre, appelez [**ICreateDevEnum :: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) avec la valeur CLSID \_ ActiveMovieCategories.</span><span class="sxs-lookup"><span data-stu-id="3d055-245">To enumerate the list of filter categories, call [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) with the value CLSID\_ActiveMovieCategories.</span></span> <span data-ttu-id="3d055-246">Les monikers retournés par cette méthode prennent en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3d055-246">The monikers returned by this method support the following properties.</span></span>



| <span data-ttu-id="3d055-247">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="3d055-247">Property Name</span></span>  | <span data-ttu-id="3d055-248">Description</span><span class="sxs-lookup"><span data-stu-id="3d055-248">Description</span></span>                                                                            |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d055-249">Convivial</span><span class="sxs-lookup"><span data-stu-id="3d055-249">"FriendlyName"</span></span> | <span data-ttu-id="3d055-250">Nom de la catégorie (VT \_ BSTR).</span><span class="sxs-lookup"><span data-stu-id="3d055-250">Category name (VT\_BSTR).</span></span>                                                              |
| <span data-ttu-id="3d055-251">Mérite</span><span class="sxs-lookup"><span data-stu-id="3d055-251">"Merit"</span></span>        | <span data-ttu-id="3d055-252">Mérite de catégorie (VT \_ I4).</span><span class="sxs-lookup"><span data-stu-id="3d055-252">Category merit (VT\_I4).</span></span> <span data-ttu-id="3d055-253">Si cette propriété est absente, Treat comme **mérite \_ n' \_ \_ utilise pas**.</span><span class="sxs-lookup"><span data-stu-id="3d055-253">If this property is absent, treat as **MERIT\_DO\_NOT\_USE**.</span></span> |
| <span data-ttu-id="3d055-254">IDENTIFICATEUR</span><span class="sxs-lookup"><span data-stu-id="3d055-254">"CLSID"</span></span>        | <span data-ttu-id="3d055-255">CLSID de catégorie (VT \_ BSTR).</span><span class="sxs-lookup"><span data-stu-id="3d055-255">Category CLSID (VT\_BSTR).</span></span>                                                             |



 

<span data-ttu-id="3d055-256">Pour ajouter une nouvelle catégorie de filtre à cette liste, appelez [**IFilterMapper2 :: CreateCategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory).</span><span class="sxs-lookup"><span data-stu-id="3d055-256">To add a new filter category to this list, call [**IFilterMapper2::CreateCategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory).</span></span>

## <a name="dmo-categories"></a><span data-ttu-id="3d055-257">Catégories DMO</span><span class="sxs-lookup"><span data-stu-id="3d055-257">DMO Categories</span></span>

<span data-ttu-id="3d055-258">Les objets DMOs (DirectX Media Objects) utilisent un mécanisme d’énumération différent des filtres DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3d055-258">DirectX Media Objects (DMOs) use a different enumeration mechanism from DirectShow filters.</span></span> <span data-ttu-id="3d055-259">Pour plus d’informations, consultez [inscription d’un DMO](registering-a-dmo.md).</span><span class="sxs-lookup"><span data-stu-id="3d055-259">For more information, see [Registering a DMO](registering-a-dmo.md).</span></span> <span data-ttu-id="3d055-260">Toutefois, vous pouvez utiliser l’énumérateur de périphérique système pour énumérer les catégories DMO.</span><span class="sxs-lookup"><span data-stu-id="3d055-260">However, you can use the System Device Enumerator to enumerate DMO categories.</span></span> <span data-ttu-id="3d055-261">Les monikers sont liés au [filtre de wrappers DMO](dmo-wrapper-filter.md) et initialisent automatiquement le filtre avec DMO.</span><span class="sxs-lookup"><span data-stu-id="3d055-261">The monikers bind to the [DMO Wrapper Filter](dmo-wrapper-filter.md) and automatically initialize the filter with the DMO.</span></span>

<span data-ttu-id="3d055-262">En outre, certaines des catégories DMO sont mappées à des catégories de filtre DirectShow dans le cadre de la connexion intelligente :</span><span class="sxs-lookup"><span data-stu-id="3d055-262">In addition, some of the DMO categories are mapped to DirectShow filter categories for the purposes of intelligent connect:</span></span>



| <span data-ttu-id="3d055-263">Catégorie DMO</span><span class="sxs-lookup"><span data-stu-id="3d055-263">DMO Category</span></span>                    | <span data-ttu-id="3d055-264">Équivalent DirectShow</span><span class="sxs-lookup"><span data-stu-id="3d055-264">DirectShow Equivalent</span></span>              |
|---------------------------------|------------------------------------|
| <span data-ttu-id="3d055-265">**\_encodeur audio DMOCATEGORY \_**</span><span class="sxs-lookup"><span data-stu-id="3d055-265">**DMOCATEGORY\_AUDIO\_ENCODER**</span></span> | <span data-ttu-id="3d055-266">**CLSID \_ AudioCompressorCategory**</span><span class="sxs-lookup"><span data-stu-id="3d055-266">**CLSID\_AudioCompressorCategory**</span></span> |
| <span data-ttu-id="3d055-267">**\_DÉcodeur audio DMOCATEGORY \_**</span><span class="sxs-lookup"><span data-stu-id="3d055-267">**DMOCATEGORY\_AUDIO\_DECODER**</span></span> | <span data-ttu-id="3d055-268">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="3d055-268">**CLSID\_LegacyAmFilterCategory**</span></span>  |
| <span data-ttu-id="3d055-269">**\_encodeur vidéo DMOCATEGORY \_**</span><span class="sxs-lookup"><span data-stu-id="3d055-269">**DMOCATEGORY\_VIDEO\_ENCODER**</span></span> | <span data-ttu-id="3d055-270">**CLSID \_ VideoCompressorCategory**</span><span class="sxs-lookup"><span data-stu-id="3d055-270">**CLSID\_VideoCompressorCategory**</span></span> |
| <span data-ttu-id="3d055-271">**\_DÉcodeur vidéo DMOCATEGORY \_**</span><span class="sxs-lookup"><span data-stu-id="3d055-271">**DMOCATEGORY\_VIDEO\_DECODER**</span></span> | <span data-ttu-id="3d055-272">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="3d055-272">**CLSID\_LegacyAmFilterCategory**</span></span>  |



 

<span data-ttu-id="3d055-273">Notez que les catégories effet vidéo et effet audio ne sont mappées à aucune catégorie DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3d055-273">Note that the video effect and audio effect categories are not mapped to any DirectShow categories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d055-274">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3d055-274">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d055-275">Constantes et GUID</span><span class="sxs-lookup"><span data-stu-id="3d055-275">Constants and GUIDs</span></span>](constants-and-guids.md)
</dt> <dt>

[<span data-ttu-id="3d055-276">Énumération des appareils et des filtres</span><span class="sxs-lookup"><span data-stu-id="3d055-276">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="3d055-277">Connexion intelligente</span><span class="sxs-lookup"><span data-stu-id="3d055-277">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> <dt>

[<span data-ttu-id="3d055-278">Disposition des clés de Registre</span><span class="sxs-lookup"><span data-stu-id="3d055-278">Layout of the Registry Keys</span></span>](layout-of-the-registry-keys.md)
</dt> <dt>

[<span data-ttu-id="3d055-279">Utilisation du mappeur de filtre</span><span class="sxs-lookup"><span data-stu-id="3d055-279">Using the Filter Mapper</span></span>](using-the-filter-mapper.md)
</dt> <dt>

[<span data-ttu-id="3d055-280">Utilisation de l’énumérateur de périphérique système</span><span class="sxs-lookup"><span data-stu-id="3d055-280">Using the System Device Enumerator</span></span>](using-the-system-device-enumerator.md)
</dt> </dl>

 

 




