---
description: La stratégie de métadonnées de la photo pour la propriété System. GPS. Latitude.
ms.assetid: 0f8cea07-da96-4d2a-8444-6073b51e1236
title: Stratégie de métadonnées de photo System. GPS. Latitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5320869c1e8fd0d4b17bb17da455fc939bf44b9a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324944"
---
# <a name="systemgpslatitude-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. Latitude

La stratégie de métadonnées de la photo pour la propriété [System. GPS. Latitude](../properties/props-system-gps-latitude.md) .

### <a name="pkey"></a>A-la

Latitude de la \_ balise GPS \_

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ Vector \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur peut être écrite en écrivant dans System. GPS. LatitudeNumerator et System. GPS. LatitudeDenominator. Il ne peut pas être écrit directement. Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 2} |             |
| 2     | /xmp/exif:GPSLatitude    |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 2} |             |
| 2     | /xmp/exif:GPSLatitude    |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{UShort = 2} |
| 2     | /xmp/exif:gpslatitude    |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 2}       |             |
| 2     | /ifd/xmp/exif:GPSLatitude |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 2}       |             |
| 2     | /ifd/xmp/exif:GPSLatitude |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                      |
|-------|---------------------------|
| 1     | /IFD/GPS/{UShort = 2}       |
| 2     | /ifd/xmp/exif:gpslatitude |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. Latitude](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
