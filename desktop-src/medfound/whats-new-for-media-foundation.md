---
description: Microsoft Media Foundation a été introduite dans Windows Vista comme remplacement de DirectShow. bien entendu, DirectShow est toujours pris en charge dans Windows 7, mais les développeurs sont encouragés à utiliser Media Foundation dans leurs nouvelles applications multimédias numériques.
ms.assetid: c345c0d9-5325-4f73-b9ec-1673ad10e3e4
title: Nouveautés pour Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0270c28e5aca2a1f0fdad893743a1e8fb630fa5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231701"
---
# <a name="whats-new-for-media-foundation"></a>Nouveautés de Media Foundation

Microsoft Media Foundation a été introduite dans Windows Vista comme remplacement de DirectShow. bien entendu, DirectShow est toujours pris en charge dans Windows 7, mais les développeurs sont encouragés à utiliser Media Foundation dans leurs nouvelles applications multimédias numériques.

Les améliorations apportées à Media Foundation peuvent être résumées comme suit :

-   Meilleure prise en charge du format, y compris MPEG-4
-   Prise en charge des périphériques de capture et des codecs matériels
-   Modèle de programmation simplifié
-   Améliorations apportées à la plateforme

## <a name="better-format-support"></a>Meilleure prise en charge du format

le pipeline audio/video de Media Foundation a été implémenté dans Windows Vista, mais il prenait en charge un ensemble limité de formats et de conteneurs de fichiers, ce qui signifiait que certaines applications devaient revenir sur des technologies plus anciennes, comme DirectShow. dans Windows 7, Media Foundation comprend les nouveaux codecs, sources de média et récepteurs de média suivants :

-   Décodeur AAC
-   Encodeur AAC
-   Source de fichier AVI/WAVE
-   Décodeur vidéo DV
-   Décodeur vidéo H. 264
-   Encodeur vidéo H. 264
-   Décodeur MJPEG
-   Récepteur de fichiers MP3\*
-   Source de fichier MP4/3GP
-   Récepteur de fichiers MP4/3GP

> [!Note]  
> Le récepteur de fichiers MP3 n’inclut pas d’encodeur audio MP3.

 

Pour plus d’informations, consultez [formats multimédias pris en charge dans Media Foundation](supported-media-formats-in-media-foundation.md).

## <a name="hardware-device-support"></a>Prise en charge des périphériques matériels

Media Foundation prend désormais en charge les types suivants de périphériques matériels dans le pipeline audio/vidéo :

-   Appareils de capture vidéo UVC 1,1, tels que les webcams
-   Périphériques de capture audio
-   Encodeurs et décodeurs matériels
-   Processeurs vidéo matériels, tels que les convertisseurs d’espace colorimétrique

Les codecs matériels peuvent effectuer un transcodage vidéo très rapide. par exemple, une application peut transférer des fichiers Windows Media Video (WMV) vers un téléphone portable qui prend uniquement en charge les fichiers 3gp. À l’aide d’un encodeur matériel, l’application peut Transcoder le fichier dans le backgound, juste avant de le transférer à l’appareil.

Les périphériques matériels sont représentés en Media Foundation par un objet proxy et sont utilisés dans le pipeline, comme les composants logiciels.

## <a name="simplified-programming-model"></a>Modèle de programmation simplifié

dans Windows Vista, Media Foundation exposé un ensemble relativement bas d’api. Ces API sont flexibles, mais trop complexes pour les tâches simples. Windows 7 ajoute de nouvelles api de haut niveau qui simplifient l’écriture d’applications multimédias en C++. Ces nouvelles API de haut niveau sont les suivantes.



| API                                | Description                                                                                                                                                                                                                                                                                                    |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Lecteur source](source-reader.md) | Le lecteur source extrait des données brutes ou décodées à partir d’un fichier multimédia. Par exemple, vous pouvez utiliser le lecteur source pour obtenir des bitmaps miniatures à partir d’un fichier vidéo ou pour analyser les données de forme d’onde dans un fichier audio. Vous pouvez également utiliser le lecteur source pour obtenir des données en temps réel à partir d’un périphérique de capture audio ou vidéo. <br/> |
| [Enregistreur du récepteur](sink-writer.md)     | Le writer du récepteur vous permet de créer des fichiers multimédias en passant des données non compressées ou encodées. Par exemple, vous pouvez l’utiliser pour recoder un fichier vidéo ou pour capturer une vidéo en direct à partir d’une webcam dans un fichier.                                                                                                         |
| [API de transcodage](transcode-api.md) | Cette fonctionnalité prend en charge les scénarios d’encodage audio/vidéo les plus courants.<br/>                                                                                                                                                                                                                               |



 

Vous pouvez toujours utiliser les API de bas niveau dans Media Foundation. Vous pouvez le faire si vous avez besoin de davantage de contrôle sur le pipeline audio/vidéo.

