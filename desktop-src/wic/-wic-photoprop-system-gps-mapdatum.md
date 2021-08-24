---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. MapDatum.
ms.assetid: be31e98f-5114-4693-a9ef-37fea334875b
title: Stratégie de métadonnées de photo System. GPS. MapDatum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8bbd3671ec9e025dd2c5ea98fc36f4937abab315b09a2227fb6249d74e577da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882339"
---
# <a name="systemgpsmapdatum-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. MapDatum

Stratégie de métadonnées de la photo pour la propriété [System. GPS. MapDatum](../properties/props-system-gps-mapdatum.md) .

### <a name="pkey"></a>A-la

\_MapDatum GPS \_

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_LPWStr VT

### <a name="input-type"></a>Type d’entrée

VT \_ LPWStr est préféré, mais VT \_ LPSTR est également accepté

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="precedence-of-paths-jpeg"></a>Priorité des chemins d’accès (JPEG)

Si le fichier est au format JPEG, le gestionnaire lit, écrit et supprime les données dans l’ordre suivant :



| Commande | Chemin                          | Format de disque | Obligatoire |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSMapDatum         | Unicode     | Oui      |
| 2     | /App1/IFD/GPS/ \\ {UShort = 18 \\ } | ASCII       | Non       |



 

### <a name="precedence-of-paths-tiff"></a>Priorité des chemins d’accès (TIFF)

Si le fichier est au format TIFF, le gestionnaire lit, écrit et supprime les données dans l’ordre suivant :



| Commande | Chemin                      | Format de disque | Obligatoire |
|-------|---------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSMapDatum | Unicode     | Oui      |
| 2     | /IFD/GPS/ \\ {UShort = 18 \\ }  | ASCII       | Non       |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. MapDatum](../properties/props-system-gps-mapdatum.md)
</dt> </dl>

 

 
