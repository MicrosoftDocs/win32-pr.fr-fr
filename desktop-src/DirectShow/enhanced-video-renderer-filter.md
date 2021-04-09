---
description: Le filtre EVR (Enhanced Video Renderer) est un mélangeur vidéo à 16 canaux et un convertisseur. Il a les mêmes fonctionnalités de base et le même modèle de plug-in que le récepteur multimédia Media Foundation EVR.
ms.assetid: ead99cb3-2be2-42c6-ac22-be0c2ddf28d5
title: Filtre de convertisseur vidéo amélioré
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ba6e7c14386ea37424364274263859844182ed7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033466"
---
# <a name="enhanced-video-renderer-filter"></a><span data-ttu-id="a347c-104">Filtre de convertisseur vidéo amélioré</span><span class="sxs-lookup"><span data-stu-id="a347c-104">Enhanced Video Renderer Filter</span></span>

> [!Note]  
> <span data-ttu-id="a347c-105">Cette rubrique s’applique à Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a347c-105">This topic applies to Windows Vista and later.</span></span>

 

<span data-ttu-id="a347c-106">Le filtre EVR (Enhanced Video Renderer) est un mélangeur vidéo à 16 canaux et un convertisseur.</span><span class="sxs-lookup"><span data-stu-id="a347c-106">The Enhanced Video Renderer (EVR) filter is a 16-channel video mixer and renderer.</span></span> <span data-ttu-id="a347c-107">Il a les mêmes fonctionnalités de base et le même modèle de plug-in que le récepteur multimédia Media Foundation EVR.</span><span class="sxs-lookup"><span data-stu-id="a347c-107">It has the same core functionality and plug-in model as the Media Foundation EVR media sink.</span></span>

