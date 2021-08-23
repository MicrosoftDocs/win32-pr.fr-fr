---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. DestLongitudeRef.
ms.assetid: 2a0abb9b-41e3-49ba-a60b-3096d9c032bd
title: Stratégie de métadonnées de photo System. GPS. DestLongitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fca1095138b35767da94e2eeed85a11892ba6edea3fa32f37ea6bd85fb76462
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964948"
---
# <a name="systemgpsdestlongituderef-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. DestLongitudeRef

Stratégie de métadonnées de la photo pour la propriété [System. GPS. DestLongitudeRef](../properties/props-system-gps-destlongituderef.md) .

### <a name="pkey"></a>A-la

\_GPS. DestLongitudeRef

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_LPWStr VT

### <a name="input-propvariant-type"></a>Type de PROPVARIANT d’entrée

VT \_ LPWStr est préféré, mais VT \_ LPSTR est également accepté.

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="precedence-of-paths-jpeg"></a>Priorité des chemins d’accès (JPEG)

Si le fichier est au format JPEG, le gestionnaire lit, écrit et supprime les données dans l’ordre suivant :



| Commande | Chemin                          | Format de disque | Obligatoire |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSDestLongitudeRef | Unicode     | Oui      |
| 2     | /App1/IFD/GPS/ \\ {UShort = 21 \\ } | ASCII       | Non       |



 

### <a name="precedence-of-paths-tiff"></a>Priorité des chemins d’accès (TIFF)

Si le fichier est au format TIFF, le gestionnaire lit, écrit et supprime les données dans l’ordre suivant :



| Commande | Chemin                              | Format de disque | Obligatoire |
|-------|-----------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSDestLongitudeRef | Unicode     | Oui      |
| 2     | /IFD/GPS/ \\ {UShort = 21 \\ }          | ASCII       | Non       |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. DestLongitudeRef](../properties/props-system-gps-destlongituderef.md)
</dt> </dl>

 

 
