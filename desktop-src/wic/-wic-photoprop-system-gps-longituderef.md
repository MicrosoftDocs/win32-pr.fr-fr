---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. LongitudeRef.
ms.assetid: 6e7b3b87-70e5-4c6a-a9b3-959eab38f1f0
title: Stratégie de métadonnées de photo System. GPS. LongitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a93d37b59ca7c77bc05e049860cf4e2608eb60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534108"
---
# <a name="systemgpslongituderef-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. LongitudeRef

Stratégie de métadonnées de la photo pour la propriété [System. GPS. LongitudeRef](../properties/props-system-gps-longituderef.md) .

### <a name="pkey"></a>A-la

\_LongitudeRef GPS \_

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_LPWStr VT

### <a name="input-type"></a>Type d’entrée

Chaîne.

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="precedence-of-paths-jpeg"></a>Priorité des chemins d’accès (JPEG)

Si le fichier est au format JPEG, le gestionnaire lit, écrit et supprime les données dans l’ordre suivant :



| Commande | Chemin d’accès                         | Format de disque | Obligatoire |
|-------|------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSLongitudeRef    | Unicode     | Oui      |
| 2     | /App1/IFD/GPS/ \\ {UShort = 3 \\ } | ASCII       | Non       |



 

### <a name="precedence-of-paths-tiff"></a>Priorité des chemins d’accès (TIFF)

Si le fichier est au format TIFF, le gestionnaire lit, écrit et supprime les données dans l’ordre suivant :



| Commande | Chemin d’accès                          | Format de disque | Obligatoire |
|-------|-------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSLongitudeRef | Unicode     | Oui      |
| 2     | /IFD/GPS/ \\ {UShort = 3 \\ }       | ASCII       | Non       |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. LongitudeRef](../properties/props-system-gps-longituderef.md)
</dt> </dl>

 

 
