---
description: Le décodeur vidéo MPEG4 2e partie décode les flux vidéo qui ont été encodés en fonction de la norme MPEG4 2e partie.
ms.assetid: 56e32d3c-9bd0-41fe-bb22-e4ff37b7cc5c
title: Décodeur vidéo MPEG-4 part 2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 777e6144684c799eb58f75afd4811ccc8871a46b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201869"
---
# <a name="mpeg-4-part-2-video-decoder"></a>Décodeur vidéo MPEG-4 part 2

Le décodeur vidéo MPEG4 2e partie décode les flux vidéo qui ont été encodés en fonction de la norme MPEG4 2e partie.

Vous pouvez créer une instance du décodeur vidéo MPEG4 partie 2 en appelant **CoCreateInstance**. Pour créer une instance du décodeur qui se comporte comme un objet de média DirectX (DMO), utilisez l’identificateur de classe **CLSID \_ CMpeg4sDecMediaObject**. Pour créer un Istance du décodeur qui se comporte comme une transformation de Media Foundation (MFT), utilisez l’identificateur de classe **CLSID \_ CMpeg4sDecMFT**.

## <a name="input-types"></a>Types d’entrée

Le décodeur vidéo MPEG4 2e partie prend en charge les types de média d’entrée suivants.

-   MEDIASUBTYPE \_ M4S2
-   MEDIASUBTYPE \_ m4s2
-   MEDIASUBTYPE \_ mp4v
-   MEDIASUBTYPE \_ mp4v
-   MEDIASUBTYPE \_ fichiers MP4 à (déprécié)
-   MEDIASUBTYPE \_ fichiers MP4 à (déprécié)

## <a name="output-types"></a>Types de sortie

Le décodeur vidéo MPEG4 2e partie prend en charge les sous-types de médias de sortie suivants lorsqu’il joue le rôle de DMO.

-   MEDIASUBTYPE \_ YV12
-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ YVYU
-   MEDIASUBTYPE \_ NV11
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ Rgb24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

Le décodeur vidéo MPEG4 2e partie prend en charge les sous-types de médias de sortie suivants lorsqu’il joue le rôle de MFT.

-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YV12

## <a name="formats"></a>Formats

Le décodeur vidéo MPEG4 2ème partie accepte les formats suivants.

-   [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)
-   [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (VIH2)
-   [**MFVideoInfo**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoinfo)
-   [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) (seule la partie VIH2 de l’en-tête est utilisée.)

## <a name="interfaces-for-the-dmo"></a>Interfaces pour DMO

Si vous créez une instance du décodeur vidéo MPEG4 2e partie 2 comme DMO, le décodeur expose les interfaces suivantes.

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)

Vous pouvez obtenir une interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) en appelant **CoCreateInstance**, et vous pouvez obtenir une interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) en appelant **QueryInterface**.

## <a name="interfaces-for-the-mft"></a>Interfaces pour la MFT

Si vous créez une instance du décodeur vidéo MPEG2 partie 2 en tant que MFT, le décodeur expose les interfaces suivantes.

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)

Vous pouvez obtenir un pointeur vers l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) en appelant **CoCreateInstance**, et vous pouvez obtenir un pointeur vers l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) en appelant [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes). Vous pouvez obtenir un pointeur vers l’interface [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise) ou [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2) en appelant **QueryInterface** sur la table MFT. Vous pouvez obtenir un pointeur vers l’interface [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) ou [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) en appelant [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) et en passant l’identificateur de service **MF \_ rate \_ Control \_ service**.

## <a name="profiles-and-levels"></a>Profils et niveaux

La spécification MPEG4 définit plusieurs profils, chacun d’entre eux spécifiant les outils qu’un encodeur peut utiliser pour générer un flux encodé. Le décodeur vidéo MPEG4 part2 prend en charge deux de ces profils : un profil visuel simple et un profil simple avancé. En d’autres termes, le décodeur vidéo MPEG4 partie 2 peut décoder les flux qui ont été encodés selon le profil d’élément visuel simple ou le profil simple avancé.

Le profil visuel simple prend en charge la transmission de base d’une vidéo à faible vitesse de transmission en mode progressive. Il prend uniquement en charge les images intra et de prédiction. Il prend également en charge le mode d’en-tête abrégé, qui offre une compatibilité descendante avec le profil de base H. 263. À compter de Windows 10, le décodeur vidéo MPEG-4 part 2 prend également en charge H. 263v2 (H. 263 +) qui prend en charge les tailles d’images personnalisées.

Le profil simple avancé prend en charge tous les outils du profil visuel simple et, en outre, prend en charge la vidéo entrelacée, les images B, la compensation de mouvement Quarter-PEL, les tables de quantification supplémentaires et la compensation de mouvement globale.

La spécification MPEG4 définit également plusieurs niveaux, chacun d’entre eux spécifiant des contraintes sur le flux de sortie généré par un encodeur.

Le tableau suivant présente les profils et les niveaux, ainsi que les résolutions classiques, prises en charge par le décodeur vidéo MPEG4 2e partie 2.



| Profil         | Level | Résolution standard |
|-----------------|-------|--------------------|
| Visuel simple   | 0     | 176 x 144          |
| Visuel simple   | 1     | 176 x 144          |
| Visuel simple   | 2     | 352 x 288          |
| Visuel simple   | 3     | 352 x 288          |
| SimpleVisual    | 4a    | 640 x 480          |
| Visuel simple   | 5     | 720 x 576          |
| Advanced simple | 0     | 176 x 144          |
| Advanced simple | 1     | 176 x 144          |
| Advanced simple | 2     | 352 x 288          |
| Advanced simple | 3     | 352 x 288          |
| Advanced simple | 3b    | 352 x 288          |
| Advanced simple | 4     | 352 x 756          |
| Advanced simple | 5     | 720 x 576          |



 

Pour plus d’informations sur les profils et les niveaux, consultez la spécification MPEG4 2ème partie 2 (ISO/IEC 14496-2) : Information Technology--Coding of Audio-Visual Objects--part 2 : Visual.

## <a name="decoder-properties"></a>Propriétés du décodeur

Pour définir des propriétés sur le décodeur vidéo MPEG4 2e partie 2, utilisez l’interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) ou l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

Le décodeur vidéo MPEG4 2e partie prend en charge les propriétés suivantes.



<table>
<thead>
<tr class="header">
<th>Propriété</th>
<th>Description</th>
<th>Valeur par défaut</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avdecvideoswpowerlevel-property"><strong>CODECAPI_AVDecVideoSWPowerLevel</strong></a></td>
<td>Spécifie le niveau de puissance.<br/> <dl> Windows 7<br />
En écriture seule.<br />
</dl></td>
<td>100</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avdecvideothumbnailgenerationmode-property"><strong>CODECAPI_AVDecVideoThumbnailGenerationMode</strong></a></td>
<td>Spécifie le mode de génération de miniatures.<br/> <dl> Windows 7<br />
En écriture seule.<br />
</dl></td>
<td><strong>VARIANT_FALSE</strong></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Notes

Les identificateurs globaux uniques (GUID) pour les sous-types de média RVB diffèrent selon qu’un décodeur agit comme DMO ou MFT. Les GUID pour les sous-types de média non RVB sont les mêmes, qu’un décodeur agisse comme DMO ou MFT. Pour plus d’informations sur les GUID qui représentent des sous-types de médias, consultez [types de médias](media-types.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MP4SDecd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> </dl>

 

 
