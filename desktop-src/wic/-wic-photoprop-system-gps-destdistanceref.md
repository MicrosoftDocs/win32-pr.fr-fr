---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. DestDistanceRef.
ms.assetid: eb671f34-7366-4182-b72e-0dd7830751e0
title: Stratégie de métadonnées de photo System. GPS. DestDistanceRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bba6e04bee00aaed868fcc02059403fe479f8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529213"
---
# <a name="systemgpsdestdistanceref-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. DestDistanceRef

Stratégie de métadonnées de la photo pour la propriété [System. GPS. DestDistanceRef](../properties/props-system-gps-destdistanceref.md) .

### <a name="pkey"></a>A-la

DestDistanceRef de la \_

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_LPWStr VT

### <a name="input-type"></a>Type d’entrée

VT \_ LPWStr ou VT \_ LPSTR sont acceptés.

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policies"></a>Stratégies JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                         | Format de disque |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 25}    | ascii       |
| 2     | /xmp/exif:GPSDestDistanceRef | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                         | Format de disque |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 25}    | ascii       |
| 2     | /xmp/exif:GPSDestDistanceRef | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                         |
|-------|------------------------------|
| 1     | /App1/IFD/GPS/{UShort = 25}    |
| 2     | /xmp/exif:gpsdestdistanceref |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                             | Format de disque |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 25}             | ascii       |
| 2     | /ifd/xmp/exif:GPSDestDistanceRef | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                             | Format de disque |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 25}             | ascii       |
| 2     | /ifd/xmp/exif:GPSDestDistanceRef | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                             |
|-------|----------------------------------|
| 1     | /IFD/GPS/{UShort = 25}             |
| 2     | /ifd/xmp/exif:gpsdestdistanceref |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. DestDistanceRef](../properties/props-system-gps-destdistanceref.md)
</dt> </dl>

 

 
