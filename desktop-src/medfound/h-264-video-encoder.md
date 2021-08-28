---
description: 'Le Microsoft Media Foundation encodeur vidéo H. 264 est une transformation Media Foundation qui prend en charge les profils H. 264 suivants :'
ms.assetid: 4d4c768f-b76a-40ca-8736-2f592a4f4cc4
title: Encodeur vidéo H. 264
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 875974c53be265fbcace8cf99e2bdd78d69cdda5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467526"
---
# <a name="h264-video-encoder"></a>Encodeur vidéo H. 264

Le Microsoft Media Foundation encodeur vidéo H. 264 est une [transformation Media Foundation](media-foundation-transforms.md) qui prend en charge les profils H. 264 suivants :

-   Profil de base
-   Profil Main
-   Profil élevé (requiert Windows 8)

L’encodeur vidéo H. 264 expose les interfaces suivantes :

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a>Types d’entrée

Le type de média d’entrée doit avoir l’un des sous-types suivants :

-   **MFVideoFormat_I420**
-   **MFVideoFormat_IYUV**
-   **MFVideoFormat_NV12**
-   **MFVideoFormat_YUY2**
-   **MFVideoFormat_YV12**

Pour plus d’informations sur ces sous-types, consultez [GUID sous-type de vidéo](video-subtype-guids.md).

Le type de sortie doit être défini avant le type d’entrée. Tant que le type de sortie n’est pas défini, la méthode [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) de l’encodeur retourne **MF_E_TRANSFORM_TYPE_NOT_SET**.

## <a name="output-types"></a>Types de sortie

L’encodeur prend en charge un seul sous-type de sortie :

-   **MFVideoFormat_H264**

Définissez les attributs suivants sur le type de média de sortie.




| Attribut | Description | 
|-----------|-------------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Type principal. Doit être <strong>MFMediaType_Video</strong>. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Sous-type de vidéo. Doit être <strong>MFVideoFormat_H264</strong>. | 
| <a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a> | Vitesse moyenne des bits encodés, en bits par seconde. Doit être supérieur à zéro. | 
| <a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a> | Fréquence d’images. | 
| <a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a> | Taille du frame. | 
| <a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a> | Mode entrelacé. | 
| <a href="mf-mt-mpeg2-profile-attribute.md"><strong>MF_MT_MPEG2_PROFILE</strong></a> | Profil d’encodage H. 264.<br /> Les valeurs prises en charge sont les suivantes :<br /><ul><li><strong>eAVEncH264VProfile_Base</strong> (par défaut)</li><li><strong>eAVEncH264VProfile_Main</strong></li><li><strong>eAVEncH264VProfile_High</strong> (requiert Windows 8)</li></ul> | 
| <a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a> | facultatif. Spécifie le niveau d’encodage H. 264.<br /> La valeur par défaut est – 1, ce qui indique que l’encodeur va sélectionner le niveau d’encodage.<br /> Il est recommandé de ne pas définir le niveau dans le type de média et de permettre à l’encodeur de sélectionner le niveau. L’encodeur peut dériver le niveau approprié pour un flux vidéo donné, en tenant compte des contraintes de format et des caractéristiques de la vidéo. Pour plus d’informations sur les contraintes de profil et de niveau, reportez-vous à l’annexe A de l’ITU-T H. 264.<br /> | 
| <a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a> | facultatif. Spécifie les proportions en pixels. La valeur par défaut est 1:1. | 




 

Une fois le type de sortie défini, l’encodeur vidéo met à jour le type en ajoutant l’attribut [**MF_MT_MPEG_SEQUENCE_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) . Cet attribut contient l’en-tête de séquence.

## <a name="codec-properties"></a>Propriétés du codec

L’encodeur H. 264 implémente l’interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) pour définir les paramètres d’encodage. Il prend en charge les propriétés suivantes.

Pour connaître la configuration requise du codec pour la certification de l’encodeur TPM, **consultez la section** ci-dessous.

les propriétés suivantes sont prises en charge dans Windows 7.



