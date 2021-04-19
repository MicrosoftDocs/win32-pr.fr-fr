---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. longitude.
ms.assetid: 36539e20-d00c-4bbb-b9ee-1cf5e4b8df4b
title: Stratégie de métadonnées de photo System. GPS. Longitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25eb9869bc536f97adfc8f3c0f5b1f70c8bf030f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106537067"
---
# <a name="systemgpslongitude-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. Longitude

Stratégie de métadonnées de la photo pour la propriété [System. GPS. longitude](../properties/props-system-gps-longitude.md) .

### <a name="pkey"></a>A-la

\_Longitude GPS \_

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ Vector \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur peut être écrite en écrivant dans System. GPS. LongitudeNumerator et System. GPS. LongitudeDenominator. Il ne peut pas être écrit directement. Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 4} |             |
| 2     | /xmp/exif:GPSLongitude   |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 4} |             |
| 2     | /xmp/exif:GPSLongitude   |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{UShort = 4} |
| 2     | /xmp/exif:gpslongitude   |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                       | Format de disque |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 4}        |             |
| 2     | /ifd/xmp/exif:GPSLongitude |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                       | Format de disque |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 4}        |             |
| 2     | /ifd/xmp/exif:GPSLongitude |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                       |
|-------|----------------------------|
| 1     | /IFD/GPS/{UShort = 4}        |
| 2     | /ifd/xmp/exif:gpslongitude |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. Longitude](../properties/props-system-gps-longitude.md)
</dt> </dl>

 

 
