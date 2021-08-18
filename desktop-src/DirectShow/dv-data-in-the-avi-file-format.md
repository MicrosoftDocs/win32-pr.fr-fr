---
description: Données DV au format de fichier AVI
ms.assetid: ae1ec184-afc3-4ec1-9b92-f53656293446
title: Données DV au format de fichier AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c048cb42fa3ba49457c115944075c064b9cfd4c31263519e9d5af3e5f0a268a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749109"
---
# <a name="dv-data-in-the-avi-file-format"></a>Données DV au format de fichier AVI

Microsoft a spécifié le format de stockage des données vidéo numériques (DV) dans les fichiers AVI. la conformité à cette spécification permet de s’assurer que les fichiers AVI créés dans ce format seront compatibles avec les futures versions de l’DirectShow architecture vidéo numérique pour Windowsplatform.

Cet article décrit le format des fichiers AVI contenant des données DV. Des FOURCCs spécifiques (codes à quatre caractères) pour les flux de données DV entrelacés et les gestionnaires de flux de décompresseur/décompresseur DV sont définis. La structure du format de flux de données DV est définie. Les spécifications de deux méthodes de stockage des données DV au format de fichier AVI sont spécifiées.

Il est supposé que le lecteur est familiarisé avec le format de données DV. (Ce format est défini dans la *spécification des magnétoscopes numériques à usage particulier*, également appelé Livre bleu.)

Il existe deux types de fichiers AVI DV : les fichiers AVI qui contiennent un flux de données DV, appelé fichiers *de type-1* ; et les fichiers AVI qui contiennent des vidéos DV en tant que flux « vids » et des fichiers audio DV en tant que flux « Auds », appelés fichiers *de type 2* .

**Fichiers AVI contenant un flux de données DV (type-1)**

Les données DV entrelacées peuvent être stockées dans leur format natif sous la forme d’un flux unique dans un fichier. AVI RIFF. Cela présente l’avantage d’utiliser le volume minimum de stockage de données pour le format DV. l’inconvénient principal est que ce format de fichier n’est pas à compatibilité descendante avec la vidéo pour Windows, car il ne contient pas de vidéo « vids » ou de flux audio « auds ». Le support est fourni pour le flux DV entrelacé par le biais des filtres de [séparateur](dv-splitter-filter.md) DV [du multiplexeur](dv-muxer-filter.md) et DV fournis avec DirectShow.

Les données DV peuvent être stockées dans un seul flux au sein d’un fichier. AVI, en spécifiant le « IAVs » (flux audio et vidéo entrelacé) FOURCC (code à quatre caractères) dans le membre **fccType** et l’un ou l’autre des dvsl « DVSD », « dvhd » ou « FOURCCs » dans le membre **fccHandler** du bloc d’en-tête de flux « Strh ». Les images par seconde du flux vidéo doivent être spécifiées dans les membres **dwRate** et **dwScale** et le nombre total de blocs vidéo dans le segment « movi » du membre **dwLength** .

Le gestionnaire de flux « DVSD » FOURCC spécifie que les données DV sont définies dans la partie 2 de la *spécification des magnétoscopes numériques à usage particulier*. La vidéo est au format 525 lignes à 29,97 Hz (525-60) ou 625 lignes à 25,00 Hz (625-50).

Le gestionnaire de flux « dvhd » FOURCC spécifie que les données DV sont définies dans la partie 3 de la *spécification des magnétoscopes numériques à usage particulier*. La vidéo est au format 1125 lignes à 30,00 Hz (1125-60) ou 1250 lignes à 25,00 Hz (1250-50).

Le gestionnaire de flux « dvsl » FOURCC spécifie que les données DV sont définies dans la partie 6 de la *spécification des magnétoscopes numériques à usage particulier*. La vidéo est au format de haute compression SD (SDL).

> [!Note]  
> Le reste de cet article fournit des définitions pour les flux « DVSD ».

 

Le bloc d’en-tête de flux doit être suivi d’un bloc de format de flux [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) .

