---
description: Stratégie de métadonnées de la photo pour la propriété System. title.
ms.assetid: 84da345e-ec03-48fe-8fda-043b706e4e1c
title: Stratégie de métadonnées de photo System. title
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa43b31595928fa3c2c936de8710131c20f17b1a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880682"
---
# <a name="systemtitle-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. title

Stratégie de métadonnées de la photo pour la propriété [System. title](../properties/props-system-title.md) .

### <a name="pkey"></a>A-la

Titre de la \_ section

### <a name="containers"></a>Containers

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



| JSON | Chemin d’accès                                | Format de disque    |
|-------|-------------------------------------|----------------|
| 1     | /App1/IFD/{UShort = 40091}            | \_octets Unicode |
| 2     | /XMP/ &lt; xmpalt &gt; DC : title         | unicode        |
| 3     | /XMP/DC : titre                       | unicode        |
| 4     | /App1/IFD/EXIF/{UShort = 37510}       | unicode        |
| 5     | /App1/IFD/{UShort = 270}              | ascii          |
| 6     | /app13/irb/8bimiptc/iptc/caption    |                |
| 7     | /XMP/ &lt; xmpalt &gt; DC : description   | unicode        |
| 8     | /XMP/DC : description                 | unicode        |
| 9     | /app13/irb/8bimiptc/iptc/caption    |                |
| 10    | /XMP/ &lt; xmpalt &gt; EXIF : UserComment | unicode        |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                                | Format de disque    |
|-------|-------------------------------------|----------------|
| 1     | /App1/IFD/{UShort = 40091}            | \_octets Unicode |
| 2     | /XMP/DC : titre                       | unicode        |
| 3     | /XMP/ &lt; xmpalt &gt; DC : title         | unicode        |
| 4     | /App1/IFD/EXIF/{UShort = 37510}       | unicode        |
| 5     | /XMP/ &lt; xmpalt &gt; EXIF : UserComment | unicode        |
| 6     | /App1/IFD/{UShort = 270}              | ascii          |
| 7     | /app13/irb/8bimiptc/iptc/caption    |                |
| 8     | /XMP/DC : description                 | unicode        |
| 9     | /XMP/ &lt; xmpalt &gt; DC : description   | unicode        |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                                |
|-------|-------------------------------------|
| 1     | /App1/IFD/{UShort = 40091}            |
| 2     | /XMP/DC : titre                       |
| 3     | /App1/IFD/EXIF/{UShort = 37510}       |
| 4     | /XMP/ &lt; xmpalt &gt; EXIF : UserComment |
| 5     | /App1/IFD/{UShort = 270}              |
| 6     | /app13/irb/8bimiptc/iptc/caption    |
| 7     | /XMP/DC : description                 |



 

### <a name="tiff-policy"></a>Stratégie TIFF

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                                    | Format de disque    |
|-------|-----------------------------------------|----------------|
| 1     | /IFD/{UShort = 40091}                     | \_octets Unicode |
| 2     | /IFD/XMP/ &lt; xmpalt &gt; DC : title         | unicode        |
| 3     | /IFD/XMP/DC : titre                       | unicode        |
| 4     | /IFD/EXIF/{UShort = 37510}                | unicode        |
| 5     | /IFD/{UShort = 270}                       | ascii          |
| 6     | /ifd/iptc/caption                       |                |
| 7     | /IFD/XMP/ &lt; xmpalt &gt; DC : description   | unicode        |
| 8     | /IFD/XMP/DC : description                 | unicode        |
| 9     | /ifd/iptc/caption                       |                |
| 10    | /ifd/irb/8bimiptc/iptc/caption          |                |
| 11    | /IFD/XMP/ &lt; xmpalt &gt; EXIF : UserComment | unicode        |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                                    | Format de disque    |
|-------|-----------------------------------------|----------------|
| 1     | /IFD/{UShort = 40091}                     | \_octets Unicode |
| 2     | /IFD/XMP/DC : titre                       | unicode        |
| 3     | /IFD/XMP/ &lt; xmpalt &gt; DC : title         | unicode        |
| 4     | /IFD/EXIF/{UShort = 37510}                | unicode        |
| 5     | /IFD/XMP/ &lt; xmpalt &gt; EXIF : UserComment | unicode        |
| 6     | /IFD/{UShort = 270}                       | ascii          |
| 7     | /ifd/iptc/caption                       |                |
| 8     | /ifd/irb/8bimiptc/iptc/caption          |                |
| 9     | /IFD/XMP/DC : description                 | unicode        |
| 10    | /IFD/XMP/ &lt; xmpalt &gt; DC : description   | unicode        |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                                    |
|-------|-----------------------------------------|
| 1     | /IFD/{UShort = 40091}                     |
| 2     | /IFD/XMP/DC : titre                       |
| 3     | /IFD/EXIF/{UShort = 37510}                |
| 4     | /IFD/XMP/ &lt; xmpalt &gt; EXIF : UserComment |
| 5     | /IFD/{UShort = 270}                       |
| 6     | /ifd/iptc/caption                       |
| 7     | /ifd/irb/8bimiptc/iptc/caption          |
| 8     | /IFD/XMP/DC : description                 |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System.Title](../properties/props-system-title.md)
</dt> </dl>

 

 
