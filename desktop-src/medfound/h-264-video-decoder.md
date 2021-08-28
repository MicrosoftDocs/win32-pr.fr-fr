---
description: Le Media Foundation le décodeur vidéo H. 264 est une transformation Media Foundation qui prend en charge le décodage des profils de base, principal et élevé, jusqu’au niveau 5,1.
ms.assetid: 783a3618-981a-4573-9e9e-ebf5eeb75d06
title: Décodeur vidéo H. 264
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d70b7e0f01dcf283729aebd58e2f361513edaba2ea12fde217968a7935cda9f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449169"
---
# <a name="h264-video-decoder"></a>Décodeur vidéo H. 264

Le Media Foundation le décodeur vidéo H. 264 est une [transformation Media Foundation](media-foundation-transforms.md) qui prend en charge le décodage des profils de base, principal et élevé, jusqu’au niveau 5,1.

Le décodeur vidéo H. 264 expose les interfaces suivantes.

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (pris en charge dans Windows 8)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

Pour créer une instance du décodeur, effectuez l’une des opérations suivantes :

-   Appelez la fonction [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) ou [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .
-   Appelez [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance). Le CLSID du décodeur est **CLSID \_ CMSH264DecoderMFT**, déclaré dans wmcodecdsp. h.

## <a name="input-types"></a>Types d’entrée

Le type d’entrée doit contenir au moins les deux attributs suivants :



| Attribut                                                 | Description                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**\_type de \_ majeurese MF MT \_**](mf-mt-major-type-attribute.md) | **\_Vidéo MFMediaType**                                                                        |
| [**\_sous- \_ type MF MT**](mf-mt-subtype-attribute.md)        | [MFVideoFormat \_ H264 –](video-subtype-guids.md) ou MFVideoFormat \_ H264 – \_ es |



 