Les données DV réelles sont stockées en tant que \# \# segments « DC » dans le bloc « movi » (le \# \# format représente l’identificateur de flux). Chaque segment contient une trame de données, soit 10 ou 12 séquences DV DIF pour les systèmes 525-60 ou 625-50, respectivement. Le format de séquence DIF DV SD (« DVSD ») est défini dans la partie 2 de la *spécification des magnétoscopes numériques à usage particulier*.

L’exemple suivant illustre la forme de formulaire RIFF AIFF pour un fichier AVI avec un flux de données DV, développée avec des blocs d’en-tête terminés.


```C++
00000000 RIFF (0FAE35D4) 'AVI '
0000000C     LIST (00000106) 'hdrl'
00000018         avih (00000038)
                     dwMicroSecPerFrame    : 33367
                     dwMaxBytesPerSec      : 3728000
                     dwPaddingGranularity  : 0
                     dwFlags               : 0x810 HASINDEX | TRUSTCKTYPE
                     dwTotalFrames         : 2192
                     dwInitialFrames       : 0
                     dwStreams             : 1
                     dwSuggestedBufferSize : 120000
                     dwWidth               : 720
                     dwHeight              : 480
                     dwReserved            : 0x0
00000058         LIST (0000006C) 'strl'
00000064             strh (00000038)
                         fccType               : 'iavs'
                         fccHandler            : 'dvsd'
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 100 (29.970 Frames/Sec)
                         dwRate                : 2997
                         dwStart               : 0
                         dwLength              : 2192
                         dwSuggestedBufferSize : 120000
                         dwQuality             : 0
                         dwSampleSize          : 0
                         rcFrame               : 0,0,720,480
000000A4             strf (00000020)
                         dwDVAAuxSrc     : 0x........
                         dwDVAAuxCtl     : 0x........
                         dwDVAAuxSrc1    : 0x........
                         dwDVAAuxCtl1    : 0x........
                         dwDVVAuxSrc     : 0x........
                         dwDVVAuxCtl     : 0x........
                         dwDVReserved[2] : 0,0
000000CC     LIST (0FADAC00) 'movi'
0FADACD4     idx1 (00008900)
```



**fichiers AVI contenant des Flux dv Video et dv Audio (Type-2)**

Les données DV entrelacées peuvent être fractionnées en un flux vidéo et un à quatre flux audio au sein d’un fichier. AVI RIFF. cela présente l’avantage de bénéficier d’une compatibilité descendante avec la vidéo pour Windows, car elle contient un flux « vids » vidéo standard et au moins un flux audio standard « auds ». l’inconvénient principal est que ce format de fichier nécessite que les données audio soient stockées de façon redondante sous forme de flux audio. Le flux « vidéo » est en fait le flux de données DV entrelacées natives. Toutefois, en tant que flux « vids » standard avec un type de gestionnaire « DVSD », le [décodeur vidéo DV](dv-video-decoder-filter.md) est utilisé. Ce format requiert également l’utilisation du filtre de [séparateur DV](dv-splitter-filter.md) pour fractionner les fichiers « capturés » avant de les écrire en tant que fichiers AVI.

Les données DV peuvent être stockées sous la forme d’un flux vidéo avec un nombre distinct de flux audio dans un fichier RIFF AVI. Le flux vidéo est spécifié avec un en-tête de flux vidéo standard (la valeur du membre **fccType** est’vids'). Le membre **fccHandler** est spécifié en tant que « DVSD », « dvhd » ou « dvsl ». Les images par seconde du flux vidéo doivent être spécifiées dans les membres **dwRate** et **dwScale** et le nombre total de blocs vidéo dans le segment « movi » du membre **dwLength** .

Dans ce fichier AVI contenant la vidéo DV en tant que flux de données « vids » et DV audio en tant que flux « Auds », le bloc format de flux vidéo est une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) standard. Le bloc de format de flux peut éventuellement être étendu pour inclure le segment [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) , en accroissant la taille de segment de format de flux de 40 octets (taille de la structure **BITMAPINFOHEADER** ) à 72 octets (taille de **BITMAPINFOHEADER** plus structures **DVINFO** ) et immédiatement après la structure de données **BITMAPINFOHEADER** avec une structure de données **DVINFO** .

