---
description: Stratégie de métadonnées de la photo pour la propriété System. GPS. ProcessingMethod.
ms.assetid: 840021a8-ec1d-4916-93b2-7cc1803e2d8c
title: Stratégie de métadonnées de photo System. GPS. ProcessingMethod
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800515d3a7870fa2dc9b5a6ec8c19178889482fa820f66d7d98e8e3ff09870f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931739"
---
# <a name="systemgpsprocessingmethod-photo-metadata-policy"></a>Stratégie de métadonnées de photo System. GPS. ProcessingMethod

Stratégie de métadonnées de la photo pour la propriété [System. GPS. ProcessingMethod](../properties/props-system-gps-processingmethod.md) .

### <a name="pkey"></a>A-la

\_ProcessingMethod GPS \_

### <a name="containers"></a>Containers

JPEG, TIFF

### <a name="read-only"></a>Lecture seule

Non

### <a name="output-propvariant-type"></a>Type PROPVARIANT de sortie

\_LPWStr VT

### <a name="input-propvariant-type"></a>Type de PROPVARIANT d’entrée

VT \_ LPWStr est préféré, mais VT \_ LPSTR est également accepté.

### <a name="conflict-resolution-policy"></a>Stratégie de résolution des conflits

Les valeurs de différents schémas sont conciliées.

### <a name="jpeg-policies"></a>Stratégies JPEG

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 27}     |             |
| 2     | /xmp/exif:GPSProcessingMethod | unicode     |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                          | Format de disque |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 27}     |             |
| 2     | /xmp/exif:GPSProcessingMethod | unicode     |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                          |
|-------|-------------------------------|
| 1     | /App1/IFD/GPS/{UShort = 27}     |
| 2     | /xmp/exif:gpsprocessingmethod |



 

### <a name="tiff-policies"></a>Stratégies TIFF

### <a name="read-paths"></a>Lire les chemins



| Commande | Chemin                              | Format de disque |
|-------|-----------------------------------|-------------|
| 1     | /ifd/xmp/exif:GPSProcessingMethod | unicode     |
| 2     | /IFD/GPS/{UShort = 27}              |             |



 

### <a name="write-paths"></a>Chemins d’accès en écriture



| Commande | Chemin                              | Format de disque |
|-------|-----------------------------------|-------------|
| 1     | /ifd/xmp/exif:GPSProcessingMethod | unicode     |
| 2     | /IFD/GPS/{UShort = 27}              |             |



 

### <a name="remove-paths"></a>Supprimer les chemins



| Commande | Chemin                              |
|-------|-----------------------------------|
| 1     | /ifd/xmp/exif:gpsprocessingmethod |
| 2     | /IFD/GPS/{UShort = 27}              |



 

## <a name="remarks"></a>Remarques

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[System. GPS. ProcessingMethod](../properties/props-system-gps-processingmethod.md)
</dt> </dl>

 

 
