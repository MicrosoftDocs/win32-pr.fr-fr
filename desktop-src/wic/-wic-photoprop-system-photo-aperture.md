---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. orifice.
ms.assetid: 3048eb9d-4ed4-4b5b-960e-9d0fd6704041
title: Stratégie de métadonnées de photo System. photo. orifice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc02826b0602d0052f129640901ac3564a0eadb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524425"
---
# <a name="systemphotoaperture-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. orifice

Stratégie de métadonnées de la photo pour la propriété [System. photo. orifice](../properties/props-system-photo-aperture.md) .

### <a name="pkey"></a>A-la

Ouverture de photo de l' \_ hypergraphique \_

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ R8

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur est générée à partir de System. photo. ApertureNumerator et de System. photo. ApertureDenominator. Il ne peut pas être écrit directement. Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37378} |             |
| 2     | /xmp/exif:ApertureValue       |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37378} |             |
| 2     | /xmp/exif:ApertureValue       |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 37378} |
| 2     | /xmp/exif:aperturevalue       |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                        | Format de disque |
|-------|-----------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37378}    |             |
| 2     | /ifd/xmp/exif:ApertureValue |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                        | Format de disque |
|-------|-----------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37378}    |             |
| 2     | /ifd/xmp/exif:ApertureValue |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                        |
|-------|-----------------------------|
| 1     | /IFD/EXIF/{UShort = 37378}    |
| 2     | /ifd/xmp/exif:aperturevalue |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. ouverture](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
