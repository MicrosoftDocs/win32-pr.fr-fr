---
description: Les GUID de sous-type de vidéo suivants sont définis dans le fichier d’en-tête mfapi. h. Pour spécifier le sous-type, définissez l' \_ attribut de sous-type MF MT \_ sur le type de média.
ms.assetid: 7dfd85e6-936e-4b78-a2cb-a5d59153e1c4
title: GUID de sous-type de vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38829480aed7372496fc196cc6c55d781b672a2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235788"
---
# <a name="video-subtype-guids"></a>GUID de sous-type de vidéo

Les GUID de sous-type de vidéo suivants sont définis dans le fichier d’en-tête mfapi. h. Pour spécifier le sous-type, définissez l’attribut de sous- [**\_ \_ type MF MT**](mf-mt-subtype-attribute.md) sur le type de média.

Quand ces sous-types sont utilisés, affectez à l’attribut de [ \_ \_ \_ type principal MF MT](mf-mt-major-type-attribute.md) la valeur **MFMediaType \_ Video**.

-   [Formats RVB non compressés](#uncompressed-rgb-formats)
-   [Formats YUV : 8 bits et en palette](#yuv-formats-8-bit-and-palettized)
-   [Formats YUV : 10 bits et 16 bits](#yuv-formats-10-bit-and-16-bit)
-   [Formats de luminance et de profondeur](#luminance-and-depth-formats)
-   [Types de vidéo encodés](#encoded-video-types)
-   [Création de GUID de sous-type à partir de valeurs FOURCCs et D3DFORMAT](#creating-subtype-guids-from-fourccs-and-d3dformat-values)
-   [Rubriques connexes](#related-topics)

## <a name="uncompressed-rgb-formats"></a>Formats RVB non compressés



| GUID                             | Description                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------|
| **MFVideoFormat \_ RGB8**          | RVB, 8 bits par pixel (BPP). (Même disposition en mémoire que **D3DFMT \_ P8**.)                            |
| **MFVideoFormat \_ RGB555**        | RGB 555, 16 bpp. (Même disposition en mémoire que **D3DFMT \_ X1R5G5B5**.)                                  |
| **MFVideoFormat \_ RGB565**        | RGB 565, 16 bpp. (Même disposition en mémoire que **D3DFMT \_ R5G6B5**.)                                    |
| **MFVideoFormat \_ Rgb24**         | RVB, 24 BPP.                                                                                    |
| **MFVideoFormat \_ RGB32**         | RGB, 32 BPP.                                                                                    |
| **MFVideoFormat \_ ARGB32**        | RGB, 32 BPP avec canal alpha.                                                                 |
| **MFVideoFormat \_ A2R10G10B10**   | RVB, 10 BPP pour chaque couleur et 2 BPP pour alpha. (Même disposition en mémoire que **D3DFMT \_ A2B10G10R10**) |
| **MFVideoFormat \_ A16B16G16R16F** | RVB, 16 bpp avec canal alpha. (Même disposition en mémoire que **D3DFMT \_ A16B16G16R16F**)               |



 

> [!Note]  
> Ces sous-types ne correspondent pas aux GUID de sous-type RGB utilisés dans les kits de développement logiciel (SDK) précédents, tels que les DirectShow.

 

## <a name="yuv-formats-8-bit-and-palettized"></a>Formats YUV : 8 bits et en palette



| GUID                    | Format | échantillonnage | Condensé ou planaire | Bits par canal |
|-------------------------|--------|----------|------------------|------------------|
| **MFVideoFormat \_ AI44** | AI44   | 4:4:4    | Riche           | En palette       |
| **MFVideoFormat \_ AYUV** | AYUV   | 4:4:4    | Riche           | 8                |
| **MFVideoFormat \_ I420** | I420   | 4:2:0    | Planaire           | 8                |
| **MFVideoFormat \_ IYUV** | IYUV   | 4:2:0    | Planaire           | 8                |
| **MFVideoFormat \_ NV11** | NV11   | 4:1:1    | Planaire           | 8                |
| **MFVideoFormat \_ NV12** | NV12   | 4:2:0    | Planaire           | 8                |
| **MFVideoFormat \_ UYVY** | UYVY   | 4:2:2    | Riche           | 8                |
| **MFVideoFormat \_ Y41P** | Y41P   | 4:1:1    | Riche           | 8                |
| **MFVideoFormat \_ Y41T** | Y41T   | 4:1:1    | Riche           | 8                |
| **MFVideoFormat \_ Y42T** | Y42T   | 4:2:2    | Riche           | 8                |
| **MFVideoFormat \_ YUY2** | YUY2   | 4:2:2    | Riche           | 8                |
| **MFVideoFormat \_ YVU9** | YVU9   | 8:4:4    | Planaire           | 9                |
| **MFVideoFormat \_ YV12** | YV12   | 4:2:0    | Planaire           | 8                |
| **MFVideoFormat \_ YVYU** | YVYU   | 4:2:2    | Riche           | 8                |



 

Les formats YUV recommandés sont décrits en détail dans la rubrique [formats YUV 8 bits recommandés pour le rendu vidéo](recommended-8-bit-yuv-formats-for-video-rendering.md).

> [!Note]  
> I420 et IYUV ont la même disposition en mémoire, mais reçoivent des GUID de sous-type distincts. Les GUID de sous-type correspondent aux Codes FOURCC « I420 » et « IYUV »; Pour plus d’informations, consultez [Video FOURCCs](video-fourccs.md) .

 

## <a name="yuv-formats-10-bit-and-16-bit"></a>Formats YUV : 10 bits et 16 bits



| GUID                    | Format | échantillonnage | Condensé ou planaire | Bits par canal |
|-------------------------|--------|----------|------------------|------------------|
| **MFVideoFormat \_ P010** | P010   | 4:2:0    | Planaire           | 10               |
| **MFVideoFormat \_ P016** | P016   | 4:2:0    | Planaire           | 16               |
| **MFVideoFormat \_ P210** | P210   | 4:2:2    | Planaire           | 10               |
| **MFVideoFormat \_ P216** | P216   | 4:2:2    | Planaire           | 16               |
| **MFVideoFormat \_ V210** | v210   | 4:2:2    | Riche           | 10               |
| **MFVideoFormat \_ v216** | v216   | 4:2:2    | Riche           | 16               |
| **MFVideoFormat \_ V410** | v40    | 4:4:4    | Riche           | 10               |
| **MFVideoFormat \_ Y210** | Y210   | 4:2:2    | Riche           | 10               |
| **MFVideoFormat \_ Y216** | Y216   | 4:2:2    | Riche           | 16               |
| **MFVideoFormat \_ Y410** | Y40    | 4:4:4    | Riche           | 10               |
| **MFVideoFormat \_ Y416** | Y416   | 4:4:4    | Riche           | 16               |



 

Pour plus d’informations sur ces formats, consultez [formats vidéo YUV 10 bits et 16 bits](10-bit-and-16-bit-yuv-video-formats.md).

## <a name="luminance-and-depth-formats"></a>Formats de luminance et de profondeur



| GUID                   | Description                                                          |
|------------------------|----------------------------------------------------------------------|
| **MFVideoFormat \_ N8**  | luminance 8 bits uniquement. (BPP). (Même disposition en mémoire que **D3DFMT \_ N8**.) |
| **MFVideoFormat \_ L16** | luminance de 16 bits uniquement. (Même disposition en mémoire que **D3DFMT \_ L16**.)      |
| **MFVideoFormat \_ D16** | profondeur de la mémoire tampon z 16 bits. (Même disposition en mémoire que **D3DFMT \_ D16**.)      |



 

## <a name="encoded-video-types"></a>Types de vidéo encodés



| GUID                        | FOURCC         | Description                                                                                                                                                                                                                                                                                                 |
|-----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFVideoFormat \_ DV25**     | 'dv25'         | DVCPRO 25 (525-60 ou 625-50).                                                                                                                                                                                                                                                                               |
| **MFVideoFormat \_ DV50**     | 'dv50'         | DVCPRO 50 (525-60 ou 625-50).                                                                                                                                                                                                                                                                               |
| **\_DVC MFVideoFormat**      | DVC         | Vidéo DVC/DV.                                                                                                                                                                                                                                                                                               |
| **MFVideoFormat \_ DVH1**     | 'dvh1'         | DVCPRO 100 (1080/60i, 1080/50i, ou 720/60P).                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ DVHD**     | 'dvhd'         | HD-magnétoscope numérique (1125-60 ou 1250-50).                                                                                                                                                                                                                                                                               |
| **MFVideoFormat \_ DVSD**     | 'dvsd'         | SDL-magnétoscope numérique (525-60 ou 625-50).                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ DVSL**     | 'dvsl'         | SD-magnétoscope numérique (525-60 ou 625-50).                                                                                                                                                                                                                                                                                 |
| **MFVideoFormat \_ H263**     | 'H263'         | Vidéo H. 263.                                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ H264 –**     | H264 –         | Vidéo H. 264.<br/> Les exemples de supports contiennent des données de flux binaire H. 264 avec des codes de démarrage et des SPS/PPS entrelacés. Chaque échantillon contient une image complète, qu’il s’agisse d’un champ ou d’un cadre.<br/>                                                                                                       |
| **MFVideoFormat \_ H265**     | 'H265'         | Vidéo H. 265.                                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ H264 – \_ es** | Non applicable | Flux élémentaire H. 264.<br/> Ce type de média est identique à **MFVideoFormat \_ H264 –**, sauf que les exemples de média contiennent un flux binaire H. 264 fragmenté. Chaque exemple peut contenir une image partielle. plusieurs images complètes ; ou une ou plusieurs images complètes plus une image partielle.<br/>           |
| **MFVideoFormat \_ HEVC**     | HEVC         | Le profil principal HEVC et le profil d’image reste principal.<br/> Chaque exemple contient une image complète.<br/> pris en charge dans Windows 8.1 et versions ultérieures. Le profil principal HEVC et le profil principal de profil d’image continue. <br/>                                                              |
| **MFVideoFormat \_ HEVC \_ es** | 'HEVS'         | Ce type de média est le même que **MFVideoFormat \_ HEVC**, sauf que les exemples de supports contiennent un flux binaire HEVC fragmenté. Chaque exemple peut contenir une image partielle. plusieurs images complètes ; ou une ou plusieurs images complètes plus une image partielle.<br/> pris en charge dans Windows 8.1 et versions ultérieures.<br/> |
| **MFVideoFormat \_ M4S2**     | 4S2 ' '         | Vidéo MPEG-4 part 2.                                                                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ MJPG**     | 'MJPG'         | Motion JPEG.                                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ mp43**     | 'MP43'         | Codec Microsoft MPEG 4 version 3. Ce codec n’est plus pris en charge.                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ fichiers MP4 à**     | FICHIERS MP4 À         | Codec ISO MPEG 4 version 1.                                                                                                                                                                                                                                                                                 |
| **MFVideoFormat \_ mp4v**     | Mp4v         | Vidéo MPEG-4 part 2.                                                                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ MPEG2**    | Non applicable | Vidéo MPEG-2. (Équivalent à **la \_ \_ vidéo MEDIASUBTYPE MPEG2** dans DirectShow.)                                                                                                                                                                                                                                 |
| **MFVideoFormat \_ VP80**     | 'MPG1'         | Vidéo VP8.                                                                                                                                                                                                                                                                                                  |
| **MFVideoFormat \_ VP90**     | 'MPG1'         | Vidéo VP9.                                                                                                                                                                                                                                                                                                  |
| **MFVideoFormat \_ MPG1**     | 'MPG1'         | Vidéo MPEG-1.                                                                                                                                                                                                                                                                                               |
| **MFVideoFormat \_ MSS1**     | 'MSS1'         | Windows Codec d’écran de média version 1.                                                                                                                                                                                                                                                                       |
| **MFVideoFormat \_ MSS2**     | 'MSS2'         | Windows Codec d’écran vidéo multimédia 9.                                                                                                                                                                                                                                                                         |
| **MFVideoFormat \_ WMV1**     | 'WMV1'         | Windows Codec vidéo multimédia version 7.                                                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ WMV2**     | 'WMV2'         | Windows Codec Media Video 8.                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ WMV3**     | 'WMV3'         | Windows Codec Media Video 9.                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ WVC1**     | 'WVC1'         | SMPTE 421M (« VC-1 »).                                                                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ 420O**     | '420O'         | vidéo 4:2:0 de 8 bits par canal.                                                                                                                                                                                                                                                                   |
| **MFVideoFormat \_ AV1**     | 'AV01'         | Vidéo AV1.                                                                                                                                                                                                                                                                                                |



 

## <a name="creating-subtype-guids-from-fourccs-and-d3dformat-values"></a>Création de GUID de sous-type à partir de valeurs FOURCCs et D3DFORMAT

Les formats vidéo sont souvent représentés par les valeurs FOURCCs ou **D3DFORMAT** . Une plage de GUID est réservée à la représentation de ces valeurs en tant que sous-types. Ces GUID se présentent sous la forme `XXXXXXXX-0000-0010-8000-00AA00389B71` , où `XXXXXXXX` est le code FourCC de 4 octets ou la valeur **D3DFORMAT** .

Si un format vidéo est associé à une valeur FOURCC ou **D3DFORMAT** , vous pouvez créer le GUID du sous-type correspondant comme suit : démarrez avec la **\_ base constante MFVideoFormat** et remplacez le premier **DWORD** du GUID par la valeur de la vidéo FourCC ou **D3DFORMAT** . Vous pouvez utiliser la macro [**définir le \_ \_ GUID du MediaType**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) à cet effet.

> [!Note]  
> DirectShow utilise également ce système pour la plupart des sous-types vidéo, mais pas pour les formats rvb non compressés. par conséquent, les sous-types rgb dans DirectShow ne correspondent pas aux sous-types rgb dans Media Foundation.

 

L’énumération **D3DFORMAT** est définie dans le fichier d’en-tête d3d9types. h. Le tableau suivant répertorie les formats RVB non compressés les plus courants et la valeur **D3DFORMAT** correspondante.



| Format RVB                                                              | Valeur **D3DFORMAT**     |
|-------------------------------------------------------------------------|-------------------------|
| RGB 32 bits                                                              | **D3DFMT \_ X8R8G8B8**    |
| RGB 32 bits avec canal alpha                                           | **D3DFMT \_ A8R8G8B8**    |
| RGB 24 bits                                                              | **D3DFMT \_ R8G8B8**      |
| RGB 555 (RVB 16 bits)                                                    | **D3DFMT \_ X1R5G5B5**    |
| RGB 555 avec canal alpha                                              | **D3DFMT \_ A4R4G4B4**    |
| RGB 565 (RVB 16 bits)                                                    | **D3DFMT \_ R5G6B5**      |
| en palette RGB 8 bits                                                    | **D3DFMT \_ P8**          |
| A2 R10 G10 B10 (32 bits RGB avec canal alpha ; 10 bits par canal RVB) | **D3DFMT \_ A2R10G10B10** |
| A2 B10 G10 R10 (32 bits RGB avec canal alpha ; 10 bits par canal RVB) | **D3DFMT \_ A2B10G10R10** |
| luminance 8 bits uniquement.                                                   | **D3DFMT \_ N8**          |
| luminance de 16 bits uniquement.                                                  | **D3DFMT \_ L16**         |
| profondeur de mémoire tampon z 16 bits                                                   | **D3DFMT \_ D16**         |



 

Pour plus d’informations sur FOURCCs, consultez [vidéo FOURCCs](video-fourccs.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[GUID de type de média](media-type-guids.md)
</dt> <dt>

[**\_sous- \_ type MF MT**](mf-mt-subtype-attribute.md)
</dt> <dt>

[Types de médias](media-types.md)
</dt> <dt>

[Types de média vidéo](video-media-types.md)
</dt> </dl>

 

 




