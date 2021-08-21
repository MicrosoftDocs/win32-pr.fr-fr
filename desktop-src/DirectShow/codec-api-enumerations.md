---
description: Énumérations d’API de codec
ms.assetid: 5d6e48cb-d181-448e-a96e-e5ab500427d7
title: Énumérations d’API de codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28b82d73d6bd6fefed5f3c9296a666d1053cd71b074a782858b31e94dc3a3ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079329"
---
# <a name="codec-api-enumerations"></a>Énumérations d’API de codec



| Énumération                                                                              | Description                                                                                               |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**eAVAudioChannelConfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig)                                   | Spécifie la configuration du haut-parleur pour les canaux audio dans le flux de bits audio.                       |
| [**eAVDDSurroundMode**](/windows/desktop/api/codecapi/ne-codecapi-eavddsurroundmode)                                           | Spécifie si l’audio est encodé dans Dolby Surround.                                                 |
| [**eAVDecAACDownmixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode)                                     | Spécifie si un décodeur AAC utilise des équations downmix stéréo MPEG-2/MPEG-4 standard.                    |
| [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono)                                       | Spécifie si le flux audio d’entrée est stéréo ou double mono.                                          |
| [**eAVDecAudioDualMonoReproMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode)                     | Spécifie comment le décodeur reproduit un double audio mono.                                                     |
| [**eAVDecDDOperationalMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecddoperationalmode)                               | Spécifie le mode de contrôle de compression pour un flux audio Dolby AC-3.                                     |
| [**eAVDecHEAACDynamicRangeControl**](/windows/desktop/api/codecapi/ne-codecapi-eavdecheaacdynamicrangecontrol)                 | Spécifie si un décodeur AAC effectue un contrôle de plage dynamique.                                          |
| [**eAVDecVideoInputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype)                             | Spécifie la façon dont le flux vidéo décodé est entrelacé.                                                     |
| [**eAVDecVideoSoftwareDeinterlaceMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideosoftwaredeinterlacemode)         | Spécifie le mode de désentrelacement du logiciel du décodeur vidéo.                                                    |
| [**eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel)                               | Spécifie le niveau d’économie d’énergie d’un décodeur vidéo.                                                      |
| [**eAVDSPLoudnessEqualization**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization)                         | Spécifie si l’égalisation du volume est activée dans un décodeur audio ou un processeur de signal numérique (DSP). |
| [**eAVDSPSpeakerFill**](/windows/desktop/api/codecapi/ne-codecapi-eavdspspeakerfill)                                           | Spécifie si le remplissage de l’intervenant est activé dans un décodeur audio ou DSP.                                     |
| [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono)                                       | Spécifie si le contenu audio à 2 canaux est encodé en stéréo ou en double mono.                                      |
| [**Énumération eAVEncAudioInputContent**](/windows/win32/api/codecapi/ne-codecapi-eavencaudioinputcontent)                   | Spécifie si le contenu audio contient de la musique ou de la voix.                                              |
| [**eAVEncCommonRateControlMode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode)                       | Spécifie le mode de contrôle de la fréquence.                                                                          |
| [**eAVEncCommonStreamEndHandling**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonstreamendhandling)                   | Spécifie si l’encodeur ignore les groupes d’images partielles (GOP secondes) à la fin du flux.        |
| [**eAVEncDDAtoDConverterType**](/windows/win32/api/codecapi/ne-codecapi-eavencddatodconvertertype)                           | Spécifie le type de conversion analogique-numérique (A/D) pour un flux audio Dolby Digital.                |
| [**eAVEncDDDynamicRangeCompressionControl**](/windows/win32/api/codecapi/ne-codecapi-eavencdddynamicrangecompressioncontrol) | Spécifie le profil de contrôle de plage dynamique dans un flux audio Dolby Digital.                              |
| [**eAVEncDDHeadphoneMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddheadphonemode)                                   | Spécifie le mode casque pour un flux audio Dolby Digital.                                                |
| [**eAVEncDDPreferredStereoDownMixMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddpreferredstereodownmixmode)         | Spécifie le mode de downmix stéréo par défaut pour un flux audio Dolby Digital.                             |
| [**eAVEncDDProductionRoomType**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype)                         | Spécifie le type de salle pour un flux audio Dolby Digital.                                                 |
| [**eAVEncDDService**](/windows/desktop/api/codecapi/ne-codecapi-eavencddservice)                                               | Spécifie le service audio contenu dans un flux audio Dolby Digital.                                    |
| [**eAVEncDDSurroundExMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddsurroundexmode)                                 | Spécifie si un flux audio Dolby Digital est encodé dans Dolby Digital Surround EX.                   |
| [**eAVEncInputVideoSystem**](/windows/desktop/api/codecapi/ne-codecapi-eavencinputvideosystem)                                 | Spécifie la plage nominale pour une source vidéo.                                                           |
| [**eAVEncMPACodingMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpacodingmode)                                       | Spécifie le mode d’encodage audio MPEG.                                                                   |
| [**eAVEncMPAEmphasisType**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype)                                   | Spécifie le type de filtre de désaccentuation à utiliser lors du décodage.                               |
| [**eAVEncMPALayer**](/windows/win32/api/codecapi/ne-codecapi-eavencmpalayer)                                                 | Spécifie la couche audio MPEG.                                                                           |
| [**eAVEncMPVFrameFieldMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvframefieldmode)                               | Spécifie si l’encodeur produit des champs encodés ou des frames encodés.                                  |
| [**eAVEncMPVIntraVLCTable**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvintravlctable)                                 | Spécifie la table de codage de longueur variable (VLC) à utiliser pour le codage entropie.                             |
| [**eAVEncMPVLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvlevel)                                                 | Spécifie le profil MPEG-2.                                                                             |
| [**eAVEncMPVProfile**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvprofile)                                             | Spécifie le profil MPEG-2.                                                                             |
| [**eAVEncMPVQScaleType**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvqscaletype)                                       | Spécifie si l’échelle du quantificateur est linéaire ou non linéaire.                                            |
| [**eAVEncMPVScanPattern**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvscanpattern)                                     | Spécifie le modèle d’analyse bloc macro.                                                                    |
| [**eAVEncMPVSceneDetection**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvscenedetection)                               | Spécifie le comportement de l’encodeur lorsqu’il détecte une nouvelle scène.                                            |
| [**eAVEncMuxOutput**](/windows/win32/api/codecapi/ne-codecapi-eavencmuxoutput)                                               | Spécifie le type de flux de sortie produit par un multiplexeur.                                            |
| [**eAVEncVideoChromaResolution**](/windows/win32/api/codecapi/ne-codecapi-eavencvideochromaresolution)                       | Spécifie la résolution de chrominance.                                                                              |
| [**eAVEncVideoChromaSubsampling**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideochromasubsampling)                     | Spécifie le positionnement de Chroma.                                                                                  |
| [**eAVEncVideoColorLighting**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolorlighting)                             | Spécifie les conditions d’éclairage prévues pour l’affichage d’une source vidéo.                                    |
| [**eAVEncVideoColorNominalRange**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolornominalrange)                     | Spécifie la plage nominale pour une source vidéo.                                                           |
| [**eAVEncVideoColorPrimaries**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolorprimaries)                           | Spécifie les couleurs primaires de la vidéo.                                                               |
| [**eAVEncVideoColorTransferFunction**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolortransferfunction)             | Spécifie la fonction de conversion de R’G’B’en RGB.                                                     |
| [**eAVEncVideoColorTransferMatrix**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolortransfermatrix)                 | Spécifie la matrice de conversion de l’espace de couleurs Y’Cb’Cr sur l’espace de couleurs R’G’B.                  |
| [**eAVEncVideoFilmContent**](/windows/win32/api/codecapi/ne-codecapi-eavencvideofilmcontent)                                 | Spécifie si la source d’origine de la vidéo d’entrée était film ou vidéo.                               |
| [**eAVEncVideoOutputFrameRateConversion**](/windows/win32/api/codecapi/ne-codecapi-eavencvideooutputframerateconversion)     | Spécifie si l’encodeur convertit la fréquence d’images.                                                    |
| [**eAVEncVideoOutputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavencvideooutputscantype)                           | Spécifie la manière dont l’encodeur entrelace la vidéo de sortie.                                                    |
| [**eAVEncVideoSourceScanType**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideosourcescantype)                           | Spécifie si les frames d’entrée pour un encodeur sont progressifs ou entrelacés.                          |
| [**eAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode)                                           | Spécifie la vitesse de décodage vidéo.                                                                       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de l’API codec](codec-api-reference.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 
