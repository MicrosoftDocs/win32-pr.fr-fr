---
description: La stratégie de métadonnées de la photo pour la propriété System. GPS. satellites.
ms.assetid: 5dbbbeaf-e67d-45f6-95b2-de3287202d41
title: Stratégie de métadonnées de photos System. GPS. satellites
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980393accdb1bee3d2a44dd539f3c9fb169c648b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519145"
---
# <a name="systemgpssatellites-photo-metadata-policy"></a>Stratégie de métadonnées de photos System. GPS. satellites

La stratégie de métadonnées de la photo pour la propriété [System. GPS. satellites](../properties/props-system-gps-satellites.md) .

### <a name="pkey"></a>A-la

\_Satellites GPS \_

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_LPWStr VT

### <a name="input-type"></a>Type d’entrée

Chaîne.

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policies"></a>Stratégies JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 8} | ascii       |
| 2     | /xmp/exif:GPSSatellites  | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 8} | ascii       |
| 2     | /xmp/exif:GPSSatellites  | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{UShort = 8} |
| 2     | /xmp/exif:gpssatellites  |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                        | Format de disque |
|-------|-----------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 8}         | ascii       |
| 2     | /ifd/xmp/exif:GPSSatellites | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                        | Format de disque |
|-------|-----------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 8}         | ascii       |
| 2     | /ifd/xmp/exif:GPSSatellites | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                        |
|-------|-----------------------------|
| 1     | /IFD/GPS/{UShort = 8}         |
| 2     | /ifd/xmp/exif:gpssatellites |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. satellites](../properties/props-system-gps-satellites.md)
</dt> </dl>

 

 
