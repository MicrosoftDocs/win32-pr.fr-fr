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
# <a name="media-foundation-sdk-samples"></a>Exemples du kit de développement logiciel Media Foundation

Cette section décrit des exemples d’applications qui montrent comment utiliser Media Foundation.

-   [Exemples d’encodage](#encoding-samples)
-   [Exemples de lecture](#playback-samples)
-   [Plug-ins](#plug-ins)
-   [Exemples de lecteur source](#source-reader-samples)
-   [Capture vidéo](#video-capture)
-   [Exemples divers](#miscellaneous-samples)
-   [Exemples obsolètes ou obsolètes](#deprecated-or-obsolete-samples)
-   [Rubriques connexes](#related-topics)

## <a name="encoding-samples"></a>Exemples d’encodage



| Exemple                            | Description                                                 |
|-----------------------------------|-------------------------------------------------------------|
| [Transcoder](transcode-sample.md) | Montre comment recoder un fichier multimédia au format Windows Media. |



 

## <a name="playback-samples"></a>Exemples de lecture



| Exemple                                            | Description                                                                                                                                                                                                     |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BasicPlayback](/previous-versions//bb970475(v=vs.85))          | Lit des fichiers audio et vidéo à l’aide de la [session multimédia](media-session.md). Cet exemple montre comment créer des topologies de lecture, contrôler la session multimédia et recevoir des événements de session lors de la lecture. |
| [MFPlayer](/previous-versions//bb970516(v=vs.85))                    | Illustre certaines fonctions de lecture qui ne sont pas incluses dans l’exemple [BasicPlayback](/previous-versions//bb970475(v=vs.85)) .                                                                                              |
| [ProtectedPlayback](protectedplayback-sample.md) | Lit les fichiers audio et vidéo protégés. Cet exemple montre comment utiliser la session PMP (Protected Media Path) et comment utiliser les objets activateur du contenu.                                                              |



 

## <a name="plug-ins"></a>Plug-Ins



| Exemple                                       | Sub-Area                         | Description                                                                                            |
|----------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------|
| [Décodeur](decoder-sample.md)                | Media Foundation transformer (MFT) | Décodeur vidéo.                                                                                         |
| [EVRPresenter](evrpresenter-sample.md)      | Divers                    | Présentateur personnalisé pour le [convertisseur vidéo amélioré](enhanced-video-renderer.md) (EVR).                 |
| [\_AUDIODELAY MFT](mft-audiodelay-sample.md) | MFT                              | Transformation d’effet audio. Montre comment écrire une table MFT de base pour le traitement audio.                           |
| [\_Nuances de gris MFT](mft-grayscale-sample.md)   | MFT                              | Effet vidéo en nuances de gris. Montre comment écrire une table MFT de base pour le traitement vidéo.                           |
| [MPEG1Source](mpeg1source-sample.md)        | Source du média                     | Analyse les flux de couche de systèmes MPEG-1. Montre comment écrire une source multimédia personnalisée et un gestionnaire de flux d’octets. |
| [WavSink](wavsink-sample.md)                | Récepteur multimédia                       | Un récepteur d’archive qui écrit des fichiers. wav. Montre comment écrire un récepteur multimédia personnalisé.                        |
| [WavSource](wavsource-sample.md)            | Source du média                     | Analyse les fichiers. wav. Montre comment écrire une source multimédia personnalisée et un gestionnaire de flux d’octets.                   |



 

## <a name="source-reader-samples"></a>Exemples de lecteur source



| Exemple                                      | Description                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [Clip audio](audio-clip-sample.md)         | Utilise le [lecteur source](source-reader.md) pour décoder l’audio d’un fichier multimédia.      |
| [VideoThumbnail](videothumbnail-sample.md) | Utilise le [lecteur source](source-reader.md) pour obtenir des frames uniques à partir d’un fichier vidéo. |



 

## <a name="video-capture"></a>Capture vidéo



| Exemple                                        | Description                                                                                 |
|-----------------------------------------------|---------------------------------------------------------------------------------------------|
| [MFCaptureD3D](mfcaptured3d-sample.md)       | Montre comment afficher un aperçu de la vidéo à partir d’un périphérique de capture vidéo, en utilisant Direct3D pour le rendu de la vidéo. |
| [MFCaptureToFile](mfcapturetofile-sample.md) | Montre comment capturer une vidéo d’une caméra vidéo dans un fichier.                                   |



 

## <a name="miscellaneous-samples"></a>Exemples divers



| Exemple                                         | Description                                                                                                                                           |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ASFParser](asfparser-sample.md)              | Montre comment analyser les données à partir d’un fichier ASF (Advanced Systems Format).                                                                                   |
| [DXVA-HD](dxva-hd-sample.md)                  | Montre comment utiliser la haute définition de l’accélération vidéo Microsoft DirectX (DXVA-HD).                                                                      |
| [DXVA2 \_ VideoProc](dxva2-videoproc-sample.md) | Utilise l’accélération vidéo DirectX (DXVA) 2,0 pour créer un flux de vidéo de 4:2:2 YUV. Cet exemple montre comment utiliser les fonctionnalités de traitement vidéo d’DXVA. |



 

## <a name="deprecated-or-obsolete-samples"></a>Exemples obsolètes ou obsolètes



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Exemple</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfplayer2-sample.md">MFPlayer2</a></td>
<td>Illustre certaines fonctionnalités de lecture avancées de l’API <a href="using-mfplay-for-audio-video-playback.md">MFPlay</a> .</td>
</tr>
<tr class="even">
<td><a href="/previous-versions//bb970336(v=vs.85)">PlaybackFX</a></td>
<td>Applique un effet de nuances de gris à la vidéo. Montre comment insérer des MFTs dans une topologie de lecture.<br/>
<blockquote>
[!Note]<br />
Cet exemple n’est plus inclus dans le kit de développement logiciel (SDK).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="playlist-sample.md">Playlist</a></td>
<td>Lit une séquence de fichiers audio à l’aide de la source de Sequencer.<br/>
<blockquote>
[!Note]<br />
Cet exemple n’est plus inclus dans le kit de développement logiciel (SDK).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="simplecapture-sample.md">SimpleCapture</a></td>
<td>Montre comment afficher un aperçu de la vidéo à partir d’un périphérique de capture vidéo, à l’aide de l’API MFPlay.</td>
</tr>
<tr class="odd">
<td><a href="simpleplay-sample.md">SimplePlay</a></td>
<td>Montre comment lire un fichier multimédia à l’aide de l’API MFPlay.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> <dt>

[À propos de Media Foundation](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 
