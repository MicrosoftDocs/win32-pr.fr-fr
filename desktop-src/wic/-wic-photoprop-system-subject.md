---
description: Stratégie de métadonnées de la photo pour la propriété System. Subject.
ms.assetid: 5ab7c74b-8a5e-4329-8a49-291470d406cc
title: Stratégie de métadonnées de photo System. Subject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceabbab95a52a1155db949dbc60b4525dd5f9d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534676"
---
# <a name="systemsubject-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. Subject

Stratégie de métadonnées de la photo pour la propriété [System. Subject](../properties/props-system-subject.md) .

### <a name="pkey"></a>A-la

Sujet de la \_ rubrique

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_LPWStr VT

### <a name="input-propvariant-type"></a>Type de PROPVARIANT d’entrée

VT \_ LPWStr ou VT \_ LPWStr

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                     | Format de disque    |
|-------|--------------------------|----------------|
| 1     | /App1/IFD/{UShort = 40095} | \_octets Unicode |
| 2     | /App1/IFD/{UShort = 270}   | ascii          |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                     | Format de disque    |
|-------|--------------------------|----------------|
| 1     | /App1/IFD/{UShort = 40095} | \_octets Unicode |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                     |
|-------|--------------------------|
| 1     | /App1/IFD/{UShort = 40095} |
| 2     | /App1/IFD/{UShort = 270}   |



 

### <a name="tiff-policy"></a>Stratégie TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                | Format de disque    |
|-------|---------------------|----------------|
| 1     | /IFD/{UShort = 40095} | \_octets Unicode |
| 2     | /IFD/{UShort = 270}   | ascii          |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                | Format de disque    |
|-------|---------------------|----------------|
| 1     | /IFD/{UShort = 40095} | \_octets Unicode |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                |
|-------|---------------------|
| 1     | /IFD/{UShort = 40095} |
| 2     | /IFD/{UShort = 270}   |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. Subject](../properties/props-system-subject.md)
</dt> </dl>

 

 
