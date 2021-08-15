---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. AltitudeRef.
ms.assetid: abbb2441-25ca-484b-a744-620ff2794221
title: Stratégie de métadonnées de photo System. GPS. AltitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca49213754f605dcf6df40dfa3ff00e2b7aeaf765008037c23da21e35ab9ddee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710696"
---
# <a name="systemgpsaltituderef-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. AltitudeRef

Stratégie de métadonnées de la photo pour la propriété [System. GPS. AltitudeRef](../properties/props-system-gps-altituderef.md) .

### <a name="pkey"></a>A-la

\_AltitudeRef GPS \_

### <a name="description"></a>Description

Indique l’altitude utilisée comme altitude de référence. La valeur 0 indique que l’altitude est au-dessus de la mer. La valeur 1 indique une altitude inférieure au niveau de la mer.

### <a name="containers"></a>Containers

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



| Commande | Chemin                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 5} | byte        |
| 2     | /xmp/exif:GPSAltitudeRef | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 5} | byte        |
| 2     | /xmp/exif:GPSAltitudeRef | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{UShort = 5} |
| 2     | /xmp/exif:gpsaltituderef |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                         | Format de disque |
|-------|------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 5}          | byte        |
| 2     | /ifd/xmp/exif:GPSAltitudeRef | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                         | Format de disque |
|-------|------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 5}          | byte        |
| 2     | /ifd/xmp/exif:GPSAltitudeRef | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                         |
|-------|------------------------------|
| 1     | /IFD/GPS/{UShort = 5}          |
| 2     | /ifd/xmp/exif:gpsaltituderef |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. AltitudeRef](../properties/props-system-gps-altituderef.md)
</dt> </dl>

 

 
