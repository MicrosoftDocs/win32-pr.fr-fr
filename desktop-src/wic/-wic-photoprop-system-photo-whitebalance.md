---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. WhiteBalance.
ms.assetid: 7b3a31e6-a929-41e4-b7f0-c5b3beac2519
title: Stratégie de métadonnées de photo System. photo. WhiteBalance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc333cedcd4665ace37033452ec3c7f0336f13e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518820"
---
# <a name="systemphotowhitebalance-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. WhiteBalance

Stratégie de métadonnées de la photo pour la propriété [System. photo. WhiteBalance](../properties/props-system-photo-whitebalance.md) .

### <a name="pkey"></a>A-la

\_Photo \_ WhiteBalance

### <a name="containers"></a>Conteneurs

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



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41987} | ushort      |
| 2     | /xmp/exif:WhiteBalance        | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41987} | ushort      |
| 2     | /xmp/exif:WhiteBalance        | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 41987} |
| 2     | /xmp/exif:whitebalance        |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                       | Format de disque |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41987}   | ushort      |
| 2     | /ifd/xmp/exif:WhiteBalance | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                       | Format de disque |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41987}   | ushort      |
| 2     | /ifd/xmp/exif:WhiteBalance | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                       |
|-------|----------------------------|
| 1     | /IFD/EXIF/{UShort = 41987}   |
| 2     | /ifd/xmp/exif:whitebalance |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. WhiteBalance](../properties/props-system-photo-whitebalance.md)
</dt> </dl>

 

 