| Propriété                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CODECAPI_AVEncCommonRateControlMode**](../directshow/avenccommonratecontrolmode-property.md) | Définit le mode de contrôle de la fréquence. Consultez la section Notes. Le mode par défaut est la vitesse de transmission variable (VBR) sans contrainte.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**CODECAPI_AVEncCommonQuality**](../directshow/avenccommonquality-property.md)                 | Définit le niveau de qualité. Cette propriété s’applique lorsque le mode de contrôle de la fréquence est VBR (**eAVEncCommonRateControlMode_Quality**) basé sur la qualité. La plage valide est comprise entre 1 et 100. La valeur par défaut est 70. <br/> Pour définir ce paramètre, définissez la propriété avant d’appeler [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). <br/> pour définir ce paramètre dans Windows 7, définissez la propriété avant d’appeler [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). L’encodeur ignore les modifications une fois que le type de sortie est défini. <br/> dans Windows 8, cette propriété peut être définie à tout moment pendant l’encodage. Les modifications sont appliquées à partir du frame d’entrée suivant. <br/> En interne, l’encodeur convertit cette propriété en valeur [AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md) . <br/> |



 

Les propriétés suivantes requièrent Windows 8.




| Propriété | Description | 
|----------|-------------|
| <a href="codecapi-avencadaptivemode.md">CODECAPI_AVEncAdaptiveMode</a> | Définit le mode de codage adaptatif. L’encodeur H. 264 prend en charge les modes suivants dans Windows 8 :<ul><li><strong>eAVEncAdaptiveMode_None</strong>. Pas d’encodage adaptatif. (valeur par défaut).</li><li><strong>eAVEncAdaptiveMode_FrameRate</strong>. Modifiez de manière adaptative la fréquence d’images.</li></ul><br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a> | Définit la taille de la mémoire tampon, en octets, pour l’encodage à débit binaire constant (CBR).<br /> La plage valide est [1... 2 ³ ² – 1]. <br /> Requiert Windows 8. <br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a> | Pour l’encodage VBR restreint, spécifie la vitesse à laquelle le « compartiment à fuite » est vidé, en bits par seconde. Cette propriété s’applique lorsque le mode de contrôle de la vitesse est <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong>. <br /> La plage valide est [1... 2 ³ ² – 1]. <br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> | Définit la vitesse de transmission moyenne pour le flux binaire encodé, en bits par seconde. Cette propriété est ignorée si le mode de contrôle de la vitesse est <strong>eAVEncCommonRateControlMode_Quality</strong>. <br /> La plage valide est [1... 2 ³ ² – 1]. <br /> En mode CBR et sans contrainte, la vitesse de transmission moyenne détermine la taille finale du fichier. En mode CBR, la vitesse de transmission moyenne est également la vitesse à laquelle les bits compressés sont vidés du compartiment à fuite. (Pour plus d’informations, consultez <a href="the-leaky-bucket-buffer-model.md">le modèle de tampon de compartiment avec fuite</a>.) <br /> dans Windows 7, la vitesse de transmission moyenne est spécifiée par l’attribut <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> sur le type de média. <br /> dans Windows 8, vous pouvez définir la vitesse de transmission moyenne à l’aide de l’attribut <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> ou de la propriété <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> . Si les deux sont définis, CODECAPI_AVEncCommonMeanBitRate remplace. dans Windows 8, vous pouvez définir la vitesse de transmission moyenne pendant l’encodage. Si la vitesse de transmission change, l’encodeur utilise l’encodage adaptatif.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a> | Définit le compromis de qualité/vitesse. Plage valide :<ul><li>0 – 33 : faible complexité</li><li>34 – 66 : complexité moyenne (par défaut)</li><li>67 – 100 : complexité élevée</li></ul><br /> Cette valeur affecte la façon dont l’encodeur effectue différentes opérations d’encodage, telles que la compensation de mouvement. À des niveaux de complexité plus élevés, l’encodeur s’exécute plus lentement, mais produit une meilleure qualité à la même vitesse de transmission.<br /> | 
| <a href="codecapi-avench264cabacenable.md">CODECAPI_AVEncH264CABACEnable</a> | Active ou désactive le codage arithmétique binaire CABAC (Context-adaptative) pour le codage d’entropie H. 264. La valeur par défaut est <strong>VARIANT_FALSE</strong>. <br /> CABAC n’est pas utilisé pour le profil de ligne de base.<br /> | 
| <a href="codecapi-avench264spsid.md">CODECAPI_AVEncH264SPSID</a> | Définit la valeur de <strong>seq_parameter_set_id</strong> dans l’unité de SPS nal du flux binaire H. 264. <br /> | 
| <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a> | Définit le nombre maximal de frames B consécutifs dans le flux binaire de sortie. Les valeurs autorisées sont :<ul><li>0 : n’utilisez pas les frames B (valeur par défaut).</li><li>1 : utilisez un frame B.</li><li>2 : utilisez deux frames B.</li></ul>Pour définir ce paramètre, définissez la propriété avant d’appeler <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype"><strong>IMFTransform :: SetOutputType</strong></a>. <br /> Pour le profil de ligne de base, le nombre de frames B est toujours égal à zéro. L’encodeur remplacera les valeurs autres que zéro.<br /> Pour les autres profils H. 264, si cette propriété est différente de zéro, le modèle d’encodage est IBBPBBP, où le nombre maximal de frames B consécutifs est égal à <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a>. <br /> | 
| <a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a> | Définit le nombre d’images d’un en-tête GOP sur le suivant, y compris l’ancrage de début, mais pas le suivant. <br /> La plage valide est [0... 2 ³ ² – 1]. Si la valeur est zéro, l’encodeur sélectionne la taille de groupe d’images. La valeur par défaut est zéro. <br /> | 
| <a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a> | Définit le nombre de threads de travail utilisés par un encodeur.<br /> La plage valide est comprise entre 0 et 16. Si la valeur est zéro, l’encodeur sélectionne le nombre de threads. <br /> | 
| <a href="codecapi-avencvideocontenttype.md">CODECAPI_AVEncVideoContentType</a> | Indique le type de contenu vidéo.<br /> | 
| <a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a> | Plage valide : 16 – 51. La valeur par défaut est 24. <br /> Cette propriété s’applique lorsque le mode de contrôle de la vitesse est <strong>eAVEncCommonRateControlMode_Quality</strong>. <br /> Cette propriété configure le même paramètre d’encodage que <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a>. Toutefois, <a href="codecapi-avencvideoencodeqp.md">AVEncVideoEncodeQP</a> permet à l’application de spécifier directement la valeur de QP. Si les deux propriétés sont définies, AVEncVideoEncodeQP remplace. <br /> La valeur par défaut 24 correspond à la valeur par défaut 70 pour le paramètre <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a> .<br /> | 
| <a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a> | Force l’encodeur à coder le frame suivant comme une image clé.<br /> | 
| <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> | Plage valide : comprise entre 0 et 51. La valeur par défaut est 0. <br /> Cette propriété s’applique à tous les modes de contrôle de taux. L’encodeur ne doit pas produire une valeur QP inférieure à ce qui est spécifié par la propriété <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> .<br /> | 
| <a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a> | Active ou désactive le mode faible latence. Consultez « multithread » dans la section Notes.<br /> | 




 

