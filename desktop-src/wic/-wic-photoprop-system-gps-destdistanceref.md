---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. DestDistanceRef.
ms.assetid: eb671f34-7366-4182-b72e-0dd7830751e0
title: Stratégie de métadonnées de photo System. GPS. DestDistanceRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0d7973a3be36f9a7624ed8679f364c898d69b622de067bdd2595f3b919a964f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964978"
---
# <a name="systemgpsdestdistanceref-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. DestDistanceRef

Stratégie de métadonnées de la photo pour la propriété [System. GPS. DestDistanceRef](../properties/props-system-gps-destdistanceref.md) .

### <a name="pkey"></a>A-la

DestDistanceRef de la \_

### <a name="containers"></a>Containers

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



| Commande | Chemin                         | Format de disque |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 25}    | ascii       |
| 2     | /xmp/exif:GPSDestDistanceRef | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                         | Format de disque |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 25}    | ascii       |
| 2     | /xmp/exif:GPSDestDistanceRef | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                         |
|-------|------------------------------|
| 1     | /App1/IFD/GPS/{UShort = 25}    |
| 2     | /xmp/exif:gpsdestdistanceref |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                             | Format de disque |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 25}             | ascii       |
| 2     | /ifd/xmp/exif:GPSDestDistanceRef | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                             | Format de disque |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 25}             | ascii       |
| 2     | /ifd/xmp/exif:GPSDestDistanceRef | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                             |
|-------|----------------------------------|
| 1     | /IFD/GPS/{UShort = 25}             |
| 2     | /ifd/xmp/exif:gpsdestdistanceref |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. DestDistanceRef](../properties/props-system-gps-destdistanceref.md)
</dt> </dl>

 

 
