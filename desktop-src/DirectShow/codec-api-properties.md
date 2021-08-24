---
description: Propriétés de l’API codec
ms.assetid: 5d527af7-07cf-42e2-99bb-d56c856cc1bc
title: Propriétés de l’API codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91346b6595944b8e95da5e9e43023052119e49a8b88809fce08b6fca780beba1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792909"
---
# <a name="codec-api-properties"></a>Propriétés de l’API codec

-   [Propriétés audio courantes](#common-audio-properties)
-   [Propriétés courantes du décodeur](#common-decoder-properties)
-   [Propriétés courantes de l’encodeur](#common-encoder-properties)
-   [Propriétés du décodeur vidéo](#video-decoder-properties)
-   [Propriétés du décodeur audio](#audio-decoder-properties)
-   [Propriétés de l’encodeur vidéo](#video-encoder-properties)
-   [Propriétés de l’encodeur audio](#audio-encoder-properties)
-   [Propriétés de l’encodeur vidéo MPEG](#mpeg-video-encoder-properties)
-   [Propriétés de l’encodeur audio MPEG](#mpeg-audio-encoder-properties)
-   [Propriétés du décodeur Dolby Digital Audio](#dolby-digital-audio-decoder-properties)
-   [Propriétés de l’encodeur Dolby Digital Audio](#dolby-digital-audio-encoder-properties)
-   [Propriétés du traitement des signaux numériques (DSP)](#digital-signal-processing-dsp-properties)

### <a name="common-audio-properties"></a>Propriétés audio courantes

Ces propriétés s’appliquent aux encodeurs audio et aux décodeurs audio.



| Propriété                                                      | Description                                                                    |
|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**AVAudioChannelConfig**](avaudiochannelconfig-property.md) | Obtient la configuration de l’orateur pour les canaux audio dans le flux de bits audio. |
| [**AVAudioChannelCount**](avaudiochannelcount-property.md)   | Obtient le nombre de canaux dans le flux de bits audio.                           |
| [**AVAudioSampleRate**](avaudiosamplerate-property.md)       | Obtient le taux d’échantillonnage du flux de bits audio, en échantillons par seconde.          |
| [**AVDDSurroundMode**](avddsurroundmode-property.md)         | Spécifie si l’audio est encodé dans Dolby Surround.                      |



 

### <a name="common-decoder-properties"></a>Propriétés courantes du décodeur

Ces propriétés s’appliquent à la fois aux décodeurs audio et aux décodeurs vidéo.



| Propriété                                                            | Description                                                                             |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**AVDecCommonInputFormat**](avdeccommoninputformat-property.md)   | Spécifie le format d’entrée actuel pour le décodeur.                                     |
| [**AVDecCommonMeanBitRate**](avdeccommonmeanbitrate.md)            | Obtient la vitesse de transmission moyenne actuelle du décodeur.                                          |
| [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) | Spécifie le format de sortie du décodeur.                                            |
| [**AVDecMmcssClass**](avdecmmcss-property.md)                      | Spécifie la classe du service Planificateur de classes multimédias (MMCSS) pour le thread de décodage. |



 

### <a name="common-encoder-properties"></a>Propriétés courantes de l’encodeur

Ces propriétés s’appliquent aux encodeurs audio et vidéo.



| Propriété                                                                          | Description                                                                                                     |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**AVEncCodecType**](avenccodectype-property.md)                                 | Spécifie le schéma d’encodage.                                                                                  |
| [**AVEncCommonBufferInLevel**](avenccommonbufferinlevel-property.md)             | Spécifie le niveau initial de la mémoire tampon d’encodage.                                                             |
| [**AVEncCommonBufferOutLevel**](avenccommonbufferoutlevel-property.md)           | Spécifie le niveau final de la mémoire tampon d’encodage à la fin du processus d’encodage.                            |
| [**AVEncCommonBufferSize**](avenccommonbuffersize-property.md)                   | Spécifie la taille de la mémoire tampon utilisée pendant l’encodage.                                                          |
| [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)       | Spécifie le format cible pour un encodeur.                                                                     |
| [**AVEncCommonLowLatency**](avenccommonlowlatency-property.md)                   | Spécifie si le flux de sortie doit être structuré afin que le flux encodé ait une latence de décodage faible. |
| [**AVEncCommonMaxBitRate**](avenccommonmaxbitrate-property.md)                   | Spécifie la vitesse de transmission maximale.                                                                                 |
| [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)                 | Spécifie la vitesse de transmission moyenne.                                                                                 |
| [**AVEncCommonMeanBitRateInterval**](avenccommonmeanbitrateinterval-property.md) | Spécifie l’intervalle de temps pendant lequel la vitesse de transmission moyenne s’applique.                                            |
| [**AVEncCommonMinBitRate**](avenccommonminbitrate-property.md)                   | Spécifie la vitesse de transmission minimale.                                                                                 |
| [**AVEncCommonMultipassMode**](avenccommonmultipassmode-property.md)             | Spécifie le nombre de passes d’encodage pris en charge par l’encodeur.                                              |
| [**AVEncCommonPassEnd**](avenccommonpassend-property.md)                         | Arrête le passage de l’encodage en cours ou interroge si le passage de l’encodage actuel est le dernier.                  |
| [**AVEncCommonPassStart**](avenccommonpassstart-property.md)                     | Démarre la première passe d’encodage.                                                                                 |
| [**AVEncCommonQuality**](avenccommonquality-property.md)                         | Spécifie le niveau de qualité pour l’encodage.                                                                       |
| [**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md)           | Spécifie le compromis entre la qualité et la vitesse du codage.                                                      |
| [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md)         | Spécifie le mode de contrôle de la fréquence.                                                                                |
| [**AVEncCommonRealTime**](avenccommonrealtime-property.md)                       | Spécifie si l’application requiert des performances d’encodage en temps réel.                                      |
| [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md)     | Spécifie si l’encodeur ignore les groupes d’images partielles (GOP secondes) à la fin du flux.              |
| [**AVEncMuxOutputStreamType**](avencmuxoutputstreamtype.md)                      | Spécifie le type de flux de sortie produit par un multiplexeur.                                                  |
| [**AVEncStatCommonCompletedPasses**](avencstatcommoncompletedpasses-property.md) | Spécifie le nombre de réussites d’encodage terminées.                                                              |



 

### <a name="video-decoder-properties"></a>Propriétés du décodeur vidéo



| Propriété                                                                                | Description                                                                     |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**AVDecVideoAcceleration \_ H264 –**](avdecvideoacceleration-h264-property.md)            | Active ou désactive l’accélération matérielle pour le décodage vidéo H. 264.             |
| [**AVDecVideoAcceleration \_ MPEG2**](avdecvideoacceleration-mpeg2-property.md)          | Active ou désactive l’accélération matérielle pour le décodage vidéo MPEG-2.            |
| [**AVDecVideoAcceleration \_ VC1**](avdecvideoacceleration-vc1-property.md)              | Active ou désactive l’accélération matérielle pour le décodage vidéo VC-1.              |
| [**AVDecVideoDropPicWithMissingRef**](avdecvideodroppicwithmissingref-property.md)     | Spécifie si le décodeur supprime les trames intra avec des frames de référence manquants. |
| [**AVDecVideoFastDecodeMode**](avdecvideofastdecodemode.md)                            | Obtient ou définit la vitesse de décodage vidéo.                                          |
| [**AVDecVideoImageSize**](avdecvideoimagesize.md)                                      | Obtient la taille de l’image décodée, en pixels.                                  |
| [**AVDecVideoInputScanType**](avdecvideoinputscantype-property.md)                     | Spécifie la façon dont le flux vidéo décodé est entrelacé.                           |
| [**AVDecVideoPixelAspectRatio**](avdecvideopixelaspectratio-property.md)               | Spécifie les proportions de pixels du flux vidéo décodé.                   |
| [**AVDecVideoSoftwareDeinterlaceMode**](avdecvideosoftwaredeinterlacemode-property.md) | Spécifie le mode de désentrelacement du logiciel du décodeur.                              |
| [**AVDecVideoSWPowerLevel**](avdecvideoswpowerlevel-property.md)                       | Spécifie le niveau d’économie d’énergie.                                               |
| [**AVDecVideoThumbnailGenerationMode**](avdecvideothumbnailgenerationmode-property.md) | Active ou désactive le mode de génération de miniatures.                                  |



 

### <a name="audio-decoder-properties"></a>Propriétés du décodeur audio



| Propriété                                                                        | Description                                                                                                            |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**AVDecAACDownmixMode**](avdecaacdownmixmode-property.md)                     | Spécifie si un décodeur AAC utilise des équations downmix stéréo MPEG-2/MPEG-4 standard ou utilise un downmix non standard. |
| [**AVDecAudioDualMono**](avdecaudiodualmono-property.md)                       | Spécifie si le contenu audio à 2 canaux est encodé en stéréo ou en double mono.                                                   |
| [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md)     | Spécifie comment le décodeur reproduit un double audio mono.                                                                  |
| [**AVDecHEAACDynamicRangeControl**](avdecheaacdynamicrangecontrol-property.md) | Active ou désactive le contrôle de plage dynamique dans un décodeur AAC.                                                           |



 

### <a name="video-encoder-properties"></a>Propriétés de l’encodeur vidéo



| Propriété                                                                                        | Description                                                                                                           |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**AVEncInputVideoSystem**](avencinputvideosystem-property.md)                                 | Spécifie le système vidéo du contenu source.                                                                     |
| [**AVEncStatVideoCodedFrames**](avencstatvideocodedframes-property.md)                         | Retourne le nombre de trames vidéo qui ont été encodées.                                                                 |
| [**AVEncStatVideoOutputFrameRate**](avencstatvideooutputframerate-property.md)                 | Retourne la fréquence d’images moyenne du contenu vidéo.                                                                  |
| [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md)                         | Retourne le nombre de trames vidéo reçues par l’encodeur.                                                         |
| [**AVEncVideoCBRMotionTradeoff**](avencvideocbrmotiontradeoff-property.md)                     | Spécifie le compromis entre le mouvement et les images fixes.                                                               |
| [**AVEncVideoCodedVideoAccessUnitSize**](avencvideocodedvideoaccessunitsize-property.md)       | Spécifie la taille des unités d’accès vidéo.                                                                         |
| [**AVEncVideoDefaultUpperFieldDominant**](avencvideodefaultupperfielddominant-property.md)     | Spécifie le champ qui s’affiche en premier.                                                                             |
| [**AVEncVideoDisplayDimension**](avencvideodisplaydimension-property.md)                       | Spécifie la taille du flux vidéo lorsqu’il est décodé.                                                            |
| [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md)                         | Spécifie la largeur et la hauteur de la vidéo encodée, si la vidéo est rognée.                                         |
| [**AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md)                   | Spécifie les angles gauche et supérieur du rectangle de découpage, si la vidéo est rognée.                                |
| [**AVEncVideoFieldSwap**](avencvideofieldswap-property.md)                                     | Inverse l’ordre des champs entrelacés dans la vidéo source.                                                      |
| [**AVEncVideoForceSourceScanType**](avencvideoforcesourcescantype-property.md)                 | Spécifie si les frames d’entrée sont progressifs ou entrelacés.                                                     |
| [**AVEncVideoHeaderDropFrame**](avencvideoheaderdropframe-property.md)                         | Spécifie la valeur de l’indicateur de frame de dépôt dans l’en-tête de GOP.                                                             |
| [**AVEncVideoHeaderFrames**](avencvideoheaderframes-property.md)                               | Spécifie le numéro de frame de début dans l’en-tête de GOP.                                                                |
| [**AVEncVideoHeaderHours**](avencvideoheaderhours-property.md)                                 | Spécifie le nombre d’heures de début dans l’en-tête de GOP.                                                                 |
| [**AVEncVideoHeaderMinutes**](avencvideoheaderminutes-property.md)                             | Spécifie le numéro de la minute de début dans l’en-tête de GOP.                                                               |
| [**AVEncVideoHeaderSeconds**](avencvideoheaderseconds-property.md)                             | Spécifie le deuxième numéro de départ dans l’en-tête de GOP.                                                               |
| [**AVEncVideoInputChromaResolution**](avencvideoinputchromaresolution-property.md)             | Spécifie la résolution chroma de la vidéo d’entrée.                                                                   |
| [**AVEncVideoInputChromaSubsampling**](avencvideoinputchromasubsampling-property.md)           | Spécifie l’emplacement de chrominance pour la vidéo d’entrée.                                                                      |
| [**AVEncVideoInputColorLighting**](avencvideoinputcolorlighting-property.md)                   | Spécifie les conditions d’éclairage prévues pour l’affichage de la vidéo d’entrée.                                               |
| [**AVEncVideoInputColorNominalRange**](avencvideoinputcolornominalrange-property.md)           | Spécifie la plage nominale de la vidéo d’entrée.                                                                      |
| [**AVEncVideoInputColorPrimaries**](avencvideoinputcolorprimaries-property.md)                 | Spécifie les couleurs primaires de la vidéo d’entrée.                                                                    |
| [**AVEncVideoInputColorTransferFunction**](avencvideoinputcolortransferfunction-property.md)   | Spécifie la fonction de conversion de RGB en R’G’B’pour la vidéo d’entrée                                                  |
| [**AVEncVideoInputColorTransferMatrix**](avencvideoinputcolortransfermatrix-property.md)       | Spécifie la matrice de conversion de l’espace de couleurs Y’Cb’Cr sur l’espace de couleurs R’G’B pour la vidéo d’entrée.         |
| [**AVEncVideoInverseTelecineEnable**](avencvideoinversetelecineenable-property.md)             | Spécifie si l’encodeur effectue un télécinéma inverse.                                                              |
| [**AVEncVideoInverseTelecineThreshold**](avencvideoinversetelecinethreshold-property.md)       | Définit le seuil auquel l’encodeur considère un champ vidéo redondant.                                            |
| [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md)                 | Spécifie le nombre maximal d’images entre les images clés.                                                            |
| [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md)                   | Spécifie le nombre de champs à encoder.                                                                             |
| [**AVEncVideoNoOfFieldsToSkip**](avencvideonooffieldstoskip-property.md)                       | Spécifie le nombre de champs à ignorer pendant l’encodage.                                                               |
| [**AVEncVideoOutputChromaResolution**](avencvideooutputchromaresolution-property.md)           | Spécifie la résolution chroma de la vidéo encodée.                                                                 |
| [**AVEncVideoOutputChromaSubsampling**](avencvideooutputchromasubsampling-property.md)         | Spécifie l’emplacement de chrominance pour la vidéo encodée.                                                                    |
| [**AVEncVideoOutputColorLighting**](avencvideooutputcolorlighting-property.md)                 | Spécifie les conditions d’éclairage prévues pour l’affichage de la vidéo encodée.                                             |
| [**AVEncVideoOutputColorNominalRange**](avencvideooutputcolornominalrange-property.md)         | Spécifie la plage nominale de la vidéo encodée.                                                                    |
| [**AVEncVideoOutputColorPrimaries**](avencvideooutputcolorprimaries-property.md)               | Spécifie les couleurs primaires de la vidéo encodée.                                                                  |
| [**AVEncVideoOutputColorTransferFunction**](avencvideooutputcolortransferfunction-property.md) | Spécifie la fonction de conversion de RGB en R’G’B’pour la vidéo encodée.                                               |
| [**AVEncVideoOutputColorTransferMatrix**](avencvideooutputcolortransfermatrix-property.md)     | Spécifie la matrice de conversion de l’espace de couleurs Y’Cb’Cr sur l’espace de couleurs R’G’B pour la vidéo encodée.       |
| [**AVEncVideoOutputFrameRate**](avencvideooutputframerate-property.md)                         | Spécifie la fréquence d’images sur le flux de sortie de l’encodeur, en images par seconde.                                        |
| [**AVEncVideoOutputFrameRateConversion**](avencvideooutputframerateconversion-property.md)     | Spécifie si l’encodeur convertit la fréquence d’images lorsque la fréquence d’images de sortie ne correspond pas à la fréquence d’images d’entrée. |
| [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md)                           | Spécifie la manière dont l’encodeur entrelace la vidéo de sortie.                                                                |
| [**AVEncVideoPixelAspectRatio**](avencvideopixelaspectratio-property.md)                       | Spécifie les proportions en pixels.                                                                                     |
| [**AVEncVideoSourceFilmContent**](avencvideosourcefilmcontent-property.md)                     | Spécifie si la source d’origine de la vidéo d’entrée était film ou vidéo.                                           |
| [**AVEncVideoSourceIsBW**](avencvideosourceisbw-property.md)                                   | Spécifie si la vidéo est monochrome (noir et blanc) ou si elle contient des couleurs.                                        |



 

### <a name="audio-encoder-properties"></a>Propriétés de l’encodeur audio



| Propriété                                                                        | Description                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**AVEncAudioDualMono**](avencaudiodualmono-property.md)                       | Spécifie si le contenu audio à 2 canaux est encodé en stéréo ou en double mono.                |
| [**AVEncAudioInputContent**](avencaudioinputcontent-property.md)               | Spécifie si le contenu audio contient de la musique ou de la voix.                        |
| [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md)       | Spécifie le nombre d’échantillons audio à encoder.                                    |
| [**AVEncAudioIntervalToSkip**](avencaudiointervaltoskip-property.md)           | Spécifie le nombre d’échantillons audio à ignorer par l’encodeur.                      |
| [**AVEncAudioMapDestChannel N**](avencaudiomapdestchanneln-property.md)        | Spécifie le canal audio mappé au canal *N* dans le flux audio encodé. |
| [**AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md)                          | Spécifie la vitesse de transmission moyenne du flux audio encodé.                         |
| [**AVEncStatAudioAverageBPS**](avencstataudioaveragebps-property.md)           | Retourne le nombre moyen de bits par seconde de l’audio encodé.                           |
| [**AVEncStatAudioAveragePCMValue**](avencstataudioaveragepcmvalue-property.md) | Retourne le niveau de volume moyen du contenu audio.                              |
| [**AVEncStatAudioPeakPCMValue**](avencstataudiopeakpcmvalue-property.md)       | Retourne le niveau de volume le plus élevé qui était présent dans le contenu audio.             |



 

### <a name="mpeg-video-encoder-properties"></a>Propriétés de l’encodeur vidéo MPEG



| Propriété                                                                                    | Description                                                                          |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**AVEncMPVAddSeqEndCode**](avencmpvaddseqendcode-property.md)                             | Spécifie si l’encodeur ajoute un code de fin de séquence à la fin du flux.     |
| [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md)               | Spécifie le nombre par défaut de frames B consécutifs entre I et P frames.         |
| [**AVEncMPVFrameFieldMode**](avencmpvframefieldmode-property.md)                           | Spécifie si l’encodeur produit des champs encodés ou des frames encodés.             |
| [**AVEncMPVGenerateHeaderPicDispExt**](avencmpvgenerateheaderpicdispext-property.md)       | Spécifie si l’encodeur génère des en-têtes d’extension d’affichage d’image.           |
| [**AVEncMPVGenerateHeaderPicExt**](avencmpvgenerateheaderpicext-property.md)               | Spécifie si l’encodeur génère des en-têtes d’extension d’image.                   |
| [**AVEncMPVGenerateHeaderSeqDispExt**](avencmpvgenerateheaderseqdispext-property.md)       | Spécifie si l’encodeur génère des en-têtes d’extension d’affichage de séquence.          |
| [**AVEncMPVGenerateHeaderSeqExt**](avencmpvgenerateheaderseqext-property.md)               | Spécifie si l’encodeur génère des en-têtes d’extension de séquence.                  |
| [**AVEncMPVGenerateHeaderSeqScaleExt**](avencmpvgenerateheaderseqscaleext-property.md)     | Spécifie si l’encodeur génère des en-têtes d’extension évolutifs de séquence.         |
| [**AVEncMPVGOPOpen**](avencmpvgopopen-property.md)                                         | Spécifie si l’encodeur produit des GOP secondes ouverts ou des GOP secondes fermés.                     |
| [**AVEncMPVGOPSInSeq**](avencmpvgopsinseq-property.md)                                     | Spécifie le nombre de GOP secondes entre les en-têtes de séquence.                               |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md)                                         | Spécifie le nombre maximal d’images d’un en-tête GOP à l’en-tête GOP suivant. |
| [**AVEncMPVIntraDCPrecision**](avencmpvintradcprecision-property.md)                       | Spécifie la précision des coefficients DC.                                      |
| [**AVEncMPVIntraVLCTable**](avencmpvintravlctable-property.md)                             | Spécifie la table de codage de longueur variable (VLC) à utiliser pour le codage entropie.        |
| [**AVEncMPVLevel**](avencmpvlevel-property.md)                                             | Spécifie le niveau MPEG-2.                                                          |
| [**AVEncMPVProfile**](avencmpvprofile-property.md)                                         | Spécifie le profil MPEG-2.                                                        |
| [**AVEncMPVQScaleType**](avencmpvqscaletype-property.md)                                   | Spécifie si l’échelle du quantificateur est linéaire ou non linéaire.                       |
| [**AVEncMPVQuantMatrixChromaIntra**](avencmpvquantmatrixchromaintra-property.md)           | Spécifie la matrice de quantification Chroma pour blocs macros.                      |
| [**AVEncMPVQuantMatrixChromaNonIntra**](avencmpvquantmatrixchromanonintra-property.md)     | Spécifie la matrice de quantification Chroma pour les blocs macros non-internes.                  |
| [**AVEncMPVQuantMatrixIntra**](avencmpvquantmatrixintra-property.md)                       | Spécifie la matrice de quantification de luminance pour blocs macros.                        |
| [**AVEncMPVQuantMatrixNonIntra**](avencmpvquantmatrixnonintra-property.md)                 | Spécifie la matrice de quantification de luminance pour les blocs macros non intra.                    |
| [**AVEncMPVScanPattern**](avencmpvscanpattern-property.md)                                 | Spécifie le modèle d’analyse bloc macro.                                               |
| [**AVEncMPVSceneDetection**](avencmpvscenedetection-property.md)                           | Spécifie le comportement de l’encodeur lorsqu’il détecte une nouvelle scène.                       |
| [**AVEncMPVUseConcealmentMotionVectors**](avencmpvuseconcealmentmotionvectors-property.md) | Spécifie si l’encodeur utilise des vecteurs de mouvement de masquage.                       |



 

### <a name="mpeg-audio-encoder-properties"></a>Propriétés de l’encodeur audio MPEG



| Propriété                                                                                  | Description                                                                   |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**AVEncMPACodingMode**](avencmpacodingmode-property.md)                                 | Spécifie le mode d’encodage audio MPEG-1.                                     |
| [**AVEncMPACopyright**](avencmpacopyright-property.md)                                   | Spécifie le paramètre par défaut pour le bit de copyright.                          |
| [**AVEncMPAEmphasisType**](avencmpaemphasistype-property.md)                             | Spécifie le type de filtre de désaccentuation à utiliser lors du décodage.   |
| [**AVEncMPAEnableRedundancyProtection**](avencmpaenableredundancyprotection-property.md) | Spécifie s’il faut ajouter une vérification de redondance cyclique (CRC) à l’en-tête de trame. |
| [**AVEncMPALayer**](avencmpalayer-property.md)                                           | Spécifie la couche audio MPEG.                                               |
| [**AVEncMPAOriginalBitstream**](avencmpaoriginalbitstream-property.md)                   | Spécifie le paramètre par défaut pour le bit d’origine.                           |
| [**AVEncMPAPrivateUserBit**](avencmpaprivateuserbit-property.md)                         | Définit la valeur du bit d’utilisateur privé.                                       |



 

### <a name="dolby-digital-audio-decoder-properties"></a>Propriétés du décodeur Dolby Digital Audio



| Propriété                                                                      | Description                                                                    |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**AVDecDDDynamicRangeScaleHigh**](avdecdddynamicrangescalehigh-property.md) | Spécifie la coupe de haut niveau lorsque le décodeur effectue un contrôle de plage dynamique.  |
| [**AVDecDDDynamicRangeScaleLow**](avdecdddynamicrangescalelow-property.md)   | Spécifie l’augmentation de bas niveau lorsque le décodeur effectue un contrôle de plage dynamique. |
| [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md)             | Spécifie le mode de contrôle de compression.                                        |



 

### <a name="dolby-digital-audio-encoder-properties"></a>Propriétés de l’encodeur Dolby Digital Audio



| Propriété                                                                                        | Description                                                                               |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**AVEncDDAtoDConverterType**](avencddatodconvertertype-property.md)                           | Spécifie le type de conversion analogique-à-numérique (A/D).                                 |
| [**AVEncDDCentreDownMixLevel**](avencddcentredownmixlevel-property.md)                         | Spécifie le niveau downmix du centre.                                                       |
| [**AVEncDDChannelBWLowPassFilter**](avencddchannelbwlowpassfilter-property.md)                 | Spécifie si un filtre passe-bas est appliqué aux canaux d’entrée principaux.                |
| [**AVEncDDCopyright**](avencddcopyright-property.md)                                           | Spécifie l’indicateur de copyright.                                                             |
| [**AVEncDDDCHighPassFilter**](avencdddchighpassfilter-property.md)                             | Spécifie si un filtre de réussite élevé bloquant le contrôleur de l’alimentation est appliqué.                              |
| [**AVEncDDDialogNormalization**](avencdddialognormalization-property.md)                       | Spécifie le niveau de normalisation de la boîte de dialogue.                                                 |
| [**AVEncDDDigitalDeemphasis**](avencdddigitaldeemphasis-property.md)                           | Spécifie si la mise en évidence numérique.                                                    |
| [**AVEncDDDynamicRangeCompressionControl**](avencdddynamicrangecompressioncontrol-property.md) | Spécifie le profil de contrôle de plage dynamique.                                              |
| [**AVEncDDHeadphoneMode**](avencddheadphonemode-property.md)                                   | Spécifie le mode casque.                                                             |
| [**AVEncDDLFELowPassFilter**](avencddlfelowpassfilter-property.md)                             | Spécifie si un filtre passe-bas est appliqué au canal de l’effet fréquence faible (LFE). |
| [**AVEncDDLoRoCenterMixLvl \_ x10**](avencddlorocentermixlvl-x10-property.md)                    | Spécifie le décalage de niveau appliqué au canal central pour les downmixing Lo/ro.     |
| [**AVEncDDLoRoSurroundMixLvl \_ x10**](avencddlorosurroundmixlvl-x10-property.md)                | Spécifie le décalage de niveau appliqué aux canaux Surround pour les downmixing Lo/ro.  |
| [**AVEncDDLtRtCenterMixLvl \_ x10**](avencddltrtcentermixlvl-x10-property.md)                    | Spécifie le niveau de décalage appliqué au canal central pour lt/RT downmixing.     |
| [**AVEncDDLtRtSurroundMixLvl \_ x10**](avencddltrtsurroundmixlvl-x10-property.md)                | Spécifie le décalage de niveau appliqué aux canaux Surround pour lt/RT downmixing.  |
| [**AVEncDDOriginalBitstream**](avencddoriginalbitstream-property.md)                           | Spécifie l’indicateur de flux binaire d’origine.                                                    |
| [**AVEncDDPreferredStereoDownMixMode**](avencddpreferredstereodownmixmode-property.md)         | Spécifie le mode de downmix stéréo par défaut.                                              |
| [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md)                     | Spécifie l’indicateur d’informations de production audio.                                          |
| [**AVEncDDProductionMixLevel**](avencddproductionmixlevel-property.md)                         | Spécifie le niveau de mixage.                                                               |
| [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md)                         | Spécifie le type de salle.                                                                  |
| [**AVEncDDRFPreEmphasisFilter**](avencddrfpreemphasisfilter-property.md)                       | Spécifie le paramètre de protection de la surmodulation RF.                                       |
| [**AVEncDDService**](avencddservice-property.md)                                               | Spécifie le service audio.                                                              |
| [**AVEncDDSurround3dBAttenuation**](avencddsurround3dbattenuation-property.md)                 | Spécifie si les canaux Surround sont atténués avant l’encodage.                   |
| [**AVEncDDSurround90DegreeePhaseShift**](avencddsurround90degreeephaseshift-property.md)       | Spécifie si un décalage de phase 90 est appliqué aux canaux surround.            |
| [**AVEncDDSurroundDownMixLevel**](avencddsurrounddownmixlevel-property.md)                     | Spécifie le niveau de mixage d’entourage.                                                    |
| [**AVEncDDSurroundExMode**](avencddsurroundexmode-property.md)                                 | Spécifie si le flux audio est encodé dans l’entourage EX.                             |



 

### <a name="digital-signal-processing-dsp-properties"></a>Propriétés du traitement des signaux numériques (DSP)



| Propriété                                                                | Description                               |
|-------------------------------------------------------------------------|-------------------------------------------|
| [**AVDSPLoudnessEqualization**](avdsploudnessequalization-property.md) | Active ou désactive l’égalisation sonore |
| [**AVDSPSpeakerFill**](avdspspeakerfill-property.md)                   | Active ou désactive le remplissage de l’orateur          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de l’API codec](codec-api-reference.md)
</dt> </dl>

 

 



