---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. DigitalZoom.
ms.assetid: 22a69d3e-4ec3-4652-b4bb-dfcfffc2322b
title: Stratégie de métadonnées de photo System. photo. DigitalZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19dfaf2838c8f321b1406d951fcc335076bcdfc00e3a17de0954f1a62022570e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205375"
---
# <a name="systemphotodigitalzoom-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. DigitalZoom

Stratégie de métadonnées de la photo pour la propriété [System. photo. DigitalZoom](../properties/props-system-photo-digitalzoom.md) .

### <a name="pkey"></a>A-la

\_Photo \_ DigitalZoom

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ R8

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur est générée à partir de System. photo. DigitalZoomNumerator et de System. photo. DigitalZoomDenominator. Il ne peut pas être écrit directement. Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41988} |             |
| 2     | /xmp/exif:DigitalZoomRatio    |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41988} |             |
| 2     | /xmp/exif:DigitalZoomRatio    |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 41988} |
| 2     | /xmp/exif:digitalzoomratio    |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                           | Format de disque |
|-------|--------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41988}       |             |
| 2     | /ifd/xmp/exif:DigitalZoomRatio |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                           | Format de disque |
|-------|--------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41988}       |             |
| 2     | /ifd/xmp/exif:DigitalZoomRatio |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                           |
|-------|--------------------------------|
| 1     | /IFD/EXIF/{UShort = 41988}       |
| 2     | /ifd/xmp/exif:digitalzoomratio |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. DigitalZoom](../properties/props-system-photo-digitalzoom.md)
</dt> </dl>

 

 
