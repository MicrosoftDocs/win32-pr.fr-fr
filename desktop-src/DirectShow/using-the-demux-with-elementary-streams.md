---
description: Utilisation de demux avec des flux élémentaires
ms.assetid: dd98aada-8309-428e-9609-2542195bc6ec
title: Utilisation de demux avec des flux élémentaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6b9004d6c99db96405797016b0d9854c96dae92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319534"
---
# <a name="using-the-demux-with-elementary-streams"></a>Utilisation de demux avec des flux élémentaires

Lorsque le demux MPEG-2 fournit des charges utiles PES, il envoie le flux ES octets dans des lots d’exemples de supports. La taille par défaut de l’échantillon est de 8 Ko. Le demux démarre un nouvel exemple de support sur chaque limite PES, mais peut décomposer une seule charge PES en plusieurs échantillons. Par exemple, si une charge utile PES est de 20 000, elle sera fournie dans deux échantillons de 8 Ko, suivis d’un échantillon de 4 Ko. Demux n’examine pas le contenu du flux d’octets. Il revient au décodeur d’analyser les en-têtes de séquence et de rechercher les modifications de format.

Lorsque la broche de sortie du filtre demux se connecte au décodeur, elle offre le type de média qui a été spécifié lors de la création du code confidentiel. Étant donné que demux n’examine pas le flux de bits ES, il ne valide pas le type de média. En théorie, un décodeur MPEG-2 doit être en mesure de se connecter avec uniquement le type et le sous-type majeurs remplis, pour indiquer le type de données. Le décodeur doit ensuite examiner les en-têtes de séquence qui arrivent dans les exemples de supports. Toutefois, dans la pratique, de nombreux décodeurs ne se connectent pas à moins que le type de média inclue un bloc de format complet.

Par exemple, supposons que PID 0x31 contient la vidéo sur le profil principal MPEG-2. Au minimum, vous devez effectuer les étapes suivantes.

Tout d’abord, créez un type de média pour la vidéo MPEG-2. Laisser le bloc de format pour le moment :


```C++
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = MEDIATYPE_Video ;
mt.subtype = MEDIASUBTYPE_MPEG2_VIDEO;
// Possibly create a format block (not shown here).
```



Ensuite, créez une broche de sortie sur le demux :


```C++
// Query the demux filter for IMpeg2Demultiplexer.
IMpeg2Demultiplexer *pDemux;
hr = pFilter->QueryInterface(IID_IMpeg2Demultiplexer, (void**)&pDemux);
if (SUCCEEDED(hr))
{
    // Create a new output pin.
    IPin *pPin0;
    hr = pDemux->CreateOutputPin(&mt, L"Video Pin", &pPin0);
    if (SUCCEEDED(hr))
    {
        ....
    }
}
```



Interrogez ensuite le nouveau code PIN de l’interface **IMPEG2PIDMap** et appelez **MapPID**. Spécifiez PID Number 0x30 et MEDIA \_ élémentaire \_ Stream pour les charges utiles PES.


```C++
// Query the pin for IMPEG2PIDMap. This implicitly configures the
// demux to carry a transport stream. 
IMPEG2PIDMap *pPidMap;
hr = pPin0->QueryInterface(IID_IMPEG2PIDMap, (void**)&pPidMap);
if (SUCCEEDED(hr))
{
    // Assign PID 0x31 to pin 0. Set the type to "PES payload."
    ULONG Pid = 0x031;
    hr = pPidMap->MapPID(1, &Pid, MEDIA_ELEMENTARY_STREAM);
    pPidMap->Release();
}
```



Enfin, libérez toutes les interfaces quand vous avez terminé :


```C++
pPin0->Release();
pDemux->Release();
```



Voici un exemple plus complet de définition du type de média, y compris le bloc de format. Cet exemple suppose toujours une vidéo de profil principal MPEG-2. Les détails varient en fonction du contenu du flux :


```C++
// Set up a byte array to hold the first sequence header. 
// This may or may not be required, depending on the decoder.
BYTE SeqHdr[] = { ... };  // Contains the sequence header (not shown).

AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = MEDIATYPE_Video ;
mt.subtype = MEDIASUBTYPE_MPEG2_VIDEO;
mt.formattype = FORMAT_MPEG2Video;

// Allocate the format block, including space for the sequence header. 
mt.cbFormat = sizeof(MPEG2VIDEOINFO) + sizeof(SeqHdr);
mt.pbFormat = (BYTE*)CoTaskMemAlloc(mt.cbFormat);
if (mt.pbFormat == NULL)
{
    // Out of memory; return an error code.
}
ZeroMemory(mt.pbFormat, mt.cbFormat);

// Cast the buffer pointer to an MPEG2VIDEOINFO struct.
MPEG2VIDEOINFO *pMVIH = (MPEG2VIDEOINFO*)mt.pbFormat;

RECT rcSrc = {0, 480, 0, 720};        // Source rectangle.
pMVIH->hdr.rcSource = rcSrc;
pMVIH->hdr.dwBitRate = 4000000;       // Bit rate.
pMVIH->hdr.AvgTimePerFrame = 333667;  // 29.97 fps.
pMVIH->hdr.dwPictAspectRatioX = 4;    // 4:3 aspect ratio.
pMVIH->hdr.dwPictAspectRatioY = 3;

// BITMAPINFOHEADER information.
pMVIH->hdr.bmiHeader.biSize = 40;
pMVIH->hdr.bmiHeader.biWidth = 720;
pMVIH->hdr.bmiHeader.biHeight = 480;

pMVIH->dwLevel = AM_MPEG2Profile_Main;  // MPEG-2 profile. 
pMVIH->dwProfile = AM_MPEG2Level_Main;  // MPEG-2 level.

// Copy the sequence header into the format block.
pMVIH->cbSequenceHeader = sizeof(SeqHdr); // Size of sequence header.
memcpy(pMVIH->dwSequenceHeader, SeqHdr, sizeof(SeqHdr));
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du démultiplexeur MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



