---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. FocalLengthInFilm.
ms.assetid: 3ad63a7a-5ced-4e7f-a4a0-e1463f3d3fa3
title: Stratégie de métadonnées de photo System. photo. FocalLengthInFilm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df46f3e52c447cb7902fe3cce2da201dae16d9c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412217"
---
# <a name="systemphotofocallengthinfilm-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. FocalLengthInFilm

Stratégie de métadonnées de la photo pour la propriété [System. photo. FocalLengthInFilm](../properties/props-system-photo-focallengthinfilm.md) .

### <a name="pkey"></a>A-la

FocalLengthInFilm de la \_

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



| JSON | Chemin d’accès                            | Format de disque |
|-------|---------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41989}   | ushort      |
| 2     | /xmp/exif:FocalLengthIn35mmFilm | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                            | Format de disque |
|-------|---------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41989}   | ushort      |
| 2     | /xmp/exif:FocalLengthIn35mmFilm | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                            |
|-------|---------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 41989}   |
| 2     | /xmp/exif:focallengthin35mmfilm |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                                | Format de disque |
|-------|-------------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41989}            | ushort      |
| 2     | /ifd/xmp/exif:FocalLengthIn35mmFilm | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                                | Format de disque |
|-------|-------------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41989}            | ushort      |
| 2     | /ifd/xmp/exif:FocalLengthIn35mmFilm | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                                |
|-------|-------------------------------------|
| 1     | /IFD/EXIF/{UShort = 41989}            |
| 2     | /ifd/xmp/exif:focallengthin35mmfilm |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. FocalLengthInFilm](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
