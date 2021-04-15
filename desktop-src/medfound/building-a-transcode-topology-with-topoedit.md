---
description: Cette rubrique explique comment créer une topologie de transcodage dans TopoEdit.
ms.assetid: 9a7b57f9-f606-4874-9fd3-aa37215f6f20
title: Génération d’une topologie de transcodage avec TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43ef750b4dd54ef05ab7733cc861d7a09dd5d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524647"
---
# <a name="building-a-transcode-topology-with-topoedit"></a>Génération d’une topologie de transcodage avec TopoEdit

Cette rubrique explique comment créer une topologie de transcodage dans TopoEdit.

> [!Note]  
> Cette fonctionnalité nécessite Windows 7

 

## <a name="to-build-a-transcoding-topology"></a>Pour générer une topologie de transcodage

1.  Dans le menu **fichier** , cliquez sur **afficher le transcodage**.

2.  Dans la boîte de dialogue **Sélectionner la source du média** , sélectionnez le fichier source à transcoder.
3.  Cliquez sur **Ouvrir**.
4.  Dans la boîte de dialogue **choisir un profil** de transcodage, sélectionnez l’un des profils d’encodage dans la liste déroulante.
    > [!Note]  
    > Les profils sont chargés à partir du fichier TranscodeProfiles.xml.

     

5.  Dans la boîte de dialogue **choisir le fichier cible** , sélectionnez le nom du fichier de sortie.
6.  TopoEdit crée la topologie de transcodage et affiche les nœuds de topologie dans la fenêtre d’application principale.
7.  Cliquez sur le bouton **lecture** dans la barre d’outils pour exécuter la session multimédia. Attendez la fin de l’encodage.

## <a name="transcodeprofilesxml"></a>TranscodeProfiles.xml

TopoEdit charge les profils d’encodage à partir du fichier TranscodeProfiles.xml. Ce fichier se trouve dans le répertoire bin du SDK Windows.

Le fichier commence par un élément **TedTranscodeProfiles** . Chaque profil commence par un élément **TedTranscodeProfile** . Chaque profil se compose d’un ensemble de valeurs de format `<VALUE_NAME Value="VALUE"/>` . Les valeurs suivantes sont définies :



