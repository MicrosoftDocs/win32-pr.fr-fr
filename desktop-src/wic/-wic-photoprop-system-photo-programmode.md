---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. ProgramMode.
ms.assetid: f1954dc7-d4df-4675-ab3b-a65f2354e57a
title: Stratégie de métadonnées de photo System. photo. ProgramMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f5dffa822454509134c485e4792f4be4270912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952612"
---
# <a name="systemphotoprogrammode-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. ProgramMode

Stratégie de métadonnées de la photo pour la propriété [System. photo. ProgramMode](../properties/props-system-photo-programmode.md) .

### <a name="pkey"></a>A-la

\_Photo \_ ProgramMode

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ UI4

### <a name="input-type"></a>Type d’entrée

UShort

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 34850} | ushort      |
| 2     | /xmp/exif:ExposureProgram     | unicode     |
| 3     | /xmp/exif:ProgramMode         | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 34850} | ushort      |
| 2     | /xmp/exif:ExposureProgram     | unicode     |
| 3     | /xmp/exif:ProgramMode         | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 34850} |
| 2     | /xmp/exif:exposureprogram     |
| 3     | /xmp/exif:programmode         |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 34850}      | ushort      |
| 2     | /ifd/xmp/exif:ExposureProgram | unicode     |
| 3     | /ifd/xmp/exif:ProgramMode     | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 34850}      | ushort      |
| 2     | /ifd/xmp/exif:ExposureProgram | unicode     |
| 3     | /ifd/xmp/exif:ProgramMode     | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                          |
|-------|-------------------------------|
| 1     | /IFD/EXIF/{UShort = 34850}      |
| 2     | /ifd/xmp/exif:exposureprogram |
| 3     | /ifd/xmp/exif:programmode     |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. ProgramMode](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
