---
description: Les GUID suivants prennent en charge les API vidéo Direct3D 12.
ms.assetid: CF2F3058-328A-4128-B5C6-29723B49AB1E
title: GUID vidéo Direct3D 12 (D3d11. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05f7a56227ccc2953504d8466a34d6b2160ce1e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525789"
---
# <a name="direct3d-12-video-guids"></a>GUID vidéo Direct3D 12

Les GUID suivants prennent en charge les API vidéo Direct3D 12.

## <a name="d3d12_video_decode_profile-guids"></a>D3D12 \\ _VIDEO \\ _DECODE \\ _PROFILE GUID

Le tableau suivant répertorie les GUID qui identifient les profils de décodage vidéo Direct3D 12. Les descriptions associent chaque profil de décodage vidéo Direct3D 12 au profil vidéo ou DXVA Direct3D 11 équivalent.

| Nom                                                 | Valeur                                                                                | Description
|------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| \_ \_ Profil de décodage vidéo D3D12 \_ \_ MPEG1 \_ et \_ MPEG2           | 0x86695f12, 0x340e, 0x4f04, 0x9F, 0xD3, 0x92, 0x53, 0xDD, 0x32, 0x74, 0x60 | Équivalent à DXVA2 \_ ModeMPEG2and1 \_ VLD.                 |
| D3D12 \_ de \_ profil de décodage vidéo \_ \_ MPEG2                     | 0xee27417f, 0x5e28, 0x4e65, 0xBE, 0xEA, 0x1d, égale 0x26, 0xb5, 0x08, 0xad, 0xC9           | Équivalent au \_ profil de DÉcodeur d3d11 \_ \_ MPEG2 \_ VLD et DXVA2 \_ ModeMPEG2 \_ VLD.                 |
| \_Profil de \_ décodage vidéo D3D12 \_ \_ H264 –                      | 0x1b81be68, 0xa0c7, 0x11d3, 0xb9, 0x84, 0x00, 0xC0, 0x4F, 0x2E, 0x73, 0xC5       | Équivalent au \_ profil de DÉcodeur d3d11 \_ \_ H264 – \_ VLD \_ NOFGT et \_ DXVA \_ ModeH264 \_ VLD NOFGT. |
| D3D12 \_ Video \_ Decode \_ Profile \_ H264 – \_ Stereo \_ progressif   | 0xd79be8da, 0x0cf1, 0x4c81, 0xB8, 0x2A, 0x69, 0xa4, 0xe2, 0x36, 0xf4, 0x3D          | Équivaut au \_ profil de DÉcodeur d3d11 \_ \_ H264 – \_ VLD \_ \_ de progressif stéréo \_ NOFGT et \_ \_ \_ \_ \_ à la ModeH264 de la stéréo VLD. |
| \_Profil de \_ décodage vidéo D3D12 \_ \_ H264 – \_ stéréo               | 0xf9aaccbb, 0xc2b6, 0x4cfc, 0x87, 0x79, 0x57, 0x07, 0xb1, 0x76, 0x05, 0x52          | Équivalent au \_ profil de DÉcodeur d3d11 \_ \_ H264 – \_ VLD \_ Stereo \_ NOFGT et DXVA \_ ModeH264 \_ VLD \_ stéréo \_ NOFGT |
| D3D12 \_ vidéo \_ décoder le \_ profil \_ H264 – \_ multivue            | 0x705b9d82, 0x76cf, 0x49d6, 0xB7, 0xe6, 0xac, 0x88, 0x72, 0xDB, 0x01, 0x3C          | Équivalent au \_ profil de DÉcodeur d3d11 \_ \_ H264 – \_ VLD \_ MultiView \_ NOFGT et DXVA \_ ModeH264 \_ VLD \_ MultiView \_ NOFGT. |
| \_Profil de \_ décodage vidéo D3D12 \_ \_ VC1                       | 0x1b81beA3, 0xa0c7, 0x11d3, 0xb9, 0x84, 0x00, 0xC0, 0x4F, 0x2E, 0x73, 0xC5          | Équivalent au \_ profil de DÉcodeur d3d11 \_ \_ VC1 \_ VLD et DXVA \_ ModeVC1 \_ VLD. |
| \_Profil de \_ décodage vidéo D3D12 \_ \_ VC1 \_ D2010                 | 0x1b81beA4, 0xa0c7, 0x11d3, 0xb9, 0x84, 0x00, 0xC0, 0x4F, 0x2E, 0x73, 0xC5          | Équivalent au \_ profil de DÉcodeur d3d11 \_ \_ VC1 \_ D2010 et DXVA \_ ModeVC1 \_ D2010. |
| \_Profil de \_ décodage vidéo D3D12 \_ \_ MPEG4PT2 \_ simple           | 0xefd64d74, 0xc9e8, 0x41d7, 0xa5, 0xE9, 0xE9, 0xb0, 0xe3, 0x9F, 0xa3, 0x19          | Équivalent au \_ profil de DÉcodeur d3d11 \_ \_ MPEG4PT2 \_ VLD \_ simple et DXVA \_ ModeMPEG4pt2 \_ VLD \_ simple. |
| \_Profil de \_ décodage vidéo D3D12 \_ \_ MPEG4PT2 \_ ADVSIMPLE \_ NOGMC  | 0xed418a9f, 0x010d, 0x4eda, 0x9a, 0xe3, 0x9a, 0x65, 0x35, 0x8d, 0x8d, 0x2E          | Équivaut au \_ profil de DÉcodeur d3d11 \_ \_ MPEG4PT2 \_ VLD \_ ADVSIMPLE \_ NOGMC et \_ DXVA \_ ModeMPEG4pt2 \_ \_ VLD ADVSIMPLE NOGMC. |
| \_Profil de \_ décodage vidéo D3D12 \_ \_ HEVC \_ main                 | 0x5b11d51b, 0x2f4c, 0x4452, 0xBC, 0xc3, 0x09, 0xf2, 0xa1, 0x16, 0x0C, 0xC0          | Équivalent au \_ profil de DÉcodeur d3d11 \_ \_ HEVC \_ VLD \_ main et DXVA \_ ModeHEVC \_ VLD \_ main
| \_Profil de \_ décodage vidéo D3D12 \_ \_ HEVC \_ MAIN10               | 0x107af0e0, 0xef1a, 0x4d19, 0xAB, 0xA8, 0x67, 0xa1, 0x63, 0x07, 0x3D, 0x13          | Équivalent au \_ profil de DÉcodeur d3d11 \_ \_ HEVC \_ VLD \_ MAIN10 et \_ DXVA \_ ModeHEVC \_ VLD MAIN10.
| \_Profil de \_ décodage vidéo D3D12 \_ \_ VP9                       | 0x463707f8, 0xa1d0, 0x4585, 0x87, 0x6d, 0x83, 0xAA, 0x6d, 0x60, 0xB8, 0x9e | |
| D3D12 \_ Video \_ Decode \_ Profile \_ VP9 \_ 10 \_ profichier2        | 0xa4c749ef, 0x6ecf, 0x48aa, 0x84, 0x48, 0x50, 0xa7, 0xa1, 0x16, 0x5F, 0xf7           | |
| \_Profil de \_ décodage vidéo D3D12 \_ \_ VP8                       | 0x90b899ea, 0x3a62, 0x4705, 0x88, 0xb3, 0x8d, 0xF0, 0x4B, 0x27, 0x44, 0xE7 | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_PROFILE0                       | 0xb8be4ccb, 0xcf53, 0x46ba, 0x8d, 0x59, 0xd6, 0xB8, 0xA6, 0xDA, 0x5d, 0x2A | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_PROFILE1                       | 0x6936ff0f, 0x45b1, 0x4163, 0x9C, 0xC1, 0x64, 0x6e, 0XF6, 0x94, 0x61, 0x08 | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_PROFILE2                       | 0x0c5f2aa1, 0xe541, 0x4089, 0xBB, 0x7B, 0x98, 0x11, 0x0A, 0x19, 0xd7, 0xC8 | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_12BIT_PROFILE2                 | 0x17127009, 0xa00f, 0x4ce1, 0x99, 0x4E, 0xbf, 0x40, 0x81, 0XF6, 0xf3, 0xF0 | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_12BIT_PROFILE2_420             | 0x2d80bed6, 0x9cac, 0x4835, 0x9e, 0x91, 0x32, 0x7B, 0xBC, 0x4F, 0x9e, 0xe8 | |

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>D3d11. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[API vidéo Direct3D 11](direct3d-11-video-apis.md)
</dt> </dl>

 

 