| Valeur                                                                                                                                                                                                    | Description                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AudioAvgBytesPerSecond"></span><span id="audioavgbytespersecond"></span><span id="AUDIOAVGBYTESPERSECOND"></span>**AudioAvgBytesPerSecond**<br/>                                         | Nombre moyen d’octets par seconde pour le flux audio. Équivaut à l’attribut de [**\_ \_ \_ nombre moyen d' \_ octets \_ par \_ seconde de sortie audio MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md) .<br/>                                                |
| <span id="AudioBitsPerSample"></span><span id="audiobitspersample"></span><span id="AUDIOBITSPERSAMPLE"></span>**AudioBitsPerSample**<br/>                                                         | Nombre de bits par échantillon pour le flux audio. Équivaut à l' [**attribut \_ \_ bits MF audio \_ bits \_ per \_ Sample**](mf-mt-audio-bits-per-sample-attribute.md) .<br/>                                                          |
| <span id="AudioBlockAlignment"></span><span id="audioblockalignment"></span><span id="AUDIOBLOCKALIGNMENT"></span>**AudioBlockAlignment**<br/>                                                     | Alignement de bloc pour le flux audio. Équivaut à l’attribut d' [**\_ \_ \_ \_ alignement de bloc audio MF MT**](mf-mt-audio-block-alignment-attribute.md) .<br/>                                                                     |
| <span id="AudioEncodingProfile"></span><span id="audioencodingprofile"></span><span id="AUDIOENCODINGPROFILE"></span>**AudioEncodingProfile**<br/>                                                 | Valeur spécifique au codec qui définit le profil audio. Équivaut à l' [attribut \_ \_ ENCODINGPROFILE de transcodage MF](mf-transcode-encodingprofile.md) . <br/>                                                                     |
| <span id="AudioFormat"></span><span id="audioformat"></span><span id="AUDIOFORMAT"></span>**AudioFormat**<br/>                                                                                     | Sous-type audio encodé. Équivaut à l’attribut de [**\_ sous- \_ type MF MT**](mf-mt-subtype-attribute.md) .<br/>                                                                                                                  |
| <span id="AudioNumChannels"></span><span id="audionumchannels"></span><span id="AUDIONUMCHANNELS"></span>**AudioNumChannels**<br/>                                                                 | Nombre de canaux dans le flux audio. Équivaut à l’attribut des [**\_ canaux de nombre de \_ \_ \_ canaux audio MF MT**](mf-mt-audio-num-channels-attribute.md) .<br/>                                                                         |
| <span id="AudioSamplesPerSecond"></span><span id="audiosamplespersecond"></span><span id="AUDIOSAMPLESPERSECOND"></span>**AudioSamplesPerSecond**<br/>                                             | Taux d’échantillonnage du flux audio, en échantillons par seconde. Équivaut à l’attribut des [**\_ \_ échantillons audio MF MT \_ \_ par \_ seconde**](mf-mt-audio-samples-per-second-attribute.md) .<br/>                                            |
| <span id="ContainerType"></span><span id="containertype"></span><span id="CONTAINERTYPE"></span>**ContainerType**<br/>                                                                             | Type de conteneur de fichier. Équivaut à l' [attribut \_ \_ CONTAINERTYPE de transcodage MF](mf-transcode-containertype.md) . <br/>                                                                                                       |
| <span id="ProfileName"></span><span id="profilename"></span><span id="PROFILENAME"></span>**ProfileName**<br/>                                                                                     | Nom complet du profil.<br/>                                                                                                                                                                                            |
| <span id="SkipMetadataTransfer"></span><span id="skipmetadatatransfer"></span><span id="SKIPMETADATATRANSFER"></span>**SkipMetadataTransfer**<br/>                                                 | Spécifiez 1 si les métadonnées ne doivent pas être transférées vers le fichier de sortie, ou 0 si les métadonnées doivent être transférées. Équivaut à l’attribut de [ \_ \_ \_ \_ transfert de métadonnées d’omission de transcodage MF](mf-transcode-skip-metadata-transfer.md) .<br/> |
| <span id="VideoBitrate"></span><span id="videobitrate"></span><span id="VIDEOBITRATE"></span>**VideoBitrate**<br/>                                                                                 | Débit binaire vidéo moyen. Équivaut à l’attribut de [**\_ vitesse de \_ \_ transmission moyenne de MF MT**](mf-mt-avg-bitrate-attribute.md) . <br/>                                                                                                        |
| <span id="VideoEncodeComplexity"></span><span id="videoencodecomplexity"></span><span id="VIDEOENCODECOMPLEXITY"></span>**VideoEncodeComplexity**<br/>                                             | Valeur spécifique au codec qui définit la qualité de codage. Équivaut à l' [attribut \_ \_ QUALITYVSSPEED de transcodage MF](mf-transcode-qualityvsspeed.md) . <br/>                                                                      |
| <span id="VideoEncodingProfile"></span><span id="videoencodingprofile"></span><span id="VIDEOENCODINGPROFILE"></span>**VideoEncodingProfile**<br/>                                                 | Valeur spécifique au codec qui définit le profil vidéo. Équivaut à l' [attribut \_ \_ ENCODINGPROFILE de transcodage MF](mf-transcode-encodingprofile.md) . <br/>                                                                     |
| <span id="VideoFormat"></span><span id="videoformat"></span><span id="VIDEOFORMAT"></span>**VideoFormat**<br/>                                                                                     | Sous-type de vidéo encodé. Équivaut à l’attribut de [**\_ sous- \_ type MF MT**](mf-mt-subtype-attribute.md) .<br/>                                                                                                                  |
| <span id="VideoFrameHeight"></span><span id="videoframeheight"></span><span id="VIDEOFRAMEHEIGHT"></span>**VideoFrameHeight**<br/>                                                                 | Hauteur de la vidéo de sortie. Équivaut à l’attribut de [**\_ \_ \_ taille de trame MT MF**](mf-mt-frame-size-attribute.md) .<br/>                                                                                                      |
| <span id="VideoFrameRateDenominator"></span><span id="videoframeratedenominator"></span><span id="VIDEOFRAMERATEDENOMINATOR"></span>**VideoFrameRateDenominator**<br/>                             | Dénominateur de la fréquence d’images de la vidéo de sortie. Équivaut à l’attribut de [**\_ \_ \_ fréquence d’images MF MF**](mf-mt-frame-rate-attribute.md) .<br/>                                                                               |
| <span id="VideoFrameRateNumerator"></span><span id="videoframeratenumerator"></span><span id="VIDEOFRAMERATENUMERATOR"></span>**VideoFrameRateNumerator**<br/>                                     | Numérateur de la fréquence d’images de la vidéo de sortie. Équivaut à l’attribut de [**\_ \_ \_ fréquence d’images MF MF**](mf-mt-frame-rate-attribute.md) .<br/>                                                                                 |
| <span id="VideoFrameWidth"></span><span id="videoframewidth"></span><span id="VIDEOFRAMEWIDTH"></span>**VideoFrameWidth**<br/>                                                                     | Largeur de la vidéo de sortie. Équivaut à l’attribut de [**\_ \_ \_ taille de trame MT MF**](mf-mt-frame-size-attribute.md) .<br/>                                                                                                       |
| <span id="VideoPixelAspectRatioDenominator"></span><span id="videopixelaspectratiodenominator"></span><span id="VIDEOPIXELASPECTRATIODENOMINATOR"></span>**VideoPixelAspectRatioDenominator**<br/> | Dénominateur des proportions en pixels (PAR) de la vidéo de sortie. Équivaut à l’attribut de proportions de [**\_ \_ pixels \_ \_ MT MF**](mf-mt-pixel-aspect-ratio-attribute.md) . <br/>                                               |
| <span id="VideoPixelAspectRatioNumerator"></span><span id="videopixelaspectrationumerator"></span><span id="VIDEOPIXELASPECTRATIONUMERATOR"></span>**VideoPixelAspectRatioNumerator**<br/>         | Numérateur du pair de la vidéo de sortie. Équivaut à l’attribut de proportions de [**\_ \_ pixels \_ \_ MT MF**](mf-mt-pixel-aspect-ratio-attribute.md) . <br/>                                                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 




