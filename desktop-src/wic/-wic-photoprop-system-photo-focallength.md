---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. FocalLength.
ms.assetid: a282c31f-00dd-4df5-9b93-300bb9bc8f2d
title: Stratégie de métadonnées de photo System. photo. FocalLength
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7b36240713782c98d52e4fbf4dae5c0c06082
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521058"
---
# <a name="systemphotofocallength-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. FocalLength

Stratégie de métadonnées de la photo pour la propriété [System. photo. focalLength](../properties/props-system-photo-focallength.md) .

### <a name="pkey"></a>A-la

\_Photo \_ focalLength

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ R8

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur est générée à partir de System. photo. FocalLengthNumerator et de System. photo. FocalLengthDenominator. Il ne peut pas être écrit directement. Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37386} |             |
| 2     | /xmp/exif:FocalLength         |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37386} |             |
| 2     | /xmp/exif:FocalLength         |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 37386} |
| 2     | /xmp/exif:focallength         |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37386}  |             |
| 2     | /ifd/xmp/exif:FocalLength |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37386}  |             |
| 2     | /ifd/xmp/exif:FocalLength |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                      |
|-------|---------------------------|
| 1     | /IFD/EXIF/{UShort = 37386}  |
| 2     | /ifd/xmp/exif:focallength |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. FocalLength](../properties/props-system-photo-focallength.md)
</dt> </dl>

 

 