<span data-ttu-id="a347c-108">Le filtre DirectShow EVR est documenté dans la documentation du kit de développement logiciel (SDK) Media Foundation ; Pour plus d’informations, consultez [rendu vidéo amélioré](../medfound/enhanced-video-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="a347c-108">The DirectShow EVR filter is documented in the Media Foundation SDK documentation; for more information, see [Enhanced Video Renderer](../medfound/enhanced-video-renderer.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a347c-109">Interfaces de filtre (via <strong>QueryInterface</strong>)</span><span class="sxs-lookup"><span data-stu-id="a347c-109">Filter Interfaces (through <strong>QueryInterface</strong>)</span></span></td>
<td><span data-ttu-id="a347c-110">Interfaces DirectShow :</span><span class="sxs-lookup"><span data-stu-id="a347c-110">DirectShow interfaces:</span></span>
<ul>
<li><span data-ttu-id="a347c-111"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></span><span class="sxs-lookup"><span data-stu-id="a347c-111"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></span></span></li>
<li><span data-ttu-id="a347c-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span><span class="sxs-lookup"><span data-stu-id="a347c-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span></span></li>
<li><span data-ttu-id="a347c-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="a347c-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="a347c-114"><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></span><span class="sxs-lookup"><span data-stu-id="a347c-114"><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></span></span></li>
<li><span data-ttu-id="a347c-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>IMediaEventSink</strong></a></span><span class="sxs-lookup"><span data-stu-id="a347c-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>IMediaEventSink</strong></a></span></span></li>
<li><span data-ttu-id="a347c-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="a347c-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></li>
<li><span data-ttu-id="a347c-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="a347c-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="a347c-118"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="a347c-118"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span></span></li>
</ul>
<span data-ttu-id="a347c-119">Interfaces de Media Foundation :</span><span class="sxs-lookup"><span data-stu-id="a347c-119">Media Foundation interfaces:</span></span><br/>
<ul>
<li><span data-ttu-id="a347c-120"><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="a347c-120"><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a></span></span></li>
<li><span data-ttu-id="a347c-121"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></span><span class="sxs-lookup"><span data-stu-id="a347c-121"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></span></span></li>
<li><span data-ttu-id="a347c-122"><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMFVideoPositionMapper</strong></a></span><span class="sxs-lookup"><span data-stu-id="a347c-122"><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMFVideoPositionMapper</strong></a></span></span></li>
<li><span data-ttu-id="a347c-123"><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>IMFVideoRenderer</strong></a></span><span class="sxs-lookup"><span data-stu-id="a347c-123"><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>IMFVideoRenderer</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a347c-124">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="a347c-124">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="a347c-125">Variable, en fonction du pilote Graphics.</span><span class="sxs-lookup"><span data-stu-id="a347c-125">Variable, depending on the graphics driver.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a347c-126">Interfaces pin d’entrée (via <strong>QueryInterface</strong>)</span><span class="sxs-lookup"><span data-stu-id="a347c-126">Input Pin Interfaces (through <strong>QueryInterface</strong>)</span></span></td>
<td><span data-ttu-id="a347c-127">Interfaces DirectShow :</span><span class="sxs-lookup"><span data-stu-id="a347c-127">DirectShow interfaces:</span></span>
<ul>
<li><span data-ttu-id="a347c-128"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="a347c-128"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
<li><span data-ttu-id="a347c-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="a347c-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="a347c-130"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="a347c-130"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
</ul>
<span data-ttu-id="a347c-131">Interfaces de Media Foundation :</span><span class="sxs-lookup"><span data-stu-id="a347c-131">Media Foundation interfaces:</span></span><br/>
<ul>
<li><span data-ttu-id="a347c-132"><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a></span><span class="sxs-lookup"><span data-stu-id="a347c-132"><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a></span></span></li>
<li><span data-ttu-id="a347c-133"><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="a347c-133"><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a></span></span></li>
<li><span data-ttu-id="a347c-134"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></span><span class="sxs-lookup"><span data-stu-id="a347c-134"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a347c-135">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="a347c-135">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="a347c-136">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="a347c-136">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a347c-137">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="a347c-137">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="a347c-138">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="a347c-138">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a347c-139">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="a347c-139">Filter CLSID</span></span></td>
<td><span data-ttu-id="a347c-140">CLSID_EnhancedVideoRenderer</span><span class="sxs-lookup"><span data-stu-id="a347c-140">CLSID_EnhancedVideoRenderer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a347c-141">Exécutable</span><span class="sxs-lookup"><span data-stu-id="a347c-141">Executable</span></span></td>
<td><span data-ttu-id="a347c-142">evr.dll</span><span class="sxs-lookup"><span data-stu-id="a347c-142">evr.dll</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a347c-143"><a href="merit.md">Mérite</a></span><span class="sxs-lookup"><span data-stu-id="a347c-143"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="a347c-144">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="a347c-144">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a347c-145"><a href="filter-categories.md">Catégorie de filtre</a></span><span class="sxs-lookup"><span data-stu-id="a347c-145"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="a347c-146">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="a347c-146">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="a347c-147">Notes</span><span class="sxs-lookup"><span data-stu-id="a347c-147">Remarks</span></span>

<span data-ttu-id="a347c-148">En plus des interfaces exposées via **QueryInterface**, EVR expose d’autres interfaces par le biais de la méthode [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) .</span><span class="sxs-lookup"><span data-stu-id="a347c-148">In addition to the interfaces exposed through **QueryInterface**, the EVR exposes other interfaces through the [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) method.</span></span> <span data-ttu-id="a347c-149">Certaines de ces interfaces sont implémentées par le présentateur EVR ou le mélangeur EVR, plutôt que par le EVR lui-même.</span><span class="sxs-lookup"><span data-stu-id="a347c-149">Some of these interfaces are implemented by the EVR presenter or the EVR mixer, rather than the EVR itself.</span></span> <span data-ttu-id="a347c-150">Si l’application définit un présentateur ou un mélangeur personnalisé sur le EVR, les versions personnalisées peuvent exposer un autre ensemble d’interfaces.</span><span class="sxs-lookup"><span data-stu-id="a347c-150">If the application sets a custom presenter or mixer on the EVR, the custom versions might expose a different set of interfaces.</span></span>



| <span data-ttu-id="a347c-151">Object</span><span class="sxs-lookup"><span data-stu-id="a347c-151">Object</span></span>     | <span data-ttu-id="a347c-152">Identificateur de service</span><span class="sxs-lookup"><span data-stu-id="a347c-152">Service Identifier</span></span>                                              | <span data-ttu-id="a347c-153">Interfaces</span><span class="sxs-lookup"><span data-stu-id="a347c-153">Interfaces</span></span>                                                                                                                                                                                                                                                                                                     |
|------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a347c-154">Filtre EVR</span><span class="sxs-lookup"><span data-stu-id="a347c-154">EVR filter</span></span> | <span data-ttu-id="a347c-155">\_ \_ Service de rendu vidéo Mr \_ (requêtes EVR ou Presenter)</span><span class="sxs-lookup"><span data-stu-id="a347c-155">MR\_VIDEO\_RENDER\_SERVICE(Queries EVR or presenter)</span></span><br/> | [<span data-ttu-id="a347c-156">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="a347c-156">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [<span data-ttu-id="a347c-157">**IMFVideoDisplayControl**</span><span class="sxs-lookup"><span data-stu-id="a347c-157">**IMFVideoDisplayControl**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)<br/> [<span data-ttu-id="a347c-158">**IMFVideoPositionMapper**</span><span class="sxs-lookup"><span data-stu-id="a347c-158">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [<span data-ttu-id="a347c-159">**IMFVideoPresenter**</span><span class="sxs-lookup"><span data-stu-id="a347c-159">**IMFVideoPresenter**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopresenter)<br/>                                                          |
| <span data-ttu-id="a347c-160">Filtre EVR</span><span class="sxs-lookup"><span data-stu-id="a347c-160">EVR filter</span></span> | <span data-ttu-id="a347c-161">\_ \_ Service accélérateur vidéo Mr \_ (requêtes Presenter)</span><span class="sxs-lookup"><span data-stu-id="a347c-161">MR\_VIDEO\_ACCELERATION\_SERVICE(Queries presenter)</span></span><br/>  | [<span data-ttu-id="a347c-162">**IDirect3DDeviceManager9**</span><span class="sxs-lookup"><span data-stu-id="a347c-162">**IDirect3DDeviceManager9**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)                                                                                                                                                                                                                                                      |
| <span data-ttu-id="a347c-163">Filtre EVR</span><span class="sxs-lookup"><span data-stu-id="a347c-163">EVR filter</span></span> | <span data-ttu-id="a347c-164">\_ \_ Service de mixage vidéo Mr \_ (mélangeur de requêtes)</span><span class="sxs-lookup"><span data-stu-id="a347c-164">MR\_VIDEO\_MIXER\_SERVICE(Queries mixer)</span></span><br/>             | [<span data-ttu-id="a347c-165">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="a347c-165">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [<span data-ttu-id="a347c-166">**IMFVideoMixerBitmap**</span><span class="sxs-lookup"><span data-stu-id="a347c-166">**IMFVideoMixerBitmap**</span></span>](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)<br/> [<span data-ttu-id="a347c-167">**IMFVideoMixerControl**</span><span class="sxs-lookup"><span data-stu-id="a347c-167">**IMFVideoMixerControl**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)<br/> [<span data-ttu-id="a347c-168">**IMFVideoPositionMapper**</span><span class="sxs-lookup"><span data-stu-id="a347c-168">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [<span data-ttu-id="a347c-169">**IMFVideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="a347c-169">**IMFVideoProcessor**</span></span>](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)<br/> |
| <span data-ttu-id="a347c-170">Broches d’entrée</span><span class="sxs-lookup"><span data-stu-id="a347c-170">Input pins</span></span> | <span data-ttu-id="a347c-171">\_ \_ service accélérateur vidéo \_ Mr</span><span class="sxs-lookup"><span data-stu-id="a347c-171">MR\_VIDEO\_ACCELERATION\_SERVICE</span></span>                                | [<span data-ttu-id="a347c-172">**IDirectXVideoMemoryConfiguration**</span><span class="sxs-lookup"><span data-stu-id="a347c-172">**IDirectXVideoMemoryConfiguration**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                                                                                                                                                                                                    |



 

<span data-ttu-id="a347c-173">Le EVR peut combiner jusqu’à 16 flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="a347c-173">The EVR can mix up to 16 video streams.</span></span> <span data-ttu-id="a347c-174">Le premier flux d’entrée (broche 0) est appelé le *flux de référence*.</span><span class="sxs-lookup"><span data-stu-id="a347c-174">The first input stream (pin 0) is called the *reference stream*.</span></span> <span data-ttu-id="a347c-175">Le flux de référence apparaît toujours en premier dans l’ordre de plan.</span><span class="sxs-lookup"><span data-stu-id="a347c-175">The reference stream always appears first in the z-order.</span></span> <span data-ttu-id="a347c-176">Tous les flux supplémentaires sont appelés des sous-flux et sont mélangés au-dessus du flux de référence.</span><span class="sxs-lookup"><span data-stu-id="a347c-176">Any additional streams are called substreams, and are mixed on top of the reference stream.</span></span> <span data-ttu-id="a347c-177">L’application peut modifier l’ordre de plan des sous-flux, mais aucun sous-flux ne peut être d’abord dans l’ordre de plan.</span><span class="sxs-lookup"><span data-stu-id="a347c-177">The application can change the z-order of the substreams, but no substream can be first in the z-order.</span></span>

<span data-ttu-id="a347c-178">Le pilote Graphics détermine les formats vidéo pris en charge, mais ils sont généralement limités aux éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="a347c-178">The graphics driver determines which video formats are supported, but typically they are limited to the following:</span></span>

-   <span data-ttu-id="a347c-179">Flux de référence : YUV progressif ou entrelacé, sans alpha par pixel (comme NV12 ou YUY2); ou RGB progressif.</span><span class="sxs-lookup"><span data-stu-id="a347c-179">Reference stream: Progressive or interlaced YUV with no per-pixel alpha (such as NV12 or YUY2); or progressive RGB.</span></span>
-   <span data-ttu-id="a347c-180">Sous-flux : YUV progressifs avec par pixel-alpha, tels que AYUV ou AI44.</span><span class="sxs-lookup"><span data-stu-id="a347c-180">Substreams: Progressive YUV with per-pixel-alpha, such as AYUV or AI44.</span></span>

<span data-ttu-id="a347c-181">Les formats de sous-flux disponibles peuvent dépendre du format du flux de référence.</span><span class="sxs-lookup"><span data-stu-id="a347c-181">The available substream formats might depend on the format of the reference stream.</span></span>

<span data-ttu-id="a347c-182">EVR transfère les commandes de recherche en amont via la broche 0.</span><span class="sxs-lookup"><span data-stu-id="a347c-182">The EVR forwards seek commands upstream through pin 0.</span></span> <span data-ttu-id="a347c-183">Les broches de sous-flux ne transfèrent pas les commandes de recherche.</span><span class="sxs-lookup"><span data-stu-id="a347c-183">The substream pins do not forward seek commands.</span></span> <span data-ttu-id="a347c-184">Il incombe au filtre de la source ou du séparateur de conserver les sous-flux synchronisés avec le flux de référence.</span><span class="sxs-lookup"><span data-stu-id="a347c-184">It is the responsibility of the source or splitter filter to keep the substreams synchronized with the reference stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="a347c-185">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a347c-185">Requirements</span></span>



| <span data-ttu-id="a347c-186">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a347c-186">Requirement</span></span> | <span data-ttu-id="a347c-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="a347c-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a347c-188">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a347c-188">Minimum supported client</span></span><br/> | <span data-ttu-id="a347c-189">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a347c-189">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a347c-190">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a347c-190">Minimum supported server</span></span><br/> | <span data-ttu-id="a347c-191">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a347c-191">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a347c-192">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a347c-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a347c-193">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="a347c-193">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