Le ou les flux audio sont spécifiés avec un en-tête de flux audio standard (la valeur du membre **fccType** est’Auds'). Le membre **fccHandler** n’est pas utilisé pour les flux audio.

Les données vidéo DV sont stockées en tant que \# \# segments « DC », tels que définis dans la description précédente d’un fichier AVI avec une donnée DV, et les données audio sont stockées en tant que \# \# segments « WB » dans le bloc « movi ».

> [!Note]  
> La *spécification des magnétoscopes numériques à usage particulier* peut ne pas être disponible dans certains langages et pays.

 

L’exemple suivant illustre la forme de formulaire RIFF AIFF pour un fichier AVI contenant une vidéo DV en tant que flux « vids » et audio DV en tant que flux « Auds » développés avec des blocs d’en-tête terminés (y compris les données [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) facultatives qui suivent le [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) dans le sous-bloc « Strf » pour le flux « vids »).


```C++
00000000 RIFF (103E2920) 'AVI '
0000000C     LIST (00000146) 'hdrl'
00000018         avih (00000038)
                     dwMicroSecPerFrame    : 33367
                     dwMaxBytesPerSec      : 3728000
                     dwPaddingGranularity  : 0
                     dwFlags               : 0x810 HASINDEX | TRUSTCKTYPE
                     dwTotalFrames         : 2192
                     dwInitialFrames       : 0
                     dwStreams             : 2
                     dwSuggestedBufferSize : 120000
                     dwWidth               : 720
                     dwHeight              : 480
                     dwReserved            : 0x0
00000058         LIST (00000094) 'strl'
00000064             strh (00000038)
                         fccType               : 'vids'
                         fccHandler            : 'dvsd'
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 100 (29.970 Frames/Sec)
                         dwRate                : 2997
                         dwStart               : 0
                         dwLength              : 2192
                         dwSuggestedBufferSize : 120000
                         dwQuality             : 0
                         dwSampleSize          : 0
                         rcFrame               : 0,0,720,480
000000A4             strf (00000048)
                         biSize          : 40
                         biWidth         : 720
                         biHeight        : 480
                         biPlanes        : 1
                         biBitCount      : 24
                         biCompression   : 0x64737664 'dvsd'
                         biSizeImage     : 120000
                         biXPelsPerMeter : 0
                         biYPelsPerMeter : 0
                         biClrUsed       : 0
                         biClrImportant  : 0
                         dwDVAAuxSrc     : 0x........
                         dwDVAAuxCtl     : 0x........
                         dwDVAAuxSrc1    : 0x........
                         dwDVAAuxCtl1    : 0x........
                         dwDVVAuxSrc     : 0x........
                         dwDVVAuxCtl     : 0x........
                         dwDVReserved[2] : 0,0
000000F4         LIST (0000005E) 'strl'
00000100             strh (00000038)
                         fccType               : 'auds'
                         fccHandler            : '    '
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 1 (32000.000 Samples/Sec)
                         dwRate                : 32000
                         dwStart               : 0
                         dwLength              : 2340474
                         dwSuggestedBufferSize : 4272
                         dwQuality             : 0
                         dwSampleSize          : 4
                         rcFrame               : 0,0,0,0
00000140             strf (00000012)
                         wFormatTag      : 1 PCM
                         nChannels       : 2
                         nSamplesPerSec  : 32000
                         nAvgBytesPerSec : 128000
                         nBlockAlign     : 4
                         wBitsPerSample  : 16
                         cbSize          : 0
00000814     LIST (103D0EF4) 'movi'
103D1710     idx1 (00011210)
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Format de fichier AVI](avi-file-format.md)
</dt> </dl>

 

 
