---
description: Stratégie de métadonnées de la photo pour la propriété System. Author.
ms.assetid: 2de9c452-93be-40a4-a72b-5da590534dfd
title: Stratégie de métadonnées de photos System. Author
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 817fbea6a05b182bdb401f7ed623c0ebe94bbf63
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881656"
---
# <a name="systemauthor-photo-metadata-policy"></a>Stratégie de métadonnées de photos System. Author

Stratégie de métadonnées de la photo pour la propriété [System. Author](../properties/props-system-author.md) .

### <a name="pkey"></a>A-la

Auteur de la définition de l’écriture \_

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_LPWStr VT Vector \| VT \_

### <a name="input-propvariant-type"></a>Type de PROPVARIANT d’entrée

VT \_ Vector \| VT \_ LPWStr est préféré, mais VT \_ LPWStr est également accepté.

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                             | Format de disque    |
|-------|----------------------------------|----------------|
| 1     | /App1/IFD/{UShort = 315}           | ascii          |
| 2     | /app13/irb/8bimiptc/iptc/by-line |                |
| 3     | /XMP/ &lt; xmpseq &gt; DC : Creator    | unicode        |
| 4     | /app13/irb/8bimiptc/iptc/by-line |                |
| 5     | /App1/IFD/{UShort = 40093}         | \_octets Unicode |
| 6     | /XMP/TIFF : artiste                 | unicode        |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                             | Format de disque    |
|-------|----------------------------------|----------------|
| 1     | /XMP/ &lt; xmpseq &gt; DC : Creator    | unicode        |
| 2     | /XMP/TIFF : artiste                 | unicode        |
| 3     | /app13/irb/8bimiptc/iptc/by-line |                |
| 4     | /App1/IFD/{UShort = 315}           | ascii          |
| 5     | /App1/IFD/{UShort = 40093}         | \_octets Unicode |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                             |
|-------|----------------------------------|
| 1     | /XMP/DC : Creator                  |
| 2     | /XMP/TIFF : artiste                 |
| 3     | /app13/irb/8bimiptc/iptc/by-line |
| 4     | /App1/IFD/{UShort = 315}           |
| 5     | /App1/IFD/{UShort = 40093}         |



 

### <a name="tiff-policy"></a>Stratégie TIFF

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                              | Format de disque    |
|-------|-----------------------------------|----------------|
| 1     | /IFD/{UShort = 315}                 | ascii          |
| 2     | /ifd/iptc/by-line                 |                |
| 3     | /IFD/XMP/ &lt; xmpseq &gt; DC : Creator | unicode        |
| 4     | /ifd/iptc/by-line                 |                |
| 5     | /IFD/{UShort = 40093}               | \_octets Unicode |
| 6     | /ifd/irb/8bimiptc/iptc/by-line    |                |
| 7     | /IFD/XMP/TIFF : artiste              | unicode        |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                              | Format de disque    |
|-------|-----------------------------------|----------------|
| 1     | /IFD/XMP/ &lt; xmpseq &gt; DC : Creator | unicode        |
| 2     | /IFD/XMP/TIFF : artiste              | unicode        |
| 3     | /ifd/iptc/by-line                 |                |
| 4     | /IFD/{UShort = 315}                 | \_vecteur ASCII  |
| 5     | /IFD/{UShort = 40093}               | \_octets Unicode |
| 6     | /ifd/iptc/by-line                 |                |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                           |
|-------|--------------------------------|
| 1     | /IFD/XMP/DC : Creator            |
| 2     | /IFD/XMP/TIFF : artiste           |
| 3     | /ifd/iptc/by-line              |
| 4     | /ifd/irb/8bimiptc/iptc/by-line |
| 5     | /IFD/{UShort = 315}              |
| 6     | /IFD/{UShort = 40093}            |



 

### <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System.Author](../properties/props-system-author.md)
</dt> </dl>

 

 
