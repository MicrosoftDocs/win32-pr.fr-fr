---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. RelatedSoundFile.
ms.assetid: 3b212d90-7ae2-4b7c-b77a-2017490aca40
title: Stratégie de métadonnées de photo System. photo. RelatedSoundFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07a29adb71f572868f21b1b8427e71b09616b24c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196115"
---
# <a name="systemphotorelatedsoundfile-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. RelatedSoundFile

Stratégie de métadonnées de la photo pour la propriété [System. photo. RelatedSoundFile](../properties/props-system-photo-relatedsoundfile.md) .

### <a name="pkey"></a>A-la

\_Photo \_ RelatedSoundFile

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



| JSON | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 40964} | ascii       |
| 2     | /xmp/exif:RelatedSoundFile    | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 40964} | ascii       |
| 2     | /xmp/exif:RelatedSoundFile    | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 40964} |
| 2     | /xmp/exif:RelatedSoundFile    |



 

### <a name="tiff-policy"></a>Stratégie TIFF

### <a name="read-paths"></a>Lire les chemins



| JSON | Chemin d’accès                           | Format de disque |
|-------|--------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 40964}       | ascii       |
| 2     | /ifd/xmp/exif:RelatedSoundFile | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| JSON | Chemin d’accès                           | Format de disque |
|-------|--------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 40964}       | ascii       |
| 2     | /ifd/xmp/exif:RelatedSoundFile | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| JSON | Chemin d’accès                           |
|-------|--------------------------------|
| 1     | /IFD/EXIF/{UShort = 40964}       |
| 2     | /ifd/xmp/exif:RelatedSoundFile |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. RelatedSoundFile](../properties/props-system-photo-relatedsoundfile.md)
</dt> </dl>

 

 
