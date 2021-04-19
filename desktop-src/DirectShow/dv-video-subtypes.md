---
description: Un certain nombre de sous-types sont définis pour la vidéo DV. Chaque possède un code FOURCC et une valeur GUID correspondante. Tous ces formats ne sont pas pris en charge ; Pour plus d’informations, consultez la section Notes.
ms.assetid: d8390bd4-0339-4955-992c-92b8c9f6bf88
title: Sous-types vidéo DV (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbacb15f5801d959fbc5150546cff04dea687753
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541418"
---
# <a name="dv-video-subtypes"></a>Sous-types vidéo DV

Un certain nombre de sous-types sont définis pour la vidéo DV. Chaque possède un code FOURCC et une valeur GUID correspondante. Tous ces formats ne sont pas pris en charge ; Pour plus d’informations, consultez la section Notes.

## <a name="consumer-formats"></a>Formats grand public



| FOURCC | GUID               | Débit des données | Description                  |
|--------|--------------------|-----------|------------------------------|
| 'dvsl' | MEDIASUBTYPE \_ dvsl | 12,5 Mbits/s | SD-magnétoscope numérique (525-60 ou 625-50)   |
| 'dvsd' | MEDIASUBTYPE \_ DVSD | 25 Mbits/s   | SDL-magnétoscope numérique (525-60 ou 625-50)  |
| 'dvhd' | MEDIASUBTYPE \_ dvhd | 50 Mbits/s   | HD-magnétoscope numérique (1125-60 ou 1250-50) |



 

Reportez-vous à IEC-61834 pour plus d’informations sur ces formats.

## <a name="professional-formats"></a>Formats professionnels



| FOURCC | GUID               | Débit des données | Description                                 |
|--------|--------------------|-----------|---------------------------------------------|
| 'dv25' | MEDIASUBTYPE \_ DV25 | 25 Mbits/s   | DVCPRO 25 (525-60 ou 625-50).               |
| 'dv50' | MEDIASUBTYPE \_ DV50 | 50 Mbits/s   | DVCPRO 50 (525-60 ou 625-50)                |
| 'dvh1' | MEDIASUBTYPE \_ dvh1 | 100 Mbits/s  | DVCPRO 100 (1080/60i, 1080/50i, ou 720/60P) |



 

Pour plus d’informations sur dvh1, reportez-vous à SMPTE 314M pour plus d’informations sur DV25 et DV50, et sur SMPTE 370M.

## <a name="miscellaneous"></a>Divers

Deux sous-types DV supplémentaires sont définis dans le fichier d’en-tête UUID. h. Celles-ci correspondent aux Codes FOURCC produits par certains codecs DV. elles ne correspondent à aucune norme DV définie. Ces sous-types sont obsolètes et ne doivent pas être utilisés.



| FOURCC | GUID               |
|--------|--------------------|
| MENÉS par | MEDIASUBTYPE \_ menés par |
| 'DVSD' | MEDIASUBTYPE \_ DVSD |



 

## <a name="remarks"></a>Notes

Le tableau suivant indique les débits de données pris en charge, en mégabits par seconde (Mbits/s), pour les pilotes MSDV et UVC.



| Système d’exploitation                                                                 | Pilote MSDV (IEEE 1394) | Pilote UVC    |
|----------------------------------------------------------------------------------|-------------------------|---------------|
| Windows XP Service Pack 1 ou version antérieure                                             | 12,5, 25                | Non disponible |
| Windows XP Service Pack 2 ou version ultérieure, Windows Server 2003 Service Pack 1 ou version ultérieure. | 12,5, 25, 50, 100       | 12,5, 25      |



 

Pour les flux de 25 Mbits/s, le comportement du pilote MSDV a changé dans Windows Vista avant Windows Vista, le pilote MSDV a toujours défini le type de média sur MEDIASUBTYPE \_ DVSD pour les flux de 25 Mbits/s, que la source soit SDL-magnétoscope ou DVCPRO 25. Le type de média « DV25 » n’a pas été utilisé. À compter de Windows Vista, le pilote MSDV distingue maintenant ces deux formats. Pour SDL-magnétoscope, il continue d’utiliser le sous-type « DVSD ». Pour DVCPRO 25, elle utilise désormais le sous-type « DV25 ».

Les filtres de décodage [DV](dv-splitter-filter.md) DirectShow et [DV Video](dv-video-decoder-filter.md) ne prennent en charge que les formats de magnétoscope numérique SDL. Les données peuvent être PAL ou NTSC. Des filtres ou codecs tiers peuvent être disponibles pour analyser d’autres formats DV, à condition que le débit de données soit pris en charge par le pilote MSDV ou UVC.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vidéo numérique dans DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Pilote MSDV](msdv-driver.md)
</dt> <dt>

[Sous-types de vidéos](video-subtypes.md)
</dt> </dl>

 

 




