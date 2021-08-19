---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. ImgDirectionRef.
ms.assetid: 74ae0989-6d53-4d72-abe9-84f40c0c884a
title: Stratégie de métadonnées de photo System. GPS. ImgDirectionRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e735f91133d4ec473537f063e30d2d48f801a99f8f6bc80fa228b98a9bd95437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117667896"
---
# <a name="systemgpsimgdirectionref-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. ImgDirectionRef

Stratégie de métadonnées de la photo pour la propriété [System. GPS. ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md) .

### <a name="pkey"></a>A-la

\_GPS. ImgDirectionRef

### <a name="containers"></a>Containers

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



| Commande | Chemin                         | Format de disque |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 16}    | ascii       |
| 2     | /xmp/exif:GPSImgDirectionRef | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                         | Format de disque |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 16}    | ascii       |
| 2     | /xmp/exif:GPSImgDirectionRef | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                         |
|-------|------------------------------|
| 1     | /App1/IFD/GPS/{UShort = 16}    |
| 2     | /xmp/exif:gpsimgdirectionref |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                             | Format de disque |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 16}             | ascii       |
| 2     | /ifd/xmp/exif:GPSImgDirectionRef | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                             | Format de disque |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 16}             | ascii       |
| 2     | /ifd/xmp/exif:GPSImgDirectionRef | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                             |
|-------|----------------------------------|
| 1     | /IFD/GPS/{UShort = 16}             |
| 2     | /ifd/xmp/exif:gpsimgdirectionref |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md)
</dt> </dl>

 

 
