---
description: Filtre DV du multiplexeur
ms.assetid: 4dd57202-f4de-40d9-b720-efaba8a60a7c
title: Filtre DV du multiplexeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013251f2f9c1946aaa0f7b3c95edfd2de81c4d78
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908597"
---
# <a name="dv-muxer-filter"></a><span data-ttu-id="f221d-103">Filtre DV du multiplexeur</span><span class="sxs-lookup"><span data-stu-id="f221d-103">DV Muxer Filter</span></span>

<span data-ttu-id="f221d-104">Ce filtre combine un flux vidéo encodé en vidéo numérique (DV) avec un ou deux flux audio pour produire un flux DV entrelacé.</span><span class="sxs-lookup"><span data-stu-id="f221d-104">This filter combines a digital video (DV)—encoded video stream with one or two audio streams to produce an interleaved DV stream.</span></span> <span data-ttu-id="f221d-105">Pour écrire le flux dans un fichier AVI, connectez ce filtre au filtre [multiplex MUX](avi-mux-filter.md) et connectez le fichier *AVI MUX* au filtre du [writer de fichier](file-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="f221d-105">To write the stream to an AVI file, connect this filter to the [AVI Mux](avi-mux-filter.md) filter and connect the *AVI Mux* to the [File Writer](file-writer-filter.md) filter.</span></span> <span data-ttu-id="f221d-106">Pour plus d’informations, consultez [vidéo numérique dans DirectShow](digital-video-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="f221d-106">For more information, see [Digital Video in DirectShow](digital-video-in-directshow.md).</span></span>



| <span data-ttu-id="f221d-107">Étiquette</span><span class="sxs-lookup"><span data-stu-id="f221d-107">Label</span></span> | <span data-ttu-id="f221d-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="f221d-108">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f221d-109">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="f221d-109">Filter Interfaces</span></span>                        | <span data-ttu-id="f221d-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="f221d-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span>                                                             |
| <span data-ttu-id="f221d-111">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="f221d-111">Input Pin Media Types</span></span>                    | <span data-ttu-id="f221d-112">**Vidéo**: MediaType \_ Video, MEDIASUBTYPE \_ DVSD, format \_ videoinfo **audio**: MediaType \_ audio, MEDIASUBTYPE \_ PCM, format \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="f221d-112">**Video**: MEDIATYPE\_Video, MEDIASUBTYPE\_dvsd, FORMAT\_VideoInfo **Audio**: MEDIATYPE\_Audio, MEDIASUBTYPE\_PCM, FORMAT\_WaveFormatEx</span></span> |
| <span data-ttu-id="f221d-113">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="f221d-113">Input Pin Interfaces</span></span>                     | <span data-ttu-id="f221d-114">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="f221d-114">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                 |
| <span data-ttu-id="f221d-115">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="f221d-115">Output Pin Media Types</span></span>                   | <span data-ttu-id="f221d-116">MEDIATYPE \_ entrelacé, MEDIASUBTYPE \_ DVSD, format \_ DvInfo</span><span class="sxs-lookup"><span data-stu-id="f221d-116">MEDIATYPE\_Interleaved, MEDIASUBTYPE\_dvsd, FORMAT\_DvInfo</span></span>                                                                             |
| <span data-ttu-id="f221d-117">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="f221d-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="f221d-118">[**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="f221d-118">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                       |
| <span data-ttu-id="f221d-119">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="f221d-119">Filter CLSID</span></span>                             | <span data-ttu-id="f221d-120">CLSID \_ DVMux</span><span class="sxs-lookup"><span data-stu-id="f221d-120">CLSID\_DVMux</span></span>                                                                                                                           |
| <span data-ttu-id="f221d-121">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="f221d-121">Property Page CLSID</span></span>                      | <span data-ttu-id="f221d-122">Aucune page de propriétés</span><span class="sxs-lookup"><span data-stu-id="f221d-122">No property page</span></span>                                                                                                                       |
| <span data-ttu-id="f221d-123">Exécutable</span><span class="sxs-lookup"><span data-stu-id="f221d-123">Executable</span></span>                               | <span data-ttu-id="f221d-124">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="f221d-124">qdv.dll</span></span>                                                                                                                                |
| [<span data-ttu-id="f221d-125">Mérite</span><span class="sxs-lookup"><span data-stu-id="f221d-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="f221d-126">MÉRITE \_ improbable</span><span class="sxs-lookup"><span data-stu-id="f221d-126">MERIT\_UNLIKELY</span></span>                                                                                                                        |
| [<span data-ttu-id="f221d-127">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="f221d-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="f221d-128">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="f221d-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="f221d-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="f221d-129">Remarks</span></span>

<span data-ttu-id="f221d-130">Le du multiplexeur DV peut créer deux broches d’entrée audio.</span><span class="sxs-lookup"><span data-stu-id="f221d-130">The DV Muxer can create two audio input pins.</span></span> <span data-ttu-id="f221d-131">Il prend en charge les formats audio indiqués dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f221d-131">It supports the audio formats shown in the following table.</span></span>



<span data-ttu-id="f221d-132">Code confidentiel audio 1</span><span class="sxs-lookup"><span data-stu-id="f221d-132">Audio Pin 1</span></span>

<span data-ttu-id="f221d-133">Code confidentiel audio 2</span><span class="sxs-lookup"><span data-stu-id="f221d-133">Audio Pin 2</span></span>

<span data-ttu-id="f221d-134">Format de sortie</span><span class="sxs-lookup"><span data-stu-id="f221d-134">Output Format</span></span>

<span data-ttu-id="f221d-135">Taux d’échantillonnage (kHz)</span><span class="sxs-lookup"><span data-stu-id="f221d-135">Sample Rate (kHz)</span></span>

<span data-ttu-id="f221d-136">Bits/échantillon</span><span class="sxs-lookup"><span data-stu-id="f221d-136">Bits/Sample</span></span>

<span data-ttu-id="f221d-137">Canaux</span><span class="sxs-lookup"><span data-stu-id="f221d-137">Channels</span></span>

<span data-ttu-id="f221d-138">Échantillonnage</span><span class="sxs-lookup"><span data-stu-id="f221d-138">Sample Rate</span></span>

<span data-ttu-id="f221d-139">Bits/échantillon</span><span class="sxs-lookup"><span data-stu-id="f221d-139">Bits/Sample</span></span>

<span data-ttu-id="f221d-140">Canaux</span><span class="sxs-lookup"><span data-stu-id="f221d-140">Channels</span></span>

<span data-ttu-id="f221d-141">32</span><span class="sxs-lookup"><span data-stu-id="f221d-141">32</span></span>

<span data-ttu-id="f221d-142">16</span><span class="sxs-lookup"><span data-stu-id="f221d-142">16</span></span>

<span data-ttu-id="f221d-143">Mono</span><span class="sxs-lookup"><span data-stu-id="f221d-143">Mono</span></span>

<span data-ttu-id="f221d-144">Non connecté</span><span class="sxs-lookup"><span data-stu-id="f221d-144">Unconnected</span></span>

<span data-ttu-id="f221d-145">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="f221d-145">SD 2 Channel</span></span>

<span data-ttu-id="f221d-146">32</span><span class="sxs-lookup"><span data-stu-id="f221d-146">32</span></span>

<span data-ttu-id="f221d-147">16</span><span class="sxs-lookup"><span data-stu-id="f221d-147">16</span></span>

<span data-ttu-id="f221d-148">Stéréo</span><span class="sxs-lookup"><span data-stu-id="f221d-148">Stereo</span></span>

<span data-ttu-id="f221d-149">Non connecté</span><span class="sxs-lookup"><span data-stu-id="f221d-149">Unconnected</span></span>

<span data-ttu-id="f221d-150">Canal SD 4</span><span class="sxs-lookup"><span data-stu-id="f221d-150">SD 4 Channel</span></span>

<span data-ttu-id="f221d-151">44,1 ou 48</span><span class="sxs-lookup"><span data-stu-id="f221d-151">44.1 or 48</span></span>

<span data-ttu-id="f221d-152">16</span><span class="sxs-lookup"><span data-stu-id="f221d-152">16</span></span>

<span data-ttu-id="f221d-153">Stéréo ou mono</span><span class="sxs-lookup"><span data-stu-id="f221d-153">Stereo or Mono</span></span>

<span data-ttu-id="f221d-154">Non connecté</span><span class="sxs-lookup"><span data-stu-id="f221d-154">Unconnected</span></span>

<span data-ttu-id="f221d-155">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="f221d-155">SD 2 Channel</span></span>

<span data-ttu-id="f221d-156">Non connecté</span><span class="sxs-lookup"><span data-stu-id="f221d-156">Unconnected</span></span>

<span data-ttu-id="f221d-157">32</span><span class="sxs-lookup"><span data-stu-id="f221d-157">32</span></span>

<span data-ttu-id="f221d-158">16</span><span class="sxs-lookup"><span data-stu-id="f221d-158">16</span></span>

<span data-ttu-id="f221d-159">Stéréo ou mono</span><span class="sxs-lookup"><span data-stu-id="f221d-159">Stereo or Mono</span></span>

<span data-ttu-id="f221d-160">Interdit</span><span class="sxs-lookup"><span data-stu-id="f221d-160">Disallowed</span></span>

<span data-ttu-id="f221d-161">Non connecté</span><span class="sxs-lookup"><span data-stu-id="f221d-161">Unconnected</span></span>

<span data-ttu-id="f221d-162">44,1 ou 48</span><span class="sxs-lookup"><span data-stu-id="f221d-162">44.1 or 48</span></span>

<span data-ttu-id="f221d-163">16</span><span class="sxs-lookup"><span data-stu-id="f221d-163">16</span></span>

<span data-ttu-id="f221d-164">Mono</span><span class="sxs-lookup"><span data-stu-id="f221d-164">Mono</span></span>

<span data-ttu-id="f221d-165">Interdit</span><span class="sxs-lookup"><span data-stu-id="f221d-165">Disallowed</span></span>

<span data-ttu-id="f221d-166">Non connecté</span><span class="sxs-lookup"><span data-stu-id="f221d-166">Unconnected</span></span>

<span data-ttu-id="f221d-167">44,1 ou 48</span><span class="sxs-lookup"><span data-stu-id="f221d-167">44.1 or 48</span></span>

<span data-ttu-id="f221d-168">16</span><span class="sxs-lookup"><span data-stu-id="f221d-168">16</span></span>

<span data-ttu-id="f221d-169">Stéréo</span><span class="sxs-lookup"><span data-stu-id="f221d-169">Stereo</span></span>

<span data-ttu-id="f221d-170">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="f221d-170">SD 2 Channel</span></span>

<span data-ttu-id="f221d-171">32</span><span class="sxs-lookup"><span data-stu-id="f221d-171">32</span></span>

<span data-ttu-id="f221d-172">16</span><span class="sxs-lookup"><span data-stu-id="f221d-172">16</span></span>

<span data-ttu-id="f221d-173">Mono</span><span class="sxs-lookup"><span data-stu-id="f221d-173">Mono</span></span>

<span data-ttu-id="f221d-174">32</span><span class="sxs-lookup"><span data-stu-id="f221d-174">32</span></span>

<span data-ttu-id="f221d-175">16</span><span class="sxs-lookup"><span data-stu-id="f221d-175">16</span></span>

<span data-ttu-id="f221d-176">Mono</span><span class="sxs-lookup"><span data-stu-id="f221d-176">Mono</span></span>

<span data-ttu-id="f221d-177">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="f221d-177">SD 2 Channel</span></span>

<span data-ttu-id="f221d-178">32</span><span class="sxs-lookup"><span data-stu-id="f221d-178">32</span></span>

<span data-ttu-id="f221d-179">16</span><span class="sxs-lookup"><span data-stu-id="f221d-179">16</span></span>

<span data-ttu-id="f221d-180">Stéréo ou mono\*</span><span class="sxs-lookup"><span data-stu-id="f221d-180">Stereo or Mono\*</span></span>

<span data-ttu-id="f221d-181">32</span><span class="sxs-lookup"><span data-stu-id="f221d-181">32</span></span>

<span data-ttu-id="f221d-182">16</span><span class="sxs-lookup"><span data-stu-id="f221d-182">16</span></span>

<span data-ttu-id="f221d-183">Stéréo ou mono\*</span><span class="sxs-lookup"><span data-stu-id="f221d-183">Stereo or Mono\*</span></span>

<span data-ttu-id="f221d-184">Canal SD 4</span><span class="sxs-lookup"><span data-stu-id="f221d-184">SD 4 Channel</span></span>

<span data-ttu-id="f221d-185">44,1</span><span class="sxs-lookup"><span data-stu-id="f221d-185">44.1</span></span>

<span data-ttu-id="f221d-186">16</span><span class="sxs-lookup"><span data-stu-id="f221d-186">16</span></span>

<span data-ttu-id="f221d-187">Mono</span><span class="sxs-lookup"><span data-stu-id="f221d-187">Mono</span></span>

<span data-ttu-id="f221d-188">44,1</span><span class="sxs-lookup"><span data-stu-id="f221d-188">44.1</span></span>

<span data-ttu-id="f221d-189">16</span><span class="sxs-lookup"><span data-stu-id="f221d-189">16</span></span>

<span data-ttu-id="f221d-190">Mono</span><span class="sxs-lookup"><span data-stu-id="f221d-190">Mono</span></span>

<span data-ttu-id="f221d-191">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="f221d-191">SD 2 Channel</span></span>

<span data-ttu-id="f221d-192">48</span><span class="sxs-lookup"><span data-stu-id="f221d-192">48</span></span>

<span data-ttu-id="f221d-193">16</span><span class="sxs-lookup"><span data-stu-id="f221d-193">16</span></span>

<span data-ttu-id="f221d-194">Mono</span><span class="sxs-lookup"><span data-stu-id="f221d-194">Mono</span></span>

<span data-ttu-id="f221d-195">48</span><span class="sxs-lookup"><span data-stu-id="f221d-195">48</span></span>

<span data-ttu-id="f221d-196">16</span><span class="sxs-lookup"><span data-stu-id="f221d-196">16</span></span>

<span data-ttu-id="f221d-197">Mono</span><span class="sxs-lookup"><span data-stu-id="f221d-197">Mono</span></span>

<span data-ttu-id="f221d-198">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="f221d-198">SD 2 Channel</span></span>

<span data-ttu-id="f221d-199">\* Si au moins une broche d’entrée est stéréo.</span><span class="sxs-lookup"><span data-stu-id="f221d-199">\* If at least one input pin is stereo.</span></span>



 

<span data-ttu-id="f221d-200">Dans le cadre de cette table, la broche audio 1 est définie comme la première broche d’entrée connectée à une source audio, et la broche audio 2 est définie comme deuxième broche d’entrée connectée à une source audio.</span><span class="sxs-lookup"><span data-stu-id="f221d-200">For the purpose of this table, audio pin 1 is defined as the first input pin connected to an audio source, and audio pin 2 is defined as the second input pin connected to an audio source.</span></span> <span data-ttu-id="f221d-201">Une fois qu’une broche audio est connectée, ce schéma de numérotation reste effectif, à moins que les deux broches audio soient déconnectées.</span><span class="sxs-lookup"><span data-stu-id="f221d-201">Once an audio pin is connected, this numbering scheme remains in effect unless both audio pins are disconnected.</span></span> <span data-ttu-id="f221d-202">Par exemple, si vous connectez les deux broches audio, puis déconnectez la broche audio 1, le code confidentiel restant est toujours considéré comme étant pin 2.</span><span class="sxs-lookup"><span data-stu-id="f221d-202">For example, if you connect both audio pins and then disconnect audio pin 1, the remaining pin is still considered pin 2.</span></span>

<span data-ttu-id="f221d-203">L’audio fourni à la broche 1 est enregistré dans le premier bloc audio des images DV (CH1), et l’audio fourni au code confidentiel 2 est enregistré dans le deuxième bloc audio (CH2).</span><span class="sxs-lookup"><span data-stu-id="f221d-203">Audio supplied to pin 1 is recorded to the first audio block of the DV frames (CH1), and audio supplied to pin 2 is recorded to the second audio block (CH2).</span></span> <span data-ttu-id="f221d-204">Exception : si le filtre a une seule entrée stéréo à 44,1 kHz ou 48 kHz, le canal audio de gauche est enregistré dans le premier bloc audio, et le canal audio de droite est enregistré dans le second bloc audio.</span><span class="sxs-lookup"><span data-stu-id="f221d-204">Exception: if the filter has a single stereo input at 44.1 kHz or 48 kHz, the left audio channel is recorded to the first audio block, and the right audio channel is recorded to the second audio block.</span></span>

<span data-ttu-id="f221d-205">Pour la sortie SD à 4 canaux : si l’entrée est stéréo, la piste de gauche est enregistrée en CHa ou CHc, et la piste appropriée est enregistrée dans CHb ou CHd.</span><span class="sxs-lookup"><span data-stu-id="f221d-205">For SD 4-channel output: If the input is stereo, the left track is recorded to CHa or CHc, and the right track is recorded to CHb or CHd.</span></span> <span data-ttu-id="f221d-206">Si l’entrée est mono, l’audio est enregistré dans CHa ou CHc, et CHb et CHd sont silencieux.</span><span class="sxs-lookup"><span data-stu-id="f221d-206">If the input is mono, the audio is recorded to CHa or CHc, and CHb and CHd are silent.</span></span>

<span data-ttu-id="f221d-207">En connectant et déconnectant le code PIN audio 1, il est possible d’atteindre un format non autorisé.</span><span class="sxs-lookup"><span data-stu-id="f221d-207">By connecting and disconnecting audio pin 1, it is possible to reach a disallowed format.</span></span> <span data-ttu-id="f221d-208">Dans ce cas, la méthode [**IMediaFilter ::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) du filtre retourne VFW \_ E \_ non \_ connecté.</span><span class="sxs-lookup"><span data-stu-id="f221d-208">In that case, the filter's [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method returns VFW\_E\_NOT\_CONNECTED.</span></span> <span data-ttu-id="f221d-209">Cette limitation empêche une situation dans laquelle le premier bloc audio n’a pas de son, mais le second bloc audio est audio.</span><span class="sxs-lookup"><span data-stu-id="f221d-209">This limitation prevents a situation in which the first audio block has no audio, but the second audio block does have audio.</span></span> <span data-ttu-id="f221d-210">Le deuxième bloc doit avoir un audio uniquement si le premier bloc a également du son.</span><span class="sxs-lookup"><span data-stu-id="f221d-210">The second block should have audio only if the first block also has audio.</span></span>

<span data-ttu-id="f221d-211">Le du multiplexeur DV n’autorise pas les entrées audio avec différents taux d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="f221d-211">The DV Muxer does not permit audio inputs with different sampling rates.</span></span> <span data-ttu-id="f221d-212">Toutefois, les méthodes de création de graphiques telles que [**IGraphBuilder :: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) ajoutent généralement le filtre de [wrappers ACM](acm-wrapper-filter.md) , qui convertit le deuxième flux audio pour qu’il corresponde au taux d’échantillonnage du premier flux.</span><span class="sxs-lookup"><span data-stu-id="f221d-212">However, graph-building methods such as [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) will typically add the [ACM Wrapper](acm-wrapper-filter.md) filter, which will convert the second audio stream to match the first stream's sampling rate.</span></span>

<span data-ttu-id="f221d-213">Si l’entrée audio est 48 kHz ou 32 kHz, la sortie audio est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="f221d-213">If the audio input is 48 kHz or 32 kHz, the audio output is locked.</span></span> <span data-ttu-id="f221d-214">(Il n’est pas possible de verrouiller l’audio 44,1-kHz.)</span><span class="sxs-lookup"><span data-stu-id="f221d-214">(It is not possible to lock 44.1-kHz audio.)</span></span>

<span data-ttu-id="f221d-215">Si aucune broche audio n’est connectée, la sortie contient les données audio des images DV entrantes.</span><span class="sxs-lookup"><span data-stu-id="f221d-215">If no audio pins are connected, the output contains the audio data from the incoming DV frames.</span></span> <span data-ttu-id="f221d-216">Il peut s’agir d’un silence ou de données audio valides.</span><span class="sxs-lookup"><span data-stu-id="f221d-216">This might be silence, or valid audio data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f221d-217">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f221d-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f221d-218">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="f221d-218">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="f221d-219">Vidéo numérique dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="f221d-219">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



