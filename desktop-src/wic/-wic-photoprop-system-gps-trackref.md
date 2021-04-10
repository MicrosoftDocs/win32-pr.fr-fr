---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. TrackRef.
ms.assetid: e6912177-8add-4520-b396-c28060b359c7
title: Stratégie de métadonnées de photo System. GPS. TrackRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95fc63de6eaffd697798c08ff74a46c3d15c7818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210817"
---
# <a name="systemgpstrackref-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. TrackRef

Stratégie de métadonnées de la photo pour la propriété [System. GPS. TrackRef](../properties/props-system-gps-trackref.md) .

### <a name="pkey"></a>A-la

\_TrackRef GPS \_

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_LPWStr VT

### <a name="input-type"></a>Type d’entrée

String

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policies"></a>Stratégies JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 14} | ascii       |
| 2     | /xmp/exif:GPSTrackRef     | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 14} | ascii       |
| 2     | /xmp/exif:GPSTrackRef     | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{UShort = 14} |
| 2     | /xmp/exif:gpstrackref     |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 14}      | ascii       |
| 2     | /ifd/xmp/exif:GPSTrackRef | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 14}      | ascii       |
| 2     | /ifd/xmp/exif:GPSTrackRef | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                      |
|-------|---------------------------|
| 1     | /IFD/GPS/{UShort = 14}      |
| 2     | /ifd/xmp/exif:gpstrackref |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. TrackRef](../properties/props-system-gps-trackref.md)
</dt> </dl>

 

 
