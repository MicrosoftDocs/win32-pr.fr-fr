---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. LatitudeRef.
ms.assetid: 057015fd-38b7-4053-b611-72565975cc58
title: Stratégie de métadonnées de photo System. GPS. LatitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782fbcecbed90c9c75c1ae5fe9d5409496f842a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209766"
---
# <a name="systemgpslatituderef-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. LatitudeRef

Stratégie de métadonnées de la photo pour la propriété [System. GPS. LatitudeRef](../properties/props-system-gps-latitude.md) .

### <a name="pkey"></a>A-la

\_LatitudeRef GPS \_

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_LPWStr VT

### <a name="input-type"></a>Type d’entrée

VT \_ LPWStr est préféré, mais VT \_ LPSTR est également accepté.

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="precedence-of-paths-jpeg"></a>Priorité des chemins d’accès (JPEG)

Si le fichier est au format JPEG, le gestionnaire lit, écrit et supprime les données dans l’ordre suivant :



| Commande | Chemin d’accès                         | Format de disque | Obligatoire |
|-------|------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSLatitudeRef     | Unicode     | Oui      |
| 2     | /App1/IFD/GPS/ \\ {UShort = 1 \\ } | ASCII       | Non       |



 

### <a name="precedence-of-paths-tiff"></a>Priorité des chemins d’accès (TIFF)

Si le fichier est au format TIFF, le gestionnaire lit, écrit et supprime les données dans l’ordre suivant :



| Commande | Chemin d’accès                         | Format de disque | Obligatoire |
|-------|------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSLatitudeRef | Unicode     | Oui      |
| 2     | /IFD/GPS/ \\ {UShort = 1 \\ }      | ASCII       | Non       |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. LatitudeRef](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
