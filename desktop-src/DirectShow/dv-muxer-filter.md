---
description: Filtre DV du multiplexeur
ms.assetid: 4dd57202-f4de-40d9-b720-efaba8a60a7c
title: Filtre DV du multiplexeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2154dd1fc1617ff3f717b1ace6e52c9c507a38e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747397"
---
# <a name="dv-muxer-filter"></a><span data-ttu-id="04c71-103">Filtre DV du multiplexeur</span><span class="sxs-lookup"><span data-stu-id="04c71-103">DV Muxer Filter</span></span>

<span data-ttu-id="04c71-104">Ce filtre combine un flux vidéo encodé en vidéo numérique (DV) avec un ou deux flux audio pour produire un flux DV entrelacé.</span><span class="sxs-lookup"><span data-stu-id="04c71-104">This filter combines a digital video (DV)—encoded video stream with one or two audio streams to produce an interleaved DV stream.</span></span> <span data-ttu-id="04c71-105">Pour écrire le flux dans un fichier AVI, connectez ce filtre au filtre [multiplex MUX](avi-mux-filter.md) et connectez le fichier *AVI MUX* au filtre du [writer de fichier](file-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="04c71-105">To write the stream to an AVI file, connect this filter to the [AVI Mux](avi-mux-filter.md) filter and connect the *AVI Mux* to the [File Writer](file-writer-filter.md) filter.</span></span> <span data-ttu-id="04c71-106">Pour plus d’informations, consultez [vidéo numérique dans DirectShow](digital-video-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="04c71-106">For more information, see [Digital Video in DirectShow](digital-video-in-directshow.md).</span></span>



|                                          |                                                                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04c71-107">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="04c71-107">Filter Interfaces</span></span>                        | <span data-ttu-id="04c71-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="04c71-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span>                                                             |
| <span data-ttu-id="04c71-109">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="04c71-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="04c71-110">**Vidéo**: MediaType \_ Video, MEDIASUBTYPE \_ DVSD, format \_ videoinfo **audio**: MediaType \_ audio, MEDIASUBTYPE \_ PCM, format \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="04c71-110">**Video**: MEDIATYPE\_Video, MEDIASUBTYPE\_dvsd, FORMAT\_VideoInfo **Audio**: MEDIATYPE\_Audio, MEDIASUBTYPE\_PCM, FORMAT\_WaveFormatEx</span></span> |
| <span data-ttu-id="04c71-111">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="04c71-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="04c71-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="04c71-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                 |
| <span data-ttu-id="04c71-113">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="04c71-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="04c71-114">MEDIATYPE \_ entrelacé, MEDIASUBTYPE \_ DVSD, format \_ DvInfo</span><span class="sxs-lookup"><span data-stu-id="04c71-114">MEDIATYPE\_Interleaved, MEDIASUBTYPE\_dvsd, FORMAT\_DvInfo</span></span>                                                                             |
| <span data-ttu-id="04c71-115">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="04c71-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="04c71-116">[**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="04c71-116">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                       |
| <span data-ttu-id="04c71-117">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="04c71-117">Filter CLSID</span></span>                             | <span data-ttu-id="04c71-118">CLSID \_ DVMux</span><span class="sxs-lookup"><span data-stu-id="04c71-118">CLSID\_DVMux</span></span>                                                                                                                           |
| <span data-ttu-id="04c71-119">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="04c71-119">Property Page CLSID</span></span>                      | <span data-ttu-id="04c71-120">Aucune page de propriétés</span><span class="sxs-lookup"><span data-stu-id="04c71-120">No property page</span></span>                                                                                                                       |
| <span data-ttu-id="04c71-121">Exécutable</span><span class="sxs-lookup"><span data-stu-id="04c71-121">Executable</span></span>                               | <span data-ttu-id="04c71-122">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="04c71-122">qdv.dll</span></span>                                                                                                                                |
| [<span data-ttu-id="04c71-123">Mérite</span><span class="sxs-lookup"><span data-stu-id="04c71-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="04c71-124">MÉRITE \_ improbable</span><span class="sxs-lookup"><span data-stu-id="04c71-124">MERIT\_UNLIKELY</span></span>                                                                                                                        |
| [<span data-ttu-id="04c71-125">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="04c71-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="04c71-126">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="04c71-126">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="04c71-127">Notes</span><span class="sxs-lookup"><span data-stu-id="04c71-127">Remarks</span></span>

<span data-ttu-id="04c71-128">Le du multiplexeur DV peut créer deux broches d’entrée audio.</span><span class="sxs-lookup"><span data-stu-id="04c71-128">The DV Muxer can create two audio input pins.</span></span> <span data-ttu-id="04c71-129">Il prend en charge les formats audio indiqués dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="04c71-129">It supports the audio formats shown in the following table.</span></span>



<span data-ttu-id="04c71-130">Code confidentiel audio 1</span><span class="sxs-lookup"><span data-stu-id="04c71-130">Audio Pin 1</span></span>

<span data-ttu-id="04c71-131">Code confidentiel audio 2</span><span class="sxs-lookup"><span data-stu-id="04c71-131">Audio Pin 2</span></span>

<span data-ttu-id="04c71-132">Format de sortie</span><span class="sxs-lookup"><span data-stu-id="04c71-132">Output Format</span></span>

<span data-ttu-id="04c71-133">Taux d’échantillonnage (kHz)</span><span class="sxs-lookup"><span data-stu-id="04c71-133">Sample Rate (kHz)</span></span>

<span data-ttu-id="04c71-134">Bits/échantillon</span><span class="sxs-lookup"><span data-stu-id="04c71-134">Bits/Sample</span></span>

<span data-ttu-id="04c71-135">Canaux</span><span class="sxs-lookup"><span data-stu-id="04c71-135">Channels</span></span>

<span data-ttu-id="04c71-136">Échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04c71-136">Sample Rate</span></span>

<span data-ttu-id="04c71-137">Bits/échantillon</span><span class="sxs-lookup"><span data-stu-id="04c71-137">Bits/Sample</span></span>

<span data-ttu-id="04c71-138">Canaux</span><span class="sxs-lookup"><span data-stu-id="04c71-138">Channels</span></span>

<span data-ttu-id="04c71-139">32</span><span class="sxs-lookup"><span data-stu-id="04c71-139">32</span></span>

<span data-ttu-id="04c71-140">16</span><span class="sxs-lookup"><span data-stu-id="04c71-140">16</span></span>

<span data-ttu-id="04c71-141">Mono</span><span class="sxs-lookup"><span data-stu-id="04c71-141">Mono</span></span>

<span data-ttu-id="04c71-142">Non connecté</span><span class="sxs-lookup"><span data-stu-id="04c71-142">Unconnected</span></span>

<span data-ttu-id="04c71-143">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="04c71-143">SD 2 Channel</span></span>

<span data-ttu-id="04c71-144">32</span><span class="sxs-lookup"><span data-stu-id="04c71-144">32</span></span>

<span data-ttu-id="04c71-145">16</span><span class="sxs-lookup"><span data-stu-id="04c71-145">16</span></span>

<span data-ttu-id="04c71-146">Stéréo</span><span class="sxs-lookup"><span data-stu-id="04c71-146">Stereo</span></span>

<span data-ttu-id="04c71-147">Non connecté</span><span class="sxs-lookup"><span data-stu-id="04c71-147">Unconnected</span></span>

<span data-ttu-id="04c71-148">Canal SD 4</span><span class="sxs-lookup"><span data-stu-id="04c71-148">SD 4 Channel</span></span>

<span data-ttu-id="04c71-149">44,1 ou 48</span><span class="sxs-lookup"><span data-stu-id="04c71-149">44.1 or 48</span></span>

<span data-ttu-id="04c71-150">16</span><span class="sxs-lookup"><span data-stu-id="04c71-150">16</span></span>

<span data-ttu-id="04c71-151">Stéréo ou mono</span><span class="sxs-lookup"><span data-stu-id="04c71-151">Stereo or Mono</span></span>

<span data-ttu-id="04c71-152">Non connecté</span><span class="sxs-lookup"><span data-stu-id="04c71-152">Unconnected</span></span>

<span data-ttu-id="04c71-153">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="04c71-153">SD 2 Channel</span></span>

<span data-ttu-id="04c71-154">Non connecté</span><span class="sxs-lookup"><span data-stu-id="04c71-154">Unconnected</span></span>

<span data-ttu-id="04c71-155">32</span><span class="sxs-lookup"><span data-stu-id="04c71-155">32</span></span>

<span data-ttu-id="04c71-156">16</span><span class="sxs-lookup"><span data-stu-id="04c71-156">16</span></span>

<span data-ttu-id="04c71-157">Stéréo ou mono</span><span class="sxs-lookup"><span data-stu-id="04c71-157">Stereo or Mono</span></span>

<span data-ttu-id="04c71-158">Interdit</span><span class="sxs-lookup"><span data-stu-id="04c71-158">Disallowed</span></span>

<span data-ttu-id="04c71-159">Non connecté</span><span class="sxs-lookup"><span data-stu-id="04c71-159">Unconnected</span></span>

<span data-ttu-id="04c71-160">44,1 ou 48</span><span class="sxs-lookup"><span data-stu-id="04c71-160">44.1 or 48</span></span>

<span data-ttu-id="04c71-161">16</span><span class="sxs-lookup"><span data-stu-id="04c71-161">16</span></span>

<span data-ttu-id="04c71-162">Mono</span><span class="sxs-lookup"><span data-stu-id="04c71-162">Mono</span></span>

<span data-ttu-id="04c71-163">Interdit</span><span class="sxs-lookup"><span data-stu-id="04c71-163">Disallowed</span></span>

<span data-ttu-id="04c71-164">Non connecté</span><span class="sxs-lookup"><span data-stu-id="04c71-164">Unconnected</span></span>

<span data-ttu-id="04c71-165">44,1 ou 48</span><span class="sxs-lookup"><span data-stu-id="04c71-165">44.1 or 48</span></span>

<span data-ttu-id="04c71-166">16</span><span class="sxs-lookup"><span data-stu-id="04c71-166">16</span></span>

<span data-ttu-id="04c71-167">Stéréo</span><span class="sxs-lookup"><span data-stu-id="04c71-167">Stereo</span></span>

<span data-ttu-id="04c71-168">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="04c71-168">SD 2 Channel</span></span>

<span data-ttu-id="04c71-169">32</span><span class="sxs-lookup"><span data-stu-id="04c71-169">32</span></span>

<span data-ttu-id="04c71-170">16</span><span class="sxs-lookup"><span data-stu-id="04c71-170">16</span></span>

<span data-ttu-id="04c71-171">Mono</span><span class="sxs-lookup"><span data-stu-id="04c71-171">Mono</span></span>

<span data-ttu-id="04c71-172">32</span><span class="sxs-lookup"><span data-stu-id="04c71-172">32</span></span>

<span data-ttu-id="04c71-173">16</span><span class="sxs-lookup"><span data-stu-id="04c71-173">16</span></span>

<span data-ttu-id="04c71-174">Mono</span><span class="sxs-lookup"><span data-stu-id="04c71-174">Mono</span></span>

<span data-ttu-id="04c71-175">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="04c71-175">SD 2 Channel</span></span>

<span data-ttu-id="04c71-176">32</span><span class="sxs-lookup"><span data-stu-id="04c71-176">32</span></span>

<span data-ttu-id="04c71-177">16</span><span class="sxs-lookup"><span data-stu-id="04c71-177">16</span></span>

<span data-ttu-id="04c71-178">Stéréo ou mono\*</span><span class="sxs-lookup"><span data-stu-id="04c71-178">Stereo or Mono\*</span></span>

<span data-ttu-id="04c71-179">32</span><span class="sxs-lookup"><span data-stu-id="04c71-179">32</span></span>

<span data-ttu-id="04c71-180">16</span><span class="sxs-lookup"><span data-stu-id="04c71-180">16</span></span>

<span data-ttu-id="04c71-181">Stéréo ou mono\*</span><span class="sxs-lookup"><span data-stu-id="04c71-181">Stereo or Mono\*</span></span>

<span data-ttu-id="04c71-182">Canal SD 4</span><span class="sxs-lookup"><span data-stu-id="04c71-182">SD 4 Channel</span></span>

<span data-ttu-id="04c71-183">44,1</span><span class="sxs-lookup"><span data-stu-id="04c71-183">44.1</span></span>

<span data-ttu-id="04c71-184">16</span><span class="sxs-lookup"><span data-stu-id="04c71-184">16</span></span>

<span data-ttu-id="04c71-185">Mono</span><span class="sxs-lookup"><span data-stu-id="04c71-185">Mono</span></span>

<span data-ttu-id="04c71-186">44,1</span><span class="sxs-lookup"><span data-stu-id="04c71-186">44.1</span></span>

<span data-ttu-id="04c71-187">16</span><span class="sxs-lookup"><span data-stu-id="04c71-187">16</span></span>

<span data-ttu-id="04c71-188">Mono</span><span class="sxs-lookup"><span data-stu-id="04c71-188">Mono</span></span>

<span data-ttu-id="04c71-189">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="04c71-189">SD 2 Channel</span></span>

<span data-ttu-id="04c71-190">48</span><span class="sxs-lookup"><span data-stu-id="04c71-190">48</span></span>

<span data-ttu-id="04c71-191">16</span><span class="sxs-lookup"><span data-stu-id="04c71-191">16</span></span>

<span data-ttu-id="04c71-192">Mono</span><span class="sxs-lookup"><span data-stu-id="04c71-192">Mono</span></span>

<span data-ttu-id="04c71-193">48</span><span class="sxs-lookup"><span data-stu-id="04c71-193">48</span></span>

<span data-ttu-id="04c71-194">16</span><span class="sxs-lookup"><span data-stu-id="04c71-194">16</span></span>

<span data-ttu-id="04c71-195">Mono</span><span class="sxs-lookup"><span data-stu-id="04c71-195">Mono</span></span>

<span data-ttu-id="04c71-196">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="04c71-196">SD 2 Channel</span></span>

<span data-ttu-id="04c71-197">\* Si au moins une broche d’entrée est stéréo.</span><span class="sxs-lookup"><span data-stu-id="04c71-197">\* If at least one input pin is stereo.</span></span>



 

<span data-ttu-id="04c71-198">Dans le cadre de cette table, la broche audio 1 est définie comme la première broche d’entrée connectée à une source audio, et la broche audio 2 est définie comme deuxième broche d’entrée connectée à une source audio.</span><span class="sxs-lookup"><span data-stu-id="04c71-198">For the purpose of this table, audio pin 1 is defined as the first input pin connected to an audio source, and audio pin 2 is defined as the second input pin connected to an audio source.</span></span> <span data-ttu-id="04c71-199">Une fois qu’une broche audio est connectée, ce schéma de numérotation reste effectif, à moins que les deux broches audio soient déconnectées.</span><span class="sxs-lookup"><span data-stu-id="04c71-199">Once an audio pin is connected, this numbering scheme remains in effect unless both audio pins are disconnected.</span></span> <span data-ttu-id="04c71-200">Par exemple, si vous connectez les deux broches audio, puis déconnectez la broche audio 1, le code confidentiel restant est toujours considéré comme étant pin 2.</span><span class="sxs-lookup"><span data-stu-id="04c71-200">For example, if you connect both audio pins and then disconnect audio pin 1, the remaining pin is still considered pin 2.</span></span>

<span data-ttu-id="04c71-201">L’audio fourni à la broche 1 est enregistré dans le premier bloc audio des images DV (CH1), et l’audio fourni au code confidentiel 2 est enregistré dans le deuxième bloc audio (CH2).</span><span class="sxs-lookup"><span data-stu-id="04c71-201">Audio supplied to pin 1 is recorded to the first audio block of the DV frames (CH1), and audio supplied to pin 2 is recorded to the second audio block (CH2).</span></span> <span data-ttu-id="04c71-202">Exception : si le filtre a une seule entrée stéréo à 44,1 kHz ou 48 kHz, le canal audio de gauche est enregistré dans le premier bloc audio, et le canal audio de droite est enregistré dans le second bloc audio.</span><span class="sxs-lookup"><span data-stu-id="04c71-202">Exception: if the filter has a single stereo input at 44.1 kHz or 48 kHz, the left audio channel is recorded to the first audio block, and the right audio channel is recorded to the second audio block.</span></span>

<span data-ttu-id="04c71-203">Pour la sortie SD à 4 canaux : si l’entrée est stéréo, la piste de gauche est enregistrée en CHa ou CHc, et la piste appropriée est enregistrée dans CHb ou CHd.</span><span class="sxs-lookup"><span data-stu-id="04c71-203">For SD 4-channel output: If the input is stereo, the left track is recorded to CHa or CHc, and the right track is recorded to CHb or CHd.</span></span> <span data-ttu-id="04c71-204">Si l’entrée est mono, l’audio est enregistré dans CHa ou CHc, et CHb et CHd sont silencieux.</span><span class="sxs-lookup"><span data-stu-id="04c71-204">If the input is mono, the audio is recorded to CHa or CHc, and CHb and CHd are silent.</span></span>

<span data-ttu-id="04c71-205">En connectant et déconnectant le code PIN audio 1, il est possible d’atteindre un format non autorisé.</span><span class="sxs-lookup"><span data-stu-id="04c71-205">By connecting and disconnecting audio pin 1, it is possible to reach a disallowed format.</span></span> <span data-ttu-id="04c71-206">Dans ce cas, la méthode [**IMediaFilter ::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) du filtre retourne VFW \_ E \_ non \_ connecté.</span><span class="sxs-lookup"><span data-stu-id="04c71-206">In that case, the filter's [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method returns VFW\_E\_NOT\_CONNECTED.</span></span> <span data-ttu-id="04c71-207">Cette limitation empêche une situation dans laquelle le premier bloc audio n’a pas de son, mais le second bloc audio est audio.</span><span class="sxs-lookup"><span data-stu-id="04c71-207">This limitation prevents a situation in which the first audio block has no audio, but the second audio block does have audio.</span></span> <span data-ttu-id="04c71-208">Le deuxième bloc doit avoir un audio uniquement si le premier bloc a également du son.</span><span class="sxs-lookup"><span data-stu-id="04c71-208">The second block should have audio only if the first block also has audio.</span></span>

<span data-ttu-id="04c71-209">Le du multiplexeur DV n’autorise pas les entrées audio avec différents taux d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="04c71-209">The DV Muxer does not permit audio inputs with different sampling rates.</span></span> <span data-ttu-id="04c71-210">Toutefois, les méthodes de création de graphiques telles que [**IGraphBuilder :: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) ajoutent généralement le filtre de [wrappers ACM](acm-wrapper-filter.md) , qui convertit le deuxième flux audio pour qu’il corresponde au taux d’échantillonnage du premier flux.</span><span class="sxs-lookup"><span data-stu-id="04c71-210">However, graph-building methods such as [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) will typically add the [ACM Wrapper](acm-wrapper-filter.md) filter, which will convert the second audio stream to match the first stream's sampling rate.</span></span>

<span data-ttu-id="04c71-211">Si l’entrée audio est 48 kHz ou 32 kHz, la sortie audio est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="04c71-211">If the audio input is 48 kHz or 32 kHz, the audio output is locked.</span></span> <span data-ttu-id="04c71-212">(Il n’est pas possible de verrouiller l’audio 44,1-kHz.)</span><span class="sxs-lookup"><span data-stu-id="04c71-212">(It is not possible to lock 44.1-kHz audio.)</span></span>

<span data-ttu-id="04c71-213">Si aucune broche audio n’est connectée, la sortie contient les données audio des images DV entrantes.</span><span class="sxs-lookup"><span data-stu-id="04c71-213">If no audio pins are connected, the output contains the audio data from the incoming DV frames.</span></span> <span data-ttu-id="04c71-214">Il peut s’agir d’un silence ou de données audio valides.</span><span class="sxs-lookup"><span data-stu-id="04c71-214">This might be silence, or valid audio data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04c71-215">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="04c71-215">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04c71-216">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="04c71-216">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="04c71-217">Vidéo numérique dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="04c71-217">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



