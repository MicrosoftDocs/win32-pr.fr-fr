---
description: Filtre de convertisseur DirectSound
ms.assetid: ec6cc790-8c1f-4de4-a7ca-a7073894380e
title: Filtre de convertisseur DirectSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae932340ea22213e0f9d7234599742d74208f632
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108503"
---
# <a name="directsound-renderer-filter"></a><span data-ttu-id="5f3a1-103">Filtre de convertisseur DirectSound</span><span class="sxs-lookup"><span data-stu-id="5f3a1-103">DirectSound Renderer Filter</span></span>

<span data-ttu-id="5f3a1-104">Ce filtre restitue l’audio à l’aide de DirectSound.</span><span class="sxs-lookup"><span data-stu-id="5f3a1-104">This filter renders audio using DirectSound.</span></span> <span data-ttu-id="5f3a1-105">Ce filtre est actuellement le convertisseur audio par défaut pour le son de forme d’onde.</span><span class="sxs-lookup"><span data-stu-id="5f3a1-105">This filter is currently the default audio renderer for waveform sound.</span></span>

<span data-ttu-id="5f3a1-106">Outre ses fonctionnalités de rendu de son de base, ce filtre peut traiter les appels d’API DirectSound.</span><span class="sxs-lookup"><span data-stu-id="5f3a1-106">In addition to its basic sound-rendering capabilities, this filter can process DirectSound API calls.</span></span> <span data-ttu-id="5f3a1-107">Utilisez les méthodes [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) pour définir et récupérer la fenêtre qui gérera la lecture audio.</span><span class="sxs-lookup"><span data-stu-id="5f3a1-107">Use the [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) methods to set and retrieve the window that will handle the sound playback.</span></span> <span data-ttu-id="5f3a1-108">Le convertisseur audio DirectSound est le filtre de rendu audio par défaut pour DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5f3a1-108">The DirectSound Audio Renderer is the default audio rendering filter for DirectShow.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5f3a1-109">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="5f3a1-109">Filter Interfaces</span></span></td>
<td><span data-ttu-id="5f3a1-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a>, <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a>, <strong>IDirectSound3DBuffer</strong>, <strong>IDirectSound3dListener</strong>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f3a1-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a>, <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a>, <strong>IDirectSound3DBuffer</strong>, <strong>IDirectSound3dListener</strong>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f3a1-111">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="5f3a1-111">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="5f3a1-112">Type majeur : MEDIATYPE_AudioSubtypes :</span><span class="sxs-lookup"><span data-stu-id="5f3a1-112">Major Type: MEDIATYPE_AudioSubtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="5f3a1-113">MEDIASUBTYPE_PCM</span><span class="sxs-lookup"><span data-stu-id="5f3a1-113">MEDIASUBTYPE_PCM</span></span></li>
<li><span data-ttu-id="5f3a1-114">MEDIASUBTYPE_IEEE_FLOAT</span><span class="sxs-lookup"><span data-stu-id="5f3a1-114">MEDIASUBTYPE_IEEE_FLOAT</span></span></li>
<li><span data-ttu-id="5f3a1-115">MEDIASUBTYPE_DOLBY_AC3_SPDIF</span><span class="sxs-lookup"><span data-stu-id="5f3a1-115">MEDIASUBTYPE_DOLBY_AC3_SPDIF</span></span></li>
<li><span data-ttu-id="5f3a1-116">MEDIASUBTYPE_RAW_SPORT</span><span class="sxs-lookup"><span data-stu-id="5f3a1-116">MEDIASUBTYPE_RAW_SPORT</span></span></li>
<li><span data-ttu-id="5f3a1-117">MEDIASUBTYPE_SPDIF_TAG_241h</span><span class="sxs-lookup"><span data-stu-id="5f3a1-117">MEDIASUBTYPE_SPDIF_TAG_241h</span></span></li>
<li><span data-ttu-id="5f3a1-118">MEDIASUBTYPE_DRM_Audio</span><span class="sxs-lookup"><span data-stu-id="5f3a1-118">MEDIASUBTYPE_DRM_Audio</span></span></li>
</ul>
<span data-ttu-id="5f3a1-119">Type de format : FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="5f3a1-119">Format type: FORMAT_WaveFormatEx</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f3a1-120">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="5f3a1-120">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="5f3a1-121"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f3a1-121"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f3a1-122">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="5f3a1-122">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="5f3a1-123">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="5f3a1-123">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f3a1-124">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="5f3a1-124">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="5f3a1-125">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="5f3a1-125">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f3a1-126">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="5f3a1-126">Filter CLSID</span></span></td>
<td><span data-ttu-id="5f3a1-127">CLSID_DSoundRender</span><span class="sxs-lookup"><span data-stu-id="5f3a1-127">CLSID_DSoundRender</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f3a1-128">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="5f3a1-128">Property Page CLSID</span></span></td>
<td><span data-ttu-id="5f3a1-129">CLSID_AudioProperties, CLSID_AudioRendererAdvancedProperties</span><span class="sxs-lookup"><span data-stu-id="5f3a1-129">CLSID_AudioProperties, CLSID_AudioRendererAdvancedProperties</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f3a1-130">Exécutable</span><span class="sxs-lookup"><span data-stu-id="5f3a1-130">Executable</span></span></td>
<td><span data-ttu-id="5f3a1-131">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="5f3a1-131">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f3a1-132"><a href="merit.md">Mérite</a></span><span class="sxs-lookup"><span data-stu-id="5f3a1-132"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="5f3a1-133">MERIT_PREFERRED</span><span class="sxs-lookup"><span data-stu-id="5f3a1-133">MERIT_PREFERRED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f3a1-134"><a href="filter-categories.md">Catégorie de filtre</a></span><span class="sxs-lookup"><span data-stu-id="5f3a1-134"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="5f3a1-135">CLSID_AudioRendererCategory</span><span class="sxs-lookup"><span data-stu-id="5f3a1-135">CLSID_AudioRendererCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="5f3a1-136">Notes</span><span class="sxs-lookup"><span data-stu-id="5f3a1-136">Remarks</span></span>

