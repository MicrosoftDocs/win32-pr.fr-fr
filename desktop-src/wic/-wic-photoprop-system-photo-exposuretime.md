---
description: Stratégie de métadonnées de la photo pour la propriété System. photo. ExposureTime.
ms.assetid: 26f6ff27-b326-46f8-b4be-b091acbec575
title: Stratégie de métadonnées de photo System. photo. ExposureTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4969103c682ff7d9aeb1edda1ebc2c3e5296482e51e4966b244db2caec4c3264
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117667559"
---
# <a name="systemphotoexposuretime-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. photo. ExposureTime

Stratégie de métadonnées de la photo pour la propriété [System. photo. exposuretime](../properties/props-system-photo-exposuretime.md) .

### <a name="pkey"></a>A-la

\_Photo \_ exposuretime

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Oui

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

VT \_ R8

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Cette valeur est générée à partir de System. photo. ExposureTimeNumerator et de System. photo. ExposureTimeDenominator. Il ne peut pas être écrit directement. Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policy"></a>Stratégie JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 33434} |             |
| 2     | /xmp/exif:ExposureTime        |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 33434} |             |
| 2     | /xmp/exif:ExposureTime        |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 33434} |
| 2     | /xmp/exif:exposuretime        |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                       | Format de disque |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 33434}   |             |
| 2     | /ifd/xmp/exif:ExposureTime |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                       | Format de disque |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 33434}   |             |
| 2     | /ifd/xmp/exif:ExposureTime |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                       |
|-------|----------------------------|
| 1     | /IFD/EXIF/{UShort = 33434}   |
| 2     | /ifd/xmp/exif:exposuretime |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. photo. ExposureTime](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
