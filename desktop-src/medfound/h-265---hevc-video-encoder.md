---
description: L’encodeur vidéo Media Foundation H. 265 est une transformation Media Foundation qui prend en charge l’encodage de contenu au format H. 265/HEVC.
ms.assetid: 790CFB39-6FC0-432D-A434-5262C30EABF4
title: Encodeur vidéo H. 265/HEVC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b95eee96d3313df2604919883cf631b0aef999f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196783"
---
# <a name="h265--hevc-video-encoder"></a>Encodeur vidéo H. 265/HEVC

L’encodeur vidéo Media Foundation H. 265 est une [transformation Media Foundation](media-foundation-transforms.md) qui prend en charge l’encodage de contenu au format H. 265/HEVC. L’encodeur prend en charge les profils suivants :

-   Profil Main

L’encodeur vidéo H. 265 expose les interfaces suivantes :

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a>Types d’entrée

Le type de média d’entrée doit avoir l’un des sous-types suivants :

-   **MFVideoFormat \_ IYUV**
-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ YUY2**
-   **MFVideoFormat \_ YV12**

Pour plus d’informations sur ces sous-types, consultez [GUID sous-type de vidéo](video-subtype-guids.md).

Le type de sortie doit être défini avant le type d’entrée. Tant que le type de sortie n’est pas défini, la méthode [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) de l’encodeur retourne le **type de \_ transformation MF E \_ \_ \_ non \_ défini**.

## <a name="output-types"></a>Types de sortie

L’encodeur prend en charge un seul sous-type de sortie :

-   **MFVideoFormat \_ H265**

Définissez les attributs suivants sur le type de média de sortie.




| Attribut | Description | 
|-----------|-------------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Type principal. Doit être <strong>MFMediaType_Video</strong>. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Sous-type de vidéo. Doit être <strong>MFVideoFormat_HEVC</strong>. | 
| <a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a> | Vitesse moyenne des bits encodés, en bits par seconde. Doit être supérieur à zéro. | 
| <a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a> | Fréquence d’images. | 
| <a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a> | Taille du frame. | 
| <a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a> | Mode entrelacé. | 
| <a href="mf-mt-video-profile.md">MF_MT_VIDEO_PROFILE</a> | Profil d’encodage H. 265.<br /> Les valeurs prises en charge sont les suivantes : <br /><ul><li><strong>eAVEncH265VProfile_Main_420_8</strong></li></ul> | 
| <a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a> | Spécifie le niveau de la vidéo codée. Pour plus d’informations sur les contraintes de profil et de niveau, reportez-vous à l’annexe A de l’ITU-T H. 265.<br /> | 
| <a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a> | facultatif. Spécifie les proportions en pixels. La valeur par défaut est 1:1. | 




 

Une fois le type de sortie défini, l’encodeur vidéo met à jour le type en ajoutant l’attribut d' [**\_ \_ \_ \_ en-tête de séquence MPEG MF MT**](mf-mt-mpeg-sequence-header-attribute.md) . Cet attribut contient l’en-tête de séquence.

## <a name="supported-imftransform-methods"></a>Méthodes IMFTransform prises en charge

Les méthodes suivantes de l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) sont prises en charge pour l’encodeur H. 265/HEVC :

