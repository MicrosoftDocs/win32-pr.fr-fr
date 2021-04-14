---
description: Ce filtre décode la vidéo MPEG-1, MPEG-2, H. 264.
ms.assetid: d8195c3a-97ac-4ad1-a097-18878c8fda6f
title: Décodeur vidéo Microsoft MPEG-2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8460b5b554fffc8f0dd8679810e5ef3f42bcb004
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392428"
---
# <a name="microsoft-mpeg-2-video-decoder"></a>Décodeur vidéo Microsoft MPEG-2

Ce filtre décode la vidéo MPEG-1, MPEG-2, H. 264.

> [!Note]  
> Le décodage de la vidéo H. 264 requiert Windows 7.

 

> [!Note]  
> Ce filtre n’est pas pris en charge sur les plateformes IA-64.

 

Dans le registre, le nom convivial de ce filtre est « Microsoft DTV-DVD Video décoder ».



Informations de filtre

Interfaces de filtre

[**IAMDecoderCaps**](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps)<br/> [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

Types de média de broche d’entrée

Broche d’entrée vidéo :

-   \_ \_ Pack chiffré DVD \_ de MediaType, \_ vidéo MEDIASUBTYPE MPEG2 \_
-   MEDIATYPE \_ MPEG2 \_ PES, MEDIASUBTYPE \_ MPEG2 \_ Video
-   \_Vidéo MediaType, MEDIASUBTYPE \_ MPEG1Packet
-   \_Vidéo MediaType, MEDIASUBTYPE \_ MPEG1Payload
-   \_Vidéo MediaType, \_ vidéo MEDIASUBTYPE MPEG2 \_

Broche d’entrée de la sous-image :<br/>

-   \_ \_ Pack chiffré DVD de MediaType, sous- \_ \_ image de DVD MEDIASUBTYPE \_

À compter de Windows 7, la broche d’entrée vidéo prend également en charge les types d’entrée suivants :<br/>

-   **MediaType \_ Vidéo**, **MEDIASUBTYPE \_ AVC1**
-   **MediaType \_ Vidéo**, **MEDIASUBTYPE \_ H264 –**
-   **MediaType \_ Vidéo**, **MEDIASUBTYPE \_ H264 –**
-   **MediaType \_ Vidéo**, **MEDIASUBTYPE \_ x264**
-   **MediaType \_ Vidéo**, **MEDIASUBTYPE \_ x264**

Pour plus d’informations, consultez [types de vidéo H. 264](h-264-video-types.md) . Le type de média d’entrée peut changer dynamiquement entre les types MPEG2 et H. 264.<br/>

Interfaces pin d’entrée

[**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IMFSampleProtection**](/windows/win32/api/mfidl/nn-mfidl-imfsampleprotection)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Types de média de broche de sortie

Broche de sortie vidéo :

-   \_Vidéo MediaType, DXVA \_ ModeMPEG2 \_ A (DXVA 1,0)
-   \_Vidéo MediaType, DXVA \_ ModeMPEG2 \_ C (DXVA 1,0)
-   \_Vidéo MediaType, MEDIASUBTYPE \_ I420 (décodage logiciel ou DXVA 2.0)
-   \_Vidéo MediaType, MEDIASUBTYPE \_ NV12 (décodage logiciel ou DXVA 2.0)
-   \_Vidéo MediaType, MEDIASUBTYPE \_ YUY2 (décodage logiciel ou DXVA 2.0)
-   \_Vidéo MediaType, MEDIASUBTYPE \_ IMC3 (DXVA 2.0 uniquement)
-   \_Vidéo MediaType, MEDIASUBTYPE \_ IMC4 (DXVA 2.0 uniquement)
-   \_Vidéo MediaType, MEDIASUBTYPE \_ S340 (DXVA 2.0 uniquement)
-   \_Vidéo MediaType, MEDIASUBTYPE \_ YV12 (DXVA 2.0 uniquement)

Broche de sortie ligne-21 :<br/>

-   MEDIATYPE \_ AUXLine21Data, MEDIASUBTYPE \_ Line21 \_ GOPPacket

Broche de sortie de la sous-image :<br/>

-   \_Vidéo MediaType, MEDIASUBTYPE \_ AI44
-   \_Vidéo MediaType, MEDIASUBTYPE \_ ARGB32
-   \_Vidéo MediaType, MEDIASUBTYPE \_ ARGB4444
-   \_Vidéo MediaType, MEDIASUBTYPE \_ AYUV

Interfaces de broche de sortie

[**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) (broche de sortie vidéo uniquement)<br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig)<br/>

CLSID du filtre

**CLSID \_ CMPEG2VidDecoderDS** (défini dans wmcodecdsp. h)

Exécutable

msmpeg2vdec.dll

[Mérite](merit.md)

**Mérite \_ NORMAL** -1