<span data-ttu-id="5f3a1-137">Ce filtre sert de wrapper pour un périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="5f3a1-137">This filter acts as a wrapper for an audio device.</span></span> <span data-ttu-id="5f3a1-138">Pour énumérer les périphériques audio disponibles sur le système de l’utilisateur, utilisez l’interface [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) avec la catégorie de convertisseur audio (CLSID \_ AudioRendererCategory).</span><span class="sxs-lookup"><span data-stu-id="5f3a1-138">To enumerate the audio devices available on the user's system, use the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface with the audio renderer category (CLSID\_AudioRendererCategory).</span></span> <span data-ttu-id="5f3a1-139">Pour chaque périphérique audio, la catégorie de convertisseur audio contient deux instances de filtre.</span><span class="sxs-lookup"><span data-stu-id="5f3a1-139">For each audio device, the audio renderer category contains two filter instances.</span></span> <span data-ttu-id="5f3a1-140">L’une d’entre elles correspond au convertisseur DirectSound, tandis que l’autre correspond au filtre de [convertisseur audio (WaveOut)](audio-renderer--waveout--filter.md) .</span><span class="sxs-lookup"><span data-stu-id="5f3a1-140">One of these corresponds to the DirectSound Renderer, and the other corresponds to the [Audio Renderer (WaveOut)](audio-renderer--waveout--filter.md) filter.</span></span> <span data-ttu-id="5f3a1-141">L’instance DirectSound porte le nom convivial « DirectSound : *DeviceName*», où *DeviceName* est le nom de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5f3a1-141">The DirectSound instance has the friendly name "DirectSound: *DeviceName*," where *DeviceName* is the name of the device.</span></span> <span data-ttu-id="5f3a1-142">L’instance WaveOut a le nom convivial *DeviceName*.</span><span class="sxs-lookup"><span data-stu-id="5f3a1-142">The WaveOut instance has the friendly name *DeviceName*.</span></span>

<span data-ttu-id="5f3a1-143">La catégorie de convertisseur audio contient deux instances de filtre supplémentaires, nommées « appareil DirectSound par défaut » et « appareil WaveOut par défaut ».</span><span class="sxs-lookup"><span data-stu-id="5f3a1-143">The audio renderer category contains two additional filter instances, named "Default DirectSound Device" and "Default WaveOut Device."</span></span> <span data-ttu-id="5f3a1-144">Celles-ci correspondent au périphérique audio par défaut, tel qu’il est choisi par l’utilisateur via le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="5f3a1-144">These correspond to the default sound device, as chosen by the user through the Control Panel.</span></span> <span data-ttu-id="5f3a1-145">Elles sont en réalité mappées à l’une des paires décrites dans le paragraphe précédent.</span><span class="sxs-lookup"><span data-stu-id="5f3a1-145">They are actually mappings to one of the pairs described in the previous paragraph.</span></span> <span data-ttu-id="5f3a1-146">Par exemple, si le système a deux périphériques audio, l’appareil A et l’appareil B, la catégorie de convertisseur audio contient ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="5f3a1-146">For example, if the system has two audio devices, Device A and Device B, the audio renderer category will contain the following:</span></span>

