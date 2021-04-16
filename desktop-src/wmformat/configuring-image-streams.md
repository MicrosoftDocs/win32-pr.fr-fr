---
title: Configuration de flux d’images
description: Configuration de flux d’images
ms.assetid: 29325834-8766-47f4-8b33-b5fcbcc494c1
keywords:
- flux, configuration des flux d’images
- codecs, configuration des flux d’images
- flux d’images, configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b05a21474143e227257dad240ff4d4464732ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379869"
---
# <a name="configuring-image-streams"></a>Configuration de flux d’images

Les flux d’images contiennent des images fixes au format JPEG. Bien que les flux d’images soient comme des flux vidéo en ce qu’ils utilisent des images non compressées comme entrées, elles nécessitent une configuration légèrement différente. Pour configurer un flux d’image, vous devez définir les valeurs des membres des structures de configuration vidéo comme indiqué dans le tableau suivant.



| Paramètre                                                           | Description                                                                                                                                                                      |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_Type de média WM \_ . MajorType**                                     | Définissez sur WMMEDIATYPE \_ image.                                                                                                                                                       |
| **\_Type de média WM \_ . SubType**                                       | Définissez sur WMMEDIASUBTYPE \_ Rgb24.                                                                                                                                                    |
| **\_Type de média WM \_ . bFixedSizeSamples**                             | Affectez la valeur **false**.                                                                                                                                                                |
| **\_Type de média WM \_ . bTemporalCompression**                          | Affectez la valeur **false**.                                                                                                                                                                |
| **\_Type de média WM \_ . lSampleSize**                                   | Définit la valeur 0.                                                                                                                                                                        |
| **\_Type de média WM \_ . formatType**                                    | Définissez sur WMFORMAT \_ videoinfo.                                                                                                                                                      |
| **\_Type de média WM \_ . punk**                                          | Affectez la valeur **null**.                                                                                                                                                                 |
| **\_Type de média WM \_ . cbFormat**                                      | Défini sur `sizeof(WMVIDEOINFOHEADER)`.                                                                                                                                              |
| **\_Type de média WM \_ . pbFormat**                                      | Définissez sur l’adresse d’une structure **WMVIDEOINFOHEADER** correctement configurée.                                                                                                     |
| **WMVIDEOINFOHEADER. rcSource** et **WMVIDEOINFOHEADER. rcTarget** | Définissez les deux rectangles de sorte que les angles supérieurs gauches soient des coordonnées (0, 0) et que les coins inférieurs droits soient des coordonnées (x, y) où x correspond à la largeur de l’image et y à la hauteur de l’image. |
| **WMVIDEOINFOHEADER.dwBitRate**                                   | Défini sur la vitesse de transmission du flux.                                                                                                                                               |
| **WMVIDEOINFOHEADER.dwErrorRate**                                 | Définit la valeur 0.                                                                                                                                                                        |
| **WMVIDEOINFOHEADER.dwBitErrorRate**                              | Définit la valeur 0.                                                                                                                                                                        |
| **WMVIDEOINFOHEADER. AvgTimePerFrame**                             | Définit la valeur 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER. bichasse**                                      | Définissez sur la largeur de l’image.                                                                                                                                                   |
| **BITMAPINFOHEADER. bihauteur**                                     | Définissez sur la hauteur de l’image.                                                                                                                                                  |
| **BITMAPINFOHEADER. biplans**                                     | défini sur 1.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biBitCount**                                   | Défini sur 24.                                                                                                                                                                       |
| **BITMAPINFOHEADER. bicompression**                                | Défini sur BI \_ RGB.                                                                                                                                                                  |
| **BITMAPINFOHEADER.biSizeImage**                                  | Affectez à la valeur ((x \* y \* )/8), où x est la largeur de l’image, y à la hauteur de l’image et c à la profondeur de couleur de l’image (dans ce cas, toujours 24).                     |
| **BITMAPINFOHEADER.biXPelsPerMeter**                              | Définit la valeur 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biYPelsPerMeter**                              | Définit la valeur 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biClrUsed**                                    | Définit la valeur 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biClrImportant**                               | Définit la valeur 0.                                                                                                                                                                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Configuration commune à tous les flux**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuration de flux**](configuring-streams.md)
</dt> <dt>

[**Obtenir de bons résultats avec le codec d’écran Windows Media Video 9**](getting-good-results-with-the-windows-media-video-9-screen-codec.md)
</dt> <dt>

[**Flux d’images**](image-streams.md)
</dt> </dl>

 

 