-   [**GetAttributes,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)
-   [**GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)
-   [**GetInputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)
-   [**GetInputStatus**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstatus)
-   [**GetInputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)
-   [**GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)
-   [**GetOutputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)
-   [**GetOutputStatus**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus)
-   [**GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)
-   [**GetStreamCount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount)
-   [**GetStreamLimits**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits)
-   [**ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
-   [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)
-   [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)
-   [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
-   [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)
-   [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
-   [**SetOutputBounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds)

Toutes les autres méthodes [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) retournent l’erreur E \_ NOTIMPL.

## <a name="supported-icodecapi-methods"></a>Méthodes ICodecAPI prises en charge

Les méthodes suivantes de l’interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) sont prises en charge pour l’encodeur H. 265/HEVC :

-   [**IsSupported**](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)
-   [**GetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [**GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [**GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)

Toutes les autres méthodes [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) retournent l’erreur E \_ NOTIMPL.

## <a name="codec-properties"></a>Propriétés du codec

L’encodeur H. 265 implémente l’interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) pour définir les paramètres d’encodage. Il prend en charge les propriétés suivantes.

Pour connaître la configuration requise du codec pour la certification de l’encodeur TPM, **consultez la section** ci-dessous.




| Propriété | Description | 
|----------|-------------|
| <a href="/windows/desktop/DirectShow/avenccommonratecontrolmode-property"><strong>CODECAPI_AVEncCommonRateControlMode</strong></a> | Définit le mode de contrôle de la fréquence. Les modes pris en charge sont les suivants :<br /><ul><li><strong>eAVEncCommonRateControlMode_CBR</strong></li><li><strong>eAVEncCommonRateControlMode_Quality</strong></li></ul>Si d’autres modes sont spécifiés, le contrôle de taux de <strong>eAVEncCommonRateControlMode_CBR</strong> est utilisé.<br /> Il s’agit d’une valeur VT_UI4.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> | Définit la vitesse de transmission moyenne pour le flux binaire encodé, en bits par seconde. <br /> La plage valide est [1... 2 ³ ² – 1]. <br /> Il s’agit d’une valeur VT_UI4.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a> | Définit la taille de la mémoire tampon, en octets, pour l’encodage à débit binaire constant (CBR).<br /> La plage valide est [1... 2 ³ ² – 1]. <br /> Il s’agit d’une valeur VT_UI4.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a> | Définit le débit maximal pour les modes de contrôle de débit qui autorisent une vitesse de transmission maximale. <br /> La plage valide est [1... 2 ³ ² – 1]. <br /> Il s’agit d’une valeur VT_UI4.<br /> | 
| <a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a> | Définit le nombre d’images d’un en-tête GOP sur le suivant, y compris l’ancrage de début, mais pas le suivant. <br /> La plage valide est [0... 2 ³ ² – 1]. Si la valeur est zéro, l’encodeur sélectionne la taille de groupe d’images. La valeur par défaut est zéro. <br /> Il s’agit d’une valeur VT_UI4.<br /> | 
| <a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a> | Active ou désactive le mode faible latence. <br /> Il s’agit d’une valeur VT_BOOL.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a> | Définit le compromis de qualité/vitesse. Cette valeur affecte la façon dont l’encodeur effectue différentes opérations d’encodage, telles que la compensation de mouvement. À des niveaux de complexité plus élevés, l’encodeur s’exécute plus lentement, mais produit une meilleure qualité à la même vitesse de transmission. <br /> La plage valide est comprise entre 0 et 100. En interne, cette valeur est mappée à un plus petit ensemble de niveaux de qualité/vitesse pris en charge par l’encodeur.<br /> Il s’agit d’une valeur VT_UI4.<br /> | 
| <a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a> | Force l’encodeur à coder le frame suivant comme une image clé.<br /> Il s’agit d’une valeur VT_UI4.<br /> | 
| <a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a> | Lorsque cette propriété est définie, l’encodeur utilise le QP spécifié pour encoder le frame suivant et tous les frames suivants jusqu’à ce qu’un nouveau QP soit spécifié. <br /> Plage valide : comprise entre 0 et 51 <br /> | 
| <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> | Cette propriété définit une limite au minimum de QP que l’encodeur peut utiliser pendant le RateControl CBR.<br /> Il s’agit d’une valeur VT_UI4.<br /> | 
| <a href="codecapi-avencvideomaxqp.md">CODECAPI_AVEncVideoMaxQP</a> | Cette propriété définit une limite au maximum de QP que l’encodeur peut utiliser pendant le RateControl CBR.<br /> Il s’agit d’une valeur VT_UI4.<br /> | 
| <a href="codecapi-videoencoderdisplaycontenttype.md">CODECAPI_VideoEncoderDisplayContentType</a> | Définit si le contenu est une vidéo en plein écran, par opposition au contenu d’écran qui peut avoir une fenêtre de vidéo plus petite ou n’avoir aucune vidéo du tout.<br /> Il s’agit d’une valeur VT_UI4.<br /> | 
| <a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a> | Définit le nombre de threads utilisés pour effectuer l’opération de compression. L’encodeur divise le frame en mosaïques, de sorte que le nombre de threads est égal au nombre de vignettes.<br /><ul><li>Nombre de processeurs logiques. Le nombre de threads doit être inférieur ou égal au nombre de processeurs logiques.</li><li>Taille du frame. La taille d’une vignette doit être supérieure ou égale à 265x64 pixels.</li><li>Parité. Le nombre de threads doit être une valeur paire. Si la valeur spécifiée est irrégulière, la valeur paire inférieure suivante sera utilisée.</li></ul>Il s’agit d’une valeur VT_UI4.<br /> | 




 

## <a name="certified-hardware-encoder"></a>Encodeur matériel certifié

Si un encodeur matériel certifié est présent, il est généralement utilisé à la place de l’encodeur système de la boîte de réception pour Media Foundation scénarios associés. Des encodeurs certifiés sont requis pour prendre en charge un certain ensemble de propriétés **ICodecAPI** et peuvent éventuellement prendre en charge un autre ensemble de propriétés. Le processus de certification doit garantir que les propriétés requises sont correctement prises en charge et, si une propriété facultative est prise en charge, qu’elle est également prise en charge correctement.

Voici l’ensemble des propriétés **ICodecAPI** obligatoires et facultatives pour que les encodeurs passent la certification de l’encodeur TPM.

-   [CODECAPI \_ AVEncCommonRateControlMode](../directshow/avenccommonratecontrolmode-property.md)
-   [CODECAPI \_ AVEncCommonQuality](../directshow/avenccommonquality-property.md)
-   [CODECAPI \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)
-   [CODECAPI \_ AVEncCommonBufferSize](../directshow/avenccommonbuffersize-property.md)
-   [CODECAPI \_ AVEncMPVGOPSize](../directshow/avencmpvgopsize-property.md)
-   [CODECAPI \_ AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md)
-   [CODECAPI \_ AVEncVideoForceKeyFrame](codecapi-avencvideoforcekeyframe.md)

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| DLL<br/>                      | <dl> <dt>Mfh265enc.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> </dl>

 

 