-   <span data-ttu-id="5f3a1-147">Appareil A</span><span class="sxs-lookup"><span data-stu-id="5f3a1-147">Device A</span></span>
-   <span data-ttu-id="5f3a1-148">DirectSound : appareil A</span><span class="sxs-lookup"><span data-stu-id="5f3a1-148">DirectSound: Device A</span></span>
-   <span data-ttu-id="5f3a1-149">Appareil B</span><span class="sxs-lookup"><span data-stu-id="5f3a1-149">Device B</span></span>
-   <span data-ttu-id="5f3a1-150">DirectSound : appareil B</span><span class="sxs-lookup"><span data-stu-id="5f3a1-150">DirectSound: Device B</span></span>
-   <span data-ttu-id="5f3a1-151">Appareil DirectSound par défaut</span><span class="sxs-lookup"><span data-stu-id="5f3a1-151">Default DirectSound Device</span></span>
-   <span data-ttu-id="5f3a1-152">Appareil WaveOut par défaut</span><span class="sxs-lookup"><span data-stu-id="5f3a1-152">Default WaveOut Device</span></span>

<span data-ttu-id="5f3a1-153">Si l’utilisateur A sélectionné l’appareil A comme périphérique par défaut, « appareil DirectSound par défaut » est équivalent à « DirectSound : Device A » et « appareil WaveOut par défaut » est équivalent à « périphérique A ».</span><span class="sxs-lookup"><span data-stu-id="5f3a1-153">If the user selected Device A as the default device, then "Default DirectSound Device" is equivalent to "DirectSound: Device A," and "Default WaveOut Device" is equivalent to "Device A."</span></span> <span data-ttu-id="5f3a1-154">Si l’utilisateur sélectionne l’appareil B comme périphérique par défaut, ces mappages sont modifiés.</span><span class="sxs-lookup"><span data-stu-id="5f3a1-154">If the user selects Device B as the default device, these mappings will change.</span></span>

<span data-ttu-id="5f3a1-155">« Appareil DirectSound par défaut » est affecté d’un mérite de mérite \_ .</span><span class="sxs-lookup"><span data-stu-id="5f3a1-155">"Default DirectSound Device" is assigned a merit of MERIT\_PREFERRED.</span></span> <span data-ttu-id="5f3a1-156">Les autres ont des mérites à \_ ne \_ pas \_ utiliser.</span><span class="sxs-lookup"><span data-stu-id="5f3a1-156">The others have merit MERIT\_DO\_NOT\_USE.</span></span> <span data-ttu-id="5f3a1-157">Par conséquent, la connexion intelligente choisit toujours l’appareil DirectSound par défaut.</span><span class="sxs-lookup"><span data-stu-id="5f3a1-157">Therefore, Intelligent Connect will always choose the default DirectSound device.</span></span>

<span data-ttu-id="5f3a1-158">Le filtre de convertisseur DirectSound prend en charge le son en 3D via les interfaces DirectSound **IDirectSound3DBuffer** et **IDirectSound3dListener** .</span><span class="sxs-lookup"><span data-stu-id="5f3a1-158">The DirectSound Renderer filter supports 3D sound through the DirectSound **IDirectSound3DBuffer** and **IDirectSound3dListener** interfaces.</span></span> <span data-ttu-id="5f3a1-159">Vous pouvez également interroger le filtre sur les versions actuelles de ces interfaces, **IDirectSound3DBuffer8** et **IDirectSound3dListener8**.</span><span class="sxs-lookup"><span data-stu-id="5f3a1-159">You can also query the filter for the current versions of these interfaces, **IDirectSound3DBuffer8** and **IDirectSound3dListener8**.</span></span> <span data-ttu-id="5f3a1-160">Exécutez le graphique avant d’appeler des méthodes sur ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="5f3a1-160">Run the graph before calling methods on these interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f3a1-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5f3a1-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f3a1-162">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="5f3a1-162">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




