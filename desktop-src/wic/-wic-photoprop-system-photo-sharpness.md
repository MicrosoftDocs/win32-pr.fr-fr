---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. Sharpity.
ms.assetid: 0fda4832-940b-4b5a-bd20-7e48c7800925
title: Stratégie de métadonnées de photo System. photo. Sharpity
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d635691f0b0e0801c1e37a006faa686aff0a8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196116"
---
# <a name="systemphotosharpness-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. Sharpity

Stratégie de métadonnées de la photo pour la propriété [System. photo. sharpity](../properties/props-system-photo-sharpness.md) .

### <a name="pkey"></a>A-la

\_ \_ Netteté photo

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ UI4

### <a name="input-type"></a>Type d’entrée

UShort

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41994} | ushort      |
| 2     | /XMP/EXIF : netteté           | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41994} | ushort      |
| 2     | /XMP/EXIF : netteté           | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 41994} |
| 2     | /XMP/EXIF : netteté           |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41994} | ushort      |
| 2     | /IFD/XMP/EXIF : netteté  | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41994} | ushort      |
| 2     | /IFD/XMP/EXIF : netteté  | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                     |
|-------|--------------------------|
| 1     | /IFD/EXIF/{UShort = 41994} |
| 2     | /IFD/XMP/EXIF : netteté  |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. Sharpity](../properties/props-system-photo-sharpness.md)
</dt> </dl>

 

 