## <a name="remarks"></a>Remarques

L’encodeur prend en charge les modes de contrôle de taux suivants.



| Mode                                  | Constante                                            | Description                                                                                                                                                                                                                                         |
|---------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Débit binaire constant (CBR)               | **eAVEncCommonRateControlMode_CBR**                | L’encodeur tente d’obtenir une vitesse binaire constante, à l’aide d’un modèle de « compartiment perdu ». La vitesse de transmission cible est donnée par la propriété [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) . <br/> Requiert Windows 8. <br/> |
| Taux de bits variable avec restriction (VBR)   | **eAVEncCommonRateControlMode_PeakConstrainedVBR** | L’encodeur utilise un modèle de « compartiment perdu » avec une vitesse de transmission de pic. La vitesse d’écoulement pour le compartiment avec fuite est donnée par la propriété [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md) . <br/> Requiert Windows 8. <br/>     |
| Vitesse de transmission variable (VBR) basée sur la qualité | **eAVEncCommonRateControlMode_Quality**            | L’encodeur tente d’obtenir un niveau de qualité constante, en fonction de la propriété [**AVEncCommonQuality**](../directshow/avenccommonquality-property.md) .                                                                                                           |
| VBR non restreint                     | **eAVEncCommonRateControlMode_UnconstrainedVBR**   | L’encodeur tente d’obtenir le débit cible donné par l’attribut [**MF_MT_AVG_BITRATE**](mf-mt-avg-bitrate-attribute.md) dans le type de média de sortie. Il s’agit du mode par défaut ;                                                              |



 

Les modes CBR et restriction VBR requièrent Windows 8.

dans Windows 8, l’encodeur définit les attributs suivants sur les exemples de sortie :

-   [MFSampleExtension_DecodeTimestamp](mfsampleextension-decodetimestamp.md)
-   [MFSampleExtension_VideoEncodePictureType](mfsampleextension-videoencodepicturetype.md)
-   [MFSampleExtension_VideoEncodeQP](mfsampleextension-videoencodeqp.md)

> [!Note]  
> une version précédente de la documentation indiquait incorrectement que l’encodeur est pris en charge sur Windows Server 2008 R2.

 

### <a name="multithreading"></a>Multithreading

