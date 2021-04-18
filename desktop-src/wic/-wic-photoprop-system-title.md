---
description: Stratégie de métadonnées de la photo pour la propriété System. title.
ms.assetid: 84da345e-ec03-48fe-8fda-043b706e4e1c
title: Stratégie de métadonnées de photo System. title
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b02513f3f566576999e83b09c156d36ac480c17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526194"
---
# <a name="systemtitle-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. title

Stratégie de métadonnées de la photo pour la propriété [System. title](../properties/props-system-title.md) .

### <a name="pkey"></a>A-la

Titre de la \_ section

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_LPWStr VT

### <a name="input-propvariant-type"></a>Type de PROPVARIANT d’entrée

VT \_ LPWStr ou VT \_ LPSTR

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                                | Format de disque    |
|-------|-------------------------------------|----------------|
| 1     | /App1/IFD/{UShort = 40091}            | \_octets Unicode |
| 2     | /XMP/ <xmpalt> DC : titre         | unicode        |
| 3     | /XMP/DC : titre                       | unicode        |
| 4     | /App1/IFD/EXIF/{UShort = 37510}       | unicode        |
| 5     | /App1/IFD/{UShort = 270}              | ascii          |
| 6     | /app13/irb/8bimiptc/iptc/caption    |                |
| 7     | /XMP/ <xmpalt> DC : description   | unicode        |
| 8     | /XMP/DC : description                 | unicode        |
| 9     | /app13/irb/8bimiptc/iptc/caption    |                |
| 10    | /XMP/ <xmpalt> EXIF : UserComment | unicode        |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                                | Format de disque    |
|-------|-------------------------------------|----------------|
| 1     | /App1/IFD/{UShort = 40091}            | \_octets Unicode |
| 2     | /XMP/DC : titre                       | unicode        |
| 3     | /XMP/ <xmpalt> DC : titre         | unicode        |
| 4     | /App1/IFD/EXIF/{UShort = 37510}       | unicode        |
| 5     | /XMP/ <xmpalt> EXIF : UserComment | unicode        |
| 6     | /App1/IFD/{UShort = 270}              | ascii          |
| 7     | /app13/irb/8bimiptc/iptc/caption    |                |
| 8     | /XMP/DC : description                 | unicode        |
| 9     | /XMP/ <xmpalt> DC : description   | unicode        |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                                |
|-------|-------------------------------------|
| 1     | /App1/IFD/{UShort = 40091}            |
| 2     | /XMP/DC : titre                       |
| 3     | /App1/IFD/EXIF/{UShort = 37510}       |
| 4     | /XMP/ <xmpalt> EXIF : UserComment |
| 5     | /App1/IFD/{UShort = 270}              |
| 6     | /app13/irb/8bimiptc/iptc/caption    |
| 7     | /XMP/DC : description                 |



 

### <a name="tiff-policy"></a>Stratégie TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                                    | Format de disque    |
|-------|-----------------------------------------|----------------|
| 1     | /IFD/{UShort = 40091}                     | \_octets Unicode |
| 2     | /IFD/XMP/ <xmpalt> DC : titre         | unicode        |
| 3     | /IFD/XMP/DC : titre                       | unicode        |
| 4     | /IFD/EXIF/{UShort = 37510}                | unicode        |
| 5     | /IFD/{UShort = 270}                       | ascii          |
| 6     | /ifd/iptc/caption                       |                |
| 7     | /IFD/XMP/ <xmpalt> DC : description   | unicode        |
| 8     | /IFD/XMP/DC : description                 | unicode        |
| 9     | /ifd/iptc/caption                       |                |
| 10    | /ifd/irb/8bimiptc/iptc/caption          |                |
| 11    | /IFD/XMP/ <xmpalt> EXIF : UserComment | unicode        |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                                    | Format de disque    |
|-------|-----------------------------------------|----------------|
| 1     | /IFD/{UShort = 40091}                     | \_octets Unicode |
| 2     | /IFD/XMP/DC : titre                       | unicode        |
| 3     | /IFD/XMP/ <xmpalt> DC : titre         | unicode        |
| 4     | /IFD/EXIF/{UShort = 37510}                | unicode        |
| 5     | /IFD/XMP/ <xmpalt> EXIF : UserComment | unicode        |
| 6     | /IFD/{UShort = 270}                       | ascii          |
| 7     | /ifd/iptc/caption                       |                |
| 8     | /ifd/irb/8bimiptc/iptc/caption          |                |
| 9     | /IFD/XMP/DC : description                 | unicode        |
| 10    | /IFD/XMP/ <xmpalt> DC : description   | unicode        |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                                    |
|-------|-----------------------------------------|
| 1     | /IFD/{UShort = 40091}                     |
| 2     | /IFD/XMP/DC : titre                       |
| 3     | /IFD/EXIF/{UShort = 37510}                |
| 4     | /IFD/XMP/ <xmpalt> EXIF : UserComment |
| 5     | /IFD/{UShort = 270}                       |
| 6     | /ifd/iptc/caption                       |
| 7     | /ifd/irb/8bimiptc/iptc/caption          |
| 8     | /IFD/XMP/DC : description                 |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System.Title](../properties/props-system-title.md)
</dt> </dl>

 

 
