---
description: Stratégie de métadonnées de la photo pour la propriété System. Keywords.
ms.assetid: bc9de56f-444c-45a2-9822-fba2fe618d38
title: Stratégie de métadonnées de photo System. Keywords
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5d25e7f1919527d474395397d6df62863f7b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210078"
---
# <a name="systemkeywords-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. Keywords

Stratégie de métadonnées de la photo pour la propriété [System. Keywords](../properties/props-system-keywords.md) .

### <a name="pkey"></a>A-la

\_Mots clés de mot clé

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_LPWStr VT Vector \| VT \_

### <a name="input-propvariant-type"></a>Type de PROPVARIANT d’entrée

VT \_ Vector \| VT \_ LPWStr est préféré. Un \_ LPWStr VT contenant une chaîne délimitée par des points-virgules est également accepté.

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont fusionnées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                              | Format de disque    |
|-------|-----------------------------------|----------------|
| 1     | /XMP/ <xmpbag> contrôleur de domaine : objet     | unicode        |
| 2     | /app13/irb/8bimiptc/iptc/keywords |                |
| 3     | /App1/IFD/{UShort = 18247}          | \_octets Unicode |
| 4     | /App1/IFD/{UShort = 40094}          | \_octets Unicode |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                                              | Format de disque    |
|-------|---------------------------------------------------|----------------|
| 1     | /XMP/ <xmpbag> contrôleur de domaine : objet                     | unicode        |
| 2     | /app13/irb/8bimiptc/iptc/keywords                 |                |
| 3     | /App1/IFD/{UShort = 18247}                          | \_octets Unicode |
| 4     | /App1/IFD/{UShort = 40094}                          | \_octets Unicode |
| 5     | /XMP/ <xmpbag> MicrosoftPhoto : LastKeywordXMP  | unicode        |
| 6     | /XMP/ <xmpbag> MicrosoftPhoto : LastKeywordIPTC | unicode        |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                                              |
|-------|---------------------------------------------------|
| 1     | /XMP/DC : objet                                   |
| 2     | /app13/irb/8bimiptc/iptc/keywords                 |
| 3     | /App1/IFD/{UShort = 18247}                          |
| 4     | /App1/IFD/{UShort = 40094}                          |
| 5     | /XMP/ <xmpbag> MicrosoftPhoto : LastKeywordXMP  |
| 6     | /XMP/ <xmpbag> MicrosoftPhoto : LastKeywordIPTC |



 

### <a name="tiff-policy"></a>Stratégie TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                              | Format de disque    |
|-------|-----------------------------------|----------------|
| 1     | /IFD/XMP/ <xmpbag> contrôleur de domaine : objet | unicode        |
| 2     | /ifd/iptc/keywords                |                |
| 3     | /IFD/{UShort = 18247}               | \_octets Unicode |
| 4     | /IFD/{UShort = 40094}               | \_octets Unicode |
| 5     | /ifd/irb/8bimiptc/iptc/keywords   |                |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                                                             | Format de disque    |
|-------|------------------------------------------------------------------|----------------|
| 1     | /IFD/XMP/ <xmpbag> contrôleur de domaine : objet                                | unicode        |
| 2     | /ifd/iptc/keywords                                               |                |
| 3     | /ifd/irb/8bimiptc/iptc/keywords                                  |                |
| 4     | /IFD/{UShort = 18247}                                              | \_octets Unicode |
| 5     | /IFD/{UShort = 40094}                                              | \_octets Unicode |
| 6     | /IFD/XMP/ <xmpbag> MicrosoftPhoto : LastKeywordXMP             | unicode        |
| 7     | /IFD/XMP/ <xmpbag> MicrosoftPhoto : LastKeywordIPTC            | unicode        |
| 8     | /IFD/XMP/ <xmpbag> MicrosoftPhoto : LastKeywordIPTC \_ TIFF \_ IRB | unicode        |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                                                             |
|-------|------------------------------------------------------------------|
| 1     | /IFD/XMP/DC : objet                                              |
| 2     | /ifd/iptc/keywords                                               |
| 3     | /ifd/irb/8bimiptc/iptc/keywords                                  |
| 4     | /IFD/{UShort = 18247}                                              |
| 5     | /IFD/{UShort = 40094}                                              |
| 6     | /IFD/XMP/ <xmpbag> MicrosoftPhoto : LastKeywordXMP             |
| 7     | /IFD/XMP/ <xmpbag> MicrosoftPhoto : LastKeywordIPTC            |
| 8     | /IFD/XMP/ <xmpbag> MicrosoftPhoto : LastKeywordIPTC \_ TIFF \_ IRB |



 

### <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System.Keywords](../properties/props-system-keywords.md)
</dt> </dl>

 

 
