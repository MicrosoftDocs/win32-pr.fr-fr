---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. Brightness.
ms.assetid: 3fd73845-f1d9-468c-abf8-081109880974
title: Stratégie de métadonnées de photo System. photo. Brightness
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd7328b4d40b8d1582dcc17b317b706b2695c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952828"
---
# <a name="systemphotobrightness-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. Brightness

Stratégie de métadonnées de la photo pour la propriété [System. photo. Brightness](../properties/props-system-photo-aperture.md) .

### <a name="pkey"></a>A-la

Luminosité de la photo de la \_ \_

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="input-type"></a>Type d’entrée

Double

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur est générée à partir de System. photo. ApertureNumerator et de System. photo. ApertureDenominator. Il ne peut pas être écrit directement. Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37379} |             |
| 2     | /xmp/exif:BrightnessValue     |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37379} |             |
| 2     | /xmp/exif:BrightnessValue     |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 37379} |
| 2     | /xmp/exif:brightnessvalue     |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37379}      |             |
| 2     | /ifd/xmp/exif:BrightnessValue |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37379}      |             |
| 2     | /ifd/xmp/exif:BrightnessValue |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                          |
|-------|-------------------------------|
| 1     | /IFD/EXIF/{UShort = 37379}      |
| 2     | /ifd/xmp/exif:brightnessvalue |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. Brightness](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
