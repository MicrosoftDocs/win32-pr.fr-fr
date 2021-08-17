---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. MeteringMode.
ms.assetid: cb0bf0d5-eccf-4345-a242-76769c34e02d
title: Stratégie de métadonnées de photo System. photo. MeteringMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424b14fa6216d5c88c350512d1583b311f92ef2f487e604760b1836b296d3bf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964778"
---
# <a name="systemphotometeringmode-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. MeteringMode

Stratégie de métadonnées de la photo pour la propriété [System. photo. MeteringMode](../properties/props-system-photo-meteringmode.md) .

### <a name="pkey"></a>A-la

\_Photo \_ MeteringMode

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_UI2 VT

### <a name="input-type"></a>Type d’entrée

UShort

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37383} | ushort      |
| 2     | /xmp/exif:MeteringMode        | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37383} | ushort      |
| 2     | /xmp/exif:MeteringMode        | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 37383} |
| 2     | /xmp/exif:meteringmode        |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                       | Format de disque |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37383}   | ushort      |
| 2     | /ifd/xmp/exif:MeteringMode | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                       | Format de disque |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37383}   | ushort      |
| 2     | /ifd/xmp/exif:MeteringMode | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                       |
|-------|----------------------------|
| 1     | /IFD/EXIF/{UShort = 37383}   |
| 2     | /ifd/xmp/exif:meteringmode |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. MeteringMode](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
