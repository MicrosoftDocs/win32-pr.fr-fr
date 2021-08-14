---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. Track.
ms.assetid: ac9e14a0-55f1-437e-9d27-df0fa09671c1
title: Stratégie de métadonnées de photo System. GPS. Track
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c89aee05d0c55e78fe4e55d7eacd8a8d0992fcb8d9f56312164c652cbc0bd81c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205530"
---
# <a name="systemgpstrack-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. Track

Stratégie de métadonnées de la photo pour la propriété [System. GPS. Track](../properties/props-system-gps-track.md) .

### <a name="pkey"></a>A-la

Piste de la \_ balise GPS \_

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ R8

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur est générée à partir de System. GPS. TrackNumerator et de System. GPS. TrackDenominator. Il ne peut pas être écrit directement. Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 15} |             |
| 2     | /xmp/exif:GPSTrack        |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 15} |             |
| 2     | /xmp/exif:GPSTrack        |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{UShort = 15} |
| 2     | /xmp/exif:gpstrack        |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                   | Format de disque |
|-------|------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 15}   |             |
| 2     | /ifd/xmp/exif:GPSTrack |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                   | Format de disque |
|-------|------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 15}   |             |
| 2     | /ifd/xmp/exif:GPSTrack |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                   |
|-------|------------------------|
| 1     | /IFD/GPS/{UShort = 15}   |
| 2     | /ifd/xmp/exif:gpstrack |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. Track](../properties/props-system-gps-track.md)
</dt> </dl>

 

 
