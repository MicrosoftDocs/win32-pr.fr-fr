---
description: Fonctions vidéo et image
ms.assetid: 02401edc-362b-4f6c-b10b-c46b30b3ebe7
title: Fonctions vidéo et image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab4b57f804c1da1e4a6da0ca4625e3503ed9987077a80f1f98dde91cf2e27f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432119"
---
# <a name="video-and-image-functions"></a>Fonctions vidéo et image

ces fonctions et macros manipulent les structures de format vidéo DirectShow.



| Fonction                                                             | Description                                                                                                                                                       |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_correspondances de masques de bits \_**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-bit_masks_match)                         | Compare les masques de couleur pour deux structures [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .                                                                                       |
| [**MASQUES**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-bitmasks)                                         | Récupère les masques de couleur à partir d’une structure [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                                         |
| [**CheckVideoInfoType**](checkvideoinfotype.md)                     | Vérifie un type de média qui contient une structure de format [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) pour les erreurs pouvant provoquer des dépassements de mémoire tampon ou des débordements d’entiers.   |
| [**CheckVideoInfo2Type**](checkvideoinfo2type.md)                   | Vérifie un type de média qui contient une structure de format [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) pour les erreurs pouvant provoquer des dépassements de mémoire tampon ou des débordements d’entiers. |
| [**COULEURS**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-colors)                                             | Récupère les entrées de palette d’une structure [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                                     |
| [**ContainsPalette**](containspalette.md)                           | Détermine si une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) spécifiée contient une palette.                                                           |
| [**ConvertVideoInfoToVideoInfo2**](convertvideoinfotovideoinfo2.md) | Convertit un type de média qui utilise [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) en un type qui utilise [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)                          |
| [**DIBSIZE**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize)                                           | Calcule le nombre d’octets requis par une image bitmap indépendante du périphérique (DIB, Device-Independent Bitmap).                                                                                     |
| [**GetBitCount**](getbitcount.md)                                   | Retourne le nombre de bits par pixel utilisé par un sous-type de vidéo spécifié.                                                                                           |
| [**GetBitmapFormatSize**](getbitmapformatsize.md)                   | Calcule la taille nécessaire pour une structure [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) qui peut contenir une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) spécifiée.       |
| [**GetBitmapPalette**](getbitmappalette.md)                         | Retourne la première entrée de la palette dans une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .                                                                        |
| [**GetBitmapSize**](getbitmapsize.md)                               | Calcule le nombre d’octets requis par une image bitmap indépendante du périphérique (DIB, Device-Independent Bitmap).                                                                                     |
| [**GetBitmapSubtype**](getbitmapsubtype.md)                         | Retourne le **GUID** du sous-type de média pour la bitmap spécifiée.                                                                                                      |
| [**GetSubtypeName**](getsubtypename.md)                             | Récupère le nom explicite d’un sous-type de vidéo.                                                                                                             |
| [**GetTrueColorType**](gettruecolortype.md)                         | Retourne le **GUID** du sous-type de média pour une bitmap RGB 16 bits non compressée.                                                                                          |
| [**TITRE**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header)                                             | Retourne l’adresse du [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) dans un [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader).                                      |
| [**\_Informations sur la séquence MPEG1 \_**](/previous-versions/windows/desktop/api/amvideo/nf-amvideo-mpeg1_sequence_info)                 | Retourne l’adresse de l’en-tête de séquence à l’intérieur d’une structure [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) .                                                          |
| [**PALETTISED**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-palettised)                                     | Vérifie si une image bitmap a une profondeur de couleur de 8 bits ou moins.                                                                                                      |
| [**entrées de PALETTE \_**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-palette_entries)                          | Récupère le nombre maximal de couleurs dans la palette d’une bitmap spécifiée.                                                                                      |
| [**RÉINITIALISER les \_ masques**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_masks)                                  | Remplit les champs de masque de couleur dans une structure [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) avec des zéros.                                                                            |
| [**RÉINITIALISER l' \_ en-tête**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_header)                                | Remplit un [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) avec des zéros.                                                                                                   |
| [**RÉINITIALISER la \_ palette**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_palette)                              | Remplit les entrées de palette dans une structure [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) avec des zéros.                                                                              |
| [**TAILLE de la \_ \_ palette EGA**](/previous-versions/windows/desktop/legacy/dd377602(v=vs.85))                       | Calcule la taille nécessaire pour les entrées de palette dans une bitmap RGB 4 bits.                                                                                         |
| [**masques de taille \_**](/previous-versions/windows/desktop/legacy/dd377603(v=vs.85))                                    | Calcule la taille des masques de couleur dans une structure [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .                                                                             |
| [**TAILLE \_ MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-size_mpeg1videoinfo)                  | Calcule la taille d’une structure [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) , y compris l’en-tête de séquence.                                                      |
| [**PALETTE de tailles \_**](/previous-versions/windows/desktop/legacy/dd377605(v=vs.85))                                | calcule la taille des entrées de palette dans une structure [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .                                                                         |
| [**\_PRÉEN-tête de taille**](/previous-versions/windows/desktop/legacy/dd377606(v=vs.85))                            | Calcule l’offset d’octet du champ **bmiHeader** dans une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .                                              |
| [**TAILLE \_ VIDEOHEADER**](/previous-versions/windows/desktop/legacy/dd377607(v=vs.85))                        | Calcule la taille de la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .                                                                                  |
| [**COULEURS**](/previous-versions/windows/desktop/legacy/dd407230(v=vs.85))                                   | Retourne la structure [**TRUECOLORINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-truecolorinfo) à partir d’une structure [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .                                            |
| [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md)         | Vérifie une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) pour rechercher les erreurs qui peuvent provoquer des dépassements de mémoire tampon ou des débordements d’entiers.                                   |



 

## <a name="remarks"></a>Remarques

La plupart des macros et des fonctions décrites dans la section sont conçues pour manipuler les structures **VIDEOINFOHEADER** et **VIDEOINFO** pour les bitmaps RGB. Utilisez ces macros avec précaution : la plupart d’entre elles partent du principe que la structure spécifiée a été initialisée correctement. Un grand nombre d’entre eux supposent également que la structure **BITMAPINFOHEADER** est la taille standard ; autrement dit, `biSize == sizeof(BITMAPINFOHEADER)` .

la bibliothèque de classes de base DirectShow fournit également les constantes globales suivantes, qui définissent les masques de couleur standard pour les bitmaps de couleurs vraies.



| Données globales | Description                                                   |
|-------------|---------------------------------------------------------------|
| **bits555** | Tableau de masques de couleur pour une bitmap RGB 16 bits au format 5-5-5. |
| **bits565** | Tableau de masques de couleur pour une bitmap RGB 16 bits au format 5-6-5. |
| **bits888** | Tableau de masques de couleur pour une bitmap RGB 24 bits.                 |



 

Chacune de ces constantes dans un tableau de trois **DWORD** s, contenant les masques rouge, vert et bleu, dans cet ordre.

 

 
