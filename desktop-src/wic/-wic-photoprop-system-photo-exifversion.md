---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. EXIFVersion.
ms.assetid: 0f9c5ea8-918f-4101-8492-3f408145a73e
title: Stratégie de métadonnées de photo System. photo. EXIFVersion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb823db41cb54a06fba235df5be4bb4acd55ea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210076"
---
# <a name="systemphotoexifversion-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. EXIFVersion

Stratégie de métadonnées de la photo pour la propriété [System. photo. EXIFVersion](../properties/props-system-photo-exifversion.md) .

### <a name="pkey"></a>A-la

\_Photo \_ EXIFVersion

### <a name="containers"></a>Conteneurs

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



| Commande | Chemin d’accès                          | Format de disque   |
|-------|-------------------------------|---------------|
| 1     | /App1/IFD/EXIF/{UShort = 36864} | \_version EXIF |
| 2     | /xmp/exif:ExifVersion         | unicode       |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                          | Format de disque   |
|-------|-------------------------------|---------------|
| 1     | /App1/IFD/EXIF/{UShort = 36864} | \_version EXIF |
| 2     | /xmp/exif:ExifVersion         | unicode       |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 36864} |
| 2     | /xmp/exif:ExifVersion         |



 

### <a name="tiff-policy"></a>Stratégie TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                      | Format de disque   |
|-------|---------------------------|---------------|
| 1     | /IFD/EXIF/{UShort = 36864}  | \_version EXIF |
| 2     | /ifd/xmp/exif:ExifVersion | unicode       |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                      | Format de disque   |
|-------|---------------------------|---------------|
| 1     | /IFD/EXIF/{UShort = 36864}  | \_version EXIF |
| 2     | /ifd/xmp/exif:ExifVersion | unicode       |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                      |
|-------|---------------------------|
| 1     | /IFD/EXIF/{UShort = 36864}  |
| 2     | /ifd/xmp/exif:ExifVersion |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. EXIFVersion](../properties/props-system-photo-exifversion.md)
</dt> </dl>

 

 
