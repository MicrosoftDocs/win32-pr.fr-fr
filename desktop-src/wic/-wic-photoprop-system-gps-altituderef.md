---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. AltitudeRef.
ms.assetid: abbb2441-25ca-484b-a744-620ff2794221
title: Stratégie de métadonnées de photo System. GPS. AltitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db600d218d72014c49fd3f0a8b5eb11dd4c467d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523416"
---
# <a name="systemgpsaltituderef-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. AltitudeRef

Stratégie de métadonnées de la photo pour la propriété [System. GPS. AltitudeRef](../properties/props-system-gps-altituderef.md) .

### <a name="pkey"></a>A-la

\_AltitudeRef GPS \_

### <a name="description"></a>Description

Indique l’altitude utilisée comme altitude de référence. La valeur 0 indique que l’altitude est au-dessus de la mer. La valeur 1 indique une altitude inférieure au niveau de la mer.

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_UI1 VT

### <a name="input-type"></a>Type d’entrée

Poids.

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policies"></a>Stratégies JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 5} | byte        |
| 2     | /xmp/exif:GPSAltitudeRef | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 5} | byte        |
| 2     | /xmp/exif:GPSAltitudeRef | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{UShort = 5} |
| 2     | /xmp/exif:gpsaltituderef |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                         | Format de disque |
|-------|------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 5}          | byte        |
| 2     | /ifd/xmp/exif:GPSAltitudeRef | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                         | Format de disque |
|-------|------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 5}          | byte        |
| 2     | /ifd/xmp/exif:GPSAltitudeRef | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                         |
|-------|------------------------------|
| 1     | /IFD/GPS/{UShort = 5}          |
| 2     | /ifd/xmp/exif:gpsaltituderef |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. AltitudeRef](../properties/props-system-gps-altituderef.md)
</dt> </dl>

 

 
