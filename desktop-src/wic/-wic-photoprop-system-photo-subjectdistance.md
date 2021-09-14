---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. SubjectDistance.
ms.assetid: 8d5acd7e-7227-4a79-890a-43e6dace3864
title: Stratégie de métadonnées de photo System. photo. SubjectDistance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3335b17f45cce7dc60881dc7ea8d9ffecc711016
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231024"
---
# <a name="systemphotosubjectdistance-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. SubjectDistance

Stratégie de métadonnées de la photo pour la propriété [System. photo. SubjectDistance](../properties/props-system-photo-subjectdistance.md) .

### <a name="pkey"></a>A-la

\_Photo \_ SubjectDistance

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ R8

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur est générée à partir de System. photo. SubjectDistanceNumerator et de System. photo. SubjectDistanceDenominator. Il ne peut pas être écrit directement. Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37382} |             |
| 2     | /xmp/exif:SubjectDistance     |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37382} |             |
| 2     | /xmp/exif:SubjectDistance     |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 37382} |
| 2     | /xmp/exif:subjectdistance     |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37382}      |             |
| 2     | /ifd/xmp/exif:SubjectDistance |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37382}      |             |
| 2     | /ifd/xmp/exif:SubjectDistance |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                          |
|-------|-------------------------------|
| 1     | /IFD/EXIF/{UShort = 37382}      |
| 2     | /ifd/xmp/exif:subjectdistance |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. SubjectDistance](../properties/props-system-photo-subjectdistance.md)
</dt> </dl>

 

 
