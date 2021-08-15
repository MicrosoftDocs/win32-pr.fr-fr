---
description: Stratégie de métadonnées de la photo pour la propriété System. image. CompressedBitsPerPixel.
ms.assetid: e97a5c68-6d4a-44af-8096-22680f8b16b8
title: Stratégie de métadonnées de photo System. image. CompressedBitsPerPixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a18cc76e22c5c409e19e08fc5a2e667ad374348bc753ffa85cd09003a8bdaf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118032708"
---
# <a name="systemimagecompressedbitsperpixel-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. image. CompressedBitsPerPixel

Stratégie de métadonnées de la photo pour la propriété [System. image. CompressedBitsPerPixel](../properties/props-system-image-compressedbitsperpixel.md) .

### <a name="pkey"></a>A-la

Image de la \_ \_ CompressedBitsPerPixel

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ R8

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur est générée à partir de System. image. CompressedBitsPerPixelNumerator et de System. image. CompressedBitsPerPixelDenominator. Il ne peut pas être écrit directement. Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                             | Format de disque |
|-------|----------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37122}    |             |
| 2     | /xmp/exif:CompressedBitsPerPixel |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                             |
|-------|----------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 37122}    |
| 2     | /xmp/exif:compressedbitsperpixel |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                                 | Format de disque |
|-------|--------------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37122}             |             |
| 2     | /ifd/xmp/exif:CompressedBitsPerPixel |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                                 |
|-------|--------------------------------------|
| 1     | /IFD/EXIF/{UShort = 37122}             |
| 2     | /ifd/xmp/exif:compressedbitsperpixel |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. image. CompressedBitsPerPixel](../properties/props-system-image-compressedbitsperpixel.md)
</dt> </dl>

 

 
