---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. EXIFVersion.
ms.assetid: 0f9c5ea8-918f-4101-8492-3f408145a73e
title: Stratégie de métadonnées de photo System. photo. EXIFVersion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eee0fdac7ba8e86321d4a055cb6c37c4e9c7bad3f5bcfced548cc2485b3347c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882029"
---
# <a name="systemphotoexifversion-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. EXIFVersion

Stratégie de métadonnées de la photo pour la propriété [System. photo. EXIFVersion](../properties/props-system-photo-exifversion.md) .

### <a name="pkey"></a>A-la

\_Photo \_ EXIFVersion

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_LPWStr VT

### <a name="input-type"></a>Type d’entrée

Chaîne.

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                          | Format de disque   |
|-------|-------------------------------|---------------|
| 1     | /App1/IFD/EXIF/{UShort = 36864} | \_version EXIF |
| 2     | /xmp/exif:ExifVersion         | unicode       |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                          | Format de disque   |
|-------|-------------------------------|---------------|
| 1     | /App1/IFD/EXIF/{UShort = 36864} | \_version EXIF |
| 2     | /xmp/exif:ExifVersion         | unicode       |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 36864} |
| 2     | /xmp/exif:ExifVersion         |



 

### <a name="tiff-policy"></a>Stratégie TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                      | Format de disque   |
|-------|---------------------------|---------------|
| 1     | /IFD/EXIF/{UShort = 36864}  | \_version EXIF |
| 2     | /ifd/xmp/exif:ExifVersion | unicode       |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                      | Format de disque   |
|-------|---------------------------|---------------|
| 1     | /IFD/EXIF/{UShort = 36864}  | \_version EXIF |
| 2     | /ifd/xmp/exif:ExifVersion | unicode       |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                      |
|-------|---------------------------|
| 1     | /IFD/EXIF/{UShort = 36864}  |
| 2     | /ifd/xmp/exif:ExifVersion |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. EXIFVersion](../properties/props-system-photo-exifversion.md)
</dt> </dl>

 

 
