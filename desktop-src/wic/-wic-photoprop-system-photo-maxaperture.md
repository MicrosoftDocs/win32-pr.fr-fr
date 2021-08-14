---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. MaxAperture.
ms.assetid: 9d12d265-0b0a-44d9-bbf6-ca7d748382ee
title: Stratégie de métadonnées de photo System. photo. MaxAperture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d692c12b9a5df584331a9a5ff4a82707d8549ab7891e1d9162eef318a77fe4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204711"
---
# <a name="systemphotomaxaperture-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. MaxAperture

Stratégie de métadonnées de la photo pour la propriété [System. photo. MaxAperture](../properties/props-system-photo-maxaperture.md) .

### <a name="pkey"></a>A-la

\_Photo \_ MaxAperture

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ R8

### <a name="input-type"></a>Type d’entrée

Double

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur est générée à partir de System. photo. MaxApertureNumerator et de System. photo. MaxApertureDenominator. Il ne peut pas être écrit directement. Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37381} |             |
| 2     | /xmp/exif:MaxApertureValue    |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37381} |             |
| 2     | /xmp/exif:MaxApertureValue    |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 37381} |
| 2     | /xmp/exif:maxaperturevalue    |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                           | Format de disque |
|-------|--------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37381}       |             |
| 2     | /ifd/xmp/exif:MaxApertureValue |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                           | Format de disque |
|-------|--------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37381}       |             |
| 2     | /ifd/xmp/exif:MaxApertureValue |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                           |
|-------|--------------------------------|
| 1     | /IFD/EXIF/{UShort = 37381}       |
| 2     | /ifd/xmp/exif:maxaperturevalue |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. MaxAperture](../properties/props-system-photo-maxaperture.md)
</dt> </dl>

 

 