## <a name="platform-improvements"></a>Améliorations de la plateforme

Windows 7 comprend de nombreuses améliorations apportées aux api de plateforme Media Foundation sous-jacentes. Les applications avancées peuvent utiliser ces API directement. les autres applications bénéficieront des avantages indirects. Les améliorations incluent :

-   Modifications du pipeline vidéo pour réduire la consommation d’énergie et l’utilisation de la mémoire vidéo.
-   [DXVA-HD](dxva-hd.md): Microsoft DirectX Video Acceleration High Definition (DXVA-HD) est une nouvelle API pour le traitement vidéo accéléré par le matériel. DXVA-HD offre un modèle de composition plus flexible que l’API de traitement vidéo DXVA précédente, et est mieux adapté aux formats vidéo haute définition.
-   Nouveau mécanisme pour énumérer les sources et les décodeurs, y compris les valeurs méritent et une liste préférée/bloquée. Cette fonctionnalité améliore la fiabilité globale du système. Pour plus d'informations, voir les rubriques suivantes :
    -   [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
    -   [**IMFPluginControl**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol)
    -   [Mérite du codec](codec-merit.md)

## <a name="sdk-changes"></a>Modifications du SDK

-   Nouveaux en-têtes et fichiers de bibliothèque : [Media Foundation en-têtes et bibliothèques](media-foundation-headers-and-libraries.md)
-   modifications des DLL et. lib : [modifications de la bibliothèque dans Windows 7](media-foundation-headers-and-libraries.md)
-   Exemples de nouveaux SDK :
    -   [Exemple de clip audio](audio-clip-sample.md)
    -   [DXVA-HD, exemple](dxva-hd-sample.md)
    -   [Exemple MFCaptureD3D](mfcaptured3d-sample.md)
    -   [Exemple MFCaptureToFile](mfcapturetofile-sample.md)
    -   [Exemple de transcodage](transcode-sample.md)
    -   [Exemple VideoThumbnail](videothumbnail-sample.md)
-   Améliorations apportées à [TopoEdit](topoedit.md):
    -   Prise en charge du transcodage. Consultez génération d’une [topologie de transcodage avec TopoEdit](building-a-transcode-topology-with-topoedit.md).
    -   Prise en charge de la capture audio et vidéo. Consultez le [menu Topology (topologie](topology-menu.md)).

## <a name="new-in-windows-8"></a>Nouveautés de Windows 8

voici quelques-unes des nouvelles mises à jour de Media Foundation avec Windows 8 :

-   Le [**IMFCaptureEngine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) contrôle un ou plusieurs périphériques de capture. Consultez les [attributs du moteur de capture](capture-engine-attributes.md) pour obtenir une liste d’attributs. Les autres interfaces associées à capture de média sont [**IMFCapturePhotoSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturephotosink), [**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink), [**IMFCaptureRecordSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturerecordsink), [**IMFCaptureSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink)et [**IMFCaptureSource**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesource).
-   Les extensions de classe de Media Foundation suivantes sont nouvelles pour Windows 8 :
    -   [**IMFMediaEngineEx**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex)
    -   [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex)
    -   [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)
    -   [**IMFSinkWriterEx**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterex)
    -   [**IMFSourceReaderEx**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereaderex)
    -   [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex)
    -   [**IMFWorkQueueServicesEx**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex)
-   Les [API vidéo Direct3D 11](direct3d-11-video-apis.md) sont nouvelles pour Windows 8. Windows 8 les applications de bureau peuvent toujours utiliser l' [api vidéo direct3d 9](direct3d-video-apis.md), mais Windows applications du windows Store doivent utiliser la nouvelle api vidéo direct3d 11. Pour plus d’informations sur Microsoft Direct3D 11 Video [, consultez prise en charge du décodage vidéo Direct3D 11 dans Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md).
-   Des mises à jour et des améliorations ont été apportées aux files d’attente de travail Media Foundation. Pour plus d’informations [, consultez Files d’attente de travail et améliorations du thread](media-foundation-work-queue-and-threading-improvements.md) .
-   Les [encodeurs d’appareil photo UVC 1,5 H. 264](camera-encoder-h264-uvc-1-5.md).
-   pour obtenir la liste des API Media Foundation qui peuvent être utilisées Windows avec les applications du windows store, consultez [Win32 et COM pour Windows les applications du windows store (multimédia)](media-foundation-headers-and-libraries.md).
-   Media Foundation n’est pas inclus avec les éditions N et KN de Windows 8. pour plus d’informations, consultez [Microsoft Windows Media feature Pack pour les Versions N et KN de toutes les éditions de Windows 8](https://support.microsoft.com/kb/2703761).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 




