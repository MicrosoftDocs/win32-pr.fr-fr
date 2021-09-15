---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. DOP.
ms.assetid: 62efd1cc-a2ae-4e53-a0f2-4822b8c91c42
title: Stratégie de métadonnées de photo System. GPS. DOP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c33f3bfc6b958593748396124a8cfd1a7de73fd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530248"
---
# <a name="systemgpsdop-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. DOP

Stratégie de métadonnées de la photo pour la propriété [System. GPS. DOP](../properties/props-system-gps-dop.md) .

### <a name="pkey"></a>A-la

la \_ \_ DOP GPS

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ R8

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur peut être écrite en écrivant dans System. GPS. DOPNumerator et System. GPS. DOPDenominator. Il ne peut pas être écrit directement. Les valeurs de différents schémas sont conciliées.

### <a name="precedence-of-paths-jpeg"></a>Priorité des chemins d’accès (JPEG)

Si le fichier est au format JPEG, le gestionnaire lit, écrit et supprime les données dans l’ordre suivant :



| JSON | Chemin d’accès                          | Format de disque   | Obligatoire |
|-------|-------------------------------|---------------|----------|
| 1     | /xmp/exif:GPSDOP              | XMP Rational  | Oui      |
| 2     | /App1/IFD/GPS/ \\ {UShort = 11 \\ } | EXIF (Rational) | Non       |



 

### <a name="precedence-of-paths-tiff"></a>Priorité des chemins d’accès (TIFF)

Si le fichier est au format TIFF, le gestionnaire lit, écrit et supprime les données dans l’ordre suivant :



| JSON | Chemin d’accès                     | Format de disque   | Obligatoire |
|-------|--------------------------|---------------|----------|
| 1     | /ifd/xmp/exif:GPSDop     | XMP Rational  | Oui      |
| 2     | /IFD/GPS/ \\ {UShort = 11 \\ } | EXIF (Rational) | Non       |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. DOP](../properties/props-system-gps-dop.md)
</dt> </dl>

 

 
