---
description: Cette section décrit des exemples d’applications qui montrent comment utiliser Media Foundation. Encoding SamplesPlayback SamplesPlug-InsSource Reader SamplesVideo CaptureMiscellaneous SamplesDeprecated ou des rubriques obsolètes SamplesRelated
ms.assetid: 9d460107-ec12-4df5-a7a9-d19943685599
title: Exemples du kit de développement logiciel Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f335b5ba744b098efdb7570aa861ad36fc9216cf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761419"
---
# <a name="media-foundation-sdk-samples"></a><span data-ttu-id="d46db-103">Exemples du kit de développement logiciel Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d46db-103">Media Foundation SDK Samples</span></span>

<span data-ttu-id="d46db-104">Cette section décrit des exemples d’applications qui montrent comment utiliser Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d46db-104">This section describes sample applications that demonstrate how to use Media Foundation.</span></span>

-   [<span data-ttu-id="d46db-105">Exemples d’encodage</span><span class="sxs-lookup"><span data-stu-id="d46db-105">Encoding Samples</span></span>](#encoding-samples)
-   [<span data-ttu-id="d46db-106">Exemples de lecture</span><span class="sxs-lookup"><span data-stu-id="d46db-106">Playback Samples</span></span>](#playback-samples)
-   [<span data-ttu-id="d46db-107">Plug-ins</span><span class="sxs-lookup"><span data-stu-id="d46db-107">Plug-Ins</span></span>](#plug-ins)
-   [<span data-ttu-id="d46db-108">Exemples de lecteur source</span><span class="sxs-lookup"><span data-stu-id="d46db-108">Source Reader Samples</span></span>](#source-reader-samples)
-   [<span data-ttu-id="d46db-109">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="d46db-109">Video Capture</span></span>](#video-capture)
-   [<span data-ttu-id="d46db-110">Exemples divers</span><span class="sxs-lookup"><span data-stu-id="d46db-110">Miscellaneous Samples</span></span>](#miscellaneous-samples)
-   [<span data-ttu-id="d46db-111">Exemples obsolètes ou obsolètes</span><span class="sxs-lookup"><span data-stu-id="d46db-111">Deprecated or Obsolete Samples</span></span>](#deprecated-or-obsolete-samples)
-   [<span data-ttu-id="d46db-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d46db-112">Related topics</span></span>](#related-topics)

## <a name="encoding-samples"></a><span data-ttu-id="d46db-113">Exemples d’encodage</span><span class="sxs-lookup"><span data-stu-id="d46db-113">Encoding Samples</span></span>



| <span data-ttu-id="d46db-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="d46db-114">Sample</span></span>                            | <span data-ttu-id="d46db-115">Description</span><span class="sxs-lookup"><span data-stu-id="d46db-115">Description</span></span>                                                 |
|-----------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="d46db-116">Transcoder</span><span class="sxs-lookup"><span data-stu-id="d46db-116">Transcode</span></span>](transcode-sample.md) | <span data-ttu-id="d46db-117">Montre comment recoder un fichier multimédia au format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d46db-117">Shows how to reencode a media file to Windows Media format.</span></span> |



 

## <a name="playback-samples"></a><span data-ttu-id="d46db-118">Exemples de lecture</span><span class="sxs-lookup"><span data-stu-id="d46db-118">Playback Samples</span></span>



| <span data-ttu-id="d46db-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="d46db-119">Sample</span></span>                                            | <span data-ttu-id="d46db-120">Description</span><span class="sxs-lookup"><span data-stu-id="d46db-120">Description</span></span>                                                                                                                                                                                                     |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d46db-121">[BasicPlayback](/previous-versions//bb970475(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d46db-121">[BasicPlayback](/previous-versions//bb970475(v=vs.85))</span></span>          | <span data-ttu-id="d46db-122">Lit des fichiers audio et vidéo à l’aide de la [session multimédia](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="d46db-122">Plays audio and video files by using the [Media Session](media-session.md).</span></span> <span data-ttu-id="d46db-123">Cet exemple montre comment créer des topologies de lecture, contrôler la session multimédia et recevoir des événements de session lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="d46db-123">This sample demonstrates how to create playback topologies, control the Media Session, and receive session events during playback.</span></span> |
| <span data-ttu-id="d46db-124">[MFPlayer](/previous-versions//bb970516(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d46db-124">[MFPlayer](/previous-versions//bb970516(v=vs.85))</span></span>                    | <span data-ttu-id="d46db-125">Illustre certaines fonctions de lecture qui ne sont pas incluses dans l’exemple [BasicPlayback](/previous-versions//bb970475(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d46db-125">Demonstrates some playback functions that are not included in the [BasicPlayback](/previous-versions//bb970475(v=vs.85)) sample.</span></span>                                                                                              |
| [<span data-ttu-id="d46db-126">ProtectedPlayback</span><span class="sxs-lookup"><span data-stu-id="d46db-126">ProtectedPlayback</span></span>](protectedplayback-sample.md) | <span data-ttu-id="d46db-127">Lit les fichiers audio et vidéo protégés.</span><span class="sxs-lookup"><span data-stu-id="d46db-127">Plays protected audio and video files.</span></span> <span data-ttu-id="d46db-128">Cet exemple montre comment utiliser la session PMP (Protected Media Path) et comment utiliser les objets activateur du contenu.</span><span class="sxs-lookup"><span data-stu-id="d46db-128">This sample shows how to use the protected media path (PMP) session and how to use content enabler objects.</span></span>                                                              |



 

## <a name="plug-ins"></a><span data-ttu-id="d46db-129">Plug-Ins</span><span class="sxs-lookup"><span data-stu-id="d46db-129">Plug-Ins</span></span>



| <span data-ttu-id="d46db-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="d46db-130">Sample</span></span>                                       | <span data-ttu-id="d46db-131">Sub-Area</span><span class="sxs-lookup"><span data-stu-id="d46db-131">Sub-Area</span></span>                         | <span data-ttu-id="d46db-132">Description</span><span class="sxs-lookup"><span data-stu-id="d46db-132">Description</span></span>                                                                                            |
|----------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d46db-133">Décodeur</span><span class="sxs-lookup"><span data-stu-id="d46db-133">Decoder</span></span>](decoder-sample.md)                | <span data-ttu-id="d46db-134">Media Foundation transformer (MFT)</span><span class="sxs-lookup"><span data-stu-id="d46db-134">Media Foundation transform (MFT)</span></span> | <span data-ttu-id="d46db-135">Décodeur vidéo.</span><span class="sxs-lookup"><span data-stu-id="d46db-135">Video decoder.</span></span>                                                                                         |
| [<span data-ttu-id="d46db-136">EVRPresenter</span><span class="sxs-lookup"><span data-stu-id="d46db-136">EVRPresenter</span></span>](evrpresenter-sample.md)      | <span data-ttu-id="d46db-137">Divers</span><span class="sxs-lookup"><span data-stu-id="d46db-137">Miscellaneous</span></span>                    | <span data-ttu-id="d46db-138">Présentateur personnalisé pour le [convertisseur vidéo amélioré](enhanced-video-renderer.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="d46db-138">Custom presenter for the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span>                 |
| [<span data-ttu-id="d46db-139">\_AUDIODELAY MFT</span><span class="sxs-lookup"><span data-stu-id="d46db-139">MFT\_AudioDelay</span></span>](mft-audiodelay-sample.md) | <span data-ttu-id="d46db-140">MFT</span><span class="sxs-lookup"><span data-stu-id="d46db-140">MFT</span></span>                              | <span data-ttu-id="d46db-141">Transformation d’effet audio.</span><span class="sxs-lookup"><span data-stu-id="d46db-141">Audio effect transform.</span></span> <span data-ttu-id="d46db-142">Montre comment écrire une table MFT de base pour le traitement audio.</span><span class="sxs-lookup"><span data-stu-id="d46db-142">Shows how to write a basic MFT for audio processing.</span></span>                           |
| [<span data-ttu-id="d46db-143">\_Nuances de gris MFT</span><span class="sxs-lookup"><span data-stu-id="d46db-143">MFT\_Grayscale</span></span>](mft-grayscale-sample.md)   | <span data-ttu-id="d46db-144">MFT</span><span class="sxs-lookup"><span data-stu-id="d46db-144">MFT</span></span>                              | <span data-ttu-id="d46db-145">Effet vidéo en nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="d46db-145">Grayscale video effect.</span></span> <span data-ttu-id="d46db-146">Montre comment écrire une table MFT de base pour le traitement vidéo.</span><span class="sxs-lookup"><span data-stu-id="d46db-146">Shows how to write a basic MFT for video processing.</span></span>                           |
| [<span data-ttu-id="d46db-147">MPEG1Source</span><span class="sxs-lookup"><span data-stu-id="d46db-147">MPEG1Source</span></span>](mpeg1source-sample.md)        | <span data-ttu-id="d46db-148">Source du média</span><span class="sxs-lookup"><span data-stu-id="d46db-148">Media source</span></span>                     | <span data-ttu-id="d46db-149">Analyse les flux de couche de systèmes MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="d46db-149">Parses MPEG-1 systems-layer streams.</span></span> <span data-ttu-id="d46db-150">Montre comment écrire une source multimédia personnalisée et un gestionnaire de flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="d46db-150">Shows how to write a custom media source and byte-stream handler.</span></span> |
| [<span data-ttu-id="d46db-151">WavSink</span><span class="sxs-lookup"><span data-stu-id="d46db-151">WavSink</span></span>](wavsink-sample.md)                | <span data-ttu-id="d46db-152">Récepteur multimédia</span><span class="sxs-lookup"><span data-stu-id="d46db-152">Media sink</span></span>                       | <span data-ttu-id="d46db-153">Un récepteur d’archive qui écrit des fichiers. wav.</span><span class="sxs-lookup"><span data-stu-id="d46db-153">An archive sink that writes .wav files.</span></span> <span data-ttu-id="d46db-154">Montre comment écrire un récepteur multimédia personnalisé.</span><span class="sxs-lookup"><span data-stu-id="d46db-154">Shows how to write a custom media sink.</span></span>                        |
| [<span data-ttu-id="d46db-155">WavSource</span><span class="sxs-lookup"><span data-stu-id="d46db-155">WavSource</span></span>](wavsource-sample.md)            | <span data-ttu-id="d46db-156">Source du média</span><span class="sxs-lookup"><span data-stu-id="d46db-156">Media source</span></span>                     | <span data-ttu-id="d46db-157">Analyse les fichiers. wav.</span><span class="sxs-lookup"><span data-stu-id="d46db-157">Parses .wav files.</span></span> <span data-ttu-id="d46db-158">Montre comment écrire une source multimédia personnalisée et un gestionnaire de flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="d46db-158">Shows how to write a custom media source and byte-stream handler.</span></span>                   |



 

## <a name="source-reader-samples"></a><span data-ttu-id="d46db-159">Exemples de lecteur source</span><span class="sxs-lookup"><span data-stu-id="d46db-159">Source Reader Samples</span></span>



| <span data-ttu-id="d46db-160">Exemple</span><span class="sxs-lookup"><span data-stu-id="d46db-160">Sample</span></span>                                      | <span data-ttu-id="d46db-161">Description</span><span class="sxs-lookup"><span data-stu-id="d46db-161">Description</span></span>                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="d46db-162">Clip audio</span><span class="sxs-lookup"><span data-stu-id="d46db-162">Audio Clip</span></span>](audio-clip-sample.md)         | <span data-ttu-id="d46db-163">Utilise le [lecteur source](source-reader.md) pour décoder l’audio d’un fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="d46db-163">Uses the [Source Reader](source-reader.md) to decode audio from a media file.</span></span>      |
| [<span data-ttu-id="d46db-164">VideoThumbnail</span><span class="sxs-lookup"><span data-stu-id="d46db-164">VideoThumbnail</span></span>](videothumbnail-sample.md) | <span data-ttu-id="d46db-165">Utilise le [lecteur source](source-reader.md) pour obtenir des frames uniques à partir d’un fichier vidéo.</span><span class="sxs-lookup"><span data-stu-id="d46db-165">Uses the [Source Reader](source-reader.md) to get single frames from a video file.</span></span> |



 

## <a name="video-capture"></a><span data-ttu-id="d46db-166">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="d46db-166">Video Capture</span></span>



| <span data-ttu-id="d46db-167">Exemple</span><span class="sxs-lookup"><span data-stu-id="d46db-167">Sample</span></span>                                        | <span data-ttu-id="d46db-168">Description</span><span class="sxs-lookup"><span data-stu-id="d46db-168">Description</span></span>                                                                                 |
|-----------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d46db-169">MFCaptureD3D</span><span class="sxs-lookup"><span data-stu-id="d46db-169">MFCaptureD3D</span></span>](mfcaptured3d-sample.md)       | <span data-ttu-id="d46db-170">Montre comment afficher un aperçu de la vidéo à partir d’un périphérique de capture vidéo, en utilisant Direct3D pour le rendu de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="d46db-170">Shows how to preview video from a video capture device, using Direct3D to render the video.</span></span> |
| [<span data-ttu-id="d46db-171">MFCaptureToFile</span><span class="sxs-lookup"><span data-stu-id="d46db-171">MFCaptureToFile</span></span>](mfcapturetofile-sample.md) | <span data-ttu-id="d46db-172">Montre comment capturer une vidéo d’une caméra vidéo dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="d46db-172">Shows how to capture video from a video camera to a file.</span></span>                                   |



 

## <a name="miscellaneous-samples"></a><span data-ttu-id="d46db-173">Exemples divers</span><span class="sxs-lookup"><span data-stu-id="d46db-173">Miscellaneous Samples</span></span>



| <span data-ttu-id="d46db-174">Exemple</span><span class="sxs-lookup"><span data-stu-id="d46db-174">Sample</span></span>                                         | <span data-ttu-id="d46db-175">Description</span><span class="sxs-lookup"><span data-stu-id="d46db-175">Description</span></span>                                                                                                                                           |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d46db-176">ASFParser</span><span class="sxs-lookup"><span data-stu-id="d46db-176">ASFParser</span></span>](asfparser-sample.md)              | <span data-ttu-id="d46db-177">Montre comment analyser les données à partir d’un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="d46db-177">Shows how to parse data from an Advanced Systems Format (ASF) file.</span></span>                                                                                   |
| [<span data-ttu-id="d46db-178">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="d46db-178">DXVA-HD</span></span>](dxva-hd-sample.md)                  | <span data-ttu-id="d46db-179">Montre comment utiliser la haute définition de l’accélération vidéo Microsoft DirectX (DXVA-HD).</span><span class="sxs-lookup"><span data-stu-id="d46db-179">Shows how to use Microsoft DirectX Video Acceleration High Definition (DXVA-HD).</span></span>                                                                      |
| [<span data-ttu-id="d46db-180">DXVA2 \_ VideoProc</span><span class="sxs-lookup"><span data-stu-id="d46db-180">DXVA2\_VideoProc</span></span>](dxva2-videoproc-sample.md) | <span data-ttu-id="d46db-181">Utilise l’accélération vidéo DirectX (DXVA) 2,0 pour créer un flux de vidéo de 4:2:2 YUV.</span><span class="sxs-lookup"><span data-stu-id="d46db-181">Uses DirectX Video Acceleration (DXVA) 2.0 to create a stream of 4:2:2 YUV video.</span></span> <span data-ttu-id="d46db-182">Cet exemple montre comment utiliser les fonctionnalités de traitement vidéo d’DXVA.</span><span class="sxs-lookup"><span data-stu-id="d46db-182">This sample shows how to use the video processing features of DXVA.</span></span> |



 

## <a name="deprecated-or-obsolete-samples"></a><span data-ttu-id="d46db-183">Exemples obsolètes ou obsolètes</span><span class="sxs-lookup"><span data-stu-id="d46db-183">Deprecated or Obsolete Samples</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d46db-184">Exemple</span><span class="sxs-lookup"><span data-stu-id="d46db-184">Sample</span></span></th>
<th><span data-ttu-id="d46db-185">Description</span><span class="sxs-lookup"><span data-stu-id="d46db-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d46db-186"><a href="mfplayer2-sample.md">MFPlayer2</a></span><span class="sxs-lookup"><span data-stu-id="d46db-186"><a href="mfplayer2-sample.md">MFPlayer2</a></span></span></td>
<td><span data-ttu-id="d46db-187">Illustre certaines fonctionnalités de lecture avancées de l’API <a href="using-mfplay-for-audio-video-playback.md">MFPlay</a> .</span><span class="sxs-lookup"><span data-stu-id="d46db-187">Demonstrates some advanced playback features of the <a href="using-mfplay-for-audio-video-playback.md">MFPlay</a> API.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d46db-188"><a href="/previous-versions//bb970336(v=vs.85)">PlaybackFX</a></span><span class="sxs-lookup"><span data-stu-id="d46db-188"><a href="/previous-versions//bb970336(v=vs.85)">PlaybackFX</a></span></span></td>
<td><span data-ttu-id="d46db-189">Applique un effet de nuances de gris à la vidéo.</span><span class="sxs-lookup"><span data-stu-id="d46db-189">Applies a grayscale effect to video.</span></span> <span data-ttu-id="d46db-190">Montre comment insérer des MFTs dans une topologie de lecture.</span><span class="sxs-lookup"><span data-stu-id="d46db-190">Shows how to insert MFTs into a playback topology.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d46db-191">Cet exemple n’est plus inclus dans le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="d46db-191">This sample is no longer included in the SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d46db-192"><a href="playlist-sample.md">Playlist</a></span><span class="sxs-lookup"><span data-stu-id="d46db-192"><a href="playlist-sample.md">Playlist</a></span></span></td>
<td><span data-ttu-id="d46db-193">Lit une séquence de fichiers audio à l’aide de la source de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="d46db-193">Plays a sequence of audio files using the sequencer source.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d46db-194">Cet exemple n’est plus inclus dans le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="d46db-194">This sample is no longer included in the SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d46db-195"><a href="simplecapture-sample.md">SimpleCapture</a></span><span class="sxs-lookup"><span data-stu-id="d46db-195"><a href="simplecapture-sample.md">SimpleCapture</a></span></span></td>
<td><span data-ttu-id="d46db-196">Montre comment afficher un aperçu de la vidéo à partir d’un périphérique de capture vidéo, à l’aide de l’API MFPlay.</span><span class="sxs-lookup"><span data-stu-id="d46db-196">Shows how to preview video from a video capture device, using the MFPlay API.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d46db-197"><a href="simpleplay-sample.md">SimplePlay</a></span><span class="sxs-lookup"><span data-stu-id="d46db-197"><a href="simpleplay-sample.md">SimplePlay</a></span></span></td>
<td><span data-ttu-id="d46db-198">Montre comment lire un fichier multimédia à l’aide de l’API MFPlay.</span><span class="sxs-lookup"><span data-stu-id="d46db-198">Shows how to play a media file using the MFPlay API.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="d46db-199">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d46db-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d46db-200">Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d46db-200">Microsoft Media Foundation</span></span>](microsoft-media-foundation-sdk.md)
</dt> <dt>

[<span data-ttu-id="d46db-201">À propos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d46db-201">About Media Foundation</span></span>](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 