Si le type d’entrée contient uniquement ces deux attributs, le décodeur offrira un type de sortie par défaut, qui agit comme un espace réservé. Quand le décodeur reçoit suffisamment d’échantillons d’entrée pour produire une trame de sortie, il signale une modification de format en retournant le **changement de flux de \_ \_ transformation \_ \_ MF E** à partir de [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Pour plus d’informations sur la gestion des modifications de format, consultez la documentation de **ProcessOutput** .

Pour éviter une modification de format initiale, fournissez autant d’informations que possible dans le type d’entrée, notamment :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></td>
<td>Fréquence d’images.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></td>
<td>Dimensions de l’image.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></td>
<td>Mode entrelacé.
<blockquote>
[!Note]<br />
Dans la vidéo H. 264, la structure entrelacée peut changer de manière dynamique, donc la valeur recommandée de cet attribut est <strong>MFVideoInterlace_MixedInterlaceOrProgressive</strong>. Les informations entrelacées dans le flux élémentaire vidéo sont prioritaires sur le type de média. Pour plus d’informations, consultez l' <a href="video-interlacing.md">entrelacement de vidéos</a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></td>
<td>Proportions de pixels.</td>
</tr>
</tbody>
</table>



 

Le type d’entrée doit être défini avant le type de sortie. Tant que le type d’entrée n’est pas défini, la méthode [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) de l’encodeur retourne le **type de \_ transformation MF E \_ \_ \_ non \_ défini**.

## <a name="output-types"></a>Types de sortie

Le décodeur prend en charge les sous-types de sortie suivants :

-   **MFVideoFormat \_ I420**
-   **MFVideoFormat \_ IYUV**
-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ YUY2**
-   **MFVideoFormat \_ YV12**

Pour plus d’informations sur ces sous-types, consultez [GUID sous-type de vidéo](video-subtype-guids.md).

## <a name="transform-attributes"></a>Attributs de transformation

Le décodeur H. 264 implémente la méthode [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Les applications peuvent utiliser cette méthode pour récupérer ou définir les attributs suivants.



| Attribut                                                                                       | Description                                                                                |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVDecVideoAcceleration \_ H264 –](../directshow/avdecvideoacceleration-h264-property.md)            | Active ou désactive l’accélération matérielle.                                                 |
| [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) | Active ou désactive le mode de génération de miniatures.                                             |
| [Compatible avec la prise en \_ \_ charge Direct3D MF \_](mf-sa-d3d-aware-attribute.md)                                             | Indique que le décodeur prend en charge l’accélération vidéo DirectX (DXVA). Traiter en lecture seule. |



 

dans Windows 8, le décodeur H. 264 prend également en charge les attributs suivants.



| Attribut                                                                                                     | Description                                                                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)                                                   | Active ou désactive le mode de décodage à latence faible.                                                              |
| [CODECAPI \_ AVDecNumWorkerThreads](codecapi-avdecnumworkerthreads.md)                                         | Définit le nombre de threads de travail utilisés par le décodeur.                                                      |
| [CODECAPI \_ AVDecVideoMaxCodedWidth](codecapi-avdecvideomaxcodedwidth.md)                                     | Définit la largeur maximale d’image que le décodeur acceptera comme type d’entrée.                               |
| [CODECAPI \_ AVDecVideoMaxCodedHeight](codecapi-avdecvideomaxcodedheight.md)                                   | Définit la hauteur d’image maximale que le décodeur acceptera comme type d’entrée.                              |
| [\_ \_ nombre minimal d' \_ échantillons de sortie MF \_ sa \_](mf-sa-minimum-output-sample-count.md)                               | Spécifie le nombre maximal d’échantillons de sortie.                                                             |
| [le \_ DÉcodeur MFT \_ expose les \_ \_ types \_ de sortie dans l' \_ \_ ordre natif](mft-decoder-expose-output-types-in-native-order.md) | Spécifie si un décodeur expose des types de sortie IYUV/I420 (convenant au transcodage) avant d’autres formats. |



 

dans Windows 8, le décodeur H. 264 prend en charge l’interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) . Cette interface fournit une API alternativate pour définir les propriétés de codec suivantes.

-   [CODECAPI \_ AVDecVideoMaxCodedWidth](codecapi-avdecvideomaxcodedwidth.md)
-   [CODECAPI \_ AVDecVideoAcceleration \_ H264 –](../directshow/avdecvideoacceleration-h264-property.md)
-   [CODECAPI \_ AVDecVideoMaxCodedHeight](codecapi-avdecvideomaxcodedheight.md)
-   [CODECAPI \_ AVDecVideoMaxCodedWidth](codecapi-avdecvideomaxcodedwidth.md)
-   [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)

## <a name="format-constraints"></a>Contraintes de format

Le décodeur prend en charge les formats suivants :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Profils/niveaux</td>
<td>Les profils de base, principal et élevé, jusqu’au niveau 5,1. (Pour plus d’informations, consultez la spécification ITU-T H. 264.)</td>
</tr>
<tr class="even">
<td>Formats de chrominance</td>
<td>4:2:0 Chroma ou monochrome</td>
</tr>
<tr class="odd">
<td>Résolution minimale</td>
<td>48 × 48 pixels</td>
</tr>
<tr class="even">
<td>Résolution maximale</td>
<td>4096 × 2304 pixels<br/> La résolution maximale garantie pour l’accélération DXVA est de 1920 × 1088 pixels ; à des résolutions supérieures, le décodage s’effectue avec DXVA, s’il est pris en charge par le matériel sous-jacent ; sinon, le décodage est effectué avec le logiciel.<br/>
<blockquote>
[!Note]<br />
dans Windows 7, la résolution maximale prise en charge est de 1920 × 1088 pixels pour le décodage logiciel et DXVA.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td>DXVA</td>
<td>Le décodeur prend en charge la version 2 DXVA, mais pas la version 1 de la version DXVA. Le décodage DXVA est pris en charge uniquement pour les flux de bits de ligne de base, principal et de profil principal compatibles. (Les flux de bits de base compatibles avec les principaux sont définis comme <strong>profile_idc</strong>= 66 et <strong>constrained_set1_flag</strong>= 1.)</td>
</tr>
</tbody>
</table>



 

Les données d’entrée doivent être conformes à l’annexe B de la norme ISO/IEC 14496-10. Les données doivent inclure les codes de début. Le décodeur ignore les octets jusqu’à ce qu’il trouve un jeu de paramètres de séquence (SPS) et un jeu de paramètres d’image (PPS) valides dans le flux d’octets.

Le décodeur ne prend pas en charge la technologie de grain de film.

> [!Note]  
> une version précédente de la documentation indiquait incorrectement que le décodeur est pris en charge sur Windows Server 2008 R2.

 

si la mise à jour du supplément Platform pour Windows vista est installée, le décodeur vidéo H. 264 est disponible sur Windows vista, mais n’est accessible sur Windows vista qu’à l’aide du [lecteur Source](source-reader.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                  |
| DLL<br/>                      | <dl> <dt>Msmpeg2vdec.dll</dt> </dl> |



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

 

 
