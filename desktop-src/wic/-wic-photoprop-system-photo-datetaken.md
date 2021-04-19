---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. DateTaken.
ms.assetid: 800aa01b-6064-45df-a40e-6537819df4d7
title: Stratégie de métadonnées de photo System. photo. DateTaken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc1d3fb50a9a94e4bb13b35a0a5726572d78429f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522222"
---
# <a name="systemphotodatetaken-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. DateTaken

Stratégie de métadonnées de la photo pour la propriété [System. photo. DateTaken](../properties/props-system-photo-datetaken.md) .

### <a name="pkey"></a>A-la

\_Photo \_ DateTaken

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

de VT \_ fileTime

### <a name="input-type"></a>Type d’entrée

DateTime

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                                  | Format de disque |
|-------|---------------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 36867}         | ascii       |
| 2     | /APP13/IRB/8bimiptc/IPTC/Date créé | unicode     |
| 3     | /XMP/XMP : CreateD                   | unicode     |
| 4     | /App1/IFD/EXIF/{UShort = 36868}         | ascii       |
| 5     | /APP13/IRB/8bimiptc/IPTC/Date créé | unicode     |
| 6     | /xmp/exif:DateTimeOriginal            | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                                  | Format de disque |
|-------|---------------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 36867}         | ascii       |
| 2     | /APP13/IRB/8bimiptc/IPTC/Date créé | unicode     |
| 3     | /XMP/XMP : CreateD                   | unicode     |
| 4     | /App1/IFD/EXIF/{UShort = 36868}         | ascii       |
| 5     | /xmp/exif:DateTimeOriginal            | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                                  |
|-------|---------------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 36867}         |
| 2     | /App1/IFD/EXIF/{UShort = 37521}         |
| 3     | /App1/IFD/EXIF/{UShort = 36868}         |
| 4     | /App1/IFD/EXIF/{UShort = 37522}         |
| 5     | /xmp/exif:DateTimeOriginal            |
| 6     | /XMP/XMP : CreateD                   |
| 7     | /APP13/IRB/8bimiptc/IPTC/Date créé |
| 8     | /APP13/IRB/8bimiptc/IPTC/Time créé |



 

### <a name="tiff-policy"></a>Stratégie TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                                | Format de disque |
|-------|-------------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 36867}            | ascii       |
| 2     | /IFD/IPTC/Date créé              | unicode     |
| 3     | /IFD/XMP/XMP : CreateD             | unicode     |
| 4     | /IFD/EXIF/{UShort = 36868}            | ascii       |
| 5     | /IFD/IPTC/Date créé              | unicode     |
| 6     | /IFD/IRB/8bimiptc/IPTC/Date créé | unicode     |
| 7     | /ifd/xmp/exif:DateTimeOriginal      | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                                | Format de disque |
|-------|-------------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 36867}            | ascii       |
| 2     | /IFD/IPTC/Date créé              | unicode     |
| 3     | /IFD/XMP/XMP : CreateD             | unicode     |
| 4     | /IFD/EXIF/{UShort = 36868}            | ascii       |
| 5     | /IFD/IRB/8bimiptc/IPTC/Date créé | unicode     |
| 6     | /ifd/xmp/exif:DateTimeOriginal      | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                                |
|-------|-------------------------------------|
| 1     | /IFD/EXIF/{UShort = 36867}            |
| 2     | /IFD/EXIF/{UShort = 37521}            |
| 3     | /IFD/EXIF/{UShort = 36868}            |
| 4     | /IFD/EXIF/{UShort = 37522}            |
| 5     | /ifd/xmp/exif:DateTimeOriginal      |
| 6     | /IFD/XMP/XMP : CreateD             |
| 7     | /IFD/IPTC/Date créé              |
| 8     | /IFD/IPTC/Time créé              |
| 9     | /IFD/IRB/8bimiptc/IPTC/Date créé |
| 10    | /IFD/IRB/8bimiptc/IPTC/Time créé |



 

### <a name="png-policy"></a>Stratégie PNG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 1     | /\[\*\]Texte/heure de création | ascii       |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                      | Format de disque |
|-------|---------------------------|-------------|
| 2     | /\[\*\]Texte/heure de création | ascii       |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                      |
|-------|---------------------------|
| 3     | /\[\*\]Texte/heure de création |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. DateTaken](../properties/props-system-photo-datetaken.md)
</dt> </dl>

 

 
