---
description: Vidéo FOURCCs
ms.assetid: bea4835d-fd7f-4ac3-8466-7f4e0d799a12
title: Vidéo FOURCCs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b804962308d0ecc5bf32fcddf5176905d0e17fbf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313613"
---
# <a name="video-fourccs"></a>Vidéo FOURCCs

De nombreux formats vidéo ont des Codes FOURCC qui leur sont affectés. Un code FOURCC est un entier non signé 32 bits créé par la concaténation de quatre caractères ASCII. Par exemple, le code FOURCC pour la vidéo YUY2 est « YUY2 ».

Différentes macros C/C++ sont définies pour déclarer des valeurs FOURCC dans le code source. La macro **MAKEFOURCC** est définie dans Mmsystem. h, et la macro **FCC** est définie dans Aviriff. h et dans divers autres fichiers d’en-tête. Vous pouvez également déclarer directement un code FOURCC en tant que littéral de chaîne en inversant l’ordre des caractères. Par conséquent, les instructions suivantes sont équivalentes :

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```

(dans le dernier exemple, l’inversion de l’ordre des octets est nécessaire, car Windows utilise une architecture little endian. 'Y' = 0x59, 'U' = 0x55, et' 2 ' = 0x32, donc' 2YUY’est 0x32595559.)

Certaines API [DirectX Video Acceleration 2,0](directx-video-acceleration-2-0.md) utilisent une valeur **D3DFORMAT** pour décrire un format vidéo. Un code FOURCC peut également être utilisé dans ce contexte :

``` syntax
D3DFORMAT fmt = (D3DFORMAT)MAKEFOURCC('Y','U','Y','2');
D3DFORMAT fmt = (D3DFORMAT)FCC('YUY2');
D3DFORMAT fmt = D3DFORMAT('2YUY'); // Coerce to D3DFORMAT type.
```

### <a name="fourcc-constants"></a>Constantes FOURCC

Le tableau suivant répertorie certains codes FOURCC courants.



| Valeur FOURCC | Description                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| H264 –       | Vidéo H. 264.                                                                                                          |
| 'I420'       | Vidéo YUV stockée au format 4:2:0 planaire.                                                                              |
| 'IYUV'       | Vidéo YUV stockée au format 4:2:0 planaire.                                                                              |
| 4S2 ' '       | Vidéo MPEG-4 part 2.                                                                                                  |
| FICHIERS MP4 À       | Codec Microsoft MPEG 4 version 3. Ce codec n’est plus pris en charge.                                                  |
| Mp4v       | Vidéo MPEG-4 part 2.                                                                                                  |
| 'MPG1'       | Vidéo MPEG-1.                                                                                                         |
| 'MSS1'       | contenu encodé avec le codec d’écran Windows Media Video 7.                                                          |
| 'MSS2'       | contenu encodé avec le codec d’écran Windows Media Video 9.                                                          |
| UYVY       | Vidéo YUV stockée au format 4:2:2 compressé. Semblable à YUY2 mais avec un classement des données différent.                         |
| 'WMV1'       | contenu encodé avec le codec Windows Media Video 7.                                                                 |
| 'WMV2'       | contenu encodé avec le codec Windows Media Video 8.                                                                 |
| 'WMV3'       | contenu encodé avec le codec Windows Media Video 9.                                                                 |
| 'WMVA'       | contenu encodé avec la version obsolète la plus ancienne du codec de profil avancé Windows Media Video 9.                 |
| 'WMVP'       | contenu encodé avec le codec d’Image Windows Media Video 9,1.                                                         |
| 'WVC1'       | SMPTE 421M (« VC-1 »). contenu encodé avec le profil avancé Windows Media Video 9.                                     |
| 'WVP2'       | contenu encodé avec le codec Windows Media Video 9,1 Image v2.                                                      |
| YUY2       | Vidéo YUV stockée au format 4:2:2 compressé.                                                                              |
| 'YV12'       | Vidéo YUV stockée au format 4:2:0 ou 4:1:1 planaire. Identique à I420/IYUV, sauf que les plans vous et V sont basculés. |
| YVU9       | Vidéo YUV stockée au format 16:1:1 planaire.                                                                             |
| YVYU       | Vidéo YUV stockée au format 4:2:2 compressé. Semblable à YUY2 mais avec un classement des données différent.                         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de média vidéo](video-media-types.md)
</dt> <dt>

[GUID de sous-type de vidéo](video-subtype-guids.md)
</dt> </dl>

 

 



