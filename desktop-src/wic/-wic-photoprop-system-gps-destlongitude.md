---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. DestLongitude.
ms.assetid: 885a522d-e1bf-43fb-a996-97e725b6cf0c
title: Stratégie de métadonnées de photo System. GPS. DestLongitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e0a4f56e49dfbb3397b96cf7fae35a6065b7aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523116"
---
# <a name="systemgpsdestlongitude-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. DestLongitude

Stratégie de métadonnées de la photo pour la propriété [System. GPS. DestLongitude](../properties/props-system-gps-destlongitude.md) .

### <a name="pkey"></a>A-la

\_DestLongitude GPS \_

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ Vector \| VT \_ R8

### <a name="input-propvariant-type"></a>Type de PROPVARIANT d’entrée

VT \_ Vector \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur est générée à partir de System. GPS. DestLongitudeNumerator et de System. GPS. DestLongitudeDenominator. Il ne peut pas être écrit directement. Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                       | Format de disque |
|-------|----------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 22}  |             |
| 2     | /xmp/exif:GPSDestLongitude |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                       | Format de disque |
|-------|----------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 22}  |             |
| 2     | /xmp/exif:GPSDestLongitude |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                       |
|-------|----------------------------|
| 1     | /App1/IFD/GPS/{UShort = 22}  |
| 2     | /xmp/exif:gpsdestlongitude |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                           | Format de disque |
|-------|--------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 22}           |             |
| 2     | /ifd/xmp/exif:GPSDestLongitude |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                           | Format de disque |
|-------|--------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 22}           |             |
| 2     | /ifd/xmp/exif:GPSDestLongitude |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                           |
|-------|--------------------------------|
| 1     | /IFD/GPS/{UShort = 22}           |
| 2     | /ifd/xmp/exif:gpsdestlongitude |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. DestLongitude](../properties/props-system-gps-destlongitude.md)
</dt> </dl>

 

 
