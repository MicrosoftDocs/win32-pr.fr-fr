---
description: Le décodeur vidéo Media Foundation H. 265 est une transformation Media Foundation qui prend en charge le décodage du contenu H. 265/HEVC dans l’annexe B et qui peut être utilisée pour la lecture de fichiers MP4 et M2TS.
ms.assetid: BBE754E4-2AAD-4CFD-B53F-2B66693502EE
title: Décodeur vidéo H. 265/HEVC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c764353e04da0113b51c4efb0d39fad02c84b98859e154d24866229c3a524385
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777199"
---
# <a name="h265--hevc-video-decoder"></a>Décodeur vidéo H. 265/HEVC

Le décodeur vidéo Media Foundation H. 265 est une [transformation Media Foundation](media-foundation-transforms.md) qui prend en charge le décodage du contenu h. 265/HEVC dans l’annexe B et qui peut être utilisée pour la lecture de fichiers MP4 et M2TS.

Le décodeur vidéo H. 265 expose les interfaces suivantes.

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (pris en charge dans Windows 8)
-   [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

Pour créer une instance du décodeur, appelez la fonction [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) ou [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

## <a name="input-types"></a>Types d’entrée

Le type d’entrée doit contenir au moins les deux attributs suivants :



| Attribut                                                 | Description                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**\_type de \_ majeurese MF MT \_**](mf-mt-major-type-attribute.md) | **\_Vidéo MFMediaType**                                                                        |
| [**\_sous- \_ type MF MT**](mf-mt-subtype-attribute.md)        | [MFVideoFormat \_ HEVC](video-subtype-guids.md) ou MFVideoFormat \_ HEVC \_ es |



 

Le premier sous-type de média, MFVideoFormat \_ HEVC, indique que les exemples de supports transportent le flux de sortie H. 265 avec les codes de démarrage et que le flux a des SPS/PPS entrelacés. Il suppose une trame par échantillon.

Le sous-type de média MFVideoFormat \_ HEVC \_ es permet d’indiquer que les exemples de supports transportent des flux binaires élémentaires H. 265, où chaque exemple peut contenir une image partielle, plusieurs images, certaines images et une image partielle.

Les types de média d’entrée ne peuvent pas changer dynamiquement entre deux types. Le décodeur peut détecter les modifications de format de sortie en cours en fonction de la syntaxe de flux élémentaire (proportions, dimension, indicateurs entrelacés, informations de colorimétrie) et déclencher les modifications de type de média de sortie correspondantes.

Pour le type de média d’entrée, le décodeur s’attend à ce que la source définisse le profil approprié. Par exemple, si le contenu va être 10, le type de média d’entrée doit spécifier le profil en tant que Main10.

## <a name="output-types"></a>Types de sortie

Le décodeur prend en charge les sous-types de sortie suivants :

-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ P010**

Pour plus d’informations sur ces sous-types, consultez [GUID sous-type de vidéo](video-subtype-guids.md).

## <a name="transform-attributes"></a>Attributs de transformation

Le décodeur H. 265 implémente la méthode [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Les applications peuvent utiliser cette méthode pour récupérer ou définir les attributs suivants.



| Attribut                                                                                       | Description                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)                                     | Active ou désactive le mode de décodage à latence faible.                                                                                |
| [CODECAPI \_ AVDecNumWorkerThreads](codecapi-avdecnumworkerthreads.md)                           | Définit le nombre de threads de travail utilisés par le décodeur.                                                                        |
| [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) | Active ou désactive le mode de génération de miniatures.                                                                                |
| [\_longueur de Nalu MF \_ \_ définie](mf-nalu-length-set.md)                                                 | Indique que les informations de longueur NALU sont envoyées en tant qu’objet BLOB avec chaque exemple H. 265 compressé.                              |
| [\_ \_ informations sur la longueur Nalu MF \_](mf-nalu-length-information.md)                                 | Indique les longueurs de NALUs dans l’exemple. Il s’agit d’un objet BLOB MF qui est défini sur les exemples d’entrée compressés sur le décodeur H. 265. |
| [\_ \_ nombre minimal d' \_ échantillons de sortie MF \_ sa \_](mf-sa-minimum-output-sample-count.md)                 | Spécifie le nombre maximal d’échantillons de sortie.                                                                               |



 

Le décodeur H. 265 prend en charge l’interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) . Cette interface fournit une API alternativate pour définir les propriétés de codec suivantes.

-   [CODECAPI \_ AVDecNumWorkerThreads](codecapi-avdecnumworkerthreads.md)
-   [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)

## <a name="format-constraints"></a>Contraintes de format

Le décodeur prend en charge les formats suivants :



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Profils/niveaux    | Profils main, main Still image et Main10                                                                                                                                                                                                                        |
| Formats de chrominance     | 4:2:0 Chroma                                                                                                                                                                                                                                                         |
| Résolution minimale | 48 × 48 pixels                                                                                                                                                                                                                                                       |
| Résolution maximale | 4096 × 2304 pixels<br/> La résolution maximale garantie pour l’accélération DXVA est de 1920 × 1088 pixels ; à des résolutions supérieures, le décodage s’effectue avec DXVA, s’il est pris en charge par le matériel sous-jacent ; sinon, le décodage est effectué avec le logiciel.<br/> |
| DXVA               | Le décodeur prend en charge DX11 et DX12 DXVA, mais pas DXVA version 2 ou DXVA version 1.                                                                                                                                                                                                         |



 

Les données d’entrée doivent être conformes à l’annexe B de l’ITU-T H. 265 \| ISO/IEC 23008-2. Les données doivent inclure les codes de début. Le décodeur ignore les octets jusqu’à ce qu’il trouve un jeu de paramètres de séquence (SPS) et un jeu de paramètres d’image (PPS) valides dans le flux d’octets.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| DLL<br/>                      | <dl> <dt>hevcdecoder.dll</dt> <dt>hevcdecoder_store.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> </dl>

 

 