dans Windows 8, l’encodeur prend en charge deux modes d’encodage :

-   **Encodage de la tranche.** Dans ce mode, les tranches sont encodées en parallèle. Chaque tranche est encodée sur un thread différent. Ce mode a une latence faible, car une image unique est encodée en parallèle. Toutefois, cette approche n’est pas mise à l’échelle à mesure que le nombre de cœurs augmente, car le nombre de secteurs est limité par le nombre de lignes bloc macro dans l’image d’entrée.
-   **Encodage à plusieurs frames.** Dans ce mode, l’encodeur accepte plusieurs trames d’entrée et les encode en parallèle. Ce mode évolue mieux dans un environnement multicœur, mais introduit une latence plus grande.

Par défaut, l’encodeur découpe l’encodage pour réduire la latence. Pour activer l’encodage à plusieurs frames, affectez à la propriété [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md) la valeur **VARIANT_FALSE**.

Pour définir le nombre de threads de travail utilisés par l’encodeur, définissez la propriété [CODECAPI_AVEncNumWorkerThreads](codecapi-avencnumworkerthreads.md) .

dans Windows 7, l’encodeur utilise toujours l’encodage de segment.

### <a name="certified-hardware-encoder"></a>Encodeur matériel certifié

Si un encodeur matériel certifié est présent, il est généralement utilisé à la place de l’encodeur système de la boîte de réception pour Media Foundation scénarios associés. Des encodeurs certifiés sont requis pour prendre en charge un certain ensemble de propriétés **ICodecAPI** et peuvent éventuellement prendre en charge un autre ensemble de propriétés. Le processus de certification doit garantir que les propriétés requises sont correctement prises en charge et, si une propriété facultative est prise en charge, qu’elle est également prise en charge correctement.

Voici l’ensemble des propriétés **ICodecAPI** obligatoires et facultatives pour que les encodeurs passent la certification de l’encodeur TPM.

les propriétés Windows 8 et Windows 8.1 **ICodecAPI** suivantes sont requises :

-   [CODECAPI_AVEncCommonRateControlMode](../directshow/avenccommonratecontrolmode-property.md)
-   [CODECAPI_AVEncCommonQuality](../directshow/avenccommonquality-property.md)
-   [CODECAPI_AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md)
-   [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)
-   [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md)
-   [CODECAPI_AVEncCommonBufferSize](../directshow/avenccommonbuffersize-property.md)
-   [CODECAPI_AVEncMPVGOPSize](../directshow/avencmpvgopsize-property.md)
-   [CODECAPI_AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md)
-   [CODECAPI_AVEncVideoForceKeyFrame](codecapi-avencvideoforcekeyframe.md)

les propriétés de Windows 8.1 **ICodecAPI** suivantes sont facultatives, mais sont testées dans tpm si elles sont prises en charge.

-   [CODECAPI_AVEncVideoMinQP](codecapi-avencvideominqp.md)
-   [CODECAPI_AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md)
-   [CODECAPI_AVEncVideoMarkLTRFrame](codecapi-avencvideomarkltrframe.md)
-   [CODECAPI_AVEncVideoUseLTRFrame](codecapi-avencvideouseltrframe.md)
-   [CODECAPI_AVEncVideoEncodeFrameTypeQP](codecapi-avencvideoencodeframetypeqp.md)
-   [CODECAPI_AVEncSliceControlMode](codecapi-avencslicecontrolmode.md)
-   [CODECAPI_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md)
-   [CODECAPI_AVEncVideoMaxNumRefFrame](codecapi-avencvideomaxnumrefframe.md)
-   [CODECAPI_AVEncVideoMeanAbsoluteDifference](codecapi-avencvideomeanabsolutedifference.md)
-   [CODECAPI_AVEncVideoMaxQP](codecapi-avencvideomaxqp.md)
-   [CODECAPI_AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md)
-   [CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (dynamique)
-   [CODECAPI_AVEncH264CABACEnable](codecapi-avench264cabacenable.md)

les propriétés Windows 8 et Windows 8.1 **ICodecAPI** suivantes sont facultatives, mais sont testées dans tpm si elles sont prises en charge.

-   [CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (statique)
-   [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md)

Les propriétés **ICodecAPI** suivantes sont facultatives. Ils ne sont pas testés dans TPM.

-   [CODECAPI_AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| DLL<br/>                      | <dl> <dt>Mfh264enc.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> <dt>

[Prise en charge MPEG-4 dans Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formats multimédias pris en charge dans Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Types de média vidéo](video-media-types.md)
</dt> </dl>

 

 
