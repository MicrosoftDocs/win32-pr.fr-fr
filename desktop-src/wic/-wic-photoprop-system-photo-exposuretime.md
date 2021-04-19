---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. ExposureTime.
ms.assetid: 26f6ff27-b326-46f8-b4be-b091acbec575
title: Stratégie de métadonnées de photo System. photo. ExposureTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea9078befd0cbc26272ff14ae023b1b22cb4f0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536492"
---
# <a name="systemphotoexposuretime-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. ExposureTime

Stratégie de métadonnées de la photo pour la propriété [System. photo. exposuretime](../properties/props-system-photo-exposuretime.md) .

### <a name="pkey"></a>A-la

\_Photo \_ exposuretime

### <a name="containers"></a>Conteneurs

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ R8

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur est générée à partir de System. photo. ExposureTimeNumerator et de System. photo. ExposureTimeDenominator. Il ne peut pas être écrit directement. Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 33434} |             |
| 2     | /xmp/exif:ExposureTime        |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 33434} |             |
| 2     | /xmp/exif:ExposureTime        |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 33434} |
| 2     | /xmp/exif:exposuretime        |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin d’accès                       | Format de disque |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 33434}   |             |
| 2     | /ifd/xmp/exif:ExposureTime |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin d’accès                       | Format de disque |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 33434}   |             |
| 2     | /ifd/xmp/exif:ExposureTime |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin d’accès                       |
|-------|----------------------------|
| 1     | /IFD/EXIF/{UShort = 33434}   |
| 2     | /ifd/xmp/exif:exposuretime |



 

## <a name="remarks"></a>Notes

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. ExposureTime](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
