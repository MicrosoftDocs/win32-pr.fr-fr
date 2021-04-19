---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. Track.
ms.assetid: ac9e14a0-55f1-437e-9d27-df0fa09671c1
title: Stratégie de métadonnées de photo System. GPS. Track
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 773c65eec8b165c51456f3871309644638c1e2da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535676"
---
# <a name="systemgpstrack-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. Track

Stratégie de métadonnées de la photo pour la propriété [System. GPS. Track](../properties/props-system-gps-track.md) .

### <a name="pkey"></a>A-la

Piste de la \_ balise GPS \_

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ R8

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur est générée à partir de System. GPS. TrackNumerator et de System. GPS. TrackDenominator. Il ne peut pas être écrit directement. Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 15} |             |
| 2     | /xmp/exif:GPSTrack        |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 15} |             |
| 2     | /xmp/exif:GPSTrack        |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{UShort = 15} |
| 2     | /xmp/exif:gpstrack        |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                   | Format de disque |
|-------|------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 15}   |             |
| 2     | /ifd/xmp/exif:GPSTrack |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                   | Format de disque |
|-------|------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 15}   |             |
| 2     | /ifd/xmp/exif:GPSTrack |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                   |
|-------|------------------------|
| 1     | /IFD/GPS/{UShort = 15}   |
| 2     | /ifd/xmp/exif:gpstrack |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. Track](../properties/props-system-gps-track.md)
</dt> </dl>

 

 
