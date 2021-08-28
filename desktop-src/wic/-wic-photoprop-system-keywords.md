---
description: Stratégie de métadonnées de la photo pour la propriété System. Keywords.
ms.assetid: bc9de56f-444c-45a2-9822-fba2fe618d38
title: Stratégie de métadonnées de photo System. Keywords
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa5387bfb8cca7fffe83f7615a979d8e23ae890
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886643"
---
# <a name="systemkeywords-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. Keywords

Stratégie de métadonnées de la photo pour la propriété [System. Keywords](../properties/props-system-keywords.md) .

### <a name="pkey"></a>A-la

\_Mots clés de mot clé

### <a name="containers"></a>Containers

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



| JSON | Chemin d’accès                              | Format de disque    |
|-------|-----------------------------------|----------------|
| 1     | /XMP/ &lt; xmpbag &gt; DC : subject     | unicode        |
| 2     | /app13/irb/8bimiptc/iptc/keywords |                |
| 3     | /App1/IFD/{UShort = 18247}          | \_octets Unicode |
| 4     | /App1/IFD/{UShort = 40094}          | \_octets Unicode |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                                              | Format de disque    |
|-------|---------------------------------------------------|----------------|
| 1     | /XMP/ &lt; xmpbag &gt; DC : subject                     | unicode        |
| 2     | /app13/irb/8bimiptc/iptc/keywords                 |                |
| 3     | /App1/IFD/{UShort = 18247}                          | \_octets Unicode |
| 4     | /App1/IFD/{UShort = 40094}                          | \_octets Unicode |
| 5     | /XMP/ &lt; xmpbag &gt; MicrosoftPhoto : LastKeywordXMP  | unicode        |
| 6     | /XMP/ &lt; xmpbag &gt; MicrosoftPhoto : LastKeywordIPTC | unicode        |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                                              |
|-------|---------------------------------------------------|
| 1     | /XMP/DC : objet                                   |
| 2     | /app13/irb/8bimiptc/iptc/keywords                 |
| 3     | /App1/IFD/{UShort = 18247}                          |
| 4     | /App1/IFD/{UShort = 40094}                          |
| 5     | /XMP/ &lt; xmpbag &gt; MicrosoftPhoto : LastKeywordXMP  |
| 6     | /XMP/ &lt; xmpbag &gt; MicrosoftPhoto : LastKeywordIPTC |



 

### <a name="tiff-policy"></a>Stratégie TIFF

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                              | Format de disque    |
|-------|-----------------------------------|----------------|
| 1     | /IFD/XMP/ &lt; xmpbag &gt; DC : subject | unicode        |
| 2     | /ifd/iptc/keywords                |                |
| 3     | /IFD/{UShort = 18247}               | \_octets Unicode |
| 4     | /IFD/{UShort = 40094}               | \_octets Unicode |
| 5     | /ifd/irb/8bimiptc/iptc/keywords   |                |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                                                             | Format de disque    |
|-------|------------------------------------------------------------------|----------------|
| 1     | /IFD/XMP/ &lt; xmpbag &gt; DC : subject                                | unicode        |
| 2     | /ifd/iptc/keywords                                               |                |
| 3     | /ifd/irb/8bimiptc/iptc/keywords                                  |                |
| 4     | /IFD/{UShort = 18247}                                              | \_octets Unicode |
| 5     | /IFD/{UShort = 40094}                                              | \_octets Unicode |
| 6     | /IFD/XMP/ &lt; xmpbag &gt; MicrosoftPhoto : LastKeywordXMP             | unicode        |
| 7     | /IFD/XMP/ &lt; xmpbag &gt; MicrosoftPhoto : LastKeywordIPTC            | unicode        |
| 8     | /IFD/XMP/ &lt; xmpbag &gt; MicrosoftPhoto : LastKeywordIPTC \_ TIFF \_ IRB | unicode        |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                                                             |
|-------|------------------------------------------------------------------|
| 1     | /IFD/XMP/DC : objet                                              |
| 2     | /ifd/iptc/keywords                                               |
| 3     | /ifd/irb/8bimiptc/iptc/keywords                                  |
| 4     | /IFD/{UShort = 18247}                                              |
| 5     | /IFD/{UShort = 40094}                                              |
| 6     | /IFD/XMP/ &lt; xmpbag &gt; MicrosoftPhoto : LastKeywordXMP             |
| 7     | /IFD/XMP/ &lt; xmpbag &gt; MicrosoftPhoto : LastKeywordIPTC            |
| 8     | /IFD/XMP/ &lt; xmpbag &gt; MicrosoftPhoto : LastKeywordIPTC \_ TIFF \_ IRB |



 

### <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System.Keywords](../properties/props-system-keywords.md)
</dt> </dl>

 

 