[Catégorie de filtre](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Notes

Ce filtre a deux broches d’entrée et trois broches de sortie.

Broches d’entrée :

-   Entrée vidéo
-   Entrée de sous-image

Broches de sortie :

-   Sortie vidéo
-   Sortie ligne-21
-   Sortie de sous-image

Le filtre ne crée pas la broche de sortie de sous-image, sauf si la broche d’entrée vidéo est connectée avec un type de média de **\_ \_ \_ Pack chiffré de DVD MediaType** .

### <a name="mpeg-12-support"></a>Support MPEG-1/2

Pour MPEG-1 et MPEG-2, le décodeur prend en charge les formats suivants :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Profils/niveaux</td>
<td>N’importe quelle combinaison des profils et niveaux suivants :<br/>
<ul>
<li>Profils : simple, main</li>
<li>Niveaux : faible, principal, élevé, élevé 1440</li>
</ul></td>
</tr>
<tr class="even">
<td>Formats de chrominance</td>
<td>4:2:0 Chroma</td>
</tr>
<tr class="odd">
<td>Résolution maximale</td>
<td>1920 × 1088 pixels</td>
</tr>
<tr class="even">
<td>DXVA</td>
<td>Le décodeur prend en charge la version 1 et la version 2 de DirectX Video Acceleration (DXVA).</td>
</tr>
</tbody>
</table>



 

Le décodeur ne prend pas en charge les flux binaires évolutifs. L’entrée doit être un flux vidéo élémentaire.

Le décodeur ne prend pas en charge les formats de chrominance 4:2:2.

### <a name="h264-support"></a>Prise en charge H. 264

Pour H. 264, le décodeur prend en charge les formats suivants :



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Profils/niveaux    | Les profils de base, principal et élevé, jusqu’au niveau 5,1. (Pour plus d’informations, consultez la spécification ITU-T H. 264.)                                                                                                                                                                          |
| Formats de chrominance     | 4:2:0 Chroma ou monochrome                                                                                                                                                                                                                                                |
| Résolution minimale | 48 × 48 pixels                                                                                                                                                                                                                                                            |
| Résolution maximale | 1920 × 1088 pixels                                                                                                                                                                                                                                                        |
| DXVA               | Le décodeur prend en charge la version 2 DXVA, mais pas la version 1 de la version DXVA. Le décodage DXVA est pris en charge uniquement pour les flux de bits de ligne de base, principal et de profil principal compatibles. (Les flux de bits de base compatibles avec les principaux sont définis comme **profil \_ idc**= 66 et **\_ \_ indicateur Set1 restreint**= 1.) |



 

Le décodeur ne prend pas en charge la technologie de grain de film.

Pour plus d’informations sur les types de média H. 264, consultez la page [types de vidéo h. 264](h-264-video-types.md).

### <a name="codec-properties"></a>Propriétés du codec

Les broches d’entrée prennent en charge les jeux de propriétés suivants via [**IKsPropertySet**](ikspropertyset.md):

-   [**Jeu de propriétés protection de copie de DVD**](dvd-copy-protection-property-set.md)
-   [**Jeu de propriétés**](dvd-subpicture-property-set.md) de sous-image de DVD (code confidentiel de sous-image uniquement)

Les broches d’entrée prennent en charge les propriétés suivantes par le biais de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Propriété                                                                  | Nécessite      |
|---------------------------------------------------------------------------|---------------|
| [**AVDecCommonInputFormat**](avdeccommoninputformat-property.md)         | Windows Vista |
| [**AVDecVideoInputScanType**](avdecvideoinputscantype-property.md)       | Windows Vista |
| [**AVDecVideoPixelAspectRatio**](avdecvideopixelaspectratio-property.md) | Windows Vista |



 

Le filtre prend en charge les propriétés suivantes par le biais de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Propriété                                                                                | Nécessite      |
|-----------------------------------------------------------------------------------------|---------------|
| [**AVDecMmcssClass**](avdecmmcss-property.md)                                          | Windows Vista |
| [**AVDecVideoAcceleration \_ H264 –**](avdecvideoacceleration-h264-property.md)            | Windows 7     |
| [**AVDecVideoAcceleration \_ MPEG2**](avdecvideoacceleration-mpeg2-property.md)          | Windows 7     |
| [**AVDecVideoDropPicWithMissingRef**](avdecvideodroppicwithmissingref-property.md)     | Windows 7     |
| [**AVDecVideoFastDecodeMode**](avdecvideofastdecodemode.md)                            | Windows 7     |
| [**AVDecVideoImageSize**](avdecvideoimagesize.md)                                      | Windows 7     |
| [**AVDecVideoSoftwareDeinterlaceMode**](avdecvideosoftwaredeinterlacemode-property.md) | Windows 7     |
| [**AVDecVideoThumbnailGenerationMode**](avdecvideothumbnailgenerationmode-property.md) | Windows 7     |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista Édition familiale Premium, Windows Vista Édition intégrale, Windows 7 Édition familiale Premium, Windows 7 professionnel, Windows 7 entreprise, applications de bureau Windows 7 édition intégrale \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> <dt>

[**Types de supports DVD**](dvd-media-types.md)
</dt> <dt>

[Types vidéo H. 264](h-264-video-types.md)
</dt> </dl>

 

 
