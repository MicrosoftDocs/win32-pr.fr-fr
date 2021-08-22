---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. longitude.
ms.assetid: 36539e20-d00c-4bbb-b9ee-1cf5e4b8df4b
title: Stratégie de métadonnées de photo System. GPS. Longitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff05dd8ada6e10bbd3109187d34b220ff352ae984f92bd68281c56d3c1a29a76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087187"
---
# <a name="systemgpslongitude-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. Longitude

Stratégie de métadonnées de la photo pour la propriété [System. GPS. longitude](../properties/props-system-gps-longitude.md) .

### <a name="pkey"></a>A-la

\_Longitude GPS \_

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ Vector \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur peut être écrite en écrivant dans System. GPS. LongitudeNumerator et System. GPS. LongitudeDenominator. Il ne peut pas être écrit directement. Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 4} |             |
| 2     | /xmp/exif:GPSLongitude   |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 4} |             |
| 2     | /xmp/exif:GPSLongitude   |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{UShort = 4} |
| 2     | /xmp/exif:gpslongitude   |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                       | Format de disque |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 4}        |             |
| 2     | /ifd/xmp/exif:GPSLongitude |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                       | Format de disque |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 4}        |             |
| 2     | /ifd/xmp/exif:GPSLongitude |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                       |
|-------|----------------------------|
| 1     | /IFD/GPS/{UShort = 4}        |
| 2     | /ifd/xmp/exif:gpslongitude |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. Longitude](../properties/props-system-gps-longitude.md)
</dt> </dl>

 

 
