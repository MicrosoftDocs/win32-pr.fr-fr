---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. ImgDirectionRef.
ms.assetid: 74ae0989-6d53-4d72-abe9-84f40c0c884a
title: Stratégie de métadonnées de photo System. GPS. ImgDirectionRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80276ca8d1981935004dbec49fef588fcde330ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210279"
---
# <a name="systemgpsimgdirectionref-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. ImgDirectionRef

Stratégie de métadonnées de la photo pour la propriété [System. GPS. ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md) .

### <a name="pkey"></a>A-la

\_GPS. ImgDirectionRef

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_LPWStr VT

### <a name="input-type"></a>Type d’entrée

VT \_ LPWStr est préféré, mais VT \_ LPSTR est également accepté.

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policies"></a>Stratégies JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                         | Format de disque |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 16}    | ascii       |
| 2     | /xmp/exif:GPSImgDirectionRef | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                         | Format de disque |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 16}    | ascii       |
| 2     | /xmp/exif:GPSImgDirectionRef | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                         |
|-------|------------------------------|
| 1     | /App1/IFD/GPS/{UShort = 16}    |
| 2     | /xmp/exif:gpsimgdirectionref |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                             | Format de disque |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 16}             | ascii       |
| 2     | /ifd/xmp/exif:GPSImgDirectionRef | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                             | Format de disque |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 16}             | ascii       |
| 2     | /ifd/xmp/exif:GPSImgDirectionRef | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                             |
|-------|----------------------------------|
| 1     | /IFD/GPS/{UShort = 16}             |
| 2     | /ifd/xmp/exif:gpsimgdirectionref |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md)
</dt> </dl>

 

 
