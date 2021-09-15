---
description: Spécifie le taux de traitement bloc macro maximal pour un flux vidéo H. 264.
ms.assetid: 882F54D1-A963-4016-BEC7-F9C1AC5885FD
title: Attribut MF_MT_H264_MAX_MB_PER_SEC (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b53bdbabd9a633464ed388f2309627b69413c27
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412991"
---
# <a name="mf_mt_h264_max_mb_per_sec-attribute"></a>\_Attribut de \_ \_ nombre maximal de \_ Mo \_ par \_ seconde pour MF MT H264 –

Spécifie le taux de traitement bloc macro maximal pour un flux vidéo H. 264.

## <a name="data-type"></a>Type de données

**\[ UInt32 \]** stocké en tant que **UINT8 \[ \]**

## <a name="applies-to"></a>S’applique à

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Notes

Cet attribut s’applique aux types de média pour les flux H. 264 transmis sur USB. La valeur de l’attribut est un tableau de valeurs UINT32 qui correspondent aux champs suivants dans le descripteur de format vidéo UVC 1,5 H. 264.

| Élément de tableau | Champ de descripteur                                           |
|---------------|------------------------------------------------------------|
| 0             | **dwMaxMBperSecOneResolutionNoScalability**                |
| 1             | **dwMaxMBperSecTwoResolutionsNoScalability**               |
| 2             | **dwMaxMBperSecThreeResolutionsNoScalability**             |
| 3             | **dwMaxMBperSecFourResolutionsNoScalability**              |
| 4             | **dwMaxMBperSecOneResolutionTemporalScalability**          |
| 5             | **dwMaxMBperSecTwoResolutionsTemporalScalablility**        |
| 6             | **dwMaxMBperSecThreeResolutionsTemporalScalability**       |
| 7             | **dwMaxMBperSecFourResolutionsTemporalScalability**        |
| 8             | **dwMaxMBperSecOneResolutionTemporalQualityScalability**   |
| 9             | **dwMaxMBperSecTwoResolutionsTemporalQualityScalability**  |
| 10            | **dwMaxMBperSecThreeResolutionsTemporalQualityScalablity** |
| 11            | **dwMaxMBperSecFourResolutionsTemporalQualityScalability** |
| 12            | **dwMaxMBperSecOneResolutionFullScalability**              |
| 13            | **dwMaxMBperSecTwoResolutionsFullScalability**             |
| 14            | **dwMaxMBperSecThreeResolutionsFullScalability**           |
| 15            | **dwMaxMBperSecFourResolutionsFullScalability**            |



 

Cet attribut est également utilisé avec les [encodeurs de caméra H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 




