---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. Sharpity.
ms.assetid: 0fda4832-940b-4b5a-bd20-7e48c7800925
title: Stratégie de métadonnées de photo System. photo. Sharpity
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 717106c08cf127d8865cd19812bb8991ed4a5d64c8d6efc8a55e1846a31ca923
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118032360"
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



| Commande | Chemin                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41994} | ushort      |
| 2     | /XMP/EXIF : netteté           | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41994} | ushort      |
| 2     | /XMP/EXIF : netteté           | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 41994} |
| 2     | /XMP/EXIF : netteté           |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41994} | ushort      |
| 2     | /IFD/XMP/EXIF : netteté  | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                     | Format de disque |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41994} | ushort      |
| 2     | /IFD/XMP/EXIF : netteté  | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                     |
|-------|--------------------------|
| 1     | /IFD/EXIF/{UShort = 41994} |
| 2     | /IFD/XMP/EXIF : netteté  |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. Sharpity](../properties/props-system-photo-sharpness.md)
</dt> </dl>

 

 
